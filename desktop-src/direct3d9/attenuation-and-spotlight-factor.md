---
description: Die diffusen und Glanzlicht Komponenten der globalen Beleuchtungs Gleichung enthalten Begriffe, die die Licht Dämpfung und den Spotlight-Kegel beschreiben. Diese Begriffe werden unten beschrieben.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Dämpfung und Spotlight-Faktor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bb3cb2b1c2a3ee9e0e5d9419ff71dd9a303b6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550282"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a><span data-ttu-id="efa16-104">Dämpfung und Spotlight-Faktor (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="efa16-104">Attenuation and Spotlight Factor (Direct3D 9)</span></span>

<span data-ttu-id="efa16-105">Die diffusen und Glanzlicht Komponenten der globalen Beleuchtungs Gleichung enthalten Begriffe, die die Licht Dämpfung und den Spotlight-Kegel beschreiben.</span><span class="sxs-lookup"><span data-stu-id="efa16-105">The diffuse and specular lighting components of the global illumination equation contain terms that describe light attenuation and the spotlight cone.</span></span> <span data-ttu-id="efa16-106">Diese Begriffe werden unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="efa16-106">These terms are described below.</span></span>

## <a name="attenuation"></a><span data-ttu-id="efa16-107">Dämpfung</span><span class="sxs-lookup"><span data-stu-id="efa16-107">Attenuation</span></span>

<span data-ttu-id="efa16-108">Die Dämpfung eines Lichts hängt von der Art des Lichts und der Entfernung zwischen dem Licht und der Scheitelpunkt Position ab.</span><span class="sxs-lookup"><span data-stu-id="efa16-108">The attenuation of a light depends on the type of light and the distance between the light and the vertex position.</span></span> <span data-ttu-id="efa16-109">Verwenden Sie zum Berechnen der Dämpfung eine der folgenden Gleichungen.</span><span class="sxs-lookup"><span data-stu-id="efa16-109">To calculate attenuation, use one of the following equations.</span></span>

<span data-ttu-id="efa16-110">Atten = 1/(att0<sub>i</sub> + Att1<sub>i</sub> \* d + att2<sub>i</sub> \* d ²)</span><span class="sxs-lookup"><span data-stu-id="efa16-110">Atten = 1/( att0<sub>i</sub> + att1<sub>i</sub> \* d + att2<sub>i</sub> \* d²)</span></span>

<span data-ttu-id="efa16-111">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="efa16-111">Where:</span></span>



| <span data-ttu-id="efa16-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="efa16-112">Parameter</span></span>        | <span data-ttu-id="efa16-113">Standardwert</span><span class="sxs-lookup"><span data-stu-id="efa16-113">Default value</span></span> | <span data-ttu-id="efa16-114">type</span><span class="sxs-lookup"><span data-stu-id="efa16-114">Type</span></span>  | <span data-ttu-id="efa16-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efa16-115">Description</span></span>                                     | <span data-ttu-id="efa16-116">Range</span><span class="sxs-lookup"><span data-stu-id="efa16-116">Range</span></span>          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| <span data-ttu-id="efa16-117">att0<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="efa16-117">att0<sub>i</sub></span></span> | <span data-ttu-id="efa16-118">0,0</span><span class="sxs-lookup"><span data-stu-id="efa16-118">0.0</span></span>           | <span data-ttu-id="efa16-119">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="efa16-119">FLOAT</span></span> | <span data-ttu-id="efa16-120">Faktor für konstante Dämpfung</span><span class="sxs-lookup"><span data-stu-id="efa16-120">Constant attenuation factor</span></span>                     | <span data-ttu-id="efa16-121">0 bis + unendlich</span><span class="sxs-lookup"><span data-stu-id="efa16-121">0 to +infinity</span></span> |
| <span data-ttu-id="efa16-122">Att1<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="efa16-122">att1<sub>i</sub></span></span> | <span data-ttu-id="efa16-123">0,0</span><span class="sxs-lookup"><span data-stu-id="efa16-123">0.0</span></span>           | <span data-ttu-id="efa16-124">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="efa16-124">FLOAT</span></span> | <span data-ttu-id="efa16-125">Faktor für lineare Dämpfung</span><span class="sxs-lookup"><span data-stu-id="efa16-125">Linear attenuation factor</span></span>                       | <span data-ttu-id="efa16-126">0 bis + unendlich</span><span class="sxs-lookup"><span data-stu-id="efa16-126">0 to +infinity</span></span> |
| <span data-ttu-id="efa16-127">att2<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="efa16-127">att2<sub>i</sub></span></span> | <span data-ttu-id="efa16-128">0,0</span><span class="sxs-lookup"><span data-stu-id="efa16-128">0.0</span></span>           | <span data-ttu-id="efa16-129">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="efa16-129">FLOAT</span></span> | <span data-ttu-id="efa16-130">Faktor für die quadratische Dämpfung</span><span class="sxs-lookup"><span data-stu-id="efa16-130">Quadratic attenuation factor</span></span>                    | <span data-ttu-id="efa16-131">0 bis + unendlich</span><span class="sxs-lookup"><span data-stu-id="efa16-131">0 to +infinity</span></span> |
| <span data-ttu-id="efa16-132">d</span><span class="sxs-lookup"><span data-stu-id="efa16-132">d</span></span>                | <span data-ttu-id="efa16-133">–</span><span class="sxs-lookup"><span data-stu-id="efa16-133">N/A</span></span>           | <span data-ttu-id="efa16-134">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="efa16-134">FLOAT</span></span> | <span data-ttu-id="efa16-135">Abstand zwischen Scheitelpunkt Position und heller Position</span><span class="sxs-lookup"><span data-stu-id="efa16-135">Distance from vertex position to light position</span></span> | <span data-ttu-id="efa16-136">–</span><span class="sxs-lookup"><span data-stu-id="efa16-136">N/A</span></span>            |



 

