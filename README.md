# IDEAL SAMPLING
# AIM:
To perform construction and reconstruction of ideal sampling using python code.
# APPARATUS REQUIRED:
IDE python with scipy and numpy
# PROGRAM:
```
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import resample
fs = 100
t = np.arange(0, 1, 1/fs)
f = 5
signal = np.sin(2 * np.pi * f * t)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal')
plt.title('Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
t_sampled = np.arange(0, 1, 1/fs)
signal_sampled = np.sin(2 * np.pi * f * t_sampled)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro',
basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
reconstructed_signal = resample(signal_sampled, len(t))
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs =
100 Hz)')
plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
```
# OUTPUT:
![WhatsApp Image 2025-03-18 at 11 50 34_c411d9cb](https://github.com/user-attachments/assets/265a8fa5-4d75-4828-ad2b-b0ee9d781d01)
![WhatsApp Image 2025-03-18 at 11 50 56_4ec8ad1c](https://github.com/user-attachments/assets/a57f475c-b83d-4f2b-a920-231987f90ae6)
![WhatsApp Image 2025-03-18 at 11 51 12_7bb01a24](https://github.com/user-attachments/assets/2fc02681-a867-415a-828c-b35501a731a5)

# RESULT:
Thus the given construction and reconstruction of ideal sampling has been verified successfully.

