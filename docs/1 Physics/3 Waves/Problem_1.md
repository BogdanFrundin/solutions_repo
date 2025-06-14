# Problem 1

# Problem Setup

## Selection of Regular Polygon

To study interference patterns on the water surface, we begin by selecting a regular polygon. A regular polygon has sides of equal length and angles of equal measure. Examples include:

- Equilateral triangle
- Square
- Regular pentagon

The point wave sources will be placed at the vertices of the chosen polygon, ensuring a symmetric spatial configuration.

## Determination of Vertex Coordinates

Assume the center of the polygon is placed at the origin of the coordinate system $(0,0)$. The vertices of a regular $n$-sided polygon can be calculated using:

$$
(x_i, y_i) = (R \cos{\theta_i}, R \sin{\theta_i})
$$

where:

- $R$ is the radius of the circumscribed circle (distance from center to any vertex),
- $\theta_i = \theta_0 + \frac{2\pi i}{n}$ is the angular position of vertex $i$,
- $\theta_0$ is an optional initial rotation angle,
- $i \in \{0, 1, \dots, n-1\}$.

For simplicity, we often set $\theta_0 = 0$ so that the first vertex lies on the positive $x$-axis.

Thus, the full set of vertices is given by:

$$
\{(x_i, y_i)\ |\ i = 0, 1, \dots, n-1\}
$$

## Definition of Wave Parameters

Each point source emits a circular wave characterized by several key physical parameters:

- **Amplitude**: $A$, the maximum displacement of the water surface.
- **Wavelength**: $\lambda$, the distance between consecutive wave crests.
- **Frequency**: $f$, the number of oscillations per second (measured in Hz).
- **Wave Number**: $k$, defined as:

$$
k = \frac{2\pi}{\lambda}
$$

- **Angular Frequency**: $\omega$, defined as:

$$
\omega = 2\pi f
$$

- **Initial Phase**: $\phi$, the phase offset at time $t=0$ and distance $r=0$.

The displacement $\zeta$ of the water surface from a single source at a given point $(x,y)$ and time $t$ is described by the function:

$$
\zeta(x, y, t) = A \cos\left(kr - \omega t + \phi\right)
$$

where $r$ is the distance between the source and the point $(x,y)$, given by:

$$
r = \sqrt{(x - x_i)^2 + (y - y_i)^2}
$$

with $(x_i, y_i)$ being the coordinates of the source.

### Assumptions

- All sources emit **coherent** waves, maintaining a constant phase relationship.
- All sources have **identical** amplitude, wavelength, frequency, and initial phase, unless otherwise specified.

---

# Mathematical Formulation

## Wave Equation for a Single Source

The wave generated by a single point source located at position $(x_0, y_0)$ is described by the displacement function:

$$
\eta(x, y, t) = A \cos\left(k r - \omega t + \phi\right)
$$

where:

- $\eta(x, y, t)$ is the vertical displacement of the water surface at position $(x,y)$ and time $t$,
- $A$ is the amplitude of the wave,
- $k$ is the wave number $(k = \frac{2\pi}{\lambda})$,
- $r$ is the distance from the source to the point $(x,y)$,
- $\omega$ is the angular frequency $(\omega = 2\pi f)$,
- $\phi$ is the initial phase of the wave.

The distance $r$ between the source and the point of observation is given by:

$$
r = \sqrt{(x - x_0)^2 + (y - y_0)^2}
$$

## Wave Equations for Multiple Sources

For $n$ wave sources located at the vertices $(x_i, y_i)$ of the chosen regular polygon $(i = 0, 1, \dots, n-1)$, the displacement contributed by the $i$-th source is:

$$
\eta_i(x, y, t) = A \cos\left(k r_i - \omega t + \phi\right)
$$

where:

$$
r_i = \sqrt{(x - x_i)^2 + (y - y_i)^2}
$$

Each source emits a wave with identical parameters $(A, k, \omega, \phi)$ but centered at its specific vertex.

