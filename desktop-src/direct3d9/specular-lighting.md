---
description: Das Modellieren von Glanz Reflektion erfordert, dass das System nicht nur weiß, in welcher Richtung das Licht unterwegs ist, sondern auch die Richtung des Viewers.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Glanz Beleuchtung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab378d4ca3f00ef81c5048e6ad6cc85eaeb18ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569457"
---
# <a name="specular-lighting-direct3d-9"></a><span data-ttu-id="ef1fc-103">Glanz Beleuchtung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ef1fc-103">Specular Lighting (Direct3D 9)</span></span>

<span data-ttu-id="ef1fc-104">Das Modellieren von Glanz Reflektion erfordert, dass das System nicht nur weiß, in welcher Richtung das Licht unterwegs ist, sondern auch die Richtung des Viewers.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-104">Modeling specular reflection requires that the system not only know in what direction light is traveling, but also the direction to the viewer's eye.</span></span> <span data-ttu-id="ef1fc-105">Das System verwendet eine vereinfachte Version des Phong-reflektionsmodells, das einen halben Vektor verwendet, um die Intensität der Glanz Reflektion zu annähern.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-105">The system uses a simplified version of the Phong specular-reflection model, which employs a halfway vector to approximate the intensity of specular reflection.</span></span>

<span data-ttu-id="ef1fc-106">Der Standard Beleuchtungs Zustand berechnet keine Glanzlichter.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-106">The default lighting state does not calculate specular highlights.</span></span> <span data-ttu-id="ef1fc-107">Um die Glanz Beleuchtung zu aktivieren, stellen Sie sicher, dass D3DRS \_ specularenable auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-107">To enable specular lighting, be sure to set D3DRS\_SPECULARENABLE to **TRUE**.</span></span>

## <a name="specular-lighting-equation"></a><span data-ttu-id="ef1fc-108">Glanzlicht Gleichung</span><span class="sxs-lookup"><span data-stu-id="ef1fc-108">Specular Lighting Equation</span></span>

<span data-ttu-id="ef1fc-109">Die Glanz Beleuchtung wird durch die folgende Gleichung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-109">Specular Lighting is described by the following equation.</span></span>



|                                                                             |
|-----------------------------------------------------------------------------|
| <span data-ttu-id="ef1fc-110">Glanz Beleuchtung = CS \* Sum \[ ls \* (N) H)<sup>P</sup> \* - \* Punkt-Punkt\]</span><span class="sxs-lookup"><span data-stu-id="ef1fc-110">Specular Lighting = Cₛ \* sum\[Lₛ \* (N · H)<sup>P</sup> \* Atten \* Spot\]</span></span> |



 

<span data-ttu-id="ef1fc-111">In der folgenden Tabelle werden die Variablen, ihre Typen und ihre Bereiche aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-111">The following table identifies the variables, their types, and their ranges.</span></span>



