---
description: Voraus berechnete Strahlungs Übertragung (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Voraus berechnete Strahlungs Übertragung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94829a2559888c61ae795309bac5d1ab699d7f27
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569040"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a><span data-ttu-id="1b9db-103">Voraus berechnete Strahlungs Übertragung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1b9db-103">Precomputed Radiance Transfer (Direct3D 9)</span></span>

## <a name="using-precomputed-radiance-transfer"></a><span data-ttu-id="1b9db-104">Verwenden der Voraus berechneten Strahlungs Übertragung</span><span class="sxs-lookup"><span data-stu-id="1b9db-104">Using Precomputed Radiance Transfer</span></span>

<span data-ttu-id="1b9db-105">Es gibt verschiedene Formen der Komplexität in interessanten Szenen, einschließlich der Modellierung der Beleuchtungs Umgebung (d. h. Flächen Beleuchtungs Modelle im Vergleich zu Punkt-/direktionalen) und der Art von globalen Effekten, die modelliert werden (z. b. Schatten, interreflektionen, unter Oberflächen Streuung). Herkömmliche interaktive Renderingverfahren modellieren einen begrenzten Anteil dieser Komplexität.</span><span class="sxs-lookup"><span data-stu-id="1b9db-105">There are several forms of complexity present in interesting scenes, including how the lighting environment is modeled (that is, area lighting models versus point/directional ones) and what kind of global effects are modeled (for example, shadows, interreflections, subsurface scattering.) Traditional interactive rendering techniques model a limited amount of this complexity.</span></span> <span data-ttu-id="1b9db-106">PRT aktiviert diese Effekte mit einigen erheblichen Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="1b9db-106">PRT enables these effects with some significant restrictions:</span></span>

-   <span data-ttu-id="1b9db-107">Es wird davon ausgegangen, dass Objekte starr sind (d. h. keine Deformationen).</span><span class="sxs-lookup"><span data-stu-id="1b9db-107">Objects are assumed to be rigid (that is, no deformations).</span></span>
-   <span data-ttu-id="1b9db-108">Dabei handelt es sich um einen Objekt zentrierten Ansatz (es sei denn, Objekte werden gemeinsam verschoben, diese globalen Effekte werden nicht zwischen ihnen beibehalten).</span><span class="sxs-lookup"><span data-stu-id="1b9db-108">It is an object-centric approach (unless objects are moved together, these global effects are not maintained between them).</span></span>
-   <span data-ttu-id="1b9db-109">Nur die Beleuchtung mit niedriger Frequenz wird modelliert (was zu weichen Schatten führt). Bei Hochfrequenz Lichtern (scharfe Schatten) müssten herkömmliche Techniken eingesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="1b9db-109">Only low-frequency lighting is modeled (resulting in soft shadows.) For high-frequency lights (sharp shadows), traditional techniques would have to be employed.</span></span>

<span data-ttu-id="1b9db-110">PRT erfordert eine der folgenden beiden Optionen:</span><span class="sxs-lookup"><span data-stu-id="1b9db-110">PRT requires either of the following, but not both:</span></span>

-   <span data-ttu-id="1b9db-111">hochgradig Mosaik Modelle und vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1b9db-111">highly-tessellated models and vs\_1\_1</span></span>
-   <span data-ttu-id="1b9db-112">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1b9db-112">ps\_2\_0</span></span>

### <a name="standard-diffuse-lighting-versus-prt"></a><span data-ttu-id="1b9db-113">Standard mäßige diffuse Beleuchtung im Vergleich zu PRT</span><span class="sxs-lookup"><span data-stu-id="1b9db-113">Standard Diffuse Lighting versus PRT</span></span>

<span data-ttu-id="1b9db-114">Die folgende Abbildung wird mithilfe des herkömmlichen (n) Beleuchtungs Modells gerendert.</span><span class="sxs-lookup"><span data-stu-id="1b9db-114">The following illustration is rendered using the traditional (n · l) lighting model.</span></span> <span data-ttu-id="1b9db-115">Scharfe Schatten können mit einem anderen Durchlauf und einer Form der Shadowing-Technik (Schatten Tiefe Karten oder schattenvolumes) aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="1b9db-115">Sharp shadows could be enabled using another pass and some form of shadowing technique (shadow depth maps or shadow volumes).</span></span> <span data-ttu-id="1b9db-116">Das Hinzufügen mehrerer Lichter erfordert entweder mehrere Durchgänge (wenn Schatten verwendet werden sollen) oder komplexere Shader mit herkömmlichen Techniken.</span><span class="sxs-lookup"><span data-stu-id="1b9db-116">Adding multiple lights would require either multiple passes (if shadows are to be used) or more complex shaders with traditional techniques.</span></span>

![Screenshot einer Abbildung, die mithilfe des herkömmlichen Beleuchtungs Modells gerendert wird](images/prt-diffuse-cropped.png)

<span data-ttu-id="1b9db-118">Die nächste Abbildung wird mit PRT mit der besten Näherung eines einzelnen direktionalen Lichts gerendert, das Sie auflösen kann.</span><span class="sxs-lookup"><span data-stu-id="1b9db-118">The next illustration is rendered with PRT using the best approximation of a single directional light that it can resolve.</span></span> <span data-ttu-id="1b9db-119">Dies führt dazu, dass weiche Schatten nicht mit herkömmlichen Techniken erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="1b9db-119">This results in soft shadows that would be difficult to produce with traditional techniques.</span></span> <span data-ttu-id="1b9db-120">Da PRT immer alle Beleuchtungs Umgebungen mit mehreren Lichtern oder einer Umgebungs Zuordnung modelliert, würden Sie nur die Werte (aber nicht die Anzahl) der Konstanten ändern, die vom Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b9db-120">Because PRT always models complete lighting environments adding multiple lights or using an environment map, you would only change the values (but not the number) of constants used by the shader.</span></span>

![Screenshot einer mit PRT gerenderten Abbildung](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a><span data-ttu-id="1b9db-122">PRT mit interreflektionen</span><span class="sxs-lookup"><span data-stu-id="1b9db-122">PRT with Interreflections</span></span>

<span data-ttu-id="1b9db-123">Die direkte Beleuchtung erreicht die Oberfläche direkt vom Licht.</span><span class="sxs-lookup"><span data-stu-id="1b9db-123">Direct lighting reaches the surface directly from the light.</span></span> <span data-ttu-id="1b9db-124">Interreflektionen sind Lichtreich und erreichen die Oberfläche, nachdem eine andere Oberfläche so oft wie oft ausgeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="1b9db-124">Interreflections are light reaching the surface after bouncing off some other surface some number of times.</span></span> <span data-ttu-id="1b9db-125">PRT kann dieses Verhalten modellieren, ohne die Leistung zur Laufzeit zu ändern, indem der Simulator einfach mit anderen Parametern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b9db-125">PRT can model this behavior without changing the performance at run time by simply running the simulator with different parameters.</span></span>

<span data-ttu-id="1b9db-126">Die folgende Abbildung wird nur mithilfe von Direct PRT erstellt (0 springt ohne interreflektionen).</span><span class="sxs-lookup"><span data-stu-id="1b9db-126">The following illustration is created using direct PRT only (0 bounces with no interreflections).</span></span>

![Screenshot einer Abbildung, die nur mit Direct PRT gerendert wird](images/prt-nointerreflections.png)

<span data-ttu-id="1b9db-128">Die folgende Abbildung wird mithilfe von PRT mit interreflektionen erstellt (2 springt with interreflektionen).</span><span class="sxs-lookup"><span data-stu-id="1b9db-128">The following illustration is created using PRT with interreflections (2 bounces with interreflections).</span></span>

![Screenshot einer Abbildung, die mithilfe von PRT mit interreflektionen gerendert wird](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a><span data-ttu-id="1b9db-130">PRT with subsurface Scattering</span><span class="sxs-lookup"><span data-stu-id="1b9db-130">PRT with Subsurface Scattering</span></span>

<span data-ttu-id="1b9db-131">Unter Surface im ist ein Verfahren, das die Art und Weise anzeigt, wie das Licht durch bestimmte Materialien verläuft.</span><span class="sxs-lookup"><span data-stu-id="1b9db-131">Subsurface scattering is a technique that models how light passes through certain materials.</span></span> <span data-ttu-id="1b9db-132">Drücken Sie als Beispiel eine Beleuchtung mit beleuchteter Taschenlampe.</span><span class="sxs-lookup"><span data-stu-id="1b9db-132">As an example, press a lit flashlight against the palm of your hand.</span></span> <span data-ttu-id="1b9db-133">Das Licht aus der Taschenlampe durchläuft Ihre Hand, springt um (Ändern der Farbe im Prozess) und beendet von der anderen Seite.</span><span class="sxs-lookup"><span data-stu-id="1b9db-133">The light from the flashlight passes through your hand, bounces around (changing color in the process), and exits from the other side of your hand.</span></span> <span data-ttu-id="1b9db-134">Dies kann auch mit einfachen Änderungen am Simulator und ohne Änderungen an der Laufzeit modelliert werden.</span><span class="sxs-lookup"><span data-stu-id="1b9db-134">This can also be modeled with simple changes to the simulator and no changes to the runtime.</span></span>

<span data-ttu-id="1b9db-135">In der folgenden Abbildung wird PRT mit unter Oberflächen Streuung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1b9db-135">The following illustration demonstrates PRT with subsurface scattering.</span></span>

![Screenshot einer Abbildung, die durch die Verwendung von PRT mit der unter Oberflächen Streuung gerendert wird](images/prt-subsurface.png)

## <a name="how-prt-works"></a><span data-ttu-id="1b9db-137">Funktionsweise von PRT</span><span class="sxs-lookup"><span data-stu-id="1b9db-137">How PRT Works</span></span>

<span data-ttu-id="1b9db-138">Die folgenden Begriffe sind hilfreich, um zu verstehen, wie PRT funktioniert, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1b9db-138">The following terms are useful for understanding how PRT works, as illustrated in the following diagram.</span></span>

<span data-ttu-id="1b9db-139">Quell Ausstrahlung: die Quell Ausstrahlung stellt die Beleuchtungs Umgebung als Ganzes dar.</span><span class="sxs-lookup"><span data-stu-id="1b9db-139">Source Radiance: The source radiance represents the lighting environment as a whole.</span></span> <span data-ttu-id="1b9db-140">In PRT wird eine beliebige Umgebung mithilfe der kugelförmigen harmonischen Basis angezeigt. diese Beleuchtung wird vorausgesetzt, dass Sie relativ zum-Objekt ist (dieselbe Annahme wird in Umgebungs Zuordnungen vorgenommen).</span><span class="sxs-lookup"><span data-stu-id="1b9db-140">In PRT an arbitrary environment is approximated using the spherical harmonic basis - this lighting is assumed to be distant relative to the object (the same assumption that is made with environment maps.)</span></span>

<span data-ttu-id="1b9db-141">Exit-Ausdruck: die Ausgangs-Glanz ist das Licht, das von einem Punkt auf der Oberfläche von einer beliebigen möglichen Quelle verlässt (reflektierte Strahlen, unter Oberflächen-Scattering, Ausgabe).</span><span class="sxs-lookup"><span data-stu-id="1b9db-141">Exit Radiance: Exit radiance is the light leaving from a point on the surface from any possible source (reflected radiance, subsurface scattering, emission).</span></span>

<span data-ttu-id="1b9db-142">Übertragungs Vektoren: Übertragungs Vektoren ordnen Quell Strahlen in eine Ausgangs-und vorab berechnete Verwendung einer komplexen Light-Transport-Simulation.</span><span class="sxs-lookup"><span data-stu-id="1b9db-142">Transfer Vectors: Transfer vectors map Source Radiance into exit radiance and are precomputed offline using a complex light transport simulation.</span></span>

![Diagramm zur Funktionsweise von PRT](images/prt-lightingpicture.png)

<span data-ttu-id="1b9db-144">PRT Faktoren den Renderingprozess in zwei Phasen, wie im folgenden Diagramm dargestellt:</span><span class="sxs-lookup"><span data-stu-id="1b9db-144">PRT factors the rendering process into two stages, as shown in the following diagram:</span></span>

1.  <span data-ttu-id="1b9db-145">Eine teure Light-Transport-Simulation führt eine Vorberechnung der Übertragungskoeffizienten aus, die zur Laufzeit verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1b9db-145">An expensive light transport simulation precomputes transfer coefficients that can be used at run time.</span></span>
2.  <span data-ttu-id="1b9db-146">In einer relativ einfachen Lauf Zeit Phase wird zunächst die Beleuchtungs Umgebung unter Verwendung der kugelförmigen harmonischen Basis und dann diese Beleuchtungs Koeffizienten und die Voraus berechneten Übertragungskoeffizienten (aus Phase 1) mit einem einfachen Shader verwendet, was zu einem exitglanz führt (das Licht, das das Objekt verlässt).</span><span class="sxs-lookup"><span data-stu-id="1b9db-146">A relatively lightweight run-time stage first approximates the lighting environment using the spherical harmonic basis, then uses these lighting coefficients and the precomputed transfer coefficients (from stage 1) with a simple shader, resulting in exit radiance (the light leaving the object).</span></span>

![Diagramm des PRT-Datenflusses](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a><span data-ttu-id="1b9db-148">Verwenden der PRT-API</span><span class="sxs-lookup"><span data-stu-id="1b9db-148">How to Use the PRT API</span></span>

1.  <span data-ttu-id="1b9db-149">Berechnen Sie die Übertragungs Vektoren mit einem der COMPUTE-... Methoden von [**ID3DXPRTEngine**](id3dxprtengine.md).</span><span class="sxs-lookup"><span data-stu-id="1b9db-149">Compute the transfer vectors with one of the Compute... methods of [**ID3DXPRTEngine**](id3dxprtengine.md).</span></span>

    <span data-ttu-id="1b9db-150">Der direkte Umgang mit diesen Übertragungs Vektoren erfordert eine beträchtliche Menge an Arbeitsspeicher-und shaderberechnung.</span><span class="sxs-lookup"><span data-stu-id="1b9db-150">Directly dealing with these transfer vectors requires a significant amount of memory and shader computation.</span></span> <span data-ttu-id="1b9db-151">Durch die Komprimierung wird der erforderliche Arbeitsspeicher und die Shader-Berechnung erheblich reduziert.</span><span class="sxs-lookup"><span data-stu-id="1b9db-151">Compression significantly reduces the amount of memory and shader computation required.</span></span>

    <span data-ttu-id="1b9db-152">Die abschließenden Beleuchtungs Werte werden in einem Vertex-Shader berechnet, der die folgende komprimierte renderinggleichung implementiert.</span><span class="sxs-lookup"><span data-stu-id="1b9db-152">The final lighting values are calculated in a vertex shader that implements the following compressed rendering equation.</span></span>

    ![Gleichung des PRT-Rendering](images/prt-shaderequation.png)

    <span data-ttu-id="1b9db-154">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="1b9db-154">Where:</span></span>

    

    | <span data-ttu-id="1b9db-155">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b9db-155">Parameter</span></span>      | <span data-ttu-id="1b9db-156">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b9db-156">Description</span></span>                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="1b9db-157">Neutraler</span><span class="sxs-lookup"><span data-stu-id="1b9db-157">Rₚ</span></span>             | <span data-ttu-id="1b9db-158">Ein einzelner Kanal mit exitstrahlung bei Scheitelpunkt p und wird bei jedem Scheitelpunkt im Mesh ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="1b9db-158">A single channel of exit radiance at vertex p and is evaluated at every vertex on the mesh.</span></span>                     |
    | <span data-ttu-id="1b9db-159">Gegründete</span><span class="sxs-lookup"><span data-stu-id="1b9db-159">Mₖ</span></span>             | <span data-ttu-id="1b9db-160">Der Mittelwert für Cluster k.</span><span class="sxs-lookup"><span data-stu-id="1b9db-160">The mean for cluster k.</span></span> <span data-ttu-id="1b9db-161">Dies ist ein "Order ²"-Vektor von Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="1b9db-161">This is an Order² vector of coefficients.</span></span>                                               |
    | <span data-ttu-id="1b9db-162">k</span><span class="sxs-lookup"><span data-stu-id="1b9db-162">k</span></span>              | <span data-ttu-id="1b9db-163">Die Cluster-ID für Vertex p.</span><span class="sxs-lookup"><span data-stu-id="1b9db-163">The cluster ID for vertex p.</span></span>                                                                                    |
    | <span data-ttu-id="1b9db-164">L<sup>'</sup></span><span class="sxs-lookup"><span data-stu-id="1b9db-164">L<sup>'</sup></span></span>  | <span data-ttu-id="1b9db-165">Die Näherung der Quell Ausstrahlung in die sh-Basisfunktionen.</span><span class="sxs-lookup"><span data-stu-id="1b9db-165">The approximation of the source radiance into the SH basis functions.</span></span> <span data-ttu-id="1b9db-166">Dies ist ein "Order ²"-Vektor von Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="1b9db-166">This is an Order² vector of coefficients.</span></span> |
    | <span data-ttu-id="1b9db-167">j</span><span class="sxs-lookup"><span data-stu-id="1b9db-167">j</span></span>              | <span data-ttu-id="1b9db-168">Eine ganze Zahl, die die Anzahl der PCA-Vektoren summiert.</span><span class="sxs-lookup"><span data-stu-id="1b9db-168">An integer that sums over the number of PCA vectors.</span></span>                                                            |
    | <span data-ttu-id="1b9db-169">w-<sub>PJ</sub></span><span class="sxs-lookup"><span data-stu-id="1b9db-169">w<sub>pj</sub></span></span> | <span data-ttu-id="1b9db-170">Die Jth-PCA-Gewichtung für Punkt p.</span><span class="sxs-lookup"><span data-stu-id="1b9db-170">The jth PCA weight for point p.</span></span> <span data-ttu-id="1b9db-171">Dies ist ein einzelner Koeffizient.</span><span class="sxs-lookup"><span data-stu-id="1b9db-171">This is a single coefficient.</span></span>                                                   |
    | <span data-ttu-id="1b9db-172">B-<sub>kJ</sub></span><span class="sxs-lookup"><span data-stu-id="1b9db-172">B<sub>kj</sub></span></span> | <span data-ttu-id="1b9db-173">Der Jth PCA-Basis Vektor für Cluster k.</span><span class="sxs-lookup"><span data-stu-id="1b9db-173">The jth PCA basis vector for cluster k.</span></span> <span data-ttu-id="1b9db-174">Dies ist ein "Order ²"-Vektor von Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="1b9db-174">This is an Order² vector of coefficients.</span></span>                               |

    

     

    <span data-ttu-id="1b9db-175">Der Extraktions-... [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Methoden ermöglichen den Zugriff auf komprimierte Daten aus der Simulation.</span><span class="sxs-lookup"><span data-stu-id="1b9db-175">The Extract... methods of [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) provide access to compressed data from the simulation.</span></span>

2.  <span data-ttu-id="1b9db-176">Berechnen der Quell Ausstrahlung.</span><span class="sxs-lookup"><span data-stu-id="1b9db-176">Compute the source radiance.</span></span>

    <span data-ttu-id="1b9db-177">Es gibt mehrere Hilfsfunktionen in der API, die eine Vielzahl von gängigen Beleuchtungs Szenarios verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="1b9db-177">There are several helper functions in the API to handle a variety of common lighting scenarios.</span></span>

    

    | <span data-ttu-id="1b9db-178">Funktion</span><span class="sxs-lookup"><span data-stu-id="1b9db-178">Function</span></span>                                                         | <span data-ttu-id="1b9db-179">Zweck</span><span class="sxs-lookup"><span data-stu-id="1b9db-179">Purpose</span></span>                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="1b9db-180">**D3DXSHEvalDirectionalLight**</span><span class="sxs-lookup"><span data-stu-id="1b9db-180">**D3DXSHEvalDirectionalLight**</span></span>](d3dxshevaldirectionallight.md) | <span data-ttu-id="1b9db-181">Gleicht ein herkömmliches Direktionales Licht.</span><span class="sxs-lookup"><span data-stu-id="1b9db-181">Approximates a conventional directional light.</span></span>                                                              |
    | [<span data-ttu-id="1b9db-182">**D3DXSHEvalSphericalLight**</span><span class="sxs-lookup"><span data-stu-id="1b9db-182">**D3DXSHEvalSphericalLight**</span></span>](d3dxshevalsphericallight.md)     | <span data-ttu-id="1b9db-183">Entspricht lokalen kugelförmigen Lichtquellen.</span><span class="sxs-lookup"><span data-stu-id="1b9db-183">Approximates local spherical light sources.</span></span> <span data-ttu-id="1b9db-184">(Beachten Sie, dass PRT nur bei Entfernungs Beleuchtungs Umgebungen funktioniert.)</span><span class="sxs-lookup"><span data-stu-id="1b9db-184">(Note that PRT only works with distance lighting environments.)</span></span> |
    | [<span data-ttu-id="1b9db-185">**D3DXSHEvalConeLight**</span><span class="sxs-lookup"><span data-stu-id="1b9db-185">**D3DXSHEvalConeLight**</span></span>](d3dxshevalconelight.md)               | <span data-ttu-id="1b9db-186">Gleicht eine entfernte Bereichs-Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="1b9db-186">Approximates a distant area light source.</span></span> <span data-ttu-id="1b9db-187">Ein Beispiel wäre die Sun (sehr kleiner Kegelwinkel).</span><span class="sxs-lookup"><span data-stu-id="1b9db-187">An example would be the sun (very small cone angle).</span></span>              |
    | [<span data-ttu-id="1b9db-188">**D3DXSHEvalHemisphereLight**</span><span class="sxs-lookup"><span data-stu-id="1b9db-188">**D3DXSHEvalHemisphereLight**</span></span>](d3dxshevalhemispherelight.md)   | <span data-ttu-id="1b9db-189">Wertet ein Licht aus, bei dem es sich um eine lineare interpolung zwischen zwei Farben handelt (eine auf jedem Pol einer Kugel).</span><span class="sxs-lookup"><span data-stu-id="1b9db-189">Evaluates a light that is a linear interpolation between two colors (one on each pole of a sphere).</span></span>         |

    

     

3.  <span data-ttu-id="1b9db-190">Berechnen Sie die Exit-Strahlkraft.</span><span class="sxs-lookup"><span data-stu-id="1b9db-190">Compute the exit radiance.</span></span>

    <span data-ttu-id="1b9db-191">Gleichung 1 muss nun entweder mit einem Scheitelpunkt oder einem Pixelshader an jedem Punkt ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="1b9db-191">Equation 1 now has to be evaluated at every point using either a vertex or pixel shader.</span></span> <span data-ttu-id="1b9db-192">Bevor der Shader ausgewertet werden kann, müssen Konstanten vorab berechnet und in die Konstante Tabelle geladen werden (Weitere Informationen finden Sie im [PRT-Demo Beispiel](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) ).</span><span class="sxs-lookup"><span data-stu-id="1b9db-192">Before the shader can be evaluated, constants have to be precomputed and loaded into the constant table (see the [PRT Demo Sample](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) for details).</span></span> <span data-ttu-id="1b9db-193">Der Shader selbst ist eine einfache Implementierung dieser Gleichung.</span><span class="sxs-lookup"><span data-stu-id="1b9db-193">The shader itself is a straightforward implementation of this equation.</span></span>

    ```
    struct VS_OUTPUT
    {
        float4 Position   : POSITION;   // vertex position 
        float2 TextureUV  : TEXCOORD0;  // vertex texture coordinates 
        float4 Diffuse    : COLOR0;     // vertex diffuse color
    };

    VS_OUTPUT Output;   
    Output.Position = mul(vPos, mWorldViewProjection);

    float4 vExitR = float4(0,0,0,0);
    float4 vExitG = float4(0,0,0,0);
    float4 vExitB = float4(0,0,0,0);
        
    for (int i=0; i < (NUM_PCA_VECTORS/4); i++) 
    {
       vExitR += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*0];
       vExitG += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*1];
       vExitB += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*2];
    }
       
    float4 vExitRadiance = vClusteredPCA[iClusterOffset];
    vExitRadiance.r += dot(vExitR,1);
    vExitRadiance.g += dot(vExitG,1);
    vExitRadiance.b += dot(vExitB,1);

    Output.Diffuse = vExitRadiance;
    ```

    

## <a name="references"></a><span data-ttu-id="1b9db-194">References</span><span class="sxs-lookup"><span data-stu-id="1b9db-194">References</span></span>

<span data-ttu-id="1b9db-195">Weitere Informationen zu PRT-und sphärischen Harmonisierungen finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="1b9db-195">For more information about PRT and spherical harmonics, see the following papers:</span></span>


```
Precomputed Radiance Transfer for Real-Time Rendering in Dynamic, 
Low-Frequency Lighting Environments 
P.-P. Sloan, J. Kautz, J. Snyder
SIGGRAPH 2002 

Clustered Principal Components for Precomputed Radiance Transfer 
P.-P. Sloan, J. Hall, J. Hart, J. Snyder 
SIGGRAPH 2003 

Efficient Evaluation of Irradiance Environment Maps 
P.-P. Sloan 
ShaderX 2,  W. Engel 

Spherical Harmonic Lighting: The Gritty Details 
R. Green 
GDC 2003 

An Efficient Representation for Irradiance Environment Maps 
R. Ramamoorthi, P. Hanrahan 

A Practical Model for Subsurface Light Transport 
H. W. Jensen, S. R. Marschner, M. Levoy, and P. Hanrahan 
SIGGRAPH 2001 

Bi-Scale Radiance Transfer 
P.-P. Sloan, X. Liu, H.-Y. Shum, J. Snyder
SIGGRAPH 2003 

Fast, Arbitrary BRDF Shading for Low-Frequency Lighting Using Spherical 
Harmonics 
J. Kautz, P.-P. Sloan, J. Snyder
12th Eurographics Workshop on Rendering 

Precomputing Interactive Dynamic Deformable Scenes 
D. James, K. Fatahalian 
SIGGRAPH 2003 

All-Frequency Shadows Using Non-linear Wavelet Lighting Approximation 
R. Ng, R. Ramamoorth, P. Hanrahan 
SIGGRAPH 2003 

Matrix Radiance Transfer 
J. Lehtinen, J. Kautz
SIGGRAPH 2003 

Math World 
E. W. Weisstein, Wolfram Research, Inc. 

Quantum Theory of Angular Momentum 
D. A. Varshalovich, A.N. Moskalev, V.K. Khersonskii 
```



## <a name="related-topics"></a><span data-ttu-id="1b9db-196">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b9db-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b9db-197">Erweiterte Themen</span><span class="sxs-lookup"><span data-stu-id="1b9db-197">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="1b9db-198">PRT-Gleichungen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1b9db-198">PRT Equations (Direct3D 9)</span></span>](prt-equations.md)
</dt> <dt>

[<span data-ttu-id="1b9db-199">Darstellen von PRT mit Texturen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1b9db-199">Representing PRT With Textures (Direct3D 9)</span></span>](representing-prt-with-textures.md)
</dt> <dt>

[<span data-ttu-id="1b9db-200">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="1b9db-200">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="1b9db-201">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="1b9db-201">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="1b9db-202">**ID3DXPRTEngine**</span><span class="sxs-lookup"><span data-stu-id="1b9db-202">**ID3DXPRTEngine**</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="1b9db-203">**ID3DXTextureGutterHelper**</span><span class="sxs-lookup"><span data-stu-id="1b9db-203">**ID3DXTextureGutterHelper**</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="1b9db-204">Voraus berechnete Strahlungs Übertragungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="1b9db-204">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="1b9db-205">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1b9db-205">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



