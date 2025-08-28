# Idealised Pine Island example using Kalman Ensembling
This example describes how to use [EnsembleKalmanProcesses][1] alongside the [model-ensembler][2]. This example is derived from the code in the original library example for learning parameterisations of a sine wave (examples/SinusoidInterface). This current set up is for use on the BAS HPC, on the older workstations (e.g. bslws02). These use an old version of julia (1.8.3) which is not compatible with later versions of EnsembleKalmanProcesses (versions 2.4.0 and later). This example should therefore default to using version 2.3.1 if not specified in the Project.toml file. 

## Description

This example is derived from the code in the original library example for learning parameterisations of a sine wave.

**This is still under development, but the workflow should run from end to end**

(Note that below is for c shell. Have to manually install WAVI at the julia step.)

### Running

```
python -m venv venv
source venv/bin/activate.csh
pip install --upgrade setuptools pip
pip install -r requirements.txt

# Enter julia REPL
julia
]
activate .
instantiate
Ctrl+D
Ctrl+D

# Back in bash
model_ensemble -rt 1 -st 1 -ct 1 -p -v ensemble.yaml dummy
# Or for SLURM
model_ensemble -p -rt 30 -st 10 -ct 30 -v ensemble.yaml
```

## License

This is a derived example from the Julia library and thus the original attribution license is in LICENSE.example, with the workflow being additionally licensed using the Apache 2.0 license, contained under LICENSE.


[1]: https://github.com/CliMA/EnsembleKalmanProcesses.jl
[2]: https://github.com/JimCircadian/model-ensembler
