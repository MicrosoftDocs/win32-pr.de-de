---
description: Viele Rendering- und Inhaltsgenerierungstechniken erfordern eine eindeutige, nicht überlappende Karte eines 2D-Signals (z. B. einer Textur) auf einem Gitternetz.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Verwenden von UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8faeaa0a416f6f062c81c4101ff47d5222ca75d
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826328"
---
# <a name="using-uvatlas-direct3d-9"></a><span data-ttu-id="15adb-103">Verwenden von UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="15adb-103">Using UVAtlas (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="15adb-104">UVAtlas wurde ursprünglich in der jetzt veralteten D3DX9-Utilty-Bibliothek ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="15adb-104">UVAtlas was originally shipped in the now-deprecated D3DX9 utilty library.</span></span> <span data-ttu-id="15adb-105">Die neueste Version ist unter [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15adb-105">The latest version is available at [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas).</span></span>

<span data-ttu-id="15adb-106">Viele Rendering- und Inhaltsgenerierungstechniken erfordern eine eindeutige, nicht überlappende Karte eines 2D-Signals (z. B. einer Textur) auf einem Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="15adb-106">Many rendering and content generation techniques require a unique, non-overlapping map of a 2D signal (such as a texture) onto a mesh.</span></span> <span data-ttu-id="15adb-107">Zu diesen Techniken gehören:</span><span class="sxs-lookup"><span data-stu-id="15adb-107">Such techniques include:</span></span>

-   <span data-ttu-id="15adb-108">Normal-/Verschiebungszuordnung</span><span class="sxs-lookup"><span data-stu-id="15adb-108">Normal/displacement mapping</span></span>
-   <span data-ttu-id="15adb-109">Texturraum-PRT-Simulationen und Lichtkarten</span><span class="sxs-lookup"><span data-stu-id="15adb-109">Texture-space PRT simulations and light maps</span></span>
-   <span data-ttu-id="15adb-110">Oberflächenzeichnung</span><span class="sxs-lookup"><span data-stu-id="15adb-110">Surface painting</span></span>
-   <span data-ttu-id="15adb-111">Texturraumbeleuchtung</span><span class="sxs-lookup"><span data-stu-id="15adb-111">Texture-space lighting</span></span>

<span data-ttu-id="15adb-112">Das manuelle Generieren einer eindeutigen UV-Zuordnung ist oft zeitaufwändig und mühsam. Dies gilt insbesondere, wenn die Eingabegeometrie komplex ist und eine effiziente/verzerrungsfreie Texturraumnutzung gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="15adb-112">Generating a unique UV mapping manually is often time-consuming and tedious; this is especially true when the input geometry is complex and efficient/low-distortion texture-space utilization is desired.</span></span> <span data-ttu-id="15adb-113">Die folgende Abbildung zeigt ein Beispielgitternetz und den entsprechenden Texturat atlas.</span><span class="sxs-lookup"><span data-stu-id="15adb-113">The following illustration shows an example mesh and its corresponding texture atlas.</span></span>

![Zeigt ein Beispielgitternetz und den entsprechenden Texturat atlas.](images/uvatlas1.jpg)

<span data-ttu-id="15adb-115">Dieses Beispiel zeigt ein Gitternetz (links) und die entsprechende Normalkarte des UV-Raumes (auf der rechten Seite).</span><span class="sxs-lookup"><span data-stu-id="15adb-115">This example shows a mesh (on the left) and the corresponding UV-space normal map (on the right).</span></span> <span data-ttu-id="15adb-116">Beachten Sie, dass der Texturat atlas mehrere Gruppen oder Cluster von Daten enthält. Jeder Cluster wird als Diagramm bezeichnet und enthält im obigen Beispiel die normalen Daten für einen Teil des Gitternetzes.</span><span class="sxs-lookup"><span data-stu-id="15adb-116">Notice that the texture atlas contains several groups or clusters of data; each cluster is called a chart and in the example above, displays contains the normal data for a portion of the mesh.</span></span>

<span data-ttu-id="15adb-117">Die D3DX UVAtlas-APIs generieren automatisch einen optimalen, nicht überlappenden Texturat atlas.</span><span class="sxs-lookup"><span data-stu-id="15adb-117">The D3DX UVAtlas APIs automatically generate an optimal, non-overlapping texture atlas.</span></span> <span data-ttu-id="15adb-118">Die APIs stellen Eingabeparameter bereit, die Folgendes ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="15adb-118">The APIs provide input parameters that allow you to:</span></span>

