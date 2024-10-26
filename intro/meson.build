intro_srcs = run_command('../list_sources.sh', check: true).stdout().strip().split('\n')

foreach src: intro_srcs
    executable(src.replace('.c', ''), src, include_directories: inc_dir, link_with: libunp)
endforeach