## Superposition Principle

According to the superposition principle, the total displacement $\eta_{\text{total}}(x, y, t)$ on the water surface is the sum of the displacements due to all individual sources:

$$
\eta_{\text{total}}(x, y, t) = \sum_{i=0}^{n-1} \eta_i(x, y, t)
$$

Explicitly, this can be written as:

$$
\eta_{\text{total}}(x, y, t) = A \sum_{i=0}^{n-1} \cos\left(k \sqrt{(x - x_i)^2 + (y - y_i)^2} - \omega t + \phi\right)
$$

This resulting function $\eta_{\text{total}}(x, y, t)$ describes the interference pattern generated by the multiple coherent sources positioned at the vertices of the regular polygon.

---

# Analysis of Interference

## Behavior of the Total Displacement

The total displacement $\eta_{\text{total}}(x, y, t)$, resulting from the superposition of waves emitted by all sources, is a function of both spatial coordinates $(x, y)$ and time $t$. It captures the dynamic interference effects across the water surface.

At any fixed moment in time, $\eta_{\text{total}}(x, y, t)$ provides a snapshot of the interference pattern, characterized by spatial variations in amplitude due to the constructive and destructive interactions of individual wave contributions.

Formally:

$$
\eta_{\text{total}}(x, y, t) = A \sum_{i=0}^{n-1} \cos\left(k \sqrt{(x - x_i)^2 + (y - y_i)^2} - \omega t + \phi\right)
$$

## Constructive and Destructive Interference

Interference phenomena arise from the phase relationships between the individual wave contributions at each point:

- **Constructive Interference**: Occurs when the phase difference between waves leads to reinforcement, resulting in a local maximum in displacement amplitude.

Mathematically, constructive interference at a point $(x, y)$ occurs when the phases satisfy:

$$
k(r_i - r_j) = 2m\pi
$$

for integers $m$, and for all pairs of sources $i$, $j$.

- **Destructive Interference**: Occurs when the phase difference between waves leads to cancellation, resulting in a local minimum or null in displacement amplitude.

Destructive interference occurs when:

$$
k(r_i - r_j) = (2m + 1)\pi
$$

for integers $m$.

Thus, the local interference condition depends on the relative path differences $r_i - r_j$ between sources.

## Influence of Polygon Geometry

The geometry of the chosen regular polygon — specifically, the number of sides $n$ and the spacing between vertices — significantly affects the resulting interference pattern:

- **Number of Sides ($n$)**: Increasing $n$ increases the number of wave sources, leading to more complex interference structures. For larger $n$, the system approaches circular symmetry.

- **Vertex Spacing**: The distance between adjacent vertices affects the spatial frequency of interference fringes. Closer vertices result in broader fringes; more widely spaced vertices yield finer, more intricate patterns.

- **Symmetry**: Due to the regularity of the polygon, the interference pattern inherits a high degree of symmetry. For example:
  - An equilateral triangle results in a threefold rotational symmetry in the interference pattern.
  - A square leads to fourfold symmetry, with prominent constructive regions aligned along the diagonals.
  - A pentagon results in fivefold symmetry, creating more complex but still ordered patterns.

Understanding how these geometric factors influence $\eta_{\text{total}}(x, y, t)$ is crucial for predicting and interpreting the observed interference structures.

---

# Code and Plots

## One source 

![alt text](single_drop_animation.gif)

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation, PillowWriter
from google.colab import files  # For downloading the file

# Parameters
amplitude = 1.0        # Amplitude of the waves
wavelength = 1.0       # Wavelength of the waves
frequency = 1.0        # Frequency of the waves
k = 2 * np.pi / wavelength  # Wave number
omega = 2 * np.pi * frequency  # Angular frequency
initial_phase = 0.0    # Initial phase

