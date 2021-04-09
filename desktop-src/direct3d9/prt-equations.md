---
description: Um einen Shader, der PRT implementiert, vollständig zu verstehen, ist es hilfreich, die Formel abzuleiten, die der Shader zum Berechnen der Ausgangs Strahlung verwendet.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: PRT-Gleichungen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65559fada82fda7f7eed1c7d05543883a06a19e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124819"
---
# <a name="prt-equations-direct3d-9"></a><span data-ttu-id="10aa8-103">PRT-Gleichungen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="10aa8-103">PRT Equations (Direct3D 9)</span></span>

<span data-ttu-id="10aa8-104">Um einen Shader, der PRT implementiert, vollständig zu verstehen, ist es hilfreich, die Formel abzuleiten, die der Shader zum Berechnen der Ausgangs Strahlung verwendet.</span><span class="sxs-lookup"><span data-stu-id="10aa8-104">To fully understand a shader that implements PRT, it is useful to derive the formula the shader uses to calculate exit radiance.</span></span>

<span data-ttu-id="10aa8-105">Um zu beginnen, ist die folgende Gleichung die allgemeine Gleichung zur Berechnung der Beendigungs Strahlen, die sich aus der direkten Beleuchtung eines diffusen Objekts mit willkürlicher, entfernter Beleuchtung ergibt.</span><span class="sxs-lookup"><span data-stu-id="10aa8-105">To start off, the following equation is the general equation to calculate exit radiance resulting from direct lighting on a diffuse object with arbitrary distant lighting.</span></span>

![Gleichung der Beendigungs Strahlung, die sich aus der direkten Beleuchtung eines diffusen Objekts mit willkürlicher, entfernter Beleuchtung ergibt](images/prt-theory-eq1.png)

<span data-ttu-id="10aa8-107">Dabei gilt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="10aa8-107">where:</span></span>



| <span data-ttu-id="10aa8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="10aa8-108">Parameter</span></span>     | <span data-ttu-id="10aa8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10aa8-109">Description</span></span>                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10aa8-110">Neutraler</span><span class="sxs-lookup"><span data-stu-id="10aa8-110">Rₚ</span></span>            | <span data-ttu-id="10aa8-111">Der Ausgangs Glanz bei Scheitelpunkt p.</span><span class="sxs-lookup"><span data-stu-id="10aa8-111">The exit radiance at vertex p.</span></span> <span data-ttu-id="10aa8-112">Ausgewertet an jedem Scheitelpunkt im Mesh.</span><span class="sxs-lookup"><span data-stu-id="10aa8-112">Evaluated at every vertex on the mesh.</span></span>                                   |
| <span data-ttu-id="10aa8-113">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="10aa8-113">p<sub>d</sub></span></span> | <span data-ttu-id="10aa8-114">Die Albedo der Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="10aa8-114">The albedo of the surface.</span></span>                                                                              |
| <span data-ttu-id="10aa8-115">pi</span><span class="sxs-lookup"><span data-stu-id="10aa8-115">pi</span></span>            | <span data-ttu-id="10aa8-116">Eine Konstante, die als normalisierungs Faktor für die Energieeinsparung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="10aa8-116">A constant, used as an energy conservation normalization factor.</span></span>                                        |
| <span data-ttu-id="10aa8-117">L (s)</span><span class="sxs-lookup"><span data-stu-id="10aa8-117">L(s)</span></span>          | <span data-ttu-id="10aa8-118">Die Beleuchtungs Umgebung (Quell Ausstrahlung).</span><span class="sxs-lookup"><span data-stu-id="10aa8-118">The lighting environment (source radiance).</span></span>                                                             |
| <span data-ttu-id="10aa8-119">VP ₍ s ₎</span><span class="sxs-lookup"><span data-stu-id="10aa8-119">Vₚ₍ₛ₎</span></span>         | <span data-ttu-id="10aa8-120">Eine binäre Sichtbarkeits Funktion für Punkt p.</span><span class="sxs-lookup"><span data-stu-id="10aa8-120">A binary visibility function for point p.</span></span> <span data-ttu-id="10aa8-121">Der Wert ist 1, wenn der Punkt das Licht sehen kann, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="10aa8-121">It is 1 if the point can see the light, 0 if not.</span></span>             |
| <span data-ttu-id="10aa8-122">HNP ₍ s ₎</span><span class="sxs-lookup"><span data-stu-id="10aa8-122">Hₙₚ₍ₛ₎</span></span>        | <span data-ttu-id="10aa8-123">Der Kosinus Begriff von Lambert-Gesetz.</span><span class="sxs-lookup"><span data-stu-id="10aa8-123">The cosine term from Lambert's law.</span></span> <span data-ttu-id="10aa8-124">Gleich max ((NP = s), 0), wobei NP die Oberflächen normale an Punkt p ist.</span><span class="sxs-lookup"><span data-stu-id="10aa8-124">Equal to max((Nₚ· s), 0) where Nₚ is the surface normal at point p.</span></span> |
| <span data-ttu-id="10aa8-125">s</span><span class="sxs-lookup"><span data-stu-id="10aa8-125">s</span></span>             | <span data-ttu-id="10aa8-126">Die Variable, die in die Kugel integriert ist.</span><span class="sxs-lookup"><span data-stu-id="10aa8-126">The variable that integrates over the sphere.</span></span>                                                           |



 

