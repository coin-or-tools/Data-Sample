project('Data-Sample', license: 'EPL-2.0', version: '1.3.0')

data = files(
    'afiro.mps',
    'app0110.cor',
    'app0110.stoch',
    'app0110.time',
    'app0110R.cor',
    'app0110R.stoch',
    'app0110R.time',
    'atm_5_10_1.block',
    'atm_5_10_1.mps',
    'block_milp.dec',
    'block_milp.lp',
    'brandy.mps',
    'bug.cor',
    'bug.stoch',
    'bug.time',
    'conic.mps',
    'e226.mps',
    'exmip1.5.mps',
    'exmip1.lp',
    'exmip1.mps',
    'finnis.mps',
    'galenet.mps',
    'galenetbnds.mps',
    'hello.mps',
    'input.130',
    'lseu.mps',
    'nw460.mps',
    'p0033.mps',
    'p0201.mps',
    'p0548.mps',
    'pack1.mps',
    'retail3.block',
    'retail3.mps',
    'scOneInt.mps',
    'share2qp.mps',
    'spec_sections.mps',
    'tp3.mps',
    'tp4.mps',
    'tp5.mps',
    'wedding_16.block',
    'wedding_16.mps',
)

coindatasample_dep = declare_dependency(
    variables: {'datadir': meson.current_source_dir()},
)

datadir = get_option('prefix') / get_option('datadir') / 'coin/Data/Sample'
install_data(data, install_dir: datadir)

pkg = import('pkgconfig')
pkg.generate(
    name: 'Sample',
    description: 'Sample models',
    url: 'https://github.com/coin-or-tools/Data-Sample',
    filebase: 'coindatasample',
    variables: [
        'datadir=' + join_paths(
            '${prefix}',
            get_option('datadir'),
            'coin/Data/Sample',
        ),
    ],
    dataonly: true,
)