# Grid for the water surface (reduced resolution to avoid large file size)
x = np.linspace(-10, 10, 300)  # Reduced from 500 to 300
y = np.linspace(-10, 10, 300)
X, Y = np.meshgrid(x, y)

# Position of the single source (center of the grid)
source_x, source_y = 0.0, 0.0

# Function to calculate the displacement of a single wave source
def single_wave_displacement(X, Y, t):
    r = np.sqrt((X - source_x)**2 + (Y - source_y)**2)  # Distance from source
    return amplitude * np.cos(k * r - omega * t + initial_phase)

# Animation function
def update(frame):
    t = frame / 10.0  # Time step
    Z = single_wave_displacement(X, Y, t)
    im.set_array(Z)
    return [im]

# Create the figure and axis
fig, ax = plt.subplots(figsize=(8, 8))
ax.set_title("Wave Propagation from a Single Source")
ax.set_xlabel("x")
ax.set_ylabel("y")

# Initial plot
Z = single_wave_displacement(X, Y, 0.0)
im = ax.imshow(Z, extent=[x.min(), x.max(), y.min(), y.max()], origin='lower', cmap='coolwarm')
cbar = fig.colorbar(im, ax=ax)
cbar.set_label("Displacement")

# Animation
ani = FuncAnimation(fig, update, frames=range(0, 100), interval=50, blit=True)

# Save the animation as a GIF
ani.save('single_drop_animation.gif', writer=PillowWriter(fps=10))

# Automatically download the GIF
files.download('single_drop_animation.gif')

# Display the animation in Colab
from IPython.display import HTML
HTML(ani.to_jshtml())
```

## Two sources
![alt text](two_source_interference.gif)

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation, PillowWriter
from google.colab import files  # For downloading the file

# Parameters
amplitude = 1.0        # Amplitude of the waves
wavelength = 1.0       # Wavelength of the waves
frequency = 1.0        # Frequency of the waves
k = 2 * np.pi / wavelength  # Wave number
omega = 2 * np.pi * frequency  # Angular frequency
initial_phase = 0.0    # Initial phase

# Grid for the water surface (reduced resolution to avoid large file size)
x = np.linspace(-10, 10, 300)  # Reduced from 500 to 300
y = np.linspace(-10, 10, 300)
X, Y = np.meshgrid(x, y)

# Positions of the two sources
source_x1, source_y1 = -3.0, 0.0  # First source
source_x2, source_y2 = 3.0, 0.0   # Second source

# Function to calculate the displacement of a single wave source
def single_wave_displacement(X, Y, source_x, source_y, t):
    r = np.sqrt((X - source_x)**2 + (Y - source_y)**2)  # Distance from source
    return amplitude * np.cos(k * r - omega * t + initial_phase)

# Function to calculate the total displacement due to both sources
def total_displacement(X, Y, t):
    # Displacement from the first source
    h1 = single_wave_displacement(X, Y, source_x1, source_y1, t)
    # Displacement from the second source
    h2 = single_wave_displacement(X, Y, source_x2, source_y2, t)
    # Total displacement (superposition)
    return h1 + h2

# Animation function
def update(frame):
    t = frame / 10.0  # Time step
    Z = total_displacement(X, Y, t)
    im.set_array(Z)
    return [im]

# Create the figure and axis
fig, ax = plt.subplots(figsize=(8, 8))
ax.set_title("Interference Patterns from Two Sources")
ax.set_xlabel("x")
ax.set_ylabel("y")

# Initial plot
Z = total_displacement(X, Y, 0.0)
im = ax.imshow(Z, extent=[x.min(), x.max(), y.min(), y.max()], origin='lower', cmap='coolwarm')
cbar = fig.colorbar(im, ax=ax)
cbar.set_label("Displacement")

# Animation
ani = FuncAnimation(fig, update, frames=range(0, 100), interval=50, blit=True)

# Save the animation as a GIF
ani.save('two_source_interference.gif', writer=PillowWriter(fps=10))

# Automatically download the GIF
files.download('two_source_interference.gif')

# Display the animation in Colab
from IPython.display import HTML
HTML(ani.to_jshtml())
```

## Three sources

![alt text](three_source_interference.gif)

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation, PillowWriter
from google.colab import files  # For downloading the file

# Parameters
amplitude = 1.0        # Amplitude of the waves
wavelength = 1.0       # Wavelength of the waves
frequency = 1.0        # Frequency of the waves
k = 2 * np.pi / wavelength  # Wave number
omega = 2 * np.pi * frequency  # Angular frequency
initial_phase = 0.0    # Initial phase

# Grid for the water surface (reduced resolution to avoid large file size)
x = np.linspace(-10, 10, 300)  # Reduced from 500 to 300
y = np.linspace(-10, 10, 300)
X, Y = np.meshgrid(x, y)

# Positions of the three sources (arranged in an equilateral triangle)
radius = 5.0  # Distance of sources from the center
source_x1, source_y1 = radius * np.cos(0), radius * np.sin(0)  # First source
source_x2, source_y2 = radius * np.cos(2 * np.pi / 3), radius * np.sin(2 * np.pi / 3)  # Second source
source_x3, source_y3 = radius * np.cos(4 * np.pi / 3), radius * np.sin(4 * np.pi / 3)  # Third source

# Function to calculate the displacement of a single wave source
def single_wave_displacement(X, Y, source_x, source_y, t):
    r = np.sqrt((X - source_x)**2 + (Y - source_y)**2)  # Distance from source
    return amplitude * np.cos(k * r - omega * t + initial_phase)

# Function to calculate the total displacement due to all three sources
def total_displacement(X, Y, t):
    # Displacement from the first source
    h1 = single_wave_displacement(X, Y, source_x1, source_y1, t)
    # Displacement from the second source
    h2 = single_wave_displacement(X, Y, source_x2, source_y2, t)
    # Displacement from the third source
    h3 = single_wave_displacement(X, Y, source_x3, source_y3, t)
    # Total displacement (superposition)
    return h1 + h2 + h3

# Animation function
def update(frame):
    t = frame / 10.0  # Time step
    Z = total_displacement(X, Y, t)
    im.set_array(Z)
    return [im]

# Create the figure and axis
fig, ax = plt.subplots(figsize=(8, 8))
ax.set_title("Interference Patterns from Three Sources")
ax.set_xlabel("x")
ax.set_ylabel("y")

# Initial plot
Z = total_displacement(X, Y, 0.0)
im = ax.imshow(Z, extent=[x.min(), x.max(), y.min(), y.max()], origin='lower', cmap='coolwarm')
cbar = fig.colorbar(im, ax=ax)
cbar.set_label("Displacement")

# Animation
ani = FuncAnimation(fig, update, frames=range(0, 100), interval=50, blit=True)

# Save the animation as a GIF
ani.save('three_source_interference.gif', writer=PillowWriter(fps=10))

# Automatically download the GIF
files.download('three_source_interference.gif')

