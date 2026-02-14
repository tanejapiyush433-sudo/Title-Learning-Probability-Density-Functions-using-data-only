Methodology:

Step-1: Data Collection

Download air quality dataset.

Select NO₂ feature as variable x.

Remove missing values.

Step-2: Parameter calculation

Use roll number r.

Compute:

𝑎
𝑟
=
0.5
(
𝑟
 
m
o
d
 
7
)
a
r
	​

=0.5(rmod7)

𝑏
𝑟
=
0.3
(
𝑟
 
m
o
d
 
5
+
1
)
b
r
	​

=0.3(rmod5+1)

Step-3: Data transformation

Apply nonlinear transformation:

𝑧
=
𝑥
+
𝑎
𝑟
sin
⁡
(
𝑏
𝑟
𝑥
)
z=x+a
r
	​

sin(b
r
	​

x)

Normalize transformed data.

Step-4: GAN model design

Build Generator network

Input: random noise

Output: fake z samples

Build Discriminator network

Distinguishes real vs fake samples

Step-5: Training process

Generator produces fake samples.

Discriminator compares real z and fake samples.

Loss calculated and backpropagated.

Train both networks iteratively.

Step-6: PDF estimation

After training, generate many fake samples from generator.

Use:

Histogram density OR

Kernel Density Estimation (KDE)
to estimate probability density.

Step-7: Visualization

Plot estimated PDF of generated samples.

Compare distribution shape with real data.

Step-8: Observations

Check mode coverage.

Evaluate training stability.

Analyze similarity between real and generated distributions.

Step-9: Final Output

Transformation parameters: ar, br

GAN architecture description

PDF plot from generator

Observations on performance
<img width="1278" height="595" alt="image" src="https://github.com/user-attachments/assets/ff6ff63f-0925-4943-98ec-91beda1e24ce" />
