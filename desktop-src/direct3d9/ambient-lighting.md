---
description: Ambient-Beleuchtung bietet eine konstante Beleuchtung für eine Szene.
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: Umgebungsbeleuchtung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991981a9c1d7d24714e7014d08cefeaa94fe20f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523840"
---
# <a name="ambient-lighting-direct3d-9"></a><span data-ttu-id="5fc0e-103">Umgebungsbeleuchtung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5fc0e-103">Ambient Lighting (Direct3D 9)</span></span>

<span data-ttu-id="5fc0e-104">Ambient-Beleuchtung bietet eine konstante Beleuchtung für eine Szene.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-104">Ambient lighting provides constant lighting for a scene.</span></span> <span data-ttu-id="5fc0e-105">Alle Objekt Scheitel Punkte werden gleich angezeigt, da Sie nicht von anderen Beleuchtungs Faktoren abhängen, wie z. b. Vertex-normalen, Lichtrichtung, Lichtposition, Bereich oder Dämpfung.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-105">It lights all object vertices the same because it is not dependent on any other lighting factors such as vertex normals, light direction, light position, range, or attenuation.</span></span> <span data-ttu-id="5fc0e-106">Dies ist die schnellste Art von Beleuchtung, liefert jedoch die wenigsten realistischen Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-106">It is the fastest type of lighting but it produces the least realistic results.</span></span> <span data-ttu-id="5fc0e-107">Direct3D enthält eine einzelne globale Ambient-Light-Eigenschaft, die Sie verwenden können, ohne dass ein Licht erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-107">Direct3D contains a single global ambient light property that you can use without creating any light.</span></span> <span data-ttu-id="5fc0e-108">Alternativ können Sie ein beliebiges helles Objekt festlegen, um Umgebungsbeleuchtung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-108">Alternatively, you can set any light object to provide ambient lighting.</span></span> <span data-ttu-id="5fc0e-109">Die Umgebungsbeleuchtung für eine Szene wird durch die folgende Gleichung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-109">The ambient lighting for a scene is described by the following equation.</span></span>

<span data-ttu-id="5fc0e-110">Ambient lighting = c ₐ \* \[ g ₐ + Sum (Atten<sub>i</sub> \* Spot<sub>i</sub> \* L<sub>AI</sub>)\]</span><span class="sxs-lookup"><span data-stu-id="5fc0e-110">Ambient Lighting = Cₐ\*\[Gₐ + sum(Atten<sub>i</sub>\*Spot<sub>i</sub>\*L<sub>ai</sub>)\]</span></span>

<span data-ttu-id="5fc0e-111">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="5fc0e-111">Where:</span></span>