# Display the animation in Colab
from IPython.display import HTML
HTML(ani.to_jshtml())
```

## Four sources

![alt text](four_source_interference.gif)

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation, PillowWriter
from google.colab import files  # For downloading the file

# Parameters
amplitude = 1.0        # Amplitude of the waves
wavelength = 1.0       # Wavelength of the waves
frequency = 1.0        # Frequency of the waves
k = 2 * np.pi / wavelength  # Wave number
omega = 2 * np.pi * frequency  # Angular frequency
initial_phase = 0.0    # Initial phase

# Grid for the water surface (reduced resolution to avoid large file size)
x = np.linspace(-10, 10, 300)  # Reduced from 500 to 300
y = np.linspace(-10, 10, 300)
X, Y = np.meshgrid(x, y)

# Positions of the four sources (arranged in a square)
radius = 5.0  # Distance of sources from the center
source_x1, source_y1 = radius * np.cos(0), radius * np.sin(0)  # First source
source_x2, source_y2 = radius * np.cos(np.pi / 2), radius * np.sin(np.pi / 2)  # Second source
source_x3, source_y3 = radius * np.cos(np.pi), radius * np.sin(np.pi)  # Third source
source_x4, source_y4 = radius * np.cos(3 * np.pi / 2), radius * np.sin(3 * np.pi / 2)  # Fourth source

# Function to calculate the displacement of a single wave source
def single_wave_displacement(X, Y, source_x, source_y, t):
    r = np.sqrt((X - source_x)**2 + (Y - source_y)**2)  # Distance from source
    return amplitude * np.cos(k * r - omega * t + initial_phase)

# Function to calculate the total displacement due to all four sources
def total_displacement(X, Y, t):
    # Displacement from the first source
    h1 = single_wave_displacement(X, Y, source_x1, source_y1, t)
    # Displacement from the second source
    h2 = single_wave_displacement(X, Y, source_x2, source_y2, t)
    # Displacement from the third source
    h3 = single_wave_displacement(X, Y, source_x3, source_y3, t)
    # Displacement from the fourth source
    h4 = single_wave_displacement(X, Y, source_x4, source_y4, t)
    # Total displacement (superposition)
    return h1 + h2 + h3 + h4

# Animation function
def update(frame):
    t = frame / 10.0  # Time step
    Z = total_displacement(X, Y, t)
    im.set_array(Z)
    return [im]

# Create the figure and axis
fig, ax = plt.subplots(figsize=(8, 8))
ax.set_title("Interference Patterns from Four Sources")
ax.set_xlabel("x")
ax.set_ylabel("y")

# Initial plot
Z = total_displacement(X, Y, 0.0)
im = ax.imshow(Z, extent=[x.min(), x.max(), y.min(), y.max()], origin='lower', cmap='coolwarm')
cbar = fig.colorbar(im, ax=ax)
cbar.set_label("Displacement")

# Animation
ani = FuncAnimation(fig, update, frames=range(0, 100), interval=50, blit=True)

# Save the animation as a GIF
ani.save('four_source_interference.gif', writer=PillowWriter(fps=10))

# Automatically download the GIF
files.download('four_source_interference.gif')

# Display the animation in Colab
from IPython.display import HTML
HTML(ani.to_jshtml())
```

## Five sources

![alt text](five_source_interference.gif)

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation, PillowWriter
from google.colab import files  # For downloading the file

# Parameters
amplitude = 1.0        # Amplitude of the waves
wavelength = 1.0       # Wavelength of the waves
frequency = 1.0        # Frequency of the waves
k = 2 * np.pi / wavelength  # Wave number
omega = 2 * np.pi * frequency  # Angular frequency
initial_phase = 0.0    # Initial phase

# Grid for the water surface (reduced resolution to avoid large file size)
x = np.linspace(-10, 10, 300)  # Reduced from 500 to 300
y = np.linspace(-10, 10, 300)
X, Y = np.meshgrid(x, y)

# Positions of the five sources (arranged in a regular pentagon)
radius = 5.0  # Distance of sources from the center
source_x1, source_y1 = radius * np.cos(0), radius * np.sin(0)  # First source
source_x2, source_y2 = radius * np.cos(2 * np.pi / 5), radius * np.sin(2 * np.pi / 5)  # Second source
source_x3, source_y3 = radius * np.cos(4 * np.pi / 5), radius * np.sin(4 * np.pi / 5)  # Third source
source_x4, source_y4 = radius * np.cos(6 * np.pi / 5), radius * np.sin(6 * np.pi / 5)  # Fourth source
source_x5, source_y5 = radius * np.cos(8 * np.pi / 5), radius * np.sin(8 * np.pi / 5)  # Fifth source

