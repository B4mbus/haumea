local_deps = [
  dependency('catch2-with-main', required: true),
]

test_sources = files('env.cpp')

test_exe = executable(
  'telesto_test',
  test_sources,
  include_directories: include_directories('.'),
  dependencies: [ telesto_dep, local_deps ],
  override_options: telesto_compilation_options
)

tests = [
  'Empty optional on non-existent env variable',
]

foreach test : tests
  test(test, test_exe)
endforeach
