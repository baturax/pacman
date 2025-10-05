libmakepkg_module = 'tidy'

sources = [
  '10-docs.sh.in',
  '10-libtool.sh.in',
  '10-staticlibs.sh.in',
  '50-purge.sh.in',
  '50-strip.sh.in',
  '50-zipman.sh.in',
  '90-emptydirs.sh.in',
]

foreach src : sources
  output_dir = join_paths(get_option('datadir'), 'makepkg', libmakepkg_module)

  custom_target(
    libmakepkg_module + '_' + src.underscorify(),
    command : [ SCRIPT_EDITOR, '@INPUT@', '@OUTPUT@' ],
    input : src,
    output : '@BASENAME@',
    install : true,
    install_dir : output_dir)
endforeach
