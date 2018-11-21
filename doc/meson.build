valadoc = find_program('valadoc')
gd_scan = find_program('gtkdoc-scan')

custom_target(
    'valadoc',
    command: [
        valadoc,
        '--pkg=gee-0.8',
        '--pkg=gio-unix-2.0',
        '--pkg=gtk+-3.0',
        '--pkg=posix',
        libgranite_sources,
        '--target-glib=2.50',
        '--package-name=' + granite_gi_name,
        '--package-version=' + granite_gi_version,
        '--verbose',
        '-o', 'valadocs',
        '--doclet=html'
    ],

    output: 'valadoc',
    depends: libgranite,
)

custom_target(
    'cdocs',
    command: [
        valadoc,
        '--pkg=gee-0.8',
        '--pkg=gio-unix-2.0',
        '--pkg=gtk+-3.0',
        '--pkg=posix',
        libgranite_sources,
        '--target-glib=2.50',
        '--package-name=' + granite_gi_name,
        '--package-version=' + granite_gi_version,
        '--verbose',
        '-o', 'cdocs',
        '--doclet-arg=' + 'lib/granite.h',
        '--doclet=gtkdoc'
    ],

    output: 'cdocs',
    depends: libgranite,
)