-   <span data-ttu-id="efa16-137">Atten = 1, wenn das Licht ein Direktionales Licht ist.</span><span class="sxs-lookup"><span data-stu-id="efa16-137">Atten = 1, if the light is a directional light.</span></span>
-   <span data-ttu-id="efa16-138">Atten = 0, wenn der Abstand zwischen dem Licht und dem Scheitelpunkt den hellen Bereich überschreitet.</span><span class="sxs-lookup"><span data-stu-id="efa16-138">Atten = 0, if the distance between the light and the vertex exceeds the light's range.</span></span>

<span data-ttu-id="efa16-139">Die att0-, Att1-, att2-Werte werden von den Attenuation0-, Attenuation1-und Attenuation2-Membern von [**D3DLIGHT9**](d3dlight9.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="efa16-139">The att0, att1, att2 values are specified by the Attenuation0, Attenuation1, and Attenuation2 members of [**D3DLIGHT9**](d3dlight9.md).</span></span>

<span data-ttu-id="efa16-140">Der Abstand zwischen dem Licht und der Scheitelpunkt Position ist immer positiv.</span><span class="sxs-lookup"><span data-stu-id="efa16-140">The distance between the light and the vertex position is always positive.</span></span>

<span data-ttu-id="efa16-141">d = \| L-<sub>dir</sub>\|</span><span class="sxs-lookup"><span data-stu-id="efa16-141">d = \| L<sub>dir</sub> \|</span></span>

<span data-ttu-id="efa16-142">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="efa16-142">Where:</span></span>



| <span data-ttu-id="efa16-143">Parameter</span><span class="sxs-lookup"><span data-stu-id="efa16-143">Parameter</span></span>       | <span data-ttu-id="efa16-144">Standardwert</span><span class="sxs-lookup"><span data-stu-id="efa16-144">Default value</span></span> | <span data-ttu-id="efa16-145">type</span><span class="sxs-lookup"><span data-stu-id="efa16-145">Type</span></span>      | <span data-ttu-id="efa16-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efa16-146">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="efa16-147">L-<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="efa16-147">L<sub>dir</sub></span></span> | <span data-ttu-id="efa16-148">–</span><span class="sxs-lookup"><span data-stu-id="efa16-148">N/A</span></span>           | <span data-ttu-id="efa16-149">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="efa16-149">D3DVECTOR</span></span> | <span data-ttu-id="efa16-150">Richtung Vektor von Scheitelpunkt Position zur hellen Position</span><span class="sxs-lookup"><span data-stu-id="efa16-150">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="efa16-151">Wenn d größer ist als der Bereich des Lichts, d. h. der Bereichs Member einer [**D3DLIGHT9**](d3dlight9.md) -Struktur, führt Direct3D keine weiteren Dämpfung-Berechnungen durch und wendet keine Auswirkungen vom Licht auf den Scheitelpunkt an.</span><span class="sxs-lookup"><span data-stu-id="efa16-151">If d is greater than the light's range, that is, the Range member of a [**D3DLIGHT9**](d3dlight9.md) structure, Direct3D makes no further attenuation calculations and applies no effects from the light to the vertex.</span></span>

<span data-ttu-id="efa16-152">Die Dämpfungs Konstanten fungieren als Koeffizienten in der Formel. Sie können eine Vielzahl von Dämpfungs Kurven erstellen, indem Sie einfache Anpassungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="efa16-152">The attenuation constants act as coefficients in the formula - you can produce a variety of attenuation curves by making simple adjustments to them.</span></span> <span data-ttu-id="efa16-153">Sie können Attenuation1 auf 1,0 festlegen, um ein Licht zu erstellen, das nicht abgeschwächt wird, aber weiterhin durch den Bereich beschränkt ist, oder Sie können mit verschiedenen Werten experimentieren, um verschiedene Dämpfungseffekte zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="efa16-153">You can set Attenuation1 to 1.0 to create a light that doesn't attenuate but is still limited by range, or you can experiment with different values to achieve various attenuation effects.</span></span>

<span data-ttu-id="efa16-154">Die Dämpfung im maximalen Bereich des Lichts ist nicht 0,0.</span><span class="sxs-lookup"><span data-stu-id="efa16-154">The attenuation at the maximum range of the light is not 0.0.</span></span> <span data-ttu-id="efa16-155">Um zu verhindern, dass Glühbirnen plötzlich angezeigt werden, wenn Sie sich im hellen Bereich befinden, kann eine Anwendung den hellen Bereich vergrößern.</span><span class="sxs-lookup"><span data-stu-id="efa16-155">To prevent lights from suddenly appearing when they are at the light range, an application can increase the light range.</span></span> <span data-ttu-id="efa16-156">Oder die Anwendung kann Dämpfungs Konstanten einrichten, sodass der Faktor für die Dämpfung fast 0,0 am hellen Bereich liegt.</span><span class="sxs-lookup"><span data-stu-id="efa16-156">Or, the application can set up attenuation constants so that the attenuation factor is close to 0.0 at the light range.</span></span> <span data-ttu-id="efa16-157">Der Wert für die Dämpfung wird mit den roten, grünen und blauen Komponenten der hellen Farbe multipliziert, um die Intensität des Lichts als Faktor der Entfernung zu einem Scheitelpunkt zu skalieren.</span><span class="sxs-lookup"><span data-stu-id="efa16-157">The attenuation value is multiplied by the red, green, and blue components of the light's color to scale the light's intensity as a factor of the distance light travels to a vertex.</span></span>

## <a name="spotlight-factor"></a><span data-ttu-id="efa16-158">Spotlight-Faktor</span><span class="sxs-lookup"><span data-stu-id="efa16-158">Spotlight Factor</span></span>

<span data-ttu-id="efa16-159">Die folgende Gleichung gibt den Spotlight-Faktor an.</span><span class="sxs-lookup"><span data-stu-id="efa16-159">The following equation specifies the spotlight factor.</span></span>

![Gleichung des Spotlight-Faktors](images/dx8light9.png)



| <span data-ttu-id="efa16-161">Parameter</span><span class="sxs-lookup"><span data-stu-id="efa16-161">Parameter</span></span>         | <span data-ttu-id="efa16-162">Standardwert</span><span class="sxs-lookup"><span data-stu-id="efa16-162">Default value</span></span> | <span data-ttu-id="efa16-163">type</span><span class="sxs-lookup"><span data-stu-id="efa16-163">Type</span></span>  | <span data-ttu-id="efa16-164">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efa16-164">Description</span></span>                              | <span data-ttu-id="efa16-165">Range</span><span class="sxs-lookup"><span data-stu-id="efa16-165">Range</span></span>                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| <span data-ttu-id="efa16-166">Rho<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="efa16-166">rho<sub>i</sub></span></span>   | <span data-ttu-id="efa16-167">–</span><span class="sxs-lookup"><span data-stu-id="efa16-167">N/A</span></span>           | <span data-ttu-id="efa16-168">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="efa16-168">FLOAT</span></span> | <span data-ttu-id="efa16-169">Kosinus (Winkel) für Spotlight i</span><span class="sxs-lookup"><span data-stu-id="efa16-169">cosine(angle) for spotlight i</span></span>            | <span data-ttu-id="efa16-170">–</span><span class="sxs-lookup"><span data-stu-id="efa16-170">N/A</span></span>                      |
| <span data-ttu-id="efa16-171">Phi<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="efa16-171">phi<sub>i</sub></span></span>   | <span data-ttu-id="efa16-172">0,0</span><span class="sxs-lookup"><span data-stu-id="efa16-172">0.0</span></span>           | <span data-ttu-id="efa16-173">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="efa16-173">FLOAT</span></span> | <span data-ttu-id="efa16-174">Pendel Winkel von Spotlight i im Bogenmaße</span><span class="sxs-lookup"><span data-stu-id="efa16-174">Penumbra angle of spotlight i in radians</span></span> | <span data-ttu-id="efa16-175">\[-TA<sub>i</sub>, PI)</span><span class="sxs-lookup"><span data-stu-id="efa16-175">\[theta<sub>i</sub>, pi)</span></span> |
| <span data-ttu-id="efa16-176">die<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="efa16-176">theta<sub>i</sub></span></span> | <span data-ttu-id="efa16-177">0,0</span><span class="sxs-lookup"><span data-stu-id="efa16-177">0.0</span></span>           | <span data-ttu-id="efa16-178">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="efa16-178">FLOAT</span></span> | <span data-ttu-id="efa16-179">Der Umschlag Winkel von Spotlight i im Bogenmaße</span><span class="sxs-lookup"><span data-stu-id="efa16-179">Umbra angle of spotlight i in radians</span></span>    | <span data-ttu-id="efa16-180">\[0, PI)</span><span class="sxs-lookup"><span data-stu-id="efa16-180">\[0, pi)</span></span>                 |
| <span data-ttu-id="efa16-181">Übergang</span><span class="sxs-lookup"><span data-stu-id="efa16-181">falloff</span></span>           | <span data-ttu-id="efa16-182">0,0</span><span class="sxs-lookup"><span data-stu-id="efa16-182">0.0</span></span>           | <span data-ttu-id="efa16-183">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="efa16-183">FLOAT</span></span> | <span data-ttu-id="efa16-184">Zuordnung der Rolle</span><span class="sxs-lookup"><span data-stu-id="efa16-184">Falloff factor</span></span>                           | <span data-ttu-id="efa16-185">(-unendlich, + unendlich)</span><span class="sxs-lookup"><span data-stu-id="efa16-185">(-infinity, +infinity)</span></span>   |



 

<span data-ttu-id="efa16-186">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="efa16-186">Where:</span></span>

<span data-ttu-id="efa16-187">Rho = Norm (L<sub>DCS</sub>)<sup>.</sup> Norm (L-<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="efa16-187">rho = norm(L<sub>dcs</sub>)<sup>.</sup>norm(L<sub>dir</sub>)</span></span>

<span data-ttu-id="efa16-188">und:</span><span class="sxs-lookup"><span data-stu-id="efa16-188">and:</span></span>



| <span data-ttu-id="efa16-189">Parameter</span><span class="sxs-lookup"><span data-stu-id="efa16-189">Parameter</span></span>       | <span data-ttu-id="efa16-190">Standardwert</span><span class="sxs-lookup"><span data-stu-id="efa16-190">Default value</span></span> | <span data-ttu-id="efa16-191">type</span><span class="sxs-lookup"><span data-stu-id="efa16-191">Type</span></span>      | <span data-ttu-id="efa16-192">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efa16-192">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="efa16-193">L-<sub>DCS</sub></span><span class="sxs-lookup"><span data-stu-id="efa16-193">L<sub>dcs</sub></span></span> | <span data-ttu-id="efa16-194">–</span><span class="sxs-lookup"><span data-stu-id="efa16-194">N/A</span></span>           | <span data-ttu-id="efa16-195">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="efa16-195">D3DVECTOR</span></span> | <span data-ttu-id="efa16-196">Das negative der Lichtrichtung im Kamerabereich</span><span class="sxs-lookup"><span data-stu-id="efa16-196">The negative of the light direction in camera space</span></span>         |
| <span data-ttu-id="efa16-197">L-<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="efa16-197">L<sub>dir</sub></span></span> | <span data-ttu-id="efa16-198">–</span><span class="sxs-lookup"><span data-stu-id="efa16-198">N/A</span></span>           | <span data-ttu-id="efa16-199">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="efa16-199">D3DVECTOR</span></span> | <span data-ttu-id="efa16-200">Richtung Vektor von Scheitelpunkt Position zur hellen Position</span><span class="sxs-lookup"><span data-stu-id="efa16-200">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="efa16-201">Nach dem Berechnen der Licht Dämpfung werden bei Direct3D auch Spotlight-Effekte berücksichtigt, der Winkel, den das Licht von einer Oberfläche reflektiert, und die Reflektion des aktuellen Materials, um die diffusen und Glanz Komponenten für diesen Scheitelpunkt zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="efa16-201">After computing the light attenuation, Direct3D also considers spotlight effects if applicable, the angle that the light reflects from a surface, and the reflectance of the current material to calculate the diffuse and specular components for that vertex.</span></span> <span data-ttu-id="efa16-202">Weitere Informationen finden Sie unter [Spotlight](light-types.md).</span><span class="sxs-lookup"><span data-stu-id="efa16-202">For more information, see [SpotLight](light-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="efa16-203">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="efa16-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efa16-204">Mathematik der Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="efa16-204">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



