# fftw
Small C++17/20 library providing a simple and safe interface for 1D FFT (and later 2D/3D)

The main goal is not to compete with established libraries, but to:

- Practice modern C++ API design (RAII, `std::vector`, `std::complex`).
- Better understand how to use FFTs in 1D (and later 2D/3D).
- Provide an extensible base for plugging in different backends (custom implementation, FFTW, etc.).

## Current status

- 1D complex FFT for power-of-two sizes, with an interface like:
"""
std::vector<std::complex<double>>
fft::transform(const std::vector<std::complex<double>>& input,
fft::Direction dir);
"""


- Small `main.cpp` demo with test signals (sine waves, impulses, etc.).

## Roadmap (ideas)

- Add inverse FFT (IFFT) support.
- Extend to 2D/3D.
- Integrate FFTW3 as a backend behind the same interface. [web:41][web:61]
- Add unit tests and CI with GitHub Actions.

