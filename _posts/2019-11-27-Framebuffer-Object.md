---
layout: post
title:  Framebuffer Object | Render
categories: [Framebuffer Object]
---

The frame buffer object architecture (FBO) is an extension to OpenGL for doing flexible off-screen rendering, including rendering to a texture. By capturing images that would normally be drawn to the screen, it can be used to implement a large variety of image filters, and post-processing effects. The FBO is analogous to the [render](https://org1980.github.io/Adam-Render) targets model in DirectX. It is used in OpenGL for its efficiency and ease of use.

The use of FBOs doesn't suffer from the overhead associated with OpenGL drawing context switching, and has largely superseded the pbuffer and other methods involving context switches. The FBO has two main uses: The post-processing of rendered images and composition between different scenes. Some examples are: • The rendered image is captured and subjected to Fragment Shaders or other manipulations. This allows for many of today's popular computer graphics effects to be carried out, including the addition of a blurring or bloom effect. • Can be used to create views of other scenes, for example: a TV in a house showing the view from a secondary camera.

A scene can be rendered through an FBO to a texture, then that texture can be applied to the surface of a TV. This is sometimes called "Render to Texture" or RTT. Methods involving the FBO are considered superior because: • It is easier to set up than most other methods. • Is more efficient because resources are shared within the same context. • Is more flexible because all of depth buffer, stencil buffer, etc.

can be acquired. To use an FBO one simply creates an instance of it. Along with the FBO come several attachments. One can then attach these to a chosen receiver: either a texture, or a [render](https://org1980.github.io/Food-Render) buffer. • Create an FBO and bind it.

• Attach the color buffer (either as a RenderBuffer or a texture) to the FBO. • Attach the depth buffer (either as a RenderBuffer or a texture) to the FBO. • Render the texture to screen with a pixel shader, dependent on both the Color information and depth information. • Example code for Windows and Linux.

