---
description: Nach der Anpassung der Lichtintensität für alle Dämpfungseffekte berechnet die Beleuchtungs-Engine, wie viel von dem verbleibenden Licht von einem Scheitelpunkt reflektiert wird, wenn der Winkel des Scheitel Punkts normal und die Richtung des Vorfall Lichts angezeigt wird.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Diffuse Beleuchtung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51e45093786348aaa115ec38c420acec471f718
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123374"
---
# <a name="diffuse-lighting-direct3d-9"></a><span data-ttu-id="35819-103">Diffuse Beleuchtung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="35819-103">Diffuse Lighting (Direct3D 9)</span></span>

<span data-ttu-id="35819-104">Nach der Anpassung der Lichtintensität für alle Dämpfungseffekte berechnet die Beleuchtungs-Engine, wie viel von dem verbleibenden Licht von einem Scheitelpunkt reflektiert wird, wenn der Winkel des Scheitel Punkts normal und die Richtung des Vorfall Lichts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="35819-104">After adjusting the light intensity for any attenuation effects, the lighting engine computes how much of the remaining light reflects from a vertex, given the angle of the vertex normal and the direction of the incident light.</span></span> <span data-ttu-id="35819-105">Die Beleuchtungs-Engine überspringt diesen Schritt für direktionale Lichter, da Sie nicht über die Entfernung gedämpft werden.</span><span class="sxs-lookup"><span data-stu-id="35819-105">The lighting engine skips to this step for directional lights because they do not attenuate over distance.</span></span> <span data-ttu-id="35819-106">Das System berücksichtigt zwei reflektionstypen (diffuses und Glanz) und verwendet eine andere Formel, um zu bestimmen, wie viel Licht für jede reflektiert wird.</span><span class="sxs-lookup"><span data-stu-id="35819-106">The system considers two reflection types, diffuse and specular, and uses a different formula to determine how much light is reflected for each.</span></span> <span data-ttu-id="35819-107">Nach dem Berechnen der Menge an Licht, die reflektiert wird, wendet Direct3D diese neuen Werte auf die diffusen und Glanz enden Reflectance-Eigenschaften des aktuellen Materials an.</span><span class="sxs-lookup"><span data-stu-id="35819-107">After calculating the amounts of light reflected, Direct3D applies these new values to the diffuse and specular reflectance properties of the current material.</span></span> <span data-ttu-id="35819-108">Die sich ergebenden Farbwerte sind die diffusen und Glanz baren Komponenten, die vom Raster verwendet werden, um die Schattierung und Glanz Markierung von Gouraud zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="35819-108">The resulting color values are the diffuse and specular components that the rasterizer uses to produce Gouraud shading and specular highlighting.</span></span>

<span data-ttu-id="35819-109">Diffuses Beleuchtung wird durch die folgende Gleichung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="35819-109">Diffuse lighting is described by the following equation.</span></span>

<span data-ttu-id="35819-110">Diffuse Beleuchtung = Sum \[ C<sub>d</sub> \* L<sub>d</sub> \* (N)<sup>.</sup> L<sub>dir</sub>) \* \* Punktposition\]</span><span class="sxs-lookup"><span data-stu-id="35819-110">Diffuse Lighting = sum\[C<sub>d</sub>\*L<sub>d</sub>\*(N<sup>.</sup>L<sub>dir</sub>)\*Atten\*Spot\]</span></span>