| <span data-ttu-id="5fc0e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fc0e-112">Parameter</span></span>         | <span data-ttu-id="5fc0e-113">Standardwert</span><span class="sxs-lookup"><span data-stu-id="5fc0e-113">Default value</span></span> | <span data-ttu-id="5fc0e-114">type</span><span class="sxs-lookup"><span data-stu-id="5fc0e-114">Type</span></span>          | <span data-ttu-id="5fc0e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fc0e-115">Description</span></span>                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc0e-116">C ₐ</span><span class="sxs-lookup"><span data-stu-id="5fc0e-116">Cₐ</span></span>                | <span data-ttu-id="5fc0e-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="5fc0e-117">(0,0,0,0)</span></span>     | <span data-ttu-id="5fc0e-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="5fc0e-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="5fc0e-119">Material Ambient-Farbe</span><span class="sxs-lookup"><span data-stu-id="5fc0e-119">Material ambient color</span></span>                                                                                                         |
| <span data-ttu-id="5fc0e-120">G ₐ</span><span class="sxs-lookup"><span data-stu-id="5fc0e-120">Gₐ</span></span>                | <span data-ttu-id="5fc0e-121">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="5fc0e-121">(0,0,0,0)</span></span>     | <span data-ttu-id="5fc0e-122">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="5fc0e-122">D3DCOLORVALUE</span></span> | <span data-ttu-id="5fc0e-123">Globale Ambient-Farbe</span><span class="sxs-lookup"><span data-stu-id="5fc0e-123">Global ambient color</span></span>                                                                                                           |
| <span data-ttu-id="5fc0e-124">Atten<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="5fc0e-124">Atten<sub>i</sub></span></span> | <span data-ttu-id="5fc0e-125">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="5fc0e-125">(0,0,0,0)</span></span>     | <span data-ttu-id="5fc0e-126">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="5fc0e-126">D3DCOLORVALUE</span></span> | <span data-ttu-id="5fc0e-127">Helle Dämpfung des ITH-Lichts.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-127">Light attenuation of the ith light.</span></span> <span data-ttu-id="5fc0e-128">Siehe [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="5fc0e-128">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="5fc0e-129">Stelle<sub>ich</sub></span><span class="sxs-lookup"><span data-stu-id="5fc0e-129">Spot<sub>i</sub></span></span>  | <span data-ttu-id="5fc0e-130">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="5fc0e-130">(0,0,0,0)</span></span>     | <span data-ttu-id="5fc0e-131">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="5fc0e-131">D3DVECTOR</span></span>     | <span data-ttu-id="5fc0e-132">Der Spotlight-Faktor des ITH-Lichts.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-132">Spotlight factor of the ith light.</span></span> <span data-ttu-id="5fc0e-133">Siehe [Dämpfung und Spotlight-Faktor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="5fc0e-133">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |
| <span data-ttu-id="5fc0e-134">Sum</span><span class="sxs-lookup"><span data-stu-id="5fc0e-134">sum</span></span>               | <span data-ttu-id="5fc0e-135">–</span><span class="sxs-lookup"><span data-stu-id="5fc0e-135">N/A</span></span>           | <span data-ttu-id="5fc0e-136">–</span><span class="sxs-lookup"><span data-stu-id="5fc0e-136">N/A</span></span>           | <span data-ttu-id="5fc0e-137">Summe der Umgebungsbeleuchtung</span><span class="sxs-lookup"><span data-stu-id="5fc0e-137">Sum of the ambient light</span></span>                                                                                                       |
| <span data-ttu-id="5fc0e-138">L<sub>AI</sub></span><span class="sxs-lookup"><span data-stu-id="5fc0e-138">L<sub>ai</sub></span></span>    | <span data-ttu-id="5fc0e-139">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="5fc0e-139">(0,0,0,0)</span></span>     | <span data-ttu-id="5fc0e-140">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="5fc0e-140">D3DVECTOR</span></span>     | <span data-ttu-id="5fc0e-141">Helle Ambient-Farbe des ITH-Lichts</span><span class="sxs-lookup"><span data-stu-id="5fc0e-141">Light ambient color of the ith light</span></span>                                                                                           |



 

<span data-ttu-id="5fc0e-142">Der Wert für c ₐ lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5fc0e-142">The value for Cₐ is either:</span></span>

-   <span data-ttu-id="5fc0e-143">Vertex color1, wenn AmbientMaterialSource = D3DMCS \_ color1 und die erste Scheitelpunkt Farbe in der Vertex-Deklaration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-143">vertex color1, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="5fc0e-144">Vertex color2, wenn AmbientMaterialSource = D3DMCS \_ color2 und die zweite Scheitelpunkt Farbe in der Scheitelpunkt Deklaration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-144">vertex color2, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in vertex declaration.</span></span>
-   <span data-ttu-id="5fc0e-145">Material Ambient-Farbe.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-145">material ambient color.</span></span>

> [!Note]  
> <span data-ttu-id="5fc0e-146">Wenn eine der beiden Optionen "AmbientMaterialSource" verwendet wird und die Scheitelpunkt Farbe nicht angegeben wird, wird die Umgebungs Farbe für das Material verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-146">If either AMBIENTMATERIALSOURCE option is used, and the vertex color is not provided, then the material ambient color is used.</span></span>

 

<span data-ttu-id="5fc0e-147">Verwenden Sie setmaterial, um die Material Ambient-Farbe zu verwenden, wie im folgenden Beispielcode gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-147">To use the material ambient color, use SetMaterial as shown in the example code below.</span></span>

<span data-ttu-id="5fc0e-148">G ₐ ist die globale Umgebungs Farbe.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-148">Gₐ is the global ambient color.</span></span> <span data-ttu-id="5fc0e-149">Sie wird mithilfe von setrenderstate (D3DRS \_ AMBIENT) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-149">It is set using SetRenderState(D3DRS\_AMBIENT).</span></span> <span data-ttu-id="5fc0e-150">In einer Direct3D-Szene gibt es eine globale Umgebungs Farbe.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-150">There is one global ambient color in a Direct3D scene.</span></span> <span data-ttu-id="5fc0e-151">Dieser Parameter ist keinem Direct3D Light-Objekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-151">This parameter is not associated with a Direct3D light object.</span></span>

<span data-ttu-id="5fc0e-152">L<sub>AI</sub> ist die Ambiente-Farbe des ITH-Lichts in der Szene.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-152">L<sub>ai</sub> is the ambient color of the ith light in the scene.</span></span> <span data-ttu-id="5fc0e-153">Jedes Direct3D Light verfügt über eine Reihe von Eigenschaften, von denen eine die Umgebungs Farbe ist.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-153">Each Direct3D light has a set of properties, one of which is the ambient color.</span></span> <span data-ttu-id="5fc0e-154">Der Begriff Sum (L<sub>AI</sub>) ist eine Summe aller Ambient-Farben in der Szene.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-154">The term, sum(L<sub>ai</sub>) is a sum of all the ambient colors in the scene.</span></span>

## <a name="example"></a><span data-ttu-id="5fc0e-155">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5fc0e-155">Example</span></span>

<span data-ttu-id="5fc0e-156">In diesem Beispiel wird das-Objekt mithilfe der Szene Ambient Light und einer Material Ambient-Farbe gefärbt.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-156">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span>


```
#define GRAY_COLOR  0x00bfbfbf

// create material
D3DMATERIAL9 mtrl;
ZeroMemory(&mtrl, sizeof(mtrl));
mtrl.Ambient.r = 0.75f;
mtrl.Ambient.g = 0.0f;
mtrl.Ambient.b = 0.0f;
mtrl.Ambient.a = 0.0f;
m_pd3dDevice->SetMaterial(&mtrl);
m_pd3dDevice->SetRenderState(D3DRS_AMBIENT, GRAY_COLOR);
```



<span data-ttu-id="5fc0e-157">Gemäß der Gleichung ist die resultierende Farbe für die Objekt Vertices eine Kombination aus der Material Farbe und der hellen Farbe.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-157">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="5fc0e-158">Die beiden folgenden Abbildungen zeigen die Material Farbe, die grau ist, und die helle Farbe, die hell rot ist.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-158">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![Abbildung einer grauen Kugel](images/amb1.jpg)![Abbildung einer roten Kugel](images/lightred.jpg)

<span data-ttu-id="5fc0e-161">Die resultierende Szene wird in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-161">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="5fc0e-162">Das einzige Objekt in der Szene ist eine Kugel.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-162">The only object in the scene is a sphere.</span></span> <span data-ttu-id="5fc0e-163">Ambient Light beleuchtet alle Objekt Scheitel Punkte mit der gleichen Farbe.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-163">Ambient light lights all object vertices with the same color.</span></span> <span data-ttu-id="5fc0e-164">Er ist nicht abhängig von der Scheitelpunkt normalen oder der Lichtrichtung.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-164">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="5fc0e-165">Folglich sieht die Kugel wie ein 2D-Kreis aus, da es keinen Unterschied gibt, um die Oberfläche des Objekts zu schattieren.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-165">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![Abbildung einer Kugel mit Umgebungsbeleuchtung](images/lighta.jpg)

<span data-ttu-id="5fc0e-167">Um Objekten einen realistischeren Einblick zu verschaffen, wenden Sie zusätzlich zur Umgebungsbeleuchtung diffuse oder Glanzlichter an.</span><span class="sxs-lookup"><span data-stu-id="5fc0e-167">To give objects a more realistic look, apply diffuse or specular lighting in addition to ambient lighting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fc0e-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5fc0e-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fc0e-169">Mathematik der Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="5fc0e-169">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



