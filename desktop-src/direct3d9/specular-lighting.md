---
description: Die Modellierung von Spiegelung erfordert, dass das System nicht nur weiß, in welche Richtung Licht bewegt wird, sondern auch die Richtung zum Auge des Betrachters.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Specular Lighting (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b16d71bd8d814e104cf8a90d1d1fe9b15ba10f3
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343675"
---
# <a name="specular-lighting-direct3d-9"></a><span data-ttu-id="b47fb-103">Specular Lighting (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b47fb-103">Specular Lighting (Direct3D 9)</span></span>

<span data-ttu-id="b47fb-104">Die Modellierung von Spiegelung erfordert, dass das System nicht nur weiß, in welche Richtung Licht bewegt wird, sondern auch die Richtung zum Auge des Betrachters.</span><span class="sxs-lookup"><span data-stu-id="b47fb-104">Modeling specular reflection requires that the system not only know in what direction light is traveling, but also the direction to the viewer's eye.</span></span> <span data-ttu-id="b47fb-105">Das System verwendet eine vereinfachte Version des Phong-Specular-Reflektionsmodells, das einen Halbvektor verwendet, um die Intensität der spiegelförmigen Reflektion zu ungefähren.</span><span class="sxs-lookup"><span data-stu-id="b47fb-105">The system uses a simplified version of the Phong specular-reflection model, which employs a halfway vector to approximate the intensity of specular reflection.</span></span>

<span data-ttu-id="b47fb-106">Der Standardmäßige Beleuchtungszustand berechnet keine Glanzlichter.</span><span class="sxs-lookup"><span data-stu-id="b47fb-106">The default lighting state does not calculate specular highlights.</span></span> <span data-ttu-id="b47fb-107">Stellen Sie sicher, dass D3DRS SPECULARENABLE auf TRUE festgelegt ist, um die beleuchtungsförmige \_ Beleuchtung **zu aktivieren.**</span><span class="sxs-lookup"><span data-stu-id="b47fb-107">To enable specular lighting, be sure to set D3DRS\_SPECULARENABLE to **TRUE**.</span></span>

## <a name="specular-lighting-equation"></a><span data-ttu-id="b47fb-108">Specular Lighting Equation</span><span class="sxs-lookup"><span data-stu-id="b47fb-108">Specular Lighting Equation</span></span>

<span data-ttu-id="b47fb-109">Specular Lighting wird durch die folgende Gleichung beschrieben:</span><span class="sxs-lookup"><span data-stu-id="b47fb-109">Specular Lighting is described by the following equation:</span></span>

<span data-ttu-id="b47fb-110">**Specular Lighting = Cs \* sum \[ Ls \* (N · H)<sup>P</sup> \* Atten \* Spot\]**</span><span class="sxs-lookup"><span data-stu-id="b47fb-110">**Specular Lighting = Cₛ \* sum\[Lₛ \* (N · H)<sup>P</sup> \* Atten \* Spot\]**</span></span>



 

<span data-ttu-id="b47fb-111">In der folgenden Tabelle sind die Variablen, ihre Typen und ihre Bereiche aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b47fb-111">The following table identifies the variables, their types, and their ranges.</span></span>



| <span data-ttu-id="b47fb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b47fb-112">Parameter</span></span>    | <span data-ttu-id="b47fb-113">Standardwert</span><span class="sxs-lookup"><span data-stu-id="b47fb-113">Default value</span></span> | <span data-ttu-id="b47fb-114">Typ</span><span class="sxs-lookup"><span data-stu-id="b47fb-114">Type</span></span>          | <span data-ttu-id="b47fb-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b47fb-115">Description</span></span>                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b47fb-116">Cs</span><span class="sxs-lookup"><span data-stu-id="b47fb-116">Cₛ</span></span>           | <span data-ttu-id="b47fb-117">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="b47fb-117">(0,0,0,0)</span></span>     | <span data-ttu-id="b47fb-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="b47fb-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="b47fb-119">Specular-Farbe.</span><span class="sxs-lookup"><span data-stu-id="b47fb-119">Specular color.</span></span>                                                                                                     |
| <span data-ttu-id="b47fb-120">Sum</span><span class="sxs-lookup"><span data-stu-id="b47fb-120">sum</span></span>          | <span data-ttu-id="b47fb-121">–</span><span class="sxs-lookup"><span data-stu-id="b47fb-121">N/A</span></span>           | <span data-ttu-id="b47fb-122">–</span><span class="sxs-lookup"><span data-stu-id="b47fb-122">N/A</span></span>           | <span data-ttu-id="b47fb-123">Summierung der specular-Komponente jedes Lichts.</span><span class="sxs-lookup"><span data-stu-id="b47fb-123">Summation of each light's specular component.</span></span>                                                                       |
| <span data-ttu-id="b47fb-124">N</span><span class="sxs-lookup"><span data-stu-id="b47fb-124">N</span></span>            | <span data-ttu-id="b47fb-125">–</span><span class="sxs-lookup"><span data-stu-id="b47fb-125">N/A</span></span>           | <span data-ttu-id="b47fb-126">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="b47fb-126">D3DVECTOR</span></span>     | <span data-ttu-id="b47fb-127">Scheitelpunkt normal.</span><span class="sxs-lookup"><span data-stu-id="b47fb-127">Vertex normal.</span></span>                                                                                                      |
| <span data-ttu-id="b47fb-128">H</span><span class="sxs-lookup"><span data-stu-id="b47fb-128">H</span></span>            | <span data-ttu-id="b47fb-129">–</span><span class="sxs-lookup"><span data-stu-id="b47fb-129">N/A</span></span>           | <span data-ttu-id="b47fb-130">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="b47fb-130">D3DVECTOR</span></span>     | <span data-ttu-id="b47fb-131">Halbwegsvektor.</span><span class="sxs-lookup"><span data-stu-id="b47fb-131">Half way vector.</span></span> <span data-ttu-id="b47fb-132">Weitere Informationen finden Sie im Abschnitt zur Hälfte des Vektors.</span><span class="sxs-lookup"><span data-stu-id="b47fb-132">See the section on the halfway vector.</span></span>                                                             |
| <span data-ttu-id="b47fb-133"><sup>P</sup></span><span class="sxs-lookup"><span data-stu-id="b47fb-133"><sup>P</sup></span></span> | <span data-ttu-id="b47fb-134">0,0</span><span class="sxs-lookup"><span data-stu-id="b47fb-134">0.0</span></span>           | <span data-ttu-id="b47fb-135">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="b47fb-135">FLOAT</span></span>         | <span data-ttu-id="b47fb-136">Glanzreflektionsleistung.</span><span class="sxs-lookup"><span data-stu-id="b47fb-136">Specular reflection power.</span></span> <span data-ttu-id="b47fb-137">Der Bereich ist 0 bis +unendlich.</span><span class="sxs-lookup"><span data-stu-id="b47fb-137">Range is 0 to +infinity</span></span>                                                                  |
| <span data-ttu-id="b47fb-138">Ls</span><span class="sxs-lookup"><span data-stu-id="b47fb-138">Lₛ</span></span>           | <span data-ttu-id="b47fb-139">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="b47fb-139">(0,0,0,0)</span></span>     | <span data-ttu-id="b47fb-140">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="b47fb-140">D3DCOLORVALUE</span></span> | <span data-ttu-id="b47fb-141">Helle Glanzfarbe.</span><span class="sxs-lookup"><span data-stu-id="b47fb-141">Light specular color.</span></span>                                                                                               |
| <span data-ttu-id="b47fb-142">Atten</span><span class="sxs-lookup"><span data-stu-id="b47fb-142">Atten</span></span>        | <span data-ttu-id="b47fb-143">–</span><span class="sxs-lookup"><span data-stu-id="b47fb-143">N/A</span></span>           | <span data-ttu-id="b47fb-144">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="b47fb-144">FLOAT</span></span>         | <span data-ttu-id="b47fb-145">Leichter Dämpfungswert.</span><span class="sxs-lookup"><span data-stu-id="b47fb-145">Light attenuation value.</span></span> <span data-ttu-id="b47fb-146">Weitere Informationen finden Sie [unter Dämpfung und Spotlight-Faktor (Direct3D 9).](attenuation-and-spotlight-factor.md)</span><span class="sxs-lookup"><span data-stu-id="b47fb-146">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="b47fb-147">Sofortige Zahlung</span><span class="sxs-lookup"><span data-stu-id="b47fb-147">Spot</span></span>         | <span data-ttu-id="b47fb-148">–</span><span class="sxs-lookup"><span data-stu-id="b47fb-148">N/A</span></span>           | <span data-ttu-id="b47fb-149">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="b47fb-149">FLOAT</span></span>         | <span data-ttu-id="b47fb-150">Spotlight-Faktor.</span><span class="sxs-lookup"><span data-stu-id="b47fb-150">Spotlight factor.</span></span> <span data-ttu-id="b47fb-151">Weitere Informationen finden Sie [unter Dämpfung und Spotlight-Faktor (Direct3D 9).](attenuation-and-spotlight-factor.md)</span><span class="sxs-lookup"><span data-stu-id="b47fb-151">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>        |



 

<span data-ttu-id="b47fb-152">Der Wert für Cs lautet:</span><span class="sxs-lookup"><span data-stu-id="b47fb-152">The value for Cₛ is either:</span></span>


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   <span data-ttu-id="b47fb-153">vertex color1, wenn die Spiegelmaterialquelle D3DMCS COLOR1 ist \_ und die erste Scheitelpunktfarbe in der Scheitelpunktdeklaration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b47fb-153">vertex color1, if the specular material source is D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="b47fb-154">vertex color2, wenn die Spiegelmaterialquelle D3DMCS COLOR2 ist \_ und die zweite Scheitelpunktfarbe in der Scheitelpunktdeklaration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b47fb-154">vertex color2, if specular material source is D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="b47fb-155">material specular color (Materialspekularfarbe)</span><span class="sxs-lookup"><span data-stu-id="b47fb-155">material specular color</span></span>

> [!Note]  
> <span data-ttu-id="b47fb-156">Wenn eine der beiden Quelloptionen für Glanzmaterialien verwendet wird und die Scheitelpunktfarbe nicht angegeben wird, wird die Materialspekularfarbe verwendet.</span><span class="sxs-lookup"><span data-stu-id="b47fb-156">If either specular material source option is used and the vertex color is not provided, then the material specular color is used.</span></span>

 

<span data-ttu-id="b47fb-157">Glanzkomponenten werden so klammert, dass sie von 0 bis 255 liegen, nachdem alle Beleuchtungen separat verarbeitet und interpoliert wurden.</span><span class="sxs-lookup"><span data-stu-id="b47fb-157">Specular components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span>

## <a name="the-halfway-vector"></a><span data-ttu-id="b47fb-158">Der Halbwegvektor</span><span class="sxs-lookup"><span data-stu-id="b47fb-158">The Halfway Vector</span></span>

<span data-ttu-id="b47fb-159">Der halbe Vektor (H) befindet sich in der Mitte zwischen zwei Vektoren: der Vektor von einem Objektvertex zur Lichtquelle und der Vektor von einem Objektvertex zur Kameraposition.</span><span class="sxs-lookup"><span data-stu-id="b47fb-159">The halfway vector (H) exists midway between two vectors: the vector from an object vertex to the light source, and the vector from an object vertex to the camera position.</span></span> <span data-ttu-id="b47fb-160">Direct3D bietet zwei Möglichkeiten, den Mittelvektor zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="b47fb-160">Direct3D provides two ways to compute the halfway vector.</span></span> <span data-ttu-id="b47fb-161">Wenn D3DRS LOCALVIEWER auf TRUE festgelegt ist, berechnet das System den Hälftenvektor anhand der Position der Kamera und der Position des Scheitelpunkts zusammen mit dem Richtungsvektor des \_ Lichts. </span><span class="sxs-lookup"><span data-stu-id="b47fb-161">When D3DRS\_LOCALVIEWER is set to **TRUE**, the system calculates the halfway vector using the position of the camera and the position of the vertex, along with the light's direction vector.</span></span> <span data-ttu-id="b47fb-162">Die folgende Formel veranschaulicht dies.</span><span class="sxs-lookup"><span data-stu-id="b47fb-162">The following formula illustrates this.</span></span>

<span data-ttu-id="b47fb-163">**H = norm(norm(Cp - Vp) + L <sub>dir</sub>)**</span><span class="sxs-lookup"><span data-stu-id="b47fb-163">**H = norm(norm(Cₚ - Vₚ) + L<sub>dir</sub>)**</span></span>



 



| <span data-ttu-id="b47fb-164">Parameter</span><span class="sxs-lookup"><span data-stu-id="b47fb-164">Parameter</span></span>       | <span data-ttu-id="b47fb-165">Standardwert</span><span class="sxs-lookup"><span data-stu-id="b47fb-165">Default value</span></span> | <span data-ttu-id="b47fb-166">Typ</span><span class="sxs-lookup"><span data-stu-id="b47fb-166">Type</span></span>      | <span data-ttu-id="b47fb-167">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b47fb-167">Description</span></span>                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| <span data-ttu-id="b47fb-168">Cp</span><span class="sxs-lookup"><span data-stu-id="b47fb-168">Cₚ</span></span>              | <span data-ttu-id="b47fb-169">–</span><span class="sxs-lookup"><span data-stu-id="b47fb-169">N/A</span></span>           | <span data-ttu-id="b47fb-170">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="b47fb-170">D3DVECTOR</span></span> | <span data-ttu-id="b47fb-171">Kameraposition.</span><span class="sxs-lookup"><span data-stu-id="b47fb-171">Camera position.</span></span>                                             |
| <span data-ttu-id="b47fb-172">Vp</span><span class="sxs-lookup"><span data-stu-id="b47fb-172">Vₚ</span></span>              | <span data-ttu-id="b47fb-173">–</span><span class="sxs-lookup"><span data-stu-id="b47fb-173">N/A</span></span>           | <span data-ttu-id="b47fb-174">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="b47fb-174">D3DVECTOR</span></span> | <span data-ttu-id="b47fb-175">Scheitelpunktposition.</span><span class="sxs-lookup"><span data-stu-id="b47fb-175">Vertex position.</span></span>                                             |
| <span data-ttu-id="b47fb-176">L<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="b47fb-176">L<sub>dir</sub></span></span> | <span data-ttu-id="b47fb-177">–</span><span class="sxs-lookup"><span data-stu-id="b47fb-177">N/A</span></span>           | <span data-ttu-id="b47fb-178">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="b47fb-178">D3DVECTOR</span></span> | <span data-ttu-id="b47fb-179">Richtungsvektor von der Scheitelpunktposition zur Lichtposition.</span><span class="sxs-lookup"><span data-stu-id="b47fb-179">Direction vector from vertex position to the light position.</span></span> |



 

<span data-ttu-id="b47fb-180">Die Ermittlung des Hälftenvektors auf diese Weise kann rechenintensiv sein.</span><span class="sxs-lookup"><span data-stu-id="b47fb-180">Determining the halfway vector in this manner can be computationally intensive.</span></span> <span data-ttu-id="b47fb-181">Alternativ weist das Festlegen von D3DRS LOCALVIEWER = FALSE das System an, so zu agieren, als wäre der Blickpunkt unendlich weit von der \_ Z-Achse  entfernt.</span><span class="sxs-lookup"><span data-stu-id="b47fb-181">As an alternative, setting D3DRS\_LOCALVIEWER = **FALSE** instructs the system to act as though the viewpoint is infinitely distant on the z-axis.</span></span> <span data-ttu-id="b47fb-182">Dies wird in der folgenden Formel widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="b47fb-182">This is reflected in the following formula.</span></span>

<span data-ttu-id="b47fb-183">**H = norm((0,0,1) + L <sub>dir</sub>)**</span><span class="sxs-lookup"><span data-stu-id="b47fb-183">**H = norm((0,0,1) + L<sub>dir</sub>)**</span></span>



 

<span data-ttu-id="b47fb-184">Diese Einstellung ist weniger rechenintensiv, aber viel weniger genau, daher wird sie am besten von Anwendungen verwendet, die eine orthogonale Projektion verwenden.</span><span class="sxs-lookup"><span data-stu-id="b47fb-184">This setting is less computationally intensive, but much less accurate, so it is best used by applications that use orthogonal projection.</span></span>

## <a name="example"></a><span data-ttu-id="b47fb-185">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b47fb-185">Example</span></span>

<span data-ttu-id="b47fb-186">In diesem Beispiel wird das -Objekt mithilfe der Szenenspezifikationslichtfarbe und einer Materialspezifikationsfarbe farbig dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b47fb-186">In this example, the object is colored using the scene specular light color and a material specular color.</span></span> <span data-ttu-id="b47fb-187">Der Code ist unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b47fb-187">The code is shown below.</span></span>


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



<span data-ttu-id="b47fb-188">Gemäß der Gleichung ist die resultierende Farbe für die Objektvertices eine Kombination aus der Materialfarbe und der hellen Farbe.</span><span class="sxs-lookup"><span data-stu-id="b47fb-188">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="b47fb-189">Die folgenden beiden Abbildungen zeigen die Farbe des Glanzmaterials , die grau ist, und die Glanzlichtfarbe, die weiß ist.</span><span class="sxs-lookup"><span data-stu-id="b47fb-189">The following two illustration show the specular material color, which is gray, and the specular light color, which is white.</span></span>

![Abbildung einer grauen Kugel](images/amb1.jpg)![Abbildung einer weißen Kugel](images/lightwhite.jpg)

<span data-ttu-id="b47fb-192">Die resultierende Glanzlichtermarkerung wird in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b47fb-192">The resulting specular highlight is shown in the following illustration.</span></span>

![Abbildung des Glanzlichts](images/lights.jpg)

<span data-ttu-id="b47fb-194">Die Kombination des Glanzlichts mit der Umgebungs- und diffusen Beleuchtung erzeugt die folgende Abbildung.</span><span class="sxs-lookup"><span data-stu-id="b47fb-194">Combining the specular highlight with the ambient and diffuse lighting produces the following illustration.</span></span> <span data-ttu-id="b47fb-195">Wenn alle drei Arten von Beleuchtung angewendet werden, ähnelt dies eindeutiger einem realistischen Objekt.</span><span class="sxs-lookup"><span data-stu-id="b47fb-195">With all three types of lighting applied, this more clearly resembles a realistic object.</span></span>

![Abbildung der Kombination von Glanzlicht, Umgebungslicht und diffuser Beleuchtung](images/lightads.jpg)

<span data-ttu-id="b47fb-197">Die Berechnung der Glanzlichter ist aufwendiger als die diffuse Beleuchtung.</span><span class="sxs-lookup"><span data-stu-id="b47fb-197">Specular lighting is more intensive to calculate than diffuse lighting.</span></span> <span data-ttu-id="b47fb-198">Es wird in der Regel verwendet, um visuelle Hinweise zum Oberflächenmaterial bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b47fb-198">It is typically used to provide visual clues about the surface material.</span></span> <span data-ttu-id="b47fb-199">Die Glanzlichter unterscheiden sich in Größe und Farbe mit dem Material der Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="b47fb-199">The specular highlight varies in size and color with the material of the surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b47fb-200">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b47fb-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b47fb-201">Mathematik der Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="b47fb-201">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



