# Designing the external force field for the morphological term



The velocity field, serving as an external force field for contour evolution, needs to be designed to achieve the segmentation of overlapping cells.  For simplicity, we reassign the velocity field $vH_0$ in the integrand of the morphological term $\mathrm{M}(\phi)=\int vH_0 \phi d \vec{x}$ (denoted by Eq.12 in the paper) as $h$.  In order to induce contour evolution in a manner akin to the drainage process of the watershed method mentioned in the paper, the velocity field $h$, serving as the external force term for contour evolution, demands meticulous design.  As described in the paper, the drainage process leaves behind textures inside the region, which contain the contour of cell instances in overlapping areas. Therefore, to distinguish it from simple morphological transformations, we have renamed the morphological term  $\mathrm{M}(\phi)$ as the texture term：

$\mathrm{T}(\phi)=\int h \phi d \vec{x}$

Specifically, we designed the external force field $h$ based on the contour of the evolving region and the detected cutting line from the preceding segmentation step. Due to space limitations, we summarize the detailed exposition using Chinese, including variable definitions and derivation process, in pages 101 to 102 of the [dissertation](http://ir.sia.cn/handle/173321/33300?mode=full&submit_simple=Show+full+item+record) *(Title: Research on Dual-stage Accurate Segmentation Method of*
*Cevical Cell Smear Images*). Additionally, the comprehensive derivation of the mathmatical toolbox for DCTLSM method proposed by the papar is also summarized in pages 36 to 39  and pages 151 to 156  of the dissertation. 