<span data-ttu-id="10aa8-127">Durch die Verwendung von sphärischen Basisfunktionen, wie z. b. sphärischen Harmonics, gleicht die folgende Gleichung der Beleuchtungs Umgebung</span><span class="sxs-lookup"><span data-stu-id="10aa8-127">Using spherical basis functions, such as spherical harmonics, the following equation approximates the lighting environment.</span></span>

![Gleichung der Beleuchtungs Umgebung](images/prt-theory-eq2.png)

<span data-ttu-id="10aa8-129">Dabei gilt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="10aa8-129">where:</span></span>



| <span data-ttu-id="10aa8-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="10aa8-130">Parameter</span></span>        | <span data-ttu-id="10aa8-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10aa8-131">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="10aa8-132">L (s)</span><span class="sxs-lookup"><span data-stu-id="10aa8-132">L(s)</span></span>             | <span data-ttu-id="10aa8-133">Die Beleuchtungs Umgebung (Quell Ausstrahlung).</span><span class="sxs-lookup"><span data-stu-id="10aa8-133">The lighting environment (source radiance).</span></span>              |
| <span data-ttu-id="10aa8-134">i</span><span class="sxs-lookup"><span data-stu-id="10aa8-134">i</span></span>                | <span data-ttu-id="10aa8-135">Eine ganze Zahl, die die Anzahl der Basisfunktionen summiert.</span><span class="sxs-lookup"><span data-stu-id="10aa8-135">An integer that sums over the number of basis functions.</span></span> |
| <span data-ttu-id="10aa8-136">O</span><span class="sxs-lookup"><span data-stu-id="10aa8-136">O</span></span>                | <span data-ttu-id="10aa8-137">Die Reihenfolge der sphärischen Harmonics.</span><span class="sxs-lookup"><span data-stu-id="10aa8-137">The order of spherical harmonics.</span></span>                        |
| <span data-ttu-id="10aa8-138">l<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="10aa8-138">l<sub>i</sub></span></span>    | <span data-ttu-id="10aa8-139">Ein Koeffizient.</span><span class="sxs-lookup"><span data-stu-id="10aa8-139">A coefficient.</span></span>                                           |
| <span data-ttu-id="10aa8-140">Y<sub>i (s)</sub></span><span class="sxs-lookup"><span data-stu-id="10aa8-140">Y<sub>i(s)</sub></span></span> | <span data-ttu-id="10aa8-141">Eine Basis Funktion über der Kugel.</span><span class="sxs-lookup"><span data-stu-id="10aa8-141">Some basis function over the sphere.</span></span>                     |



 

