# Whiteboard


- HLSLMaterialSettins.h sets up a path to VSCode.  HLSLMaterialErrorHook.* looks like it tries to use that setting, but I don't see how or where that's supposed to be working.
- HLSLMaterial has a nice feature that since these files are parsed directly into a custom node, the usf/ush files don't need to be tracked, and you don't need to have shader directories configured.  I want to work with usf/ush files directly, to use functions and includes, so i'm going to break that basic simplicity of setup... so question is, what's the best way to do that?  Should HLSLMaterial be thought of as an editor or project plugin?  Does the project or the engine own the shader paths? should path management be integrated into HLSLMaterial or managed in some other, higher level source?
- I think I still want to break this down to one material function per HLSL function for reusability
- for proper function support, return types aren't required to be void anymore
- I like the auto-documentation features for tooltips - maybe expand on that for auto-generating in-house docs
- I may tackle making usf/ush files a first-class asset type so they would be importable/updatable  like fbx files (would need to have the ability to auto-update, as that's kind of the whole point here) - this could be the phase that creates the function library asset 