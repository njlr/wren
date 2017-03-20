include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'wren',
  header_namespace = '',
  exported_headers = subdir_glob([
    ('src/include', '**/*.h'),
  ]),
  headers = subdir_glob([
    ('src/cli', 'vm.h'),
    ('src/cli', 'modules.h'),
    ('src/module', '**/*.h'),
    ('src/module', '**/*.inc'),
    ('src/optional', '**/*.h'),
    ('src/vm', '**/*.h'),
  ]),
  srcs = glob([
    'src/cli/modules.c',
    'src/cli/vm.c',
    'src/module/**/*.c',
    'src/optional/**/*.c',
    'src/vm/**/*.c',
  ]),
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)

cxx_binary(
  name = 'wren-cli',
  header_namespace = 'wren',
  headers = subdir_glob([
    ('src/cli', '**/*.h'),
  ]),
  srcs = [
    'src/cli/main.c',
  ],
  deps = [
    ':wren',
  ],
)
