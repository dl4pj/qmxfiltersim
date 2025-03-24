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

## Images

![image info](images/image.png)
![image info](out/bpf10m.svg)
![image info](out/bpf15m.svg)
![image info](out/bpf20m.svg)
![image info](out/bpf6m.svg)
![image info](out/lpf10m.svg)
![image info](out/lpf15m.svg)
![image info](out/lpf20m.svg)
![image info](out/lpf6m.svg)
![image info](out/lpfbpf10m.svg)
![image info](out/lpfbpf15m.svg)
![image info](out/lpfbpf20m.svg)
![image info](out/lpfbpf6m.svg)

## Notes
LC combinations of the BPF of QMX20-10
```
C403 30p  313.6nH  10m 
C401 33p  529.9n 
C404 33p  960.4n
C402 56p  1416.1n  20m
```