<span data-ttu-id="10aa8-142">Die Auflistung dieser Koeffizienten, L ", bietet die optimale Näherung für die Funktion l (s) mit den Basisfunktionen Y (s).</span><span class="sxs-lookup"><span data-stu-id="10aa8-142">The collection of these coefficients, L', provides the optimal approximation for function L(s) with the basis functions Y(s).</span></span> <span data-ttu-id="10aa8-143">Durch ersetzen und verteilen ergibt sich die folgende Gleichung.</span><span class="sxs-lookup"><span data-stu-id="10aa8-143">Substituting and distributing yields the following equation.</span></span>

![Gleichung der Beendigungs Strahlung nach dem Ersetzen von l (s) und verteilen](images/prt-theory-eq3.png)

<span data-ttu-id="10aa8-145">Der integrale Wert von Y<sub>i (s)</sub>VP ₍ s ₎ HNP ₍ s ₎ ist ein Transfer Koeffizienten t<sub>Pi</sub> , den der Simulator für jeden Scheitelpunkt im Mesh vorberechnet.</span><span class="sxs-lookup"><span data-stu-id="10aa8-145">The integral of Y<sub>i(s)</sub>Vₚ₍ₛ₎Hₙₚ₍ₛ₎ is a transfer coefficient t<sub>pi</sub> that the simulator precomputes for every vertex on the mesh.</span></span> <span data-ttu-id="10aa8-146">Wenn Sie ersetzen, wird die folgende Gleichung erzeugt.</span><span class="sxs-lookup"><span data-stu-id="10aa8-146">Substituting this yields the following equation.</span></span>

![Gleichung der Beendigungs Glanz, nachdem der Übertragungskoeffizienten ersetzt wurde.](images/prt-theory-eq4.png)

<span data-ttu-id="10aa8-148">Wenn Sie dies in eine Vektor Notation ändern, ergibt sich die folgende nicht komprimierte Gleichung, um die Ausgangs Glanz für jeden Kanal zu berechnen</span><span class="sxs-lookup"><span data-stu-id="10aa8-148">Changing this to vector notation yields the following uncompressed equation to calculate exit radiance for each channel.</span></span>

![Gleichung der Beendigungs Strahlung nach dem Wechsel zur Vektor Notation](images/prt-theory-eq5.png)

<span data-ttu-id="10aa8-150">Dabei gilt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="10aa8-150">where:</span></span>



| <span data-ttu-id="10aa8-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="10aa8-151">Parameter</span></span>     | <span data-ttu-id="10aa8-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10aa8-152">Description</span></span>                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10aa8-153">Neutraler</span><span class="sxs-lookup"><span data-stu-id="10aa8-153">Rₚ</span></span>            | <span data-ttu-id="10aa8-154">Der Ausgangs Glanz bei Scheitelpunkt p.</span><span class="sxs-lookup"><span data-stu-id="10aa8-154">The exit radiance at vertex p.</span></span>                                                                                                                                                      |
| <span data-ttu-id="10aa8-155">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="10aa8-155">p<sub>d</sub></span></span> | <span data-ttu-id="10aa8-156">Die Albedo der Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="10aa8-156">The albedo of the surface.</span></span>                                                                                                                                                          |
| <span data-ttu-id="10aa8-157">Int</span><span class="sxs-lookup"><span data-stu-id="10aa8-157">L'</span></span>            | <span data-ttu-id="10aa8-158">Der Vektor von l<sub>i</sub>und ist die Projektion der Quell Ausstrahlung in die kugelförmigen harmonischen Basisfunktionen.</span><span class="sxs-lookup"><span data-stu-id="10aa8-158">The vector of l<sub>i</sub>, and is the projection of the source radiance into the spherical harmonic basis functions.</span></span> <span data-ttu-id="10aa8-159">Dies ist ein Order ²-Vektor mit sphärischen harmonischen Koeffizient.</span><span class="sxs-lookup"><span data-stu-id="10aa8-159">This is an order² vector of spherical harmonic coefficients.</span></span> |
| <span data-ttu-id="10aa8-160">TP</span><span class="sxs-lookup"><span data-stu-id="10aa8-160">Tₚ</span></span>            | <span data-ttu-id="10aa8-161">Ein "Order ²"-Übertragungs Vektor für Vertex p.</span><span class="sxs-lookup"><span data-stu-id="10aa8-161">An order² transfer vector for vertex p.</span></span> <span data-ttu-id="10aa8-162">Der Simulator dividiert die Übertragungskoeffizienten durch p.</span><span class="sxs-lookup"><span data-stu-id="10aa8-162">The simulator divides the transfer coefficients by p.</span></span>                                                                                       |



 