-   <span data-ttu-id="15adb-119">Minimieren Sie Texturstreckung, Verzerrung und Untersampling.</span><span class="sxs-lookup"><span data-stu-id="15adb-119">Minimize texture stretch, distortion, and undersampling.</span></span>
-   <span data-ttu-id="15adb-120">Maximieren der Texturraum-Komprimierungsdichte zur effizienten Verwendung des Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="15adb-120">Maximize texture-space packing density for efficient use of memory.</span></span>
-   <span data-ttu-id="15adb-121">Stellen Sie eine gleichmäßige Stichprobenentnahme über das Gitternetz bereit, um Diskontinuitäten bei der Stichprobenhäufigkeit zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="15adb-121">Provide an even sampling across the mesh, minimizing discontinuities in sampling frequency.</span></span>

## <a name="how-uvatlas-works"></a><span data-ttu-id="15adb-122">Funktionsweise von UVAtlas</span><span class="sxs-lookup"><span data-stu-id="15adb-122">How UVAtlas Works</span></span>

<span data-ttu-id="15adb-123">Die UVAtlas-APIs (siehe [UVAtlas-Funktionen)](dx9-graphics-reference-d3dx-functions-uvatlas.md)generieren einen Texturat atlas, indem sie eine Oberfläche in Diagramme partitionieren und die Diagramme in einen Texturat atlas packen.</span><span class="sxs-lookup"><span data-stu-id="15adb-123">The UVAtlas APIs (see [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generate a texture atlas by partitioning a surface into charts and packing the charts into a texture atlas.</span></span> <span data-ttu-id="15adb-124">Verwenden Sie [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) und [**D3DXUVAtlasPack,**](d3dxuvatlaspack.md) um diese Schritte separat auszuführen. oder verwenden [**Sie D3DXUVAtlasCreate,**](d3dxuvatlascreate.md) um einen einzelnen Aufruf zu partitionieren, zu parametrisieren und zu packen.</span><span class="sxs-lookup"><span data-stu-id="15adb-124">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) and [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) to perform these steps separately; or use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) to partition, parameterize and pack in a single call.</span></span>