# Function to calculate the displacement of a single wave source
def single_wave_displacement(X, Y, source_x, source_y, t):
    r = np.sqrt((X - source_x)**2 + (Y - source_y)**2)  # Distance from source
    return amplitude * np.cos(k * r - omega * t + initial_phase)

# Function to calculate the total displacement due to all five sources
def total_displacement(X, Y, t):
    # Displacement from the first source
    h1 = single_wave_displacement(X, Y, source_x1, source_y1, t)
    # Displacement from the second source
    h2 = single_wave_displacement(X, Y, source_x2, source_y2, t)
    # Displacement from the third source
    h3 = single_wave_displacement(X, Y, source_x3, source_y3, t)
    # Displacement from the fourth source
    h4 = single_wave_displacement(X, Y, source_x4, source_y4, t)
    # Displacement from the fifth source
    h5 = single_wave_displacement(X, Y, source_x5, source_y5, t)
    # Total displacement (superposition)
    return h1 + h2 + h3 + h4 + h5

# Animation function
def update(frame):
    t = frame / 10.0  # Time step
    Z = total_displacement(X, Y, t)
    im.set_array(Z)
    return [im]

# Create the figure and axis
fig, ax = plt.subplots(figsize=(8, 8))
ax.set_title("Interference Patterns from Five Sources")
ax.set_xlabel("x")
ax.set_ylabel("y")

# Initial plot
Z = total_displacement(X, Y, 0.0)
im = ax.imshow(Z, extent=[x.min(), x.max(), y.min(), y.max()], origin='lower', cmap='coolwarm')
cbar = fig.colorbar(im, ax=ax)
cbar.set_label("Displacement")

# Animation
ani = FuncAnimation(fig, update, frames=range(0, 100), interval=50, blit=True)

# Save the animation as a GIF
ani.save('five_source_interference.gif', writer=PillowWriter(fps=10))

# Automatically download the GIF
files.download('five_source_interference.gif')

# Display the animation in Colab
from IPython.display import HTML
HTML(ani.to_jshtml())
```

## Thirty sources

![alt text](thirty_source_interference.gif)

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation, PillowWriter
from google.colab import files  # For downloading the file

# Parameters
amplitude = 1.0        # Amplitude of the waves
wavelength = 1.0       # Wavelength of the waves
frequency = 1.0        # Frequency of the waves
k = 2 * np.pi / wavelength  # Wave number
omega = 2 * np.pi * frequency  # Angular frequency
initial_phase = 0.0    # Initial phase

# Grid for the water surface (reduced resolution to avoid large file size)
x = np.linspace(-10, 10, 300)  # Reduced from 500 to 300
y = np.linspace(-10, 10, 300)
X, Y = np.meshgrid(x, y)

# Positions of the four sources (arranged in a square)
radius = 5.0  # Distance of sources from the center
source_x1, source_y1 = radius * np.cos(0), radius * np.sin(0)  # First source
source_x2, source_y2 = radius * np.cos(np.pi / 2), radius * np.sin(np.pi / 2)  # Second source
source_x3, source_y3 = radius * np.cos(np.pi), radius * np.sin(np.pi)  # Third source
source_x4, source_y4 = radius * np.cos(3 * np.pi / 2), radius * np.sin(3 * np.pi / 2)  # Fourth source

# Function to calculate the displacement of a single wave source
def single_wave_displacement(X, Y, source_x, source_y, t):
    r = np.sqrt((X - source_x)**2 + (Y - source_y)**2)  # Distance from source
    return amplitude * np.cos(k * r - omega * t + initial_phase)

# Function to calculate the total displacement due to all four sources
def total_displacement(X, Y, t):
    # Displacement from the first source
    h1 = single_wave_displacement(X, Y, source_x1, source_y1, t)
    # Displacement from the second source
    h2 = single_wave_displacement(X, Y, source_x2, source_y2, t)
    # Displacement from the third source
    h3 = single_wave_displacement(X, Y, source_x3, source_y3, t)
    # Displacement from the fourth source
    h4 = single_wave_displacement(X, Y, source_x4, source_y4, t)
    # Total displacement (superposition)
    return h1 + h2 + h3 + h4

# Animation function
def update(frame):
    t = frame / 10.0  # Time step
    Z = total_displacement(X, Y, t)
    im.set_array(Z)
    return [im]

# Create the figure and axis
fig, ax = plt.subplots(figsize=(8, 8))
ax.set_title("Interference Patterns from Four Sources")
ax.set_xlabel("x")
ax.set_ylabel("y")

# Initial plot
Z = total_displacement(X, Y, 0.0)
im = ax.imshow(Z, extent=[x.min(), x.max(), y.min(), y.max()], origin='lower', cmap='coolwarm')
cbar = fig.colorbar(im, ax=ax)
cbar.set_label("Displacement")

# Animation
ani = FuncAnimation(fig, update, frames=range(0, 100), interval=50, blit=True)

# Save the animation as a GIF
ani.save('four_source_interference.gif', writer=PillowWriter(fps=10))

# Automatically download the GIF
files.download('four_source_interference.gif')

# Display the animation in Colab
from IPython.display import HTML
HTML(ani.to_jshtml())
```