<span data-ttu-id="10aa8-163">Beide Vektoren sind ein Order ²-Vektor mit sphärischen harmonischen Koeffizienten. Beachten Sie, dass es sich hierbei einfach um ein Punktprodukt handelt.</span><span class="sxs-lookup"><span data-stu-id="10aa8-163">Both of these vectors are an order² vector of spherical harmonic coefficients, so notice that this is simply a dot product.</span></span> <span data-ttu-id="10aa8-164">Abhängig von der Bestellung kann der Punkt teuer sein, sodass die Komprimierung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="10aa8-164">Depending on the order, the dot can be expensive so compression can be used.</span></span> <span data-ttu-id="10aa8-165">Mit einem Algorithmus namens "Clustered Principal Component Analysis (CPCA)" werden die Daten effizient komprimiert.</span><span class="sxs-lookup"><span data-stu-id="10aa8-165">An algorithm called Clustered Principal Component Analysis (CPCA) efficiently compresses the data.</span></span> <span data-ttu-id="10aa8-166">Dies ermöglicht die Verwendung einer sphärischen harmonischen Näherung höherer Ordnung, was zu schärferen Schatten führt.</span><span class="sxs-lookup"><span data-stu-id="10aa8-166">This enables the use of a higher-order spherical harmonic approximation which results in sharper shadows.</span></span>

<span data-ttu-id="10aa8-167">CPCA stellt die folgende Gleichung bereit, um den Übertragungs Vektor anzugleichen.</span><span class="sxs-lookup"><span data-stu-id="10aa8-167">CPCA provides the following equation to approximate the transfer vector.</span></span>

![Gleichung des ungefäckten Übertragungs Vektors](images/prt-theory-eq6.png)

<span data-ttu-id="10aa8-169">Dabei gilt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="10aa8-169">where:</span></span>



