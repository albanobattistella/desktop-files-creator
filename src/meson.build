desktop_files_creator_sources = [
  'main.vala',
  'window.vala',
]

desktop_files_creator_deps = [
  dependency('gio-2.0', version: '>= 2.50'),
  dependency('gtk+-3.0', version: '>= 3.22'),
]

gnome = import('gnome')

desktop_files_creator_sources += gnome.compile_resources('desktop_files_creator-resources',
  'desktop_files_creator.gresource.xml',
  c_name: 'desktop_files_creator'
)

executable('desktop-files-creator', desktop_files_creator_sources,
  vala_args: '--target-glib=2.50',  dependencies: desktop_files_creator_deps,
  install: true,
)
