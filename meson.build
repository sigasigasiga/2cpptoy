project('2cpptoy', 'cpp', default_options: ['cpp_std=c++20'])

cpp2_dep = dependency('cpp2')
cppfront = find_program('cppfront')

g = generator(cppfront,
  output: '@BASENAME@.cpp',
  arguments: ['@INPUT@', '-o', '@OUTPUT@']
)

sources = g.process('src/main.cpp2')

executable('toy', sources, dependencies: [cpp2_dep])