## 3d animation

![alt text](optimized_3d_wave.gif)

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation, PillowWriter
from mpl_toolkits.mplot3d import Axes3D
from google.colab import files
from IPython.display import HTML

# Parameters
amplitude = 1.5
wavelength = 2.0
frequency = 1.0
k = 2 * np.pi / wavelength
omega = 2 * np.pi * frequency
initial_phase = 0.0

# Grid
x = np.linspace(-10, 10, 150)
y = np.linspace(-10, 10, 150)
X, Y = np.meshgrid(x, y)

# Sources
source_x1, source_y1 = -3.0, 0.0
source_x2, source_y2 = 3.0, 0.0

# Displacement functions
def single_wave_displacement(X, Y, source_x, source_y, t):
    r = np.sqrt((X - source_x)**2 + (Y - source_y)**2)
    return amplitude * np.cos(k * r - omega * t + initial_phase)

def total_displacement(X, Y, t):
    h1 = single_wave_displacement(X, Y, source_x1, source_y1, t)
    h2 = single_wave_displacement(X, Y, source_x2, source_y2, t)
    return h1 + h2

# Create 3D plot
fig = plt.figure(figsize=(10, 8))
ax = fig.add_subplot(111, projection='3d')

# Initial surface
Z = total_displacement(X, Y, 0.0)
surf = ax.plot_surface(X, Y, Z, cmap='coolwarm', edgecolor='none')

# Axes settings
ax.set_zlim(-3, 3)
ax.set_title("Optimized 3D Wave Interference")
ax.set_xlabel("x")
ax.set_ylabel("y")
ax.set_zlabel("Displacement")
ax.view_init(elev=30, azim=45)

# Animation update function
def update(frame):
    ax.clear()
    t = frame / 15.0
    Z = total_displacement(X, Y, t)
    surf = ax.plot_surface(X, Y, Z, cmap='coolwarm', edgecolor='none')
    ax.set_zlim(-3, 3)
    ax.set_title("Optimized 3D Wave Interference")
    ax.set_xlabel("x")
    ax.set_ylabel("y")
    ax.set_zlabel("Displacement")
    ax.view_init(elev=30, azim=45)
    return [surf]

# Animation
ani = FuncAnimation(fig, update, frames=80, interval=50, blit=False)

# Save as GIF
ani.save('optimized_3d_wave.gif', writer=PillowWriter(fps=20))
files.download('optimized_3d_wave.gif')

# Show animation in Colab
HTML(ani.to_jshtml())


```
# Colab

[Colab](https://colab.research.google.com/drive/1TO2sfmIH_UcxeeS4zTR5PBCTCUUdVMKc#scrollTo=0AE2MW7QpQH0)# Problem 1

