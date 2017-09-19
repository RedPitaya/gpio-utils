project('Linux GPIO tools', 'c', default_options : ['c_std=gnu99'])

dep = []
src = ['gpio-utils.c']
inc = include_directories([])

libgpio_shared = shared_library('gpio-utils', src, dependencies : dep, include_directories : inc,
                                version : '0.1.0', soversion : '0',
                                install : true)
libgpio_static = static_library('gpio-utils', src, dependencies : dep, include_directories : inc,
                                install : true)

libgpio_header = ['gpio-utils.h']
install_headers(libgpio_header)

executable('gpio-event-mon', 'gpio-event-mon.c', include_directories : inc, link_with : libgpio_shared)
executable('gpio-hammer',    'gpio-hammer.c',    include_directories : inc, link_with : libgpio_shared)
executable('lsgpio',         'lsgpio.c',         include_directories : inc, link_with : libgpio_shared)

incgpio = include_directories(['.'])
depgpio_shared = declare_dependency(link_with : libgpio_shared, include_directories : incgpio, dependencies : dep)
depgpio_static = declare_dependency(link_with : libgpio_static, include_directories : incgpio, dependencies : dep)
