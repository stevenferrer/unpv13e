project('unpv13e', 'c',
  version : '0.1',
  default_options : [
    'warning_level=3', 
    'buildtype=debugoptimized'
  ]
)

c = meson.get_compiler('c')

unp_srcs = []
subdir('lib')
subdir('libfree')
subdir('libroute')

inc_dir = include_directories('lib')

thread_dep = dependency('threads')
resolv_dep = c.find_library('resolv')

libunp = library('unp', unp_srcs, 
  include_directories: inc_dir, 
  dependencies: [thread_dep, resolv_dep]
)
