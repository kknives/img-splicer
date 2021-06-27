project('qsplice', 'cpp')
add_project_arguments('-DIMGUI_IMPL_OPENGL_LOADER_GL3W -D_REENTRANT', language : ['cpp', 'c'])

gui_deps = [dependency('sdl2'), dependency('gl')]
magick_dep = dependency('Magick++')
imgui_inc = include_directories('imgui')
gl_inc = include_directories('imgui/GL')
imgui_src = ['imgui/imgui.cpp','imgui/imgui_draw.cpp', 'imgui/imgui_tables.cpp', 'imgui/imgui_widgets.cpp', 'imgui/imgui_demo.cpp', 'imgui/imgui_impl_sdl.cpp', 'imgui/imgui_impl_opengl3.cpp', 'imgui/GL/gl3w.c']

qsplicer_src = ['main.cpp']

executable('qsplicer',
           sources: [qsplicer_src, imgui_src],
           dependencies: [gui_deps, magick_dep],
           include_directories: [imgui_inc, gl_inc],
           link_args: ['-ldl'],
           install : true)