| <span data-ttu-id="ef1fc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef1fc-112">Parameter</span></span>    | <span data-ttu-id="ef1fc-113">Standardwert</span><span class="sxs-lookup"><span data-stu-id="ef1fc-113">Default value</span></span> | <span data-ttu-id="ef1fc-114">type</span><span class="sxs-lookup"><span data-stu-id="ef1fc-114">Type</span></span>          | <span data-ttu-id="ef1fc-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef1fc-115">Description</span></span>                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1fc-116">CS</span><span class="sxs-lookup"><span data-stu-id="ef1fc-116">Cₛ</span></span>           | <span data-ttu-id="ef1fc-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="ef1fc-117">(0,0,0,0)</span></span>     | <span data-ttu-id="ef1fc-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="ef1fc-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="ef1fc-119">Glanz Farbe.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-119">Specular color.</span></span>                                                                                                     |
| <span data-ttu-id="ef1fc-120">Sum</span><span class="sxs-lookup"><span data-stu-id="ef1fc-120">sum</span></span>          | <span data-ttu-id="ef1fc-121">–</span><span class="sxs-lookup"><span data-stu-id="ef1fc-121">N/A</span></span>           | <span data-ttu-id="ef1fc-122">–</span><span class="sxs-lookup"><span data-stu-id="ef1fc-122">N/A</span></span>           | <span data-ttu-id="ef1fc-123">Sumpunktions Zeichen für die Glanz Komponente der einzelnen Leuchten.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-123">Summation of each light's specular component.</span></span>                                                                       |
| <span data-ttu-id="ef1fc-124">N</span><span class="sxs-lookup"><span data-stu-id="ef1fc-124">N</span></span>            | <span data-ttu-id="ef1fc-125">–</span><span class="sxs-lookup"><span data-stu-id="ef1fc-125">N/A</span></span>           | <span data-ttu-id="ef1fc-126">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="ef1fc-126">D3DVECTOR</span></span>     | <span data-ttu-id="ef1fc-127">Vertex normal.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-127">Vertex normal.</span></span>                                                                                                      |
| <span data-ttu-id="ef1fc-128">H</span><span class="sxs-lookup"><span data-stu-id="ef1fc-128">H</span></span>            | <span data-ttu-id="ef1fc-129">–</span><span class="sxs-lookup"><span data-stu-id="ef1fc-129">N/A</span></span>           | <span data-ttu-id="ef1fc-130">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="ef1fc-130">D3DVECTOR</span></span>     | <span data-ttu-id="ef1fc-131">Halber-Wege-Vektor.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-131">Half way vector.</span></span> <span data-ttu-id="ef1fc-132">Weitere Informationen finden Sie im Abschnitt zum halben Vektor.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-132">See the section on the halfway vector.</span></span>                                                             |
| <span data-ttu-id="ef1fc-133"><sup>P</sup></span><span class="sxs-lookup"><span data-stu-id="ef1fc-133"><sup>P</sup></span></span> | <span data-ttu-id="ef1fc-134">0,0</span><span class="sxs-lookup"><span data-stu-id="ef1fc-134">0.0</span></span>           | <span data-ttu-id="ef1fc-135">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="ef1fc-135">FLOAT</span></span>         | <span data-ttu-id="ef1fc-136">Glanz Fähigkeit der Reflektion.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-136">Specular reflection power.</span></span> <span data-ttu-id="ef1fc-137">Der Bereich liegt zwischen 0 und + unendlich.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-137">Range is 0 to +infinity</span></span>                                                                  |
| <span data-ttu-id="ef1fc-138">Ls</span><span class="sxs-lookup"><span data-stu-id="ef1fc-138">Lₛ</span></span>           | <span data-ttu-id="ef1fc-139">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="ef1fc-139">(0,0,0,0)</span></span>     | <span data-ttu-id="ef1fc-140">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="ef1fc-140">D3DCOLORVALUE</span></span> | <span data-ttu-id="ef1fc-141">Helle Glanz Farbe.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-141">Light specular color.</span></span>                                                                                               |
| <span data-ttu-id="ef1fc-142">Ratte</span><span class="sxs-lookup"><span data-stu-id="ef1fc-142">Atten</span></span>        | <span data-ttu-id="ef1fc-143">–</span><span class="sxs-lookup"><span data-stu-id="ef1fc-143">N/A</span></span>           | <span data-ttu-id="ef1fc-144">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="ef1fc-144">FLOAT</span></span>         | <span data-ttu-id="ef1fc-145">Heller Dämpfungswert.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-145">Light attenuation value.</span></span> <span data-ttu-id="ef1fc-146">Siehe [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="ef1fc-146">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="ef1fc-147">Sofortige Zahlung</span><span class="sxs-lookup"><span data-stu-id="ef1fc-147">Spot</span></span>         | <span data-ttu-id="ef1fc-148">–</span><span class="sxs-lookup"><span data-stu-id="ef1fc-148">N/A</span></span>           | <span data-ttu-id="ef1fc-149">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="ef1fc-149">FLOAT</span></span>         | <span data-ttu-id="ef1fc-150">Spotlight-Faktor.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-150">Spotlight factor.</span></span> <span data-ttu-id="ef1fc-151">Siehe [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="ef1fc-151">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>        |



 

<span data-ttu-id="ef1fc-152">Der Wert für CS lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ef1fc-152">The value for Cₛ is either:</span></span>


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   <span data-ttu-id="ef1fc-153">Vertex color1, wenn die Glanz materialquelle D3DMCS \_ color1 und die erste Scheitelpunkt Farbe in der Scheitelpunkt Deklaration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-153">vertex color1, if the specular material source is D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="ef1fc-154">Vertex color2, wenn die Glanz materialquelle D3DMCS \_ color2 ist, und die zweite Scheitelpunkt Farbe in der Vertex-Deklaration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-154">vertex color2, if specular material source is D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="ef1fc-155">Material Glanz Farbe</span><span class="sxs-lookup"><span data-stu-id="ef1fc-155">material specular color</span></span>

> [!Note]  
> <span data-ttu-id="ef1fc-156">Wenn eine der beiden Optionen für die Quell Text Quelle verwendet wird und die Scheitelpunkt Farbe nicht angegeben wird, wird die Glanz Farbe für das Material verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-156">If either specular material source option is used and the vertex color is not provided, then the material specular color is used.</span></span>

 

<span data-ttu-id="ef1fc-157">Glanz Komponenten werden an einen Wert zwischen 0 und 255 gebunden, nachdem alle Lichter separat verarbeitet und interpoliert wurden.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-157">Specular components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span>

## <a name="the-halfway-vector"></a><span data-ttu-id="ef1fc-158">Der halbe Vektor</span><span class="sxs-lookup"><span data-stu-id="ef1fc-158">The Halfway Vector</span></span>

<span data-ttu-id="ef1fc-159">Der halbe Vektor (H) ist in der Mitte zwischen zwei Vektoren vorhanden: der Vektor von einem Objekt Scheitelpunkt zur hellen Quelle und der Vektor von einem Objekt Scheitelpunkt bis zur Kameraposition.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-159">The halfway vector (H) exists midway between two vectors: the vector from an object vertex to the light source, and the vector from an object vertex to the camera position.</span></span> <span data-ttu-id="ef1fc-160">Direct3D bietet zwei Möglichkeiten, den halbvektor zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-160">Direct3D provides two ways to compute the halfway vector.</span></span> <span data-ttu-id="ef1fc-161">Wenn D3DRS \_ localviewer auf **true** festgelegt ist, berechnet das System den halben Vektor mithilfe der Position der Kamera und der Position des Scheitel Punkts, zusammen mit dem Richtungsvektor des Lichts.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-161">When D3DRS\_LOCALVIEWER is set to **TRUE**, the system calculates the halfway vector using the position of the camera and the position of the vertex, along with the light's direction vector.</span></span> <span data-ttu-id="ef1fc-162">Dies wird in der folgenden Formel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-162">The following formula illustrates this.</span></span>



|                                           |
|-------------------------------------------|
| <span data-ttu-id="ef1fc-163">H = Norm (Norm (CP-VP) + L-<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="ef1fc-163">H = norm(norm(Cₚ - Vₚ) + L<sub>dir</sub>)</span></span> |



 



| <span data-ttu-id="ef1fc-164">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef1fc-164">Parameter</span></span>       | <span data-ttu-id="ef1fc-165">Standardwert</span><span class="sxs-lookup"><span data-stu-id="ef1fc-165">Default value</span></span> | <span data-ttu-id="ef1fc-166">type</span><span class="sxs-lookup"><span data-stu-id="ef1fc-166">Type</span></span>      | <span data-ttu-id="ef1fc-167">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef1fc-167">Description</span></span>                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| <span data-ttu-id="ef1fc-168">Erfolgen</span><span class="sxs-lookup"><span data-stu-id="ef1fc-168">Cₚ</span></span>              | <span data-ttu-id="ef1fc-169">–</span><span class="sxs-lookup"><span data-stu-id="ef1fc-169">N/A</span></span>           | <span data-ttu-id="ef1fc-170">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="ef1fc-170">D3DVECTOR</span></span> | <span data-ttu-id="ef1fc-171">Kameraposition.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-171">Camera position.</span></span>                                             |
| <span data-ttu-id="ef1fc-172">Füttern</span><span class="sxs-lookup"><span data-stu-id="ef1fc-172">Vₚ</span></span>              | <span data-ttu-id="ef1fc-173">–</span><span class="sxs-lookup"><span data-stu-id="ef1fc-173">N/A</span></span>           | <span data-ttu-id="ef1fc-174">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="ef1fc-174">D3DVECTOR</span></span> | <span data-ttu-id="ef1fc-175">Vertex-Position.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-175">Vertex position.</span></span>                                             |
| <span data-ttu-id="ef1fc-176">L-<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="ef1fc-176">L<sub>dir</sub></span></span> | <span data-ttu-id="ef1fc-177">–</span><span class="sxs-lookup"><span data-stu-id="ef1fc-177">N/A</span></span>           | <span data-ttu-id="ef1fc-178">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="ef1fc-178">D3DVECTOR</span></span> | <span data-ttu-id="ef1fc-179">Richtung Vektor von Scheitelpunkt Position zur hellen Position.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-179">Direction vector from vertex position to the light position.</span></span> |



 

<span data-ttu-id="ef1fc-180">Die Bestimmung des halb möglichen Vektors auf diese Weise kann Rechen intensiv sein.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-180">Determining the halfway vector in this manner can be computationally intensive.</span></span> <span data-ttu-id="ef1fc-181">Alternativ \_ weist das Festlegen von D3DRS localviewer = **false** das System an, so zu agieren, als ob der Standpunkt auf der z-Achse unendlich weit entfernt ist.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-181">As an alternative, setting D3DRS\_LOCALVIEWER = **FALSE** instructs the system to act as though the viewpoint is infinitely distant on the z-axis.</span></span> <span data-ttu-id="ef1fc-182">Dies wird in der folgenden Formel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-182">This is reflected in the following formula.</span></span>



|                                     |
|-------------------------------------|
| <span data-ttu-id="ef1fc-183">H = Norm ((0,0) + L-<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="ef1fc-183">H = norm((0,0,1) + L<sub>dir</sub>)</span></span> |



 

<span data-ttu-id="ef1fc-184">Diese Einstellung ist weniger Rechen intensiv, aber weitaus weniger genau. Sie wird daher am besten von Anwendungen verwendet, die eine orthogonale Projektion verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-184">This setting is less computationally intensive, but much less accurate, so it is best used by applications that use orthogonal projection.</span></span>

## <a name="example"></a><span data-ttu-id="ef1fc-185">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ef1fc-185">Example</span></span>

<span data-ttu-id="ef1fc-186">In diesem Beispiel wird das-Objekt mithilfe der Glanzlicht Farbe der Szene und einer hellen Glanz Farbe gefärbt.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-186">In this example, the object is colored using the scene specular light color and a material specular color.</span></span> <span data-ttu-id="ef1fc-187">Der Code wird unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-187">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

light.Specular.r = 1.0f;
light.Specular.g = 1.0f;
light.Specular.b = 1.0f;
light.Specular.a = 1.0f;

light.Range = 1000;
light.Falloff = 0;
light.Attenuation0 = 1;
light.Attenuation1 = 0;
light.Attenuation2 = 0;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );
m_pd3dDevice->SetRenderState( D3DRS_SPECULARENABLE, TRUE );

mtrl.Specular.r = 0.5f;
mtrl.Specular.g = 0.5f;
mtrl.Specular.b = 0.5f;
mtrl.Specular.a = 0.5f;
mtrl.Power = 20;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_SPECULARMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="ef1fc-188">Gemäß der Gleichung ist die resultierende Farbe für die Objekt Vertices eine Kombination aus der Material Farbe und der hellen Farbe.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-188">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="ef1fc-189">Die folgende Abbildung zeigt die Glanz Farbe, die grau ist, und die helle helle Farbe, die weiß ist.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-189">The following two illustration show the specular material color, which is gray, and the specular light color, which is white.</span></span>

![Abbildung einer grauen Kugel](images/amb1.jpg)![Abbildung einer weißen Kugel](images/lightwhite.jpg)

<span data-ttu-id="ef1fc-192">Die sich ergebende Glanz Markierung wird in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-192">The resulting specular highlight is shown in the following illustration.</span></span>

![Abbildung der Glanz Markierung](images/lights.jpg)

<span data-ttu-id="ef1fc-194">Die Kombination der Glanz Markierung mit der Ambient-und diffuse Beleuchtung ergibt die folgende Abbildung.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-194">Combining the specular highlight with the ambient and diffuse lighting produces the following illustration.</span></span> <span data-ttu-id="ef1fc-195">Wenn alle drei Arten von Beleuchtung angewendet werden, ähnelt dies deutlich einem realistischen Objekt.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-195">With all three types of lighting applied, this more clearly resembles a realistic object.</span></span>

![Darstellung der Kombination der Glanz Markierung, der Umgebungsbeleuchtung und der diffusen Beleuchtung](images/lightads.jpg)

<span data-ttu-id="ef1fc-197">Die Glanz Beleuchtung ist intensiver zu berechnen als diffuses Beleuchtung.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-197">Specular lighting is more intensive to calculate than diffuse lighting.</span></span> <span data-ttu-id="ef1fc-198">Sie wird in der Regel verwendet, um visuelle Hinweise zum Oberflächenmaterial bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-198">It is typically used to provide visual clues about the surface material.</span></span> <span data-ttu-id="ef1fc-199">Die Glanz Markierung variiert in Größe und Farbe mit dem Material der-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="ef1fc-199">The specular highlight varies in size and color with the material of the surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef1fc-200">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef1fc-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef1fc-201">Mathematik der Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="ef1fc-201">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



