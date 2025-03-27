dependencies = []
dependencies += libjson.get_variable('nlohmann_json_dep')
dependencies += dependency('threads')

sources = files('libyabird.cpp')

install_headers('libyabird.h')

libyabird = library('yanet-rib',
                    sources,
                    include_directories: yanet_rootdir,
                    dependencies: dependencies,
                    install: true,
                    version: '0.1.0')

if get_option('default_library') == 'static' or get_option('default_library') == 'both'
    libyabird_static = static_library('yanet-rib-static',
                                    sources,
                                    include_directories: yanet_rootdir,
                                    dependencies: dependencies,
                                    install: true)
endif
