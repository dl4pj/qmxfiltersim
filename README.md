QMX filter simulation
=====================

Simulation of LPF and BPF filters of QMX (Highband) and QMX+ (6m) in NGSpice

## Call
```
ngspice -b qmxfiltersim.cir
```

## Output
```
./out/bpf*m.svg: S11 + S21 + VSWR of bandpass
./out/lpf*m.svg: S11 + S21 + VSWR of lowpass
./out/lpfbpf*m.svg: S11 + S21 + VSWR of first lowpass(reverse) then bandpass (receive use case)
```

## Original LPF Configuration

| band      |   name |
|-----------|--------|
| 6m (QMX+) |  lpf6m |
| 10/11/12m | lpf10m |
| 15/17m    | lpf15m |
| 20m       | lpf20m |

![6m](out/lpf6m.svg)
![10/11/12m](out/lpf10m.svg)
![15/17m](out/lpf15m.svg)
![20m](out/lpf20m.svg)

## Original BPF Configuration

![6m](out/bpf6m.svg)
![10/11/12m](out/bpf10m.svg)
![15/17m](out/bpf15m.svg)
![20m](out/bpf20m.svg)

## Receiving through LPF(reverse) and BPF

![lpfbpf10m](out/lpfbpf10m.svg)
![lpfbpf15m](out/lpfbpf15m.svg)
![lpfbpf20m](out/lpfbpf20m.svg)
![lpfbpf6m](out/lpfbpf6m.svg)

## Notes
LC combinations of the BPF of QMX20-10
```
C403 30p  313.6nH  10m 
C401 33p  529.9n 
C404 33p  960.4n
C402 56p  1416.1n  20m
```