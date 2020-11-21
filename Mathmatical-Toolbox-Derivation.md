# Mathmatical Toolbox Derivation

##Definition of $\phi$

Given two codimension-two Level Set Function(LSF) $\phi_0$ and $\phi_1$, then we have the combination LSF $\phi$ as their minimum value at each position (x,y) of domain $\Omega\subset\mathbb R^2$.

$\phi=min\{\phi_0,\phi_1\}$                                                                                                      (1)

So we can rewrite $\phi$ as

$\phi=H_1\phi_0+H_0\phi_1+(1-H_0)(1-H_1)\phi_0$

   $=H_1\phi_0+H_0\phi_1+(1-H_0)(1-H_1)\phi_1$                                                           (2)

in above formulation,  $H_0,H_1$ are defined as

$\begin{cases}H_0=H(\phi_0-\phi_1)\\H_1=H(\phi_1-\phi_0) \end{cases}$                                                                                                 (3)

$H(\cdot)$  is the **==Heaviside function==** defined as

$H(\alpha)=\begin{cases}1,\alpha>0\\0,\alpha\leqslant 0\end{cases}$                                                                                                    (4)

$\therefore \phi=H_1\phi_0+H_0\phi_1+(1-H_0-H_1+H_0H_1)\phi_0$

​      $=H_1\phi_0+H_0\phi_1+(1-H_0-H_1+H_0H_1)\phi_1$

$\because H_0H_1\equiv 0 $                                                                                                               (5)

$\therefore \phi=H_0\phi_1+(1-H_0)\phi_0=H_1\phi_0+(1-H_1)\phi_1$                                            (6)

## Calculus Toolbox

### Differential

#### $H(\phi)$  Expression

$\begin{cases}H(\phi)=\frac{1}{2}(1+H_1-H_0)H(\phi_0)+\frac{1}{2}(1+H_0-H_1)H(\phi_1)\\or\\H(\phi)=H_1H(\phi_0)+H_0H(\phi_1)+\frac{1}{2}(1-H_0)(1-H_1)(H(\phi_0)+H(\phi_1))\\or\\H(\phi)=H_0H(\phi_1)+(1-H_0)H(\phi_0)\\or\\H(\phi)=H_1H(\phi_0)+(1-H_1)H(\phi_1)\end{cases}$          (7)               

**Derivation:**

---

$H(\phi)=H(H_0\phi_1+(1-H_0)\phi_0)$                                                                           

Because when $H_0=1$, then $(1-H_0)=0$, vise versa, so we can write $H(\phi)$ as

$H(\phi)=\begin{cases}H(H_0\phi_1)=H_0H(\phi_1) &if\  H_0=1\\H((1-H_0)\phi_0)=(1-H_0)H(\phi_0)&if\ H_0=0\end{cases}$       

The form of the above formula still retains the properties of the Heaviside operator, so we can rewrite $H(\phi)$ in a  compact form as

$H(\phi)=H_0H(\phi_1)+(1-H_0)H(\phi_0)$                                                                   (8)

Similarly, we have $H(\phi)$ in another form according to formula(5) as 

$H(\phi)=H_1H(\phi_0)+(1-H_1)H(\phi_1)$                                                                   (9)

Then, let's take the sum of above two forms of $H(\phi)$, we can have

$2H(\phi)=H_0H(\phi_1)+(1-H_0)H(\phi_0)+H_1H(\phi_0)+(1-H_1)H(\phi_1)$ 

Finally, we can obtain the first formula of (7). Further more, we can convert the expression of first formula of(7) to the second formula of (7) by using the  *[asynchronism](javascript:;)* property of $H_0$ and $H_1$.

---

####  $\nabla H(\phi)$ Expression

$\begin{cases}\nabla H(\phi)=\frac{1}{2}(1+H_1-H_0)\delta(\phi_0)\nabla\phi_0+\frac{1}{2}(1+H_0-H_1)\delta(\phi_1)\nabla\phi_1\\or\\\nabla H(\phi)=H_1\delta(\phi_0)\nabla \phi_0+H_0\delta(\phi_1)\nabla \phi_1+\delta_1\delta(\phi_0)\nabla(\frac{\phi_0+\phi_1}{2})\\or\\\nabla H(\phi)=H_1\delta(\phi_0)\nabla \phi_0+H_0\delta(\phi_1)\nabla \phi_1+\delta_0\delta(\phi_1)\nabla(\frac{\phi_0+\phi_1}{2})\end{cases}$       (10)

$\begin{cases}\delta_1:=\delta(\phi_1-\phi_0)\\\delta_0:=\delta(\phi_0-\phi_1)\end{cases}$                                                                                                 (11)

Where, $\delta(\cdot)$ is **==Delta function==**,defined as

$\delta(\alpha)=\begin{cases}1&if\ \alpha=0\\0 &otherwise\end{cases}$                                                                                         (12)

And it can be easily known that 

$\delta_0=\delta_1$                                                                                                                       (13)

**Derivation:**

---

We can obtain the gradient of $H(\phi)$ by using operator $\nabla$ at both side of formula(8), then we have

$\nabla H(\phi)=\nabla[H_0H(\phi_1)+(1-H_0)H(\phi_0)]$

​              $=\nabla (H_0) H(\phi_1)+H_0\nabla(H(\phi_1))+\nabla(1-H_0)H(\phi_0)+(1-H_0)\nabla(H(\phi_0))$

​             $=\delta_0\nabla(\phi_0-\phi_1)H(\phi_1)+H_0\delta(\phi_1)\nabla\phi_1-\delta_0\nabla(\phi_0-\phi_1)H(\phi_0)+(1-H_0)\delta(\phi_0)\nabla \phi_0$

Similarly, we use operator $\nabla$ at both side of formula(9), we can have another expression about the gradient of $H(\phi)$ as follows



$\nabla H(\phi)=\nabla[H_1H(\phi_0)+(1-H_1)H(\phi_1)]$

​              $=\nabla (H_1) H(\phi_0)+H_1\nabla(H(\phi_0))+\nabla(1-H_1)H(\phi_1)+(1-H_1)\nabla(H(\phi_1))$

$=\delta_1\nabla(\phi_1-\phi_0)H(\phi_0)+H_1\delta(\phi_0)\nabla\phi_0-\delta_1\nabla(\phi_1-\phi_0)H(\phi_1)+(1-H_1)\delta(\phi_1)\nabla \phi_1$

Then, let's take the sum of above two forms of $\nabla H(\phi)$, we can have

$2 \nabla H(\phi)=(1+H_1-H_0)\delta(\phi_0)\nabla\phi_0+(1+H_0-H_1)\delta(\phi_1)\nabla\phi_1$

​                 $+2[H(\phi_0)-H(\phi_1)]\delta(\phi_1-\phi_0)\nabla (\phi_1-\phi_0)$

because $[H(\phi_0)-H(\phi_1)]\delta(\phi_1-\phi_0)\equiv 0$, therefore we have

$\nabla H(\phi)=\frac{1}{2}(1+H_1-H_0)\delta(\phi_0)\nabla\phi_0+\frac{1}{2}(1+H_0-H_1)\delta(\phi_1)\nabla\phi_1$

Further more, we use the *[asynchronism](javascript:;)* property of $H_0$ and $H_1$, it can be rewrite as

$\nabla H(\phi)=H_1\delta(\phi_0)\nabla \phi_0+H_0\delta(\phi_1)\nabla \phi_1+\delta(\phi_1-\phi_0)\frac{1}{2}\delta(\phi_0)\nabla \phi_0+\delta(\phi_1-\phi_0)\frac{1}{2}\delta(\phi_1)\nabla \phi_1$

​              $=H_1\delta(\phi_0)\nabla \phi_0+H_0\delta(\phi_1)\nabla \phi_1+\delta_1\delta(\phi_0)\nabla\frac{\phi_0+\phi_1}{2}$

​              $=H_1\delta(\phi_0)\nabla \phi_0+H_0\delta(\phi_1)\nabla \phi_1+\delta_0\delta(\phi_1)\nabla\frac{\phi_0+\phi_1}{2}$

---

#### $\nabla\phi$ Expression

$\begin{cases}\nabla\phi=\nabla(\frac{\phi_1+\phi_0}{2})-(H_1-H_0)\nabla(\frac{\phi_1-\phi_0}{2})\\or\\\nabla\phi=H_1\nabla\phi_0+H_0\nabla\phi_1+\delta_0\nabla(\frac{\phi_1+\phi_0}{2})\\or\\\nabla\phi=H_1\nabla\phi_0+H_0\nabla\phi_1+\delta_1\nabla(\frac{\phi_1+\phi_0}{2})\end{cases}$                                                 (14)                                                                    

**Derivation:**

---

In virtue of formula(13), we can obtain the gradient of $\phi$ from the first line of formula(2) as

$\nabla\phi=\nabla(H_1\phi_0)+\nabla(H_0\phi_1)+\nabla((1-H_1)(1-H_0)\phi_0)$

​       $=\nabla(H_1\phi_0)+\nabla(H_0\phi_1)+\nabla((1-H_0-H_1)\phi_0)$

​       $=\delta_1\nabla(\phi_1-\phi_0)\phi_0+H_1\nabla\phi_0+\delta_0\nabla(\phi_0-\phi_1)\phi_1+H_0\nabla\phi_1$

​        $-(\delta_0\nabla(\phi_0-\phi_1)+\delta_1\nabla(\phi_1-\phi_0))\phi_0+(1-H_0-H_1)\nabla\phi_0$

​        $=\delta_0\nabla(\phi_0-\phi_1)\phi_1+H_0\nabla\phi_1-\delta_0\nabla(\phi_0-\phi_1)\phi_0+(1-H_0)\nabla\phi_0$

Similarly, from the second line of formula(2), we have

$\nabla\phi=\nabla(H_1\phi_0)+\nabla(H_0\phi_1)+\nabla((1-H_1)(1-H_0)\phi_1)$

​       $=\nabla(H_1\phi_0)+\nabla(H_0\phi_1)+\nabla((1-H_0-H_1)\phi_1)$

​       $=\delta_1\nabla(\phi_1-\phi_0)\phi_0+H_1\nabla\phi_0+\delta_0\nabla(\phi_0-\phi_1)\phi_1+H_0\nabla\phi_1$

​        $-(\delta_0\nabla(\phi_0-\phi_1)+\delta_1\nabla(\phi_1-\phi_0))\phi_1+(1-H_0-H_1)\nabla\phi_1$

​        $=\delta_1\nabla(\phi_1-\phi_0)\phi_0+H_1\nabla\phi_0-\delta_1\nabla(\phi_1-\phi_0)\phi_1+(1-H_1)\nabla\phi_1$

Then, let's take the sum of above two forms of $\nabla\phi$, we can have

 $2\nabla\phi=\nabla(\phi_0+\phi_1)+(H_0-H_1)\nabla\phi_1+(H_1-H_0)\nabla\phi_0$

​           $+2\delta_0\nabla(\phi_0-\phi_1)\phi_1+2\delta_1\nabla(\phi_1-\phi_0)\phi_0$

​           $=\nabla(\phi_0+\phi_1)-(H_1-H_0)\nabla(\phi_1-\phi_0)+2\delta_0\nabla(\phi_0-\phi_1)(\phi_1-\phi_0)$

Note that $\delta(\phi_0-\phi_1)(\phi_1-\phi_0)\equiv 0$, then we have the final form of $\nabla\phi$ as

$\nabla\phi=\nabla(\frac{\phi_1+\phi_0}{2})-(H_1-H_0)\nabla(\frac{\phi_1-\phi_0}{2})$

Further more, we use the *[asynchronism](javascript:;)* property of $H_0$ and $H_1$, and note formula(13), $\nabla\phi$ can be rewrite as

$\begin{cases}\nabla\phi=H_1\nabla\phi_0+H_0\nabla\phi_1+\delta_0\nabla(\frac{\phi_1+\phi_0}{2})\\or\\\nabla\phi=H_1\nabla\phi_0+H_0\nabla\phi_1+\delta_1\nabla(\frac{\phi_1+\phi_0}{2})\end{cases}$ 

---

#### $\hat\delta_{\phi}(\vec x)$ Expression

The **==Dirac Delta function==** defined as

$\hat\delta_{\phi}(\vec x):=\nabla H(\phi)\cdot\vec N_{\phi}=\nabla H(\phi)\cdot\frac{\nabla\phi}{|\nabla\phi|}$                                                                (15)           

where $\vec N_{\phi}$ denotes the outer normal vector of the isocontour obtained by $\phi=0$ under the assumption that $\phi$ is a LSF. So we can get the expression of $\hat\delta_{\phi}(\vec x)$ by using of caculus toolbox about $\nabla H(\phi)$ and $\nabla\phi$ as following.

$\begin{cases}\hat\delta_{\phi}(\vec x)=H_1\delta(\phi_0)|\nabla\phi_0|+H_0\delta(\phi_1)|\nabla\phi_1|+\delta_1\delta(\phi_0)|\nabla(\frac{\phi_0+\phi_1}{2})|\\or\\\hat\delta_{\phi}(\vec x)=H_1\delta(\phi_0)|\nabla\phi_0|+H_0\delta(\phi_1)|\nabla\phi_1|+\delta_0\delta(\phi_1)|\nabla(\frac{\phi_0+\phi_1}{2})|\\or\\\hat\delta_{\phi}(\vec x)=(1-H_0)\delta(\phi_0)|\nabla\phi_0|+H_0\delta(\phi_1)|\nabla\phi_1|\\or\\\hat\delta_{\phi}(\vec x)=H_1\delta(\phi_0)|\nabla\phi_0|+(1-H_1)\delta(\phi_1)|\nabla\phi_1|\end{cases}$                 (16)

**Derivation:**

---

We take the dot product of $\nabla H(\phi)$ and $\frac{\nabla\phi}{|\nabla\phi|}$ by using of the form of the second line of formula(10) and the second line of formula(14) respectively, then we have

$\nabla H(\phi)\cdot\nabla\phi=[H_1\delta(\phi_0)\nabla \phi_0+H_0\delta(\phi_1)\nabla \phi_1+\delta_1\delta(\phi_0)\nabla(\frac{\phi_0+\phi_1}{2})]$                    

​                              $\cdot[H_1\nabla\phi_0+H_0\nabla\phi_1+\delta_0\nabla(\frac{\phi_1+\phi_0}{2})]$

​                       $=H_1\delta(\phi_0)|\nabla\phi_0|^2+H_0H_1\delta(\phi_1)\nabla\phi_1\cdot\nabla\phi_0+H_1\delta_1\delta(\phi_0)\nabla\frac{\phi_1+\phi_0}{2}\cdot\nabla\phi_0$

$+H_1H_0\delta(\phi_0)\nabla\phi_0\cdot\nabla\phi_1+H_0\delta(\phi_1)|\nabla\phi_1|^2+H_0\delta_1\delta(\phi_0)\nabla\frac{\phi_1+\phi_0}{2}\cdot\nabla\phi_1$

$+H_1\delta_1\delta(\phi_0)\nabla\phi_0\cdot\nabla\frac{\phi_0+\phi_1}{2}+H_0\delta_1\delta(\phi_1)\nabla\phi_1\cdot\nabla\frac{\phi_0+\phi_1}{2}+\delta_1\delta(\phi_0)|\nabla\frac{\phi_0+\phi_1}{2}|^2$

Note that $H_0H_1\equiv 0$ and $H_i\delta_j\equiv 0$ for any pair $i,j=0 \ or \ 1$, so we can simplify the formula as

$\nabla H(\phi)\cdot\nabla\phi=H_1\delta(\phi_0)|\nabla\phi_0|^2+H_0\delta(\phi_1)|\nabla\phi_1|^2+\delta_1\delta(\phi_0)|\nabla(\frac{\phi_0+\phi_1}{2})|^2$

Now, we can rewrite the $\hat\delta_{\phi}(\vec x)$ as

$\hat\delta_{\phi}(\vec x)=\frac{1}{|\nabla\phi|}[H_1\delta(\phi_0)|\nabla\phi_0|^2+H_0\delta(\phi_1)|\nabla\phi_1|^2+\delta_1\delta(\phi_0)|\nabla(\frac{\phi_0+\phi_1}{2})|^2]$

​           $=\frac{H_1\delta(\phi_0)|\nabla\phi_0|^2+H_0\delta(\phi_1)|\nabla\phi_1|^2+\delta_1\delta(\phi_0)|\nabla(\frac{\phi_0+\phi_1}{2})|^2}{|H_1\nabla\phi_0+H_0\nabla\phi_1+\delta_0\nabla(\frac{\phi_1+\phi_0}{2})|}$

Because  the *[asynchronism](javascript:;)* property of $H_0$ , $H_1$ and $\delta_0 $(or else $\delta_1 $)

$\begin{cases}if\ H_1=1,&then\ H_0=0\ and\  \delta_0=\delta_1=0\\if\ H_0=1,&then\ H_1=0\ and\  \delta_0=\delta_1=0\\if\ \delta_0=\delta_1=1,&then\ H_0=0\ and\ H_1=0\end{cases}$                             (17)

Therefore, we can obtain the most simplified form of $\hat\delta_{\phi}(\vec x)$ as the first and second lines of formula(16). The term including $|\nabla(\frac{\phi_0+\phi_1}{2})|$ in the first and second lines of formula(16) means we can use the norm of the average value of $\nabla\phi_0$ and $\nabla\phi_1$ at the position (x,y) of domain $\Omega$, where $\phi_0=\phi_1$. Similarly, we also can use the norm of $\nabla\phi_0$ or $\nabla\phi_1$ as the norm of $\nabla\phi$ at the position (x,y), where $\phi_0=\phi_1$. 

When we substitute $|\nabla\phi_0|$ for  $|\nabla(\frac{\phi_0+\phi_1}{2})|$, then we have

$\hat\delta_{\phi}(\vec x)=H_1\delta(\phi_0)|\nabla\phi_0|+H_0\delta(\phi_1)|\nabla\phi_1|+\delta_1\delta(\phi_0)|\nabla\phi_0|$

Similarly, when  we substitute $|\nabla\phi_1|$ for  $|\nabla(\frac{\phi_0+\phi_1}{2})|$, then we have

$\hat\delta_{\phi}(\vec x)=H_1\delta(\phi_0)|\nabla\phi_0|+H_0\delta(\phi_1)|\nabla\phi_1|+\delta_0\delta(\phi_1)|\nabla\phi_1|$

Note that $H_1+\delta_1=1-H_0$ and $H_0+\delta_0=1-H_1$, we can finally get the third and fourth lines of formula(16) .

---

### Integral

#### Region Based

The region integral of $f(x,y)$(noted as $f(\vec x)$) over the exterior region of $\Omega$ noted as $\Omega^+$ , where the LSF $\phi>0$ , can be written as

$I_{\Omega^+}=\int_{\Omega^+}f(\vec x)d\vec x=\int_{\Omega}f(\vec x)H(\phi)d\vec x$                                                           (18)

According to the third line of formula(7), formula(18) can be rewritten as

$I_{\Omega^+}=\int_\Omega f(\vec x)H_0[H(\phi_1)-H(\phi_0)]d\vec x+\int_\Omega f(\vec x)H(\phi_0)d\vec x$                       (19)

Similarly, the region integral of $f(\vec x)$ over the interior region of $\Omega$ noted as $\Omega^-$ , where the LSF $\phi<0$ , can be written as

$I_{\Omega^-}=\int_{\Omega^-}f(\vec x)d\vec x=\int_{\Omega}f(\vec x)H(-\phi)d\vec x=\int_{\Omega}f(\vec x)(1-H(\phi))d\vec x$           (20)

According to the third line of formula(7), formula(20) can be rewritten as

$I_{\Omega^-}=\int_\Omega f(\vec x)H_0[H(\phi_0)-H(\phi_1)]d\vec x+\int_\Omega f(\vec x)[1-H(\phi_0)]d\vec x$             (21)

Then the region integral of a binary function $f(x,y)$ over the region $\Omega$ can be written as

$I_\Omega=\int_{\Omega}f(\vec x)d\vec x=\int_{\Omega}f(\vec x)H(\phi)d\vec x+\int_{\Omega}f(\vec x)[1-H(\phi)]d\vec x$                    (22)

#### edge Based

The boundary integral of $f(\vec x)$ along  the boundary of region $\Omega$ noted as $\partial\Omega$, where the LSF $\phi=0$, can be written as

$I_{\partial\Omega}=\int_{\partial\Omega}f(\vec x)d\vec x=\int_\Omega f(\vec x)\hat\delta_\phi(\vec x)d\vec x$                                                           (23)

$I_{\partial\Omega}=\int_\Omega f(\vec x)[H_1\delta(\phi_0)|\nabla\phi_0|+H_0\delta(\phi_1)|\nabla\phi_1|+\delta_1\delta(\phi_0)|\nabla(\frac{\phi_0+\phi_1}{2})|]d\vec x$

$\begin{matrix}I_{\partial\Omega}&=\int_\Omega f(\vec x)H_1\delta(\phi_0)|\nabla\phi_0|d\vec x\\&+\int_\Omega f(\vec x)H_0\delta(\phi_1)|\nabla\phi_1|d\vec x\\ &+\int_\Omega f(\vec x)\delta_1\delta(\phi_0)|\nabla(\frac{\phi_0+\phi_1}{2})|d\vec x\end{matrix}$                                                          (24)



