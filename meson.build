project(
  'nord-theme',
  version : '20210525',
  meson_version: '>= 0.50.0',
  license : 'GPL3'
)

variant_name = {
  'light' : 'Nord-solid',
  'darker' : 'Nord-Darker-solid',
  'dark' : 'Nord-Dark-solid',
  'lighter' : 'Nord-Lighter-solid'
}

prefix = get_option('prefix')
datadir = get_option('datadir')

install_dir = {
  'light' : datadir / 'themes' / variant_name.get('light'),
  'darker' : datadir / 'themes' / variant_name.get('darker'),
  'dark' : datadir / 'themes' / variant_name.get('dark'),
  'lighter' : datadir / 'themes' / variant_name.get('lighter'),
}

# sassc dependency
sassc = find_program('sass')

# inkscape dependency
inkscape = find_program('inkscape')
inkscape_ver = run_command(inkscape, '--version').stdout().split()[1]

subdir('common')
