# Annaengine

demo/toy Vulkan engine for learning and maybe someday an engine for an actual game

licenced under the GNU GPLv3

(c) 2019 by Anna, "witcheslive" on github.com

## Notes using Gentoo GNU/Linux

My development environment is i3 window manager on Gentoo GNU/Linux with an nVidia 1070 Ti graphics card and using Visual Studio Code for the IDE.

You can find the tarballs for the Vulkan SDK here:

<https://vulkan.lunarg.com/sdk/home#linux>

At the time of this writing, I am using version 1.1.101.0 of the Vulkan SDK

I was able to compile and run the example only by emerging the wayland package. It also uses libxcb and, naturally, xorg. This was enough for `./build_examples.sh` to compile, then run `./vkcube` in the `examples/build` folder.

There is an ebuild for GLFW, so I used that, initially I had enabled the wayland use flag but that broke. Since I am using i3 which is Very Not Wayland, it was important to have -wayland on GLFW.

vulkan-tutorial.com recommends building from source for a recent version, but 3.2.1 is the most recent version. Yay for Gentoo! Apparently it hasn't changed since August 2016 though.

Libglm seems to be easily satisfied by `sudo emerge --ask glm` with the `media-libs/glm-0.9.9.2` ebuild. There is a newer version, 0.9.9.5 as of this writing, but they are VERY recent changes (within the past few days) and are probably nothing necessary at the moment.
