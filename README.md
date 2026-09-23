# ***Oddworld: Munch's Oddysee -* RTX Remix Mod**

Important Disclaimer

The main game executables and the launcher are not included in this release due to copyright restrictions. You must own a legitimate copy of Oddworld: Munch's Oddysee to install and play this mod.



## ***Overview \& Project Statu***<i>s</i>

This project brings full ray tracing (path tracing) and updated materials to Oddworld: Munch's Oddysee using NVIDIA's RTX Remix platform. By utilizing the Remix runtime, the mod intercepts the game's original draw calls to inject modern lighting, shadows, and physically-based rendering into the classic environment.



This project has been three years in the making. Getting it to a truly playable state with modern path tracing required countless hours of reverse-engineering, tweaking, and troubleshooting.



Please note that the mod is currently about 80% complete. While the game is fully playable and features a massive visual overhaul, it is still a work in progress. There are still several models and textures that need to be properly reworked, replaced, or upscaled to fully take advantage of the new lighting engine.



## ***Version Requirements***



You must use the 2001 legacy build. To switch your game version on Steam:



Right-click Oddworld: Munch's Oddysee in your Steam Library and select Properties.



Navigate to the Betas tab.



Select the 2001 legacy build from the beta participation dropdown menu.



Wait for Steam to download the original executable and associated files.



### ***optional***



(While you cannot use the 2019 HD version to run the game, you can use its upgraded assets. You can port over the higher-quality models, menus, and audio to the 2001 legacy build by simply copying those specific folders from the 2019 installation directory into your 2001 directory. Only copy the specific asset folders (models, menus, audio, etc.)—do not copy the executables or engine files.



This mod is strictly incompatible with the 2019 HD version of the game. The HD remaster uses a modern rendering pipeline that lacks the fixed-function requirements necessary for RTX Remix to hook into the engine. You must use the 2001 legacy build.)





##### ***YOU NEED TO USE DXWRAPPER DX8TO9.DLL WHEN INSTALLING THATS A MUST!!!***

## 

## ***Custom Layouts (Modded Maps)***

Inside the mod package, you will find a custom layouts folder. This directory contains modded versions of the game's maps designed specifically for ease of use. These altered map layouts have been adjusted to bypass or mitigate some of the engine's most stubborn rendering limitations, providing a smoother, more stable path-traced experience out of the box without requiring you to constantly fight the engine's quirks.



## ***Installation***

Ensure your game is actively set to the 2001 legacy build on Steam.



this version includes rtx remix 1.5.2. its recommended to download rtx remix yourself (**https://github.com/NVIDIAGameWorks/rtx-remix/releases/tag/remix-1.5.2)** and place those files in your **BIN folder** in the game files

&#x20;

Extract the Remix runtime into games bin folder.



Download this mod package and extract it into your game directory. Ensure the mod assets are placed in the rtx-remix/mods folder, and copy the contents of the custom layouts folder to their appropriate destinations as structured in the zip file.



Launch the game. The NVIDIA RTX Remix overlay should appear at the top of your screen upon boot.



## ***Configuration \& Customization***

Adapting a legacy engine to a modern path tracer presents unique rendering challenges. The included rtx.conf file comes pre-configured with categorized texture hashes and parameter adjustments to stabilize the image as much as possible.



## ***Gameplay Tweaks (TAGTEMPLATE.XML)***

Alongside the visual overhaul and map adjustments, this mod includes significant gameplay modifications achieved by altering the game's TAGTEMPLATE.XML file. These changes are designed to streamline testing and offer a unique, less restrictive way to experience the game:



Invincibility: Abe has been made completely invincible.



Speed Boost: Munch's movement speed has been significantly increased.



Universal Possession: The possession mechanic has been unlocked. every single creature in the game can now be possessed.



Spooce Multiplier: Gathering a single bit of Spooce now grants you 900 Spooce instead of just 1.



Visual Replacements: The traditional birds that circle above Abe's head have been swapped out for the flying mines typically used by enemies.



### ***Mitigating X-Ray Vision and Culling***

The legacy engine heavily relies on aggressive occlusion culling, which initially resulted in severe X-ray vision and disappearing meshes.



***Depth-Testing Parameters:*** Anti-culling and depth-testing parameters have been tuned in the provided rtx.conf to prevent the engine from prematurely discarding geometry that the path tracer needs to see.



***Runtime Adjustments:*** If you experience visual instability or clipping geometry during gameplay, you can manually adjust these parameters. Press Alt+X in-game to open the RTX Remix overlay, open the Developer Menu settings, and adjust the anti-culling and depth-testing parameters to improve visual fidelity.



### ***Known Issues***

Minor texture flickering may still occur during rapid camera movements due to the game's original culling logic.



Because of the way the game renders mesh's when facing away lights attached to meshes behind you also disappear causing some weird lighting effects, im working hard to fix this one



water has a weird issue where it flickers due to the game thinking its geometry and rtx remix seeing 30 different textures in a sprite sheet goind at 10 frames a second causes the lighting on water to bug out, but ive gotten it to a state which isn't too harsh on the eyes



UI elements may occasionally conflict with the path-traced lighting under specific conditions. for example the spooce locks as in the totems to unlock doors with spooce etc, the text on that has a motion blur effect which for now cant be changed unless someone else decides to fix it, im clueless on that specific thing, even text rendered above the head when health indicator is on blurs and sometimes you cant see the amount of spooce used or how much you have.



As mentioned, \~20% of the game's assets still need manual PBR texture reworks and model replacements.