-   [<span data-ttu-id="15adb-125">Partitionieren und Parametrisieren eines Gitternetzes</span><span class="sxs-lookup"><span data-stu-id="15adb-125">Partitioning and Parameterizing a Mesh</span></span>](#partitioning-and-parameterizing-a-mesh)
-   [<span data-ttu-id="15adb-126">Verwenden integrierter Metrik tensors zum Steuern der Parametrisierung</span><span class="sxs-lookup"><span data-stu-id="15adb-126">Using Integrated Metric Tensors to Control Parameterization</span></span>](#using-integrated-metric-tensors-to-control-parameterization)
-   [<span data-ttu-id="15adb-127">Verwenden von Adjazenzdaten für vom Benutzer angegebene Errungen</span><span class="sxs-lookup"><span data-stu-id="15adb-127">Using Adjacency Data for User Specified Creases</span></span>](#using-adjacency-data-for-user-specified-creases)
-   [<span data-ttu-id="15adb-128">Packen von Diagrammen in einen Atlas</span><span class="sxs-lookup"><span data-stu-id="15adb-128">Packing Charts Into an Atlas</span></span>](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a><span data-ttu-id="15adb-129">Partitionieren und Parametrisieren eines Gitternetzes</span><span class="sxs-lookup"><span data-stu-id="15adb-129">Partitioning and Parameterizing a Mesh</span></span>

<span data-ttu-id="15adb-130">Zuerst wird das Gitternetz in Diagramme partitioniert, dann wird jedes Diagramm in einen eigenen \[ 0,1 \] UV-Raum parametrisiert.</span><span class="sxs-lookup"><span data-stu-id="15adb-130">First, the mesh is partitioned into charts, then each chart is parameterized into its own \[0,1\] UV-space.</span></span> <span data-ttu-id="15adb-131">Ein Zylinder kann durch ein Diagramm parametrisiert werden. Eine Kugel hingegen erfordert zwei Diagramme, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="15adb-131">A cylinder can be parameterized by one chart; a sphere on the other hand will require two charts, as shown in the following illustration.</span></span>

![Abbildung einer In zwei Diagramme partitionierten Kugel](images/uvatlas3.jpg)

<span data-ttu-id="15adb-133">Ein Gitternetz, das mit einem einzelnen Diagramm parametrisiert werden kann, wird als "homeomorph zu einem Datenträger" klassifiziert. Das bedeutet, dass Sie einen unendlich flexiblen, unendlich stretchbaren Datenträger über das Diagramm verteilen und die Geometrie perfekt abdecken können.</span><span class="sxs-lookup"><span data-stu-id="15adb-133">A mesh which can be parameterized with a single chart is classified as "homeomorphic to a disk", meaning you could spread out an infinitely flexible, infinitely stretchable disk over the chart and cover the geometry perfectly.</span></span> <span data-ttu-id="15adb-134">Diese Stretchingfunktion, die als Homeomorphie bezeichnet wird, ist eine bidirektionale Funktion. Das bedeutet, dass Sie von einer Parametrisierung zur anderen wechseln können, ohne Informationen zu verlieren.</span><span class="sxs-lookup"><span data-stu-id="15adb-134">This stretching, called a homeomorphism, is a bidirectional function; which means you can go from one parameterization to the other without losing information.</span></span>

<span data-ttu-id="15adb-135">Sehr wenige reale Gitternetze können in zwei Dimensionen parametrisiert werden, ohne das Gitternetz in Cluster oder Diagramme zu unterteilen.</span><span class="sxs-lookup"><span data-stu-id="15adb-135">Very few real-world meshes can be parameterized into two dimensions without separating the mesh into clusters, or charts.</span></span> <span data-ttu-id="15adb-136">Die folgende Abbildung zeigt ein weiteres Beispielgitternetz und den entsprechenden Texturat atlas.</span><span class="sxs-lookup"><span data-stu-id="15adb-136">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Zeigt ein Beispielgitternetz mit unterschiedlichen Formen und dem entsprechenden Texturat atlas.](images/uvatlas2.jpg)

<span data-ttu-id="15adb-138">Es gibt zwei Parameter, die die Anzahl der erstellten Diagramme bestimmen:</span><span class="sxs-lookup"><span data-stu-id="15adb-138">There are two parameters that determine the number of charts created:</span></span>

-   <span data-ttu-id="15adb-139">Die maximale Anzahl von Diagrammen, die für den Atlas zulässig sind</span><span class="sxs-lookup"><span data-stu-id="15adb-139">The maximum number of charts allowed for the atlas</span></span>
-   <span data-ttu-id="15adb-140">Die maximal zulässige Stretchingmenge für jedes Diagramm.</span><span class="sxs-lookup"><span data-stu-id="15adb-140">The maximum amount of stretch allowed for each chart</span></span>

<span data-ttu-id="15adb-141">Die Stretchingmenge bestimmt die Anzahl der generierten Diagramme und die Gesamtqualität der Stichprobenentnahme.</span><span class="sxs-lookup"><span data-stu-id="15adb-141">The amount of stretch will determine the number of charts that are generated, and the overall quality of the sampling.</span></span> <span data-ttu-id="15adb-142">Die Stretchingspanne reicht von 0,0 (ohne Stretching) bis 1,0 (beliebiger Stretchingwert).</span><span class="sxs-lookup"><span data-stu-id="15adb-142">Stretch ranges from 0.0 (no stretch) to 1.0 (any amount of stretch).</span></span> <span data-ttu-id="15adb-143">D3DXUVAtlasCreate und D3DXUVAtlasPartition geben die maximale Stretchingdauer zurück, die vom Algorithmus generiert wird.</span><span class="sxs-lookup"><span data-stu-id="15adb-143">D3DXUVAtlasCreate and D3DXUVAtlasPartition return the maximum stretch generated by the algorithm.</span></span> <span data-ttu-id="15adb-144">Die folgende Abbildung zeigt ein weiteres Beispielgitternetz und den entsprechenden Texturat atlas.</span><span class="sxs-lookup"><span data-stu-id="15adb-144">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Abbildung eines Beispielgitters und des entsprechenden Texturat atlas](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a><span data-ttu-id="15adb-146">Verwenden integrierter Metrik tensors zum Steuern der Parametrisierung</span><span class="sxs-lookup"><span data-stu-id="15adb-146">Using Integrated Metric Tensors to Control Parameterization</span></span>

<span data-ttu-id="15adb-147">Die Priorisierung des Texturraums kann auf Dreiecksbasis angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="15adb-147">Texture-space prioritization can be specified on a per-triangle basis.</span></span> <span data-ttu-id="15adb-148">Integrierte Metriktensoren können bereitgestellt werden, um zu steuern, wie Dreiecke im resultierenden Texturraumat atlas gestreckt werden.</span><span class="sxs-lookup"><span data-stu-id="15adb-148">Integrated Metric Tensors can be provided to control how triangles are stretched in the resulting texture-space atlas.</span></span> <span data-ttu-id="15adb-149">IMT-Dateien können mithilfe der D3DX IMT-Berechnungsfunktionen direkt angegeben oder basierend auf einem Eingabesignal berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="15adb-149">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions.</span></span> <span data-ttu-id="15adb-150">Ein integrierter Metrik tensor (oder IMT) ist eine symmetrische 2x2-Matrix, die beschreibt, wie ein Dreieck im Atlas gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="15adb-150">An integrated metric tensor (or IMT) is a symmetrical 2x2 matrix that describes how a triangle is stretched in the atlas.</span></span> <span data-ttu-id="15adb-151">Jedes IMT wird durch drei Gleitkommazeichen definiert, die sie aufrufen (a,b,c).</span><span class="sxs-lookup"><span data-stu-id="15adb-151">Each IMT is defined by 3 floats, call them (a,b,c).</span></span> <span data-ttu-id="15adb-152">Sie können in einer symmetrischen 2x2-Matrix wie folgt angeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="15adb-152">They can be arranged in a symmetric 2x2 matrix like this:</span></span>


```
a b
b c
```



<span data-ttu-id="15adb-153">Anschließend kann das IMT verwendet werden, um den Abstand zwischen zwei Vektoren zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="15adb-153">Then the IMT can be used to find the distance between two vectors.</span></span> <span data-ttu-id="15adb-154">Gibt die beiden Vektoren v1 und v2 an, wobei :</span><span class="sxs-lookup"><span data-stu-id="15adb-154">Given two vectors v1 and v2, where :</span></span>


```
vector v1
vector v2 = v1 + (s,t)
```



<span data-ttu-id="15adb-155">Der Abstand zwischen v1 und v2 kann wie folgt berechnet werden:</span><span class="sxs-lookup"><span data-stu-id="15adb-155">The distance between v1 and v2 can be calculated as:</span></span>


```
sqrt((s, t) * M * (s, t)^T)
```



<span data-ttu-id="15adb-156">Anders ausgedrückt: Der Vektor (s,t) könnte die Größe der Stretchung in beliebiger Richtung im u-v-Raum sein.</span><span class="sxs-lookup"><span data-stu-id="15adb-156">In other words, the vector (s,t) could be the magnitude of the stretch in an arbitrary direction in u-v space.</span></span> <span data-ttu-id="15adb-157">In diesem Fall ist der s-Vektor eine Richtung vom ersten zum zweiten Scheitelpunkt, und t ist das Kreuzprodukt von normal und s.</span><span class="sxs-lookup"><span data-stu-id="15adb-157">In this case, the s vector is a direction from the first to the second vertex, and t is the cross product of the normal and s.</span></span> <span data-ttu-id="15adb-158">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="15adb-158">For instance:</span></span>


```
(1,1) * (1,1) = (2,2)
        (1,1)
IMT(1,1,1) scales by 2
```




```
(1,-1) * (1,1) = (0,0)
         (1,1)
IMT(2,0,2) scales by 2 with no shearing
```



<span data-ttu-id="15adb-159">IMT-Dateien können direkt oder basierend auf einem Eingabesignal mithilfe der D3DX IMT-Berechnungsfunktionen angegeben oder berechnet werden: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal und D3DXComputeIMTFromTexture. \_</span><span class="sxs-lookup"><span data-stu-id="15adb-159">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal, and D3DXComputeIMTFromTexture\_graphics.</span></span>

<span data-ttu-id="15adb-160">Geben Sie IMT-Daten direkt an, wenn Sie steuern möchten, wie Texturraum einzelnen Dreiecken zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="15adb-160">Specify IMT data directly if you want to control how texture-space is allocated to individual triangles.</span></span> <span data-ttu-id="15adb-161">Ordnen Sie auf diese Weise wichtigen Bereichen eines Gitternetzes (z. B. dem Gesicht oder dem Logo eines Zeichens oder Bereichen einer Szene in der Nähe des Fußpfads eines Spielers) mehr Bereiche im Atlas zu.</span><span class="sxs-lookup"><span data-stu-id="15adb-161">By doing so, allocate more area in the atlas to important areas of a mesh (such as a character's face or chest logo, or regions of a scene near a player's walking-path).</span></span> <span data-ttu-id="15adb-162">Durch Angeben von IMT-Dateien, bei denen es sich um Vielfache der Identitätsmatrix handelt, werden die resultierenden Dreiecke gleichmäßig im Texturraum skaliert.</span><span class="sxs-lookup"><span data-stu-id="15adb-162">By specifying IMT's that are multiples of the identity matrix, the resulting triangles will be scaled uniformly in texture space.</span></span>

<span data-ttu-id="15adb-163">Beispielsweise können Sie bei einer normalen Karte mit hoher Auflösung IMT berechnen, um mehr Texturraum für Bereiche mit höherer Frequenz in der normalen Karte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="15adb-163">For example, given a high-resolution normal map, you can compute IMT to provide more texture-space to areas of higher frequency signal in the normal map.</span></span> <span data-ttu-id="15adb-164">Dreiecke, die "flach" sind (die konstanten Bereichen der ursprünglichen normalen Karte zugeordnet sind), erhalten weniger Texturraum.</span><span class="sxs-lookup"><span data-stu-id="15adb-164">Triangles that are "flat" (that mapped to constant regions of the original normal map) will receive less texture space.</span></span> <span data-ttu-id="15adb-165">Dreiecke, die viele normale Kartendetails enthalten, erhalten mehr Texturbereich im Endergebnis.</span><span class="sxs-lookup"><span data-stu-id="15adb-165">Triangles that contain a great deal of normal-map detail will receive more texture area in the final result.</span></span> <span data-ttu-id="15adb-166">Sie können dann die normale Karte in einer kleineren Textur neu zusammensetzen, aber Details beibehalten, oder Sie können die normale Karte mit der optimaleren UV-Zuordnung neu zusammensetzen.</span><span class="sxs-lookup"><span data-stu-id="15adb-166">You can then resample the normal map into a smaller texture but maintain detail, or you can recompute the normal map with the more optimal UV mapping.</span></span>

### <a name="using-adjacency-data-for-user-specified-creases"></a><span data-ttu-id="15adb-167">Verwenden von Adjazenzdaten für vom Benutzer angegebene Errungen</span><span class="sxs-lookup"><span data-stu-id="15adb-167">Using Adjacency Data for User Specified Creases</span></span>

<span data-ttu-id="15adb-168">Benutzerdefinierte Adjazenzinformationen können der Partitionierungsfunktion bereitgestellt werden, um vordefinierte Erstellungen im Gitternetz zu beschreiben und so eine Diagrammgrenze zwischen angrenzenden Gesichtern zu definieren.</span><span class="sxs-lookup"><span data-stu-id="15adb-168">User-defined adjacency information can be provided to the partitioning function to describe pre-defined creases in the mesh, and thus define a chart boundary between adjacent faces.</span></span> <span data-ttu-id="15adb-169">Dies ist eine einfache Möglichkeit für den Aufrufer, seine eigene Diagrammpartitionierung als Eingabe in den Algorithmus anzugeben. Dadurch werden Diagramme weiter verfeinern, um die Stretchung unter das maximal zulässige Maximum zu bringen.</span><span class="sxs-lookup"><span data-stu-id="15adb-169">This is a simple way for the caller to specify their own chart partitioning as input into the algorithm, which will further refine charts to bring the stretch under the maximum allowed.</span></span>

### <a name="example"></a><span data-ttu-id="15adb-170">Beispiel</span><span class="sxs-lookup"><span data-stu-id="15adb-170">Example</span></span>

<span data-ttu-id="15adb-171">In diesem Beispiel wird veranschaulicht, wie Sie die UVAtlas-APIs und den DirectX-Viewer (Dxviewer.exe) verwenden können, um Diskontinuitäten in Ihrem Modell zu finden und zu beheben, die sich erheblich auf die Größe Ihres Texturat atlas auswirken können.</span><span class="sxs-lookup"><span data-stu-id="15adb-171">This example illustrates how you might use the UVAtlas APIs and the DirectX Viewer (Dxviewer.exe) to find and fix discontinuities in your model that can dramatically affect the size of your texture atlas.</span></span> <span data-ttu-id="15adb-172">Sie können Dxviewer.exe abrufen und sich über das DirectX SDK darüber informieren.</span><span class="sxs-lookup"><span data-stu-id="15adb-172">You can get Dxviewer.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="15adb-173">Dxviewer.exe wurde nach der Version vom August 2009 aus dem DirectX SDK entfernt, sodass Sie mindestens das DirectX SDK vom August 2009 benötigen, um es zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="15adb-173">Dxviewer.exe was removed from the DirectX SDK after the August 2009 version so to get it you'll need at least the August 2009 DirectX SDK.</span></span> <span data-ttu-id="15adb-174">Informationen zum DirectX SDK finden Sie unter [Wo befindet sich das DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="15adb-174">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="15adb-175">Angenommen, Sie haben mit einem Modell in Ihrer bevorzugten Software zum Generieren von Inhalten begonnen (in diesem Beispiel wird ein in Maya erstelltes Head-Modell verwendet).</span><span class="sxs-lookup"><span data-stu-id="15adb-175">Assume you started with some model in your favorite content generation software (this example uses a dwarf head model that was created in Maya).</span></span> <span data-ttu-id="15adb-176">Exportieren Sie das texturierte Modell in eine X-Datei, und erstellen Sie mit D3DXUVAtlasCreate einen Texturat atlas.</span><span class="sxs-lookup"><span data-stu-id="15adb-176">Export the textured model to an .x file and create a texture atlas with D3DXUVAtlasCreate.</span></span> <span data-ttu-id="15adb-177">Der resultierende Texturat atlas würde in etwa wie in der folgenden Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="15adb-177">The resulting texture atlas would look something like the following illustration.</span></span>

![Abbildung eines Atlas für ein Modell](images/uvatlas5.jpg)

<span data-ttu-id="15adb-179">Der Atlas verfügt über 22 Diagramme und eine maximale Streckung von 0,994.</span><span class="sxs-lookup"><span data-stu-id="15adb-179">The atlas has 22 charts and a maximum stretch of 0.994.</span></span>

<span data-ttu-id="15adb-180">Sehen Sie sich nun das texturierte Modell an, um zu sehen, wie gut der Texturat atlas der Geometrie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="15adb-180">Now look at the textured model to see how well the texture atlas maps to the geometry.</span></span> <span data-ttu-id="15adb-181">Laden Sie dazu das Modell in das Viewer-Tool:</span><span class="sxs-lookup"><span data-stu-id="15adb-181">To do this, load the model into the viewer tool:</span></span>

-   <span data-ttu-id="15adb-182">Öffnen Sie das Viewer-Tool über die DirectX-Hilfsprogramme.</span><span class="sxs-lookup"><span data-stu-id="15adb-182">Open the viewer tool from the DirectX Utilities.</span></span>
-   <span data-ttu-id="15adb-183">Laden Sie die X-Datei, indem Sie auf die Schaltfläche Öffnen klicken.</span><span class="sxs-lookup"><span data-stu-id="15adb-183">Load the .x file by clicking the Open button.</span></span>
-   <span data-ttu-id="15adb-184">Aktivieren Sie die Anzeigeoption "Erstellen", indem Sie auf die Schaltfläche "Ansicht" klicken und im Popupfenster "Creases" auswählen.</span><span class="sxs-lookup"><span data-stu-id="15adb-184">Enabling the crease viewing option by clicking the view button and selecting Creases from popup.</span></span>

<span data-ttu-id="15adb-185">Die folgende Abbildung zeigt, was im Viewer-Tool angezeigt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="15adb-185">The following illustration shows what you should see in the viewer tool.</span></span>

![Abbildung eines texturierten Gitters im Viewer-Tool](images/uvatlas6c.jpg)

<span data-ttu-id="15adb-187">Jede Linie ist eine Faltung, die einen angrenzenden Rand zwischen zwei Diagrammen im Texturat atlas darstellt.</span><span class="sxs-lookup"><span data-stu-id="15adb-187">Each line is a crease which is an adjacent edge between two charts in the texture atlas.</span></span> <span data-ttu-id="15adb-188">Die Anzahl der vom Algorithmus generierten Diagramme wird durch geringfügige Unterschiede verursacht, die möglicherweise auf Diskontinuitäten in den Normalitäten zurückzuführen sind.</span><span class="sxs-lookup"><span data-stu-id="15adb-188">The number of charts generated by the algorithm is caused by slight differences perhaps due to discontinuities in the normals.</span></span> <span data-ttu-id="15adb-189">Diese kleinen Unterschiede können durch Verarbeitungsdaten reduziert werden, d. h. das Erzwingen von Daten, die fast gleich sind.</span><span class="sxs-lookup"><span data-stu-id="15adb-189">These small differences can be reduced by welding data, that is, forcing data that is nearly equal to be equal.</span></span> <span data-ttu-id="15adb-190">So bestärken Sie die Normalitäten und Die Skinweights:</span><span class="sxs-lookup"><span data-stu-id="15adb-190">To weld the normals and the skinweights:</span></span>

-   <span data-ttu-id="15adb-191">Führen Sie das DirectX Ops-Tool (dxops.exe) mit der folgenden Befehlszeile im Netz aus (ersetzen Sie dabei "modelName.x" durch den Namen Ihres Modells):</span><span class="sxs-lookup"><span data-stu-id="15adb-191">Run the DirectX Ops (dxops.exe) tool with the following command line on the mesh (replacing 'modelName.x' with the name of your model):</span></span>
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

<span data-ttu-id="15adb-192">Dies vergleicht die Normalwerte und Skinweights, und wenn sie sich im Wert um weniger als 2,01 unterscheiden, werden die Daten gleich gemacht.</span><span class="sxs-lookup"><span data-stu-id="15adb-192">This compares the normals and skinweights, and where they differ in value by less than 2.01, the data is made equal.</span></span> <span data-ttu-id="15adb-193">Die folgenden Abbildungen zeigen eine Nahaufnahme des Auges, um die Erbildungen vor dem Strahl (auf der linken Seite) und die Erbildungen nach der Brille (auf der rechten Seite) zu sehen:</span><span class="sxs-lookup"><span data-stu-id="15adb-193">The following illustrations shows a close up of the eye to see the creases before welding (on the left) and the creases after welding (on the right):</span></span>

![Abbildung von Erbildungen vor dem Abschluss](images/uvatlas6a.jpg)![Abbildung der Erbildungen nach dem Abschluss](images/uvatlas6b.jpg)

<span data-ttu-id="15adb-196">Abbildung 7: Entfernen von Errungen nach 160000000000000000000000</span><span class="sxs-lookup"><span data-stu-id="15adb-196">Figure 7: Removing creases by welding</span></span>

<span data-ttu-id="15adb-197">In diesem Beispiel wurden 86 Scheitelpunkte aus dem Eingabegitter entfernt.</span><span class="sxs-lookup"><span data-stu-id="15adb-197">In this example, welding removed 86 vertices from the input mesh.</span></span> <span data-ttu-id="15adb-198">Mit weniger Errungen im Gitternetz können Sie den Atlas neu generieren, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="15adb-198">With fewer creases in the mesh, you can regenerate the atlas, as the following illustration shows.</span></span>

![Abbildung des neuen Atlas mit entfernten Erbildungen](images/uvatlas8.jpg)

<span data-ttu-id="15adb-200">Der Atlas verfügt nur über 7 Diagramme und eine maximale Streckung von ca. 0,0776.</span><span class="sxs-lookup"><span data-stu-id="15adb-200">The atlas only has 7 charts and a maximum stretch of approximately 0.0776.</span></span> <span data-ttu-id="15adb-201">Der neue Atlas passt jetzt in eine kleinere Textur (in diesem Beispiel etwa 30 % kleiner).</span><span class="sxs-lookup"><span data-stu-id="15adb-201">The new atlas now fits into a smaller texture (approximately 30% smaller in this example).</span></span>

### <a name="packing-charts-into-an-atlas"></a><span data-ttu-id="15adb-202">Packen von Diagrammen in einen Atlas</span><span class="sxs-lookup"><span data-stu-id="15adb-202">Packing Charts Into an Atlas</span></span>

<span data-ttu-id="15adb-203">Nachdem ein Gitternetz in einzeln parametrisierte Diagramme partitioniert wurde, müssen die Diagramme effizient in eine einzelne Texturkarte gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="15adb-203">Once a mesh has been partitioned into individually-parameterized charts, the charts need to be packed efficiently into a single texture map.</span></span> <span data-ttu-id="15adb-204">Dies wird als zweiter Schritt von D3DXUVAtlasCreate ausgeführt oder kann explizit durch Aufrufen von D3DXUVAtlasPack aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="15adb-204">This is performed as the second step of D3DXUVAtlasCreate or can be invoked explicitly by calling D3DXUVAtlasPack.</span></span>

<span data-ttu-id="15adb-205">Gepackte Diagramme werden durch eine benutzerdefinierte Bundstegbreite getrennt.</span><span class="sxs-lookup"><span data-stu-id="15adb-205">Packed charts are separated by a user-specified gutter width.</span></span> <span data-ttu-id="15adb-206">Die Gutterbreite entspricht der Trennung zwischen Diagrammen und ermöglicht bilineare Interpolation und Mip-Zuordnung, um das Rendern von Artefakten an Diagrammgrenzen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="15adb-206">The gutter width is the amount of separation between charts, and allows for bilinear interpolation and mip-mapping to avoid rendering artifacts at chart boundaries.</span></span> <span data-ttu-id="15adb-207">D3DX stellt eine Schnittstelle zum automatischen Ausfüllen dieser Gutter bereit. Weitere Informationen finden Sie unter [**ID3DXTextureGutterHelper.**](id3dxtexturegutterhelper.md)</span><span class="sxs-lookup"><span data-stu-id="15adb-207">D3DX provides an interface for automatically filling in these gutters - see [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) for more information.</span></span>

## <a name="integrating-uvatlas-into-your-pipeline"></a><span data-ttu-id="15adb-208">Integrieren von UVAtlas in Ihre Pipeline</span><span class="sxs-lookup"><span data-stu-id="15adb-208">Integrating UVAtlas Into Your Pipeline</span></span>

<span data-ttu-id="15adb-209">Diese Funktionen können nicht nur vor dem Zeichnen von Texturen als Interpreten aufgerufen werden, sie können auch in eine automatisierte Grafikpipeline integriert werden.</span><span class="sxs-lookup"><span data-stu-id="15adb-209">In addition to being artist-invoked prior to texture painting, these functions can be integrated into an automated art pipeline.</span></span> <span data-ttu-id="15adb-210">Beispielsweise kann ein UVAtlas-Aufruf automatisch ausgegeben werden, nachdem ein Medienobjekt aktualisiert wurde, bevor eine PRT-Simulation oder ein normaler Zuordnungsdurchlauf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15adb-210">For example, a UVAtlas call can be issued automatically after an asset is updated, prior to performing a PRT simulation or normal mapping pass.</span></span> <span data-ttu-id="15adb-211">Dadurch wird vermieden, dass die UV-Zuordnung eines Objekts manuell repariert werden muss, wenn die Topologie des Gittermodells geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="15adb-211">This avoids any need to manually manual repair of an object's UV mapping if the mesh's topology has been modified.</span></span>

<span data-ttu-id="15adb-212">Informationen zur Verwendung der UVAtlas-Funktionen finden Sie im UV [Atlas Command-Line Tool (uvatlas.exe).](https://github.com/Microsoft/UVAtlas)</span><span class="sxs-lookup"><span data-stu-id="15adb-212">See the [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) for example usage of the UVAtlas functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15adb-213">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15adb-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15adb-214">Weiterführende Themen</span><span class="sxs-lookup"><span data-stu-id="15adb-214">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