| <span data-ttu-id="10aa8-170">Parameter</span><span class="sxs-lookup"><span data-stu-id="10aa8-170">Parameter</span></span>      | <span data-ttu-id="10aa8-171">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10aa8-171">Description</span></span>                                          |
|----------------|------------------------------------------------------|
| <span data-ttu-id="10aa8-172">TP</span><span class="sxs-lookup"><span data-stu-id="10aa8-172">Tₚ</span></span>             | <span data-ttu-id="10aa8-173">Der Übertragungs Vektor für Scheitelpunkt p.</span><span class="sxs-lookup"><span data-stu-id="10aa8-173">The transfer vector for vertex p.</span></span>                    |
| <span data-ttu-id="10aa8-174">Gegründete</span><span class="sxs-lookup"><span data-stu-id="10aa8-174">Mₖ</span></span>             | <span data-ttu-id="10aa8-175">Der Mittelwert für Cluster k.</span><span class="sxs-lookup"><span data-stu-id="10aa8-175">The mean for cluster k.</span></span>                              |
| <span data-ttu-id="10aa8-176">j</span><span class="sxs-lookup"><span data-stu-id="10aa8-176">j</span></span>              | <span data-ttu-id="10aa8-177">Eine ganze Zahl, die die Anzahl der PCA-Vektoren summiert.</span><span class="sxs-lookup"><span data-stu-id="10aa8-177">An integer that sums over the number of PCA vectors.</span></span> |
| <span data-ttu-id="10aa8-178">N</span><span class="sxs-lookup"><span data-stu-id="10aa8-178">N</span></span>              | <span data-ttu-id="10aa8-179">Die Anzahl der PCA-Vektoren.</span><span class="sxs-lookup"><span data-stu-id="10aa8-179">The number of PCA vectors.</span></span>                           |
| <span data-ttu-id="10aa8-180">w-<sub>PJ</sub></span><span class="sxs-lookup"><span data-stu-id="10aa8-180">w<sub>pj</sub></span></span> | <span data-ttu-id="10aa8-181">Die Jth-PCA-Gewichtung für Punkt p.</span><span class="sxs-lookup"><span data-stu-id="10aa8-181">The jth PCA weight for point p.</span></span>                      |
| <span data-ttu-id="10aa8-182">B-<sub>kJ</sub></span><span class="sxs-lookup"><span data-stu-id="10aa8-182">B<sub>kj</sub></span></span> | <span data-ttu-id="10aa8-183">Der Jth PCA-Basis Vektor für Cluster k.</span><span class="sxs-lookup"><span data-stu-id="10aa8-183">The jth PCA basis vector for cluster k.</span></span>              |



 

<span data-ttu-id="10aa8-184">Ein Cluster ist einfach eine bestimmte Anzahl von Vertices, die denselben Mittel Vektor verwenden.</span><span class="sxs-lookup"><span data-stu-id="10aa8-184">A cluster is simply some number of vertices that share the same mean vector.</span></span> <span data-ttu-id="10aa8-185">Im folgenden wird erläutert, wie der Cluster Mittelwert, die PCA-Gewichtungen, die PCA-Basis Vektoren und die Cluster-IDs für die Scheitel Punkte erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="10aa8-185">How to get the cluster mean, the PCA weights, the PCA basis vectors, and the cluster ids for the vertices is discussed below.</span></span>

<span data-ttu-id="10aa8-186">Durch diese beiden Gleichungen ergibt sich Folgendes:</span><span class="sxs-lookup"><span data-stu-id="10aa8-186">Substituting these two equations yields:</span></span>

![Gleichung der Beendigungs Glanz, nachdem der Übertragungs Vektor ersetzt wurde.](images/prt-theory-eq7.png)

<span data-ttu-id="10aa8-188">Anschließend ergibt die Verteilung des Punkt Produkts die folgende Gleichung.</span><span class="sxs-lookup"><span data-stu-id="10aa8-188">Then distributing the dot product yields the following equation.</span></span>

![Gleichung der Beendigungs Glanz nach der Verteilung des Punkt Produkts](images/prt-theory-eq8.png)

<span data-ttu-id="10aa8-190">Da beide (MK) L ') und (B<sub>kJ</sub>) L ') sind konstant pro Scheitelpunkt. das Beispiel berechnet diese Werte mit der CPU und übergibt sie als Konstanten an den Vertexshader. Da sich w<sub>PJ</sub> für jeden Scheitelpunkt ändert, speichert das Beispiel diese pro-Vertex-Daten im Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="10aa8-190">Because both (Mₖ· L') and (B<sub>kj</sub>· L') are constant per vertex, the sample calculates these values with the CPU and passes them as constants into the vertex shader; because w<sub>pj</sub> changes for each vertex, the sample stores this per-vertex data in the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10aa8-191">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="10aa8-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10aa8-192">Voraus berechnete Strahlungs Übertragung</span><span class="sxs-lookup"><span data-stu-id="10aa8-192">Precomputed Radiance Transfer</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