| <span data-ttu-id="35819-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="35819-111">Parameter</span></span>       | <span data-ttu-id="35819-112">Standardwert</span><span class="sxs-lookup"><span data-stu-id="35819-112">Default value</span></span> | <span data-ttu-id="35819-113">type</span><span class="sxs-lookup"><span data-stu-id="35819-113">Type</span></span>          | <span data-ttu-id="35819-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35819-114">Description</span></span>                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35819-115">Sum</span><span class="sxs-lookup"><span data-stu-id="35819-115">sum</span></span>             | <span data-ttu-id="35819-116">–</span><span class="sxs-lookup"><span data-stu-id="35819-116">N/A</span></span>           | <span data-ttu-id="35819-117">–</span><span class="sxs-lookup"><span data-stu-id="35819-117">N/A</span></span>           | <span data-ttu-id="35819-118">Sumdieren der diffusen Komponente jeder Beleuchtung.</span><span class="sxs-lookup"><span data-stu-id="35819-118">Summation of each light's diffuse component.</span></span>                                                                  |
| <span data-ttu-id="35819-119">C<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="35819-119">C<sub>d</sub></span></span>   | <span data-ttu-id="35819-120">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="35819-120">(0,0,0,0)</span></span>     | <span data-ttu-id="35819-121">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="35819-121">D3DCOLORVALUE</span></span> | <span data-ttu-id="35819-122">Diffuse Farbe.</span><span class="sxs-lookup"><span data-stu-id="35819-122">Diffuse color.</span></span>                                                                                                |
| <span data-ttu-id="35819-123">L<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="35819-123">L<sub>d</sub></span></span>   | <span data-ttu-id="35819-124">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="35819-124">(0,0,0,0)</span></span>     | <span data-ttu-id="35819-125">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="35819-125">D3DCOLORVALUE</span></span> | <span data-ttu-id="35819-126">Helle diffuse Farbe.</span><span class="sxs-lookup"><span data-stu-id="35819-126">Light diffuse color.</span></span>                                                                                          |
| <span data-ttu-id="35819-127">N</span><span class="sxs-lookup"><span data-stu-id="35819-127">N</span></span>               | <span data-ttu-id="35819-128">–</span><span class="sxs-lookup"><span data-stu-id="35819-128">N/A</span></span>           | <span data-ttu-id="35819-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="35819-129">D3DVECTOR</span></span>     | <span data-ttu-id="35819-130">Scheitelpunkt normal</span><span class="sxs-lookup"><span data-stu-id="35819-130">Vertex normal</span></span>                                                                                                 |
| <span data-ttu-id="35819-131">L-<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="35819-131">L<sub>dir</sub></span></span> | <span data-ttu-id="35819-132">–</span><span class="sxs-lookup"><span data-stu-id="35819-132">N/A</span></span>           | <span data-ttu-id="35819-133">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="35819-133">D3DVECTOR</span></span>     | <span data-ttu-id="35819-134">Richtung Vektor von Objekt Scheitelpunkt zu Licht.</span><span class="sxs-lookup"><span data-stu-id="35819-134">Direction vector from object vertex to the light.</span></span>                                                             |
| <span data-ttu-id="35819-135">Ratte</span><span class="sxs-lookup"><span data-stu-id="35819-135">Atten</span></span>           | <span data-ttu-id="35819-136">–</span><span class="sxs-lookup"><span data-stu-id="35819-136">N/A</span></span>           | <span data-ttu-id="35819-137">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="35819-137">FLOAT</span></span>         | <span data-ttu-id="35819-138">Licht Dämpfung.</span><span class="sxs-lookup"><span data-stu-id="35819-138">Light attenuation.</span></span> <span data-ttu-id="35819-139">Siehe [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="35819-139">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="35819-140">Sofortige Zahlung</span><span class="sxs-lookup"><span data-stu-id="35819-140">Spot</span></span>            | <span data-ttu-id="35819-141">–</span><span class="sxs-lookup"><span data-stu-id="35819-141">N/A</span></span>           | <span data-ttu-id="35819-142">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="35819-142">FLOAT</span></span>         | <span data-ttu-id="35819-143">Spotlight-Faktor.</span><span class="sxs-lookup"><span data-stu-id="35819-143">Spotlight factor.</span></span> <span data-ttu-id="35819-144">Siehe [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="35819-144">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |



 

<span data-ttu-id="35819-145">Der Wert für C<sub>d</sub> ist entweder:</span><span class="sxs-lookup"><span data-stu-id="35819-145">The value for C<sub>d</sub> is either:</span></span>

-   <span data-ttu-id="35819-146">Vertex color1, wenn DiffuseMaterialSource = D3DMCS \_ color1 und die erste Scheitelpunkt Farbe in der Vertex-Deklaration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="35819-146">vertex color1, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="35819-147">Vertex color2, wenn DiffuseMaterialSource = D3DMCS \_ color2 und die zweite Scheitelpunkt Farbe in der Vertex-Deklaration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="35819-147">vertex color2, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="35819-148">Material diffuse Farbe</span><span class="sxs-lookup"><span data-stu-id="35819-148">material diffuse color</span></span>

> [!Note]  
> <span data-ttu-id="35819-149">Wenn eine der beiden Optionen DiffuseMaterialSource verwendet wird und die Scheitelpunkt Farbe nicht angegeben wird, wird die diffuse Farbe des Materials verwendet.</span><span class="sxs-lookup"><span data-stu-id="35819-149">If either DIFFUSEMATERIALSOURCE option is used, and the vertex color is not provided, the material diffuse color is used.</span></span>

 

<span data-ttu-id="35819-150">Informationen zum Berechnen der Dämpfungs-oder Spotlight-Merkmale (Spot) finden Sie unter [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="35819-150">To calculate the attenuation (Atten) or the spotlight characteristics (Spot), see [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>

<span data-ttu-id="35819-151">Bei diffusen Komponenten wird der Wert zwischen 0 und 255 gebunden, nachdem alle Lichter separat verarbeitet und interpoliert wurden.</span><span class="sxs-lookup"><span data-stu-id="35819-151">Diffuse components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span> <span data-ttu-id="35819-152">Der resultierende diffuses Beleuchtungs Wert ist eine Kombination aus Ambient-, diff-und selbst leuchtendes-hellen Werten.</span><span class="sxs-lookup"><span data-stu-id="35819-152">The resulting diffuse lighting value is a combination of the ambient, diffuse and emissive light values.</span></span>

## <a name="example"></a><span data-ttu-id="35819-153">Beispiel</span><span class="sxs-lookup"><span data-stu-id="35819-153">Example</span></span>

<span data-ttu-id="35819-154">In diesem Beispiel wird das-Objekt mithilfe der hellen diffusen Farbe und einer Material diffusen Farbe gefärbt.</span><span class="sxs-lookup"><span data-stu-id="35819-154">In this example, the object is colored using the light diffuse color and a material diffuse color.</span></span> <span data-ttu-id="35819-155">Der Code wird unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="35819-155">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

// set directional light diffuse color
light.Diffuse.r = 1.0f;
light.Diffuse.g = 1.0f;
light.Diffuse.b = 1.0f;
light.Diffuse.a = 1.0f;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );

// if a material is used, SetRenderState must be used
// vertex color = light diffuse color * material diffuse color
mtrl.Diffuse.r = 0.75f;
mtrl.Diffuse.g = 0.0f;
mtrl.Diffuse.b = 0.0f;
mtrl.Diffuse.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="35819-156">Gemäß der Gleichung ist die resultierende Farbe für die Objekt Vertices eine Kombination aus der Material Farbe und der hellen Farbe.</span><span class="sxs-lookup"><span data-stu-id="35819-156">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="35819-157">Die beiden folgenden Abbildungen zeigen die Material Farbe, die grau ist, und die helle Farbe, die hell rot ist.</span><span class="sxs-lookup"><span data-stu-id="35819-157">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![Abbildung einer grauen Kugel](images/amb1.jpg)![Abbildung einer roten Kugel](images/lightred.jpg)

<span data-ttu-id="35819-160">Die resultierende Szene wird in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="35819-160">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="35819-161">Das einzige Objekt in der Szene ist eine Kugel.</span><span class="sxs-lookup"><span data-stu-id="35819-161">The only object in the scene is a sphere.</span></span> <span data-ttu-id="35819-162">Bei der Berechnung der diffusen Beleuchtung werden das Material und die helle diffuse Farbe geändert und mit dem Punktprodukt um den Winkel zwischen der Lichtrichtung und dem Scheitelpunkt (Scheitelpunkt) geändert.</span><span class="sxs-lookup"><span data-stu-id="35819-162">The diffuse lighting calculation takes the material and light diffuse color and modifies it by the angle between the light direction and the vertex normal using the dot product.</span></span> <span data-ttu-id="35819-163">Folglich wird die Rückseite der Kugel dunkler, wenn sich die Oberfläche der Kugel von der Lichtfläche Weg lässt.</span><span class="sxs-lookup"><span data-stu-id="35819-163">As a result, the backside of the sphere gets darker as the surface of the sphere curves away from the light.</span></span>

![Abbildung einer Kugel mit diffuses Beleuchtung](images/lightd.jpg)

<span data-ttu-id="35819-165">Durch die Kombination der diffusen Beleuchtung mit der Ambient-Beleuchtung aus dem vorherigen Beispiel wird die gesamte Oberfläche des Objekts schattiert.</span><span class="sxs-lookup"><span data-stu-id="35819-165">Combining the diffuse lighting with the ambient lighting from the previous example shades the entire surface of the object.</span></span> <span data-ttu-id="35819-166">Die Umgebungsbeleuchtung schattiert die gesamte Oberfläche, und das diffuse Licht trägt dazu bei, die 3D-Form des Objekts zu verdeutlichen, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="35819-166">The ambient light shades the entire surface and the diffuse light helps reveal the object's 3D shape, as shown in the following illustration.</span></span>

![Abbildung einer Kugel mit diffuses Beleuchtung und Umgebungsbeleuchtung](images/lightad.jpg)

<span data-ttu-id="35819-168">Die Berechnung der diffusen Beleuchtung ist intensiver als Umgebungsbeleuchtung.</span><span class="sxs-lookup"><span data-stu-id="35819-168">Diffuse lighting is more intensive to calculate than ambient lighting.</span></span> <span data-ttu-id="35819-169">Da es von den Scheitelpunkt normalen und der Lichtrichtung abhängt, können Sie die Objekte Geometrie im 3D-Raum sehen, was eine realistischere Beleuchtung als Umgebungsbeleuchtung erzeugt.</span><span class="sxs-lookup"><span data-stu-id="35819-169">Because it depends on the vertex normals and light direction, you can see the objects geometry in 3D space, which produces a more realistic lighting than ambient lighting.</span></span> <span data-ttu-id="35819-170">Sie können Glanzlichter verwenden, um ein realistischeres Aussehen zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="35819-170">You can use specular highlights to achieve a more realistic look.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35819-171">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="35819-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35819-172">Mathematik der Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="35819-172">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



