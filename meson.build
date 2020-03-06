project(
  'drm_monitor',
  'c',
  license: 'MIT',
  meson_version: '>=0.49.0',
  default_options: [
    'c_std=c11',
    'warning_level=2',
    'werror=true',
  ],
)

cc = meson.get_compiler('c')

add_project_arguments(cc.get_supported_arguments([
  '-Wno-missing-braces',
  '-Wno-missing-field-initializers',
  '-Wno-unused-parameter',
]), language: 'c')

libdrm = dependency('libdrm')

executable(
  'drm_monitor',
  files('main.c'),
  dependencies: [libdrm],
  install: true,
)
