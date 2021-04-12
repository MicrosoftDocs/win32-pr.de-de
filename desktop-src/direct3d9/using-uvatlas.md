---
description: Viele Renderingverfahren und Inhalts Generierungs Techniken erfordern eine eindeutige, nicht überlappende Zuordnung eines 2D-Signals (z. b. eine Textur) zu einem Mesh.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Verwenden von uvatlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b335dd6ea94a3db0c0760b0d07a0b8df3fe4c7c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104218903"
---
# <a name="using-uvatlas-direct3d-9"></a><span data-ttu-id="44525-103">Verwenden von uvatlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="44525-103">Using UVAtlas (Direct3D 9)</span></span>

<span data-ttu-id="44525-104">Viele Renderingverfahren und Inhalts Generierungs Techniken erfordern eine eindeutige, nicht überlappende Zuordnung eines 2D-Signals (z. b. eine Textur) zu einem Mesh.</span><span class="sxs-lookup"><span data-stu-id="44525-104">Many rendering and content generation techniques require a unique, non-overlapping map of a 2D signal (such as a texture) onto a mesh.</span></span> <span data-ttu-id="44525-105">Diese Techniken umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="44525-105">Such techniques include:</span></span>

-   <span data-ttu-id="44525-106">Normale/Verschiebungs Zuordnung</span><span class="sxs-lookup"><span data-stu-id="44525-106">Normal/displacement mapping</span></span>
-   <span data-ttu-id="44525-107">Simulationen für Textur Raum-PRT und helle Karten</span><span class="sxs-lookup"><span data-stu-id="44525-107">Texture-space PRT simulations and light maps</span></span>
-   <span data-ttu-id="44525-108">Oberflächendarstellung</span><span class="sxs-lookup"><span data-stu-id="44525-108">Surface painting</span></span>
-   <span data-ttu-id="44525-109">Textur Raumbeleuchtung</span><span class="sxs-lookup"><span data-stu-id="44525-109">Texture-space lighting</span></span>

<span data-ttu-id="44525-110">Das manuelle Erstellen einer eindeutigen UV-Zuordnung ist oft zeitaufwändig und mühsam. Dies trifft vor allem dann zu, wenn die Eingabe Geometrie Komplex ist und eine effiziente/niedrige Verzerrung der Textur Raumauslastung gewünscht wird.</span><span class="sxs-lookup"><span data-stu-id="44525-110">Generating a unique UV mapping manually is often time-consuming and tedious; this is especially true when the input geometry is complex and efficient/low-distortion texture-space utilization is desired.</span></span> <span data-ttu-id="44525-111">Die folgende Abbildung zeigt ein Beispiel Netz und den zugehörigen Textur Atlas.</span><span class="sxs-lookup"><span data-stu-id="44525-111">The following illustration shows an example mesh and its corresponding texture atlas.</span></span>

![Zeigt ein Beispiel Netz und den zugehörigen Textur Atlas an.](images/uvatlas1.jpg)

<span data-ttu-id="44525-113">Dieses Beispiel zeigt ein Mesh (auf der linken Seite) und die entsprechende UV-Leerraum-normale Karte (auf der rechten Seite).</span><span class="sxs-lookup"><span data-stu-id="44525-113">This example shows a mesh (on the left) and the corresponding UV-space normal map (on the right).</span></span> <span data-ttu-id="44525-114">Beachten Sie, dass der Textur Atlas mehrere Gruppen oder Cluster von Daten enthält. Jeder Cluster wird als Diagramm bezeichnet, und im obigen Beispiel enthält die Anzeige die normalen Daten für einen Teil des Netzes.</span><span class="sxs-lookup"><span data-stu-id="44525-114">Notice that the texture atlas contains several groups or clusters of data; each cluster is called a chart and in the example above, displays contains the normal data for a portion of the mesh.</span></span>

<span data-ttu-id="44525-115">Die D3DX uvatlas-APIs generieren automatisch einen optimalen, nicht überlappenden Textur Atlas.</span><span class="sxs-lookup"><span data-stu-id="44525-115">The D3DX UVAtlas APIs automatically generate an optimal, non-overlapping texture atlas.</span></span> <span data-ttu-id="44525-116">Die APIs bieten Eingabeparameter, die Folgendes ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="44525-116">The APIs provide input parameters that allow you to:</span></span>

-   <span data-ttu-id="44525-117">Minimieren Sie Textur Streckung, Verzerrung und Unterstichprobe.</span><span class="sxs-lookup"><span data-stu-id="44525-117">Minimize texture stretch, distortion, and undersampling.</span></span>
-   <span data-ttu-id="44525-118">Maximieren Sie die Dichte der Textur Raum Komprimierung für die effiziente Arbeitsspeicher Nutzung.</span><span class="sxs-lookup"><span data-stu-id="44525-118">Maximize texture-space packing density for efficient use of memory.</span></span>
-   <span data-ttu-id="44525-119">Stellen Sie eine gleichmäßige Stichprobenentnahme im Mesh bereit, wodurch Diskontinuitäten bei der Stichproben Häufigkeit minimiert werden</span><span class="sxs-lookup"><span data-stu-id="44525-119">Provide an even sampling across the mesh, minimizing discontinuities in sampling frequency.</span></span>

## <a name="how-uvatlas-works"></a><span data-ttu-id="44525-120">Funktionsweise von uvatlas</span><span class="sxs-lookup"><span data-stu-id="44525-120">How UVAtlas Works</span></span>

<span data-ttu-id="44525-121">Die uvatlas-APIs (siehe [uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generieren einen Textur Atlas, indem eine Oberfläche in Diagramme partitioniert und die Diagramme in einen Textur Atlas verpackt werden.</span><span class="sxs-lookup"><span data-stu-id="44525-121">The UVAtlas APIs (see [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generate a texture atlas by partitioning a surface into charts and packing the charts into a texture atlas.</span></span> <span data-ttu-id="44525-122">Verwenden Sie [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) und [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) , um diese Schritte separat auszuführen. oder verwenden Sie [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) , um einen einzelnen-Befehl zu partitionieren, zu parametrisieren und zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="44525-122">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) and [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) to perform these steps separately; or use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) to partition, parameterize and pack in a single call.</span></span>

-   [<span data-ttu-id="44525-123">Partitionieren und parametrialisieren eines Netzes</span><span class="sxs-lookup"><span data-stu-id="44525-123">Partitioning and Parameterizing a Mesh</span></span>](#partitioning-and-parameterizing-a-mesh)
-   [<span data-ttu-id="44525-124">Verwenden integrierter metriktensoren zum Steuern der Parametrisierung</span><span class="sxs-lookup"><span data-stu-id="44525-124">Using Integrated Metric Tensors to Control Parameterization</span></span>](#using-integrated-metric-tensors-to-control-parameterization)
-   [<span data-ttu-id="44525-125">Verwenden von Daten für benutzerdefinierte Aliasnamen</span><span class="sxs-lookup"><span data-stu-id="44525-125">Using Adjacency Data for User Specified Creases</span></span>](#using-adjacency-data-for-user-specified-creases)
-   [<span data-ttu-id="44525-126">Packen von Diagrammen in einen Atlas</span><span class="sxs-lookup"><span data-stu-id="44525-126">Packing Charts Into an Atlas</span></span>](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a><span data-ttu-id="44525-127">Partitionieren und parametrialisieren eines Netzes</span><span class="sxs-lookup"><span data-stu-id="44525-127">Partitioning and Parameterizing a Mesh</span></span>

<span data-ttu-id="44525-128">Zuerst wird das Mesh in Diagramme partitioniert, dann wird jedes Diagramm in seinen eigenen \[ , 0, 1- \] UV-Bereich parametrisiert.</span><span class="sxs-lookup"><span data-stu-id="44525-128">First, the mesh is partitioned into charts, then each chart is parameterized into its own \[0,1\] UV-space.</span></span> <span data-ttu-id="44525-129">Ein Zylinder kann mit einem Diagramm parametrisiert werden. eine Kugel auf der anderen Seite erfordert zwei Diagramme, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="44525-129">A cylinder can be parameterized by one chart; a sphere on the other hand will require two charts, as shown in the following illustration.</span></span>

![Abbildung einer in zwei Diagrammen partitionierten Kugel](images/uvatlas3.jpg)

<span data-ttu-id="44525-131">Ein Mesh, das mit einem einzelnen Diagramm parametrisiert werden kann, wird als "homeomorph to a Disk" klassifiziert, d. h., Sie könnten einen unendlich flexiblen, unendlich streiebaren Datenträger über das Diagramm verteilen und die Geometrie perfekt abdecken.</span><span class="sxs-lookup"><span data-stu-id="44525-131">A mesh which can be parameterized with a single chart is classified as "homeomorphic to a disk", meaning you could spread out an infinitely flexible, infinitely stretchable disk over the chart and cover the geometry perfectly.</span></span> <span data-ttu-id="44525-132">Diese Streckung, die als homeomorphism bezeichnet wird, ist eine bidirektionale Funktion. Dies bedeutet, dass Sie von einer Parametrisierung zum anderen wechseln können, ohne dass Informationen verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="44525-132">This stretching, called a homeomorphism, is a bidirectional function; which means you can go from one parameterization to the other without losing information.</span></span>

<span data-ttu-id="44525-133">Sehr wenige reale Netze können in zwei Dimensionen parametrisiert werden, ohne das Mesh in Cluster oder Diagramme zu unterteilen.</span><span class="sxs-lookup"><span data-stu-id="44525-133">Very few real-world meshes can be parameterized into two dimensions without separating the mesh into clusters, or charts.</span></span> <span data-ttu-id="44525-134">Die folgende Abbildung zeigt ein weiteres Beispiel Mesh und den zugehörigen Textur Atlas.</span><span class="sxs-lookup"><span data-stu-id="44525-134">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Zeigt ein Beispiel Netz mit unterschiedlichen Formen und dem zugehörigen Textur Atlas.](images/uvatlas2.jpg)

<span data-ttu-id="44525-136">Es gibt zwei Parameter, die die Anzahl der erstellten Diagramme bestimmen:</span><span class="sxs-lookup"><span data-stu-id="44525-136">There are two parameters that determine the number of charts created:</span></span>

-   <span data-ttu-id="44525-137">Die maximale Anzahl von Diagrammen, die für den Atlas zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="44525-137">The maximum number of charts allowed for the atlas</span></span>
-   <span data-ttu-id="44525-138">Die maximal zulässige Streckung für jedes Diagramm.</span><span class="sxs-lookup"><span data-stu-id="44525-138">The maximum amount of stretch allowed for each chart</span></span>

<span data-ttu-id="44525-139">Der Umfang der Streckung bestimmt die Anzahl der generierten Diagramme und die Gesamtqualität der Stichprobenentnahme.</span><span class="sxs-lookup"><span data-stu-id="44525-139">The amount of stretch will determine the number of charts that are generated, and the overall quality of the sampling.</span></span> <span data-ttu-id="44525-140">Stretch reicht von 0,0 (keine Streckung) bis 1,0 (beliebige Streckung).</span><span class="sxs-lookup"><span data-stu-id="44525-140">Stretch ranges from 0.0 (no stretch) to 1.0 (any amount of stretch).</span></span> <span data-ttu-id="44525-141">D3DXUVAtlasCreate und D3DXUVAtlasPartition geben die maximale Streckung zurück, die vom Algorithmus generiert wird.</span><span class="sxs-lookup"><span data-stu-id="44525-141">D3DXUVAtlasCreate and D3DXUVAtlasPartition return the maximum stretch generated by the algorithm.</span></span> <span data-ttu-id="44525-142">Die folgende Abbildung zeigt ein weiteres Beispiel Mesh und den zugehörigen Textur Atlas.</span><span class="sxs-lookup"><span data-stu-id="44525-142">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Abbildung eines Beispiel Netzes und des zugehörigen Textur Atlas](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a><span data-ttu-id="44525-144">Verwenden integrierter metriktensoren zum Steuern der Parametrisierung</span><span class="sxs-lookup"><span data-stu-id="44525-144">Using Integrated Metric Tensors to Control Parameterization</span></span>

<span data-ttu-id="44525-145">Die Priorisierung von Textur Raum kann pro Dreieck angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="44525-145">Texture-space prioritization can be specified on a per-triangle basis.</span></span> <span data-ttu-id="44525-146">Integrierte metriktensoren können bereitgestellt werden, um zu steuern, wie Dreiecke im resultierenden Textur Raum-Atlas gestreckt werden.</span><span class="sxs-lookup"><span data-stu-id="44525-146">Integrated Metric Tensors can be provided to control how triangles are stretched in the resulting texture-space atlas.</span></span> <span data-ttu-id="44525-147">IMT kann mithilfe der D3DX IMT-Berechnungsfunktionen direkt oder basierend auf einem Eingabe Signal angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="44525-147">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions.</span></span> <span data-ttu-id="44525-148">Ein integrierter metriktensor (oder IMT) ist eine symmetrische 2 x 2-Matrix, die beschreibt, wie ein Dreieck im Atlas gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="44525-148">An integrated metric tensor (or IMT) is a symmetrical 2x2 matrix that describes how a triangle is stretched in the atlas.</span></span> <span data-ttu-id="44525-149">Jedes IMT wird durch drei Gleit Komma Werte definiert und ruft Sie auf (a, b, c).</span><span class="sxs-lookup"><span data-stu-id="44525-149">Each IMT is defined by 3 floats, call them (a,b,c).</span></span> <span data-ttu-id="44525-150">Sie können wie folgt in einer symmetrischen 2 x 2-Matrix angeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="44525-150">They can be arranged in a symmetric 2x2 matrix like this:</span></span>


```
a b
b c
```



<span data-ttu-id="44525-151">Anschließend kann der IMT verwendet werden, um den Abstand zwischen zwei Vektoren zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="44525-151">Then the IMT can be used to find the distance between two vectors.</span></span> <span data-ttu-id="44525-152">Zwei Vektoren v1 und v2, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="44525-152">Given two vectors v1 and v2, where :</span></span>


```
vector v1
vector v2 = v1 + (s,t)
```



<span data-ttu-id="44525-153">Der Abstand zwischen V1 und v2 kann wie folgt berechnet werden:</span><span class="sxs-lookup"><span data-stu-id="44525-153">The distance between v1 and v2 can be calculated as:</span></span>


```
sqrt((s, t) * M * (s, t)^T)
```



<span data-ttu-id="44525-154">Dies bedeutet, dass der Vektor (s, t) die Größe der Streckung in beliebiger Richtung in u-v-Raum aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="44525-154">In other words, the vector (s,t) could be the magnitude of the stretch in an arbitrary direction in u-v space.</span></span> <span data-ttu-id="44525-155">In diesem Fall ist der s-Vektor eine Richtung vom ersten zum zweiten Scheitelpunkt, und t ist das Kreuz Produkt des normalen und des s.</span><span class="sxs-lookup"><span data-stu-id="44525-155">In this case, the s vector is a direction from the first to the second vertex, and t is the cross product of the normal and s.</span></span> <span data-ttu-id="44525-156">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="44525-156">For instance:</span></span>


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



<span data-ttu-id="44525-157">IMT kann mithilfe der D3DX IMT-Berechnungsfunktionen (D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal und D3DXComputeIMTFromTexture) direkt oder basierend auf einem Eingabe Signal angegeben werden \_ .</span><span class="sxs-lookup"><span data-stu-id="44525-157">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal, and D3DXComputeIMTFromTexture\_graphics.</span></span>

<span data-ttu-id="44525-158">Geben Sie IMT-Daten direkt an, wenn Sie steuern möchten, wie der Textur Raum einzelnen Dreiecken zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="44525-158">Specify IMT data directly if you want to control how texture-space is allocated to individual triangles.</span></span> <span data-ttu-id="44525-159">Auf diese Weise weisen Sie den wichtigen Bereichen eines Netzes (z. b. das Gesicht oder das Brust Logo eines Zeichens oder die Bereiche einer Szene in der Nähe des Walking-Pfades eines Players) mehr Bereiche zu.</span><span class="sxs-lookup"><span data-stu-id="44525-159">By doing so, allocate more area in the atlas to important areas of a mesh (such as a character's face or chest logo, or regions of a scene near a player's walking-path).</span></span> <span data-ttu-id="44525-160">Durch die Angabe von IMT, die Vielfache der Identitätsmatrix sind, werden die resultierenden Dreiecke im Textur Bereich einheitlich skaliert.</span><span class="sxs-lookup"><span data-stu-id="44525-160">By specifying IMT's that are multiples of the identity matrix, the resulting triangles will be scaled uniformly in texture space.</span></span>

<span data-ttu-id="44525-161">Wenn Sie z. b. eine hochauflösende normale Karte haben, können Sie IMT berechnen, um mehr Textur Raum für Bereiche mit höherem Frequenz Signal in der normalen Karte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="44525-161">For example, given a high-resolution normal map, you can compute IMT to provide more texture-space to areas of higher frequency signal in the normal map.</span></span> <span data-ttu-id="44525-162">Dreiecke, die "Flat" sind (die Konstanten Bereichen der ursprünglichen normalen Karte zugeordnet sind) erhalten weniger Textur Bereich.</span><span class="sxs-lookup"><span data-stu-id="44525-162">Triangles that are "flat" (that mapped to constant regions of the original normal map) will receive less texture space.</span></span> <span data-ttu-id="44525-163">Dreiecke, die eine große Anzahl von normalkarten Details enthalten, erhalten im Endergebnis mehr Textur Bereich.</span><span class="sxs-lookup"><span data-stu-id="44525-163">Triangles that contain a great deal of normal-map detail will receive more texture area in the final result.</span></span> <span data-ttu-id="44525-164">Anschließend können Sie die normale Zuordnung in eine kleinere Textur übernehmen, aber die Details beibehalten, oder Sie können die normale Karte mit der optimalen UV-Zuordnung neu berechnen.</span><span class="sxs-lookup"><span data-stu-id="44525-164">You can then resample the normal map into a smaller texture but maintain detail, or you can recompute the normal map with the more optimal UV mapping.</span></span>

### <a name="using-adjacency-data-for-user-specified-creases"></a><span data-ttu-id="44525-165">Verwenden von Daten für benutzerdefinierte Aliasnamen</span><span class="sxs-lookup"><span data-stu-id="44525-165">Using Adjacency Data for User Specified Creases</span></span>

<span data-ttu-id="44525-166">Benutzerdefinierte Informations Informationen können für die Partitionierungsfunktion bereitgestellt werden, um vordefinierte Aliase im Mesh zu beschreiben, und definieren somit eine Diagramm Grenze zwischen angrenzenden Gesichtern.</span><span class="sxs-lookup"><span data-stu-id="44525-166">User-defined adjacency information can be provided to the partitioning function to describe pre-defined creases in the mesh, and thus define a chart boundary between adjacent faces.</span></span> <span data-ttu-id="44525-167">Dies ist eine einfache Möglichkeit für den Aufrufer, seine eigene Diagramm Partitionierung als Eingabe in den Algorithmus anzugeben, wodurch Diagramme weiter verfeinert werden, um die Streckung unter den maximal zulässigen Wert zu bringen.</span><span class="sxs-lookup"><span data-stu-id="44525-167">This is a simple way for the caller to specify their own chart partitioning as input into the algorithm, which will further refine charts to bring the stretch under the maximum allowed.</span></span>

### <a name="example"></a><span data-ttu-id="44525-168">Beispiel</span><span class="sxs-lookup"><span data-stu-id="44525-168">Example</span></span>

<span data-ttu-id="44525-169">In diesem Beispiel wird veranschaulicht, wie Sie mit den uvatlas-APIs und dem DirectX-Viewer (Dxviewer.exe) Diskontinuitäten in Ihrem Modell suchen und beheben können, die sich erheblich auf die Größe Ihres Textur Atlas auswirken können.</span><span class="sxs-lookup"><span data-stu-id="44525-169">This example illustrates how you might use the UVAtlas APIs and the DirectX Viewer (Dxviewer.exe) to find and fix discontinuities in your model that can dramatically affect the size of your texture atlas.</span></span> <span data-ttu-id="44525-170">Sie erhalten Dxviewer.exe und erfahren mehr über das DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="44525-170">You can get Dxviewer.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="44525-171">Dxviewer.exe wurde nach der Version von August 2009 aus dem DirectX SDK entfernt. damit Sie es erhalten, benötigen Sie mindestens das DirectX SDK vom August 2009.</span><span class="sxs-lookup"><span data-stu-id="44525-171">Dxviewer.exe was removed from the DirectX SDK after the August 2009 version so to get it you'll need at least the August 2009 DirectX SDK.</span></span> <span data-ttu-id="44525-172">Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="44525-172">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="44525-173">Angenommen, Sie haben mit einem Modell in Ihrer bevorzugten Inhalts Generierungs Software gestartet (in diesem Beispiel wird ein in Maya erstelltes Zwerg Hauptmodell verwendet).</span><span class="sxs-lookup"><span data-stu-id="44525-173">Assume you started with some model in your favorite content generation software (this example uses a dwarf head model that was created in Maya).</span></span> <span data-ttu-id="44525-174">Exportieren Sie das strukturierte Modell in eine x-Datei, und erstellen Sie einen Textur Atlas mit D3DXUVAtlasCreate.</span><span class="sxs-lookup"><span data-stu-id="44525-174">Export the textured model to an .x file and create a texture atlas with D3DXUVAtlasCreate.</span></span> <span data-ttu-id="44525-175">Der resultierende Textur Atlas würde in etwa wie in der folgenden Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="44525-175">The resulting texture atlas would look something like the following illustration.</span></span>

![Abbildung eines Atlas für ein Zwerg Modell](images/uvatlas5.jpg)

<span data-ttu-id="44525-177">Der Atlas verfügt über 22 Diagramme und eine maximale Streckung von 0,994.</span><span class="sxs-lookup"><span data-stu-id="44525-177">The atlas has 22 charts and a maximum stretch of 0.994.</span></span>

<span data-ttu-id="44525-178">Sehen Sie sich nun das strukturierte Modell an, um zu sehen, wie gut der Geometrie Text der Geometrie zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="44525-178">Now look at the textured model to see how well the texture atlas maps to the geometry.</span></span> <span data-ttu-id="44525-179">Laden Sie dazu das Modell in das Viewer-Tool:</span><span class="sxs-lookup"><span data-stu-id="44525-179">To do this, load the model into the viewer tool:</span></span>

-   <span data-ttu-id="44525-180">Öffnen Sie das Viewer-Tool über die DirectX-Hilfsprogramme.</span><span class="sxs-lookup"><span data-stu-id="44525-180">Open the viewer tool from the DirectX Utilities.</span></span>
-   <span data-ttu-id="44525-181">Laden Sie die x-Datei, indem Sie auf die Schaltfläche Öffnen klicken.</span><span class="sxs-lookup"><span data-stu-id="44525-181">Load the .x file by clicking the Open button.</span></span>
-   <span data-ttu-id="44525-182">Aktivieren Sie die Option Anzeige aktivieren, indem Sie auf die Schaltfläche Ansicht klicken und im Popup Fenster die Option zum Auswählen von "</span><span class="sxs-lookup"><span data-stu-id="44525-182">Enabling the crease viewing option by clicking the view button and selecting Creases from popup.</span></span>

<span data-ttu-id="44525-183">In der folgenden Abbildung wird gezeigt, was im Viewer-Tool angezeigt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="44525-183">The following illustration shows what you should see in the viewer tool.</span></span>

![Abbildung eines strukturierten Netzes im Viewer-Tool](images/uvatlas6c.jpg)

<span data-ttu-id="44525-185">Jede Zeile ist eine krease, bei der es sich um einen angrenzenden Rand zwischen zwei Diagrammen im Textur Atlas handelt.</span><span class="sxs-lookup"><span data-stu-id="44525-185">Each line is a crease which is an adjacent edge between two charts in the texture atlas.</span></span> <span data-ttu-id="44525-186">Die Anzahl der vom Algorithmus generierten Diagramme wird durch geringfügige Unterschiede verursacht, die möglicherweise aufgrund von Diskontinuitäten in den normalen auftreten.</span><span class="sxs-lookup"><span data-stu-id="44525-186">The number of charts generated by the algorithm is caused by slight differences perhaps due to discontinuities in the normals.</span></span> <span data-ttu-id="44525-187">Diese kleinen Unterschiede können durch das Schweißen von Daten reduziert werden, d. h. durch das Erzwingen von Daten, die nahezu gleich sind.</span><span class="sxs-lookup"><span data-stu-id="44525-187">These small differences can be reduced by welding data, that is, forcing data that is nearly equal to be equal.</span></span> <span data-ttu-id="44525-188">So Verschweißen Sie die normale und die skingewichtungen:</span><span class="sxs-lookup"><span data-stu-id="44525-188">To weld the normals and the skinweights:</span></span>

-   <span data-ttu-id="44525-189">Führen Sie das DirectX OPS (dxops.exe)-Tool mit der folgenden Befehlszeile im Mesh aus (ersetzen Sie "modelname. x" durch den Namen des Modells):</span><span class="sxs-lookup"><span data-stu-id="44525-189">Run the DirectX Ops (dxops.exe) tool with the following command line on the mesh (replacing 'modelName.x' with the name of your model):</span></span>
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

<span data-ttu-id="44525-190">Dadurch werden die normale und skingewichtungen verglichen, und wenn Sie sich im Wert um weniger als 2,01 unterscheiden, werden die Daten gleich.</span><span class="sxs-lookup"><span data-stu-id="44525-190">This compares the normals and skinweights, and where they differ in value by less than 2.01, the data is made equal.</span></span> <span data-ttu-id="44525-191">In den folgenden Abbildungen wird eine schließende Ansicht angezeigt, um die vor dem Schweißen (auf der linken Seite) und die Lösch Vorgängen nach dem Schweißen (auf der rechten Seite) Vorgängen anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="44525-191">The following illustrations shows a close up of the eye to see the creases before welding (on the left) and the creases after welding (on the right):</span></span>

![Abbildung der Aliase vor dem Schweißen](images/uvatlas6a.jpg)![Abbildung der Aliase nach dem Schweißen](images/uvatlas6b.jpg)

<span data-ttu-id="44525-194">Abbildung 7: Entfernen von Aliasen durch Schweißen</span><span class="sxs-lookup"><span data-stu-id="44525-194">Figure 7: Removing creases by welding</span></span>

<span data-ttu-id="44525-195">In diesem Beispiel wurden 86 Vertices aus dem eingabemesh entfernt.</span><span class="sxs-lookup"><span data-stu-id="44525-195">In this example, welding removed 86 vertices from the input mesh.</span></span> <span data-ttu-id="44525-196">Mit weniger kreasen im Mesh können Sie den Atlas neu generieren, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="44525-196">With fewer creases in the mesh, you can regenerate the atlas, as the following illustration shows.</span></span>

![Abbildung des neuen Atlas mit entfernten löschenden](images/uvatlas8.jpg)

<span data-ttu-id="44525-198">Der Atlas verfügt nur über 7 Diagramme und eine maximale Streckung von ungefähr 0,0776.</span><span class="sxs-lookup"><span data-stu-id="44525-198">The atlas only has 7 charts and a maximum stretch of approximately 0.0776.</span></span> <span data-ttu-id="44525-199">Der neue Atlas passt nun in eine kleinere Textur (etwa 30% kleiner in diesem Beispiel).</span><span class="sxs-lookup"><span data-stu-id="44525-199">The new atlas now fits into a smaller texture (approximately 30% smaller in this example).</span></span>

### <a name="packing-charts-into-an-atlas"></a><span data-ttu-id="44525-200">Packen von Diagrammen in einen Atlas</span><span class="sxs-lookup"><span data-stu-id="44525-200">Packing Charts Into an Atlas</span></span>

<span data-ttu-id="44525-201">Nachdem ein Mesh in einzeln parametrisierte Diagramme partitioniert wurde, müssen die Diagramme effizient in eine einzelne Textur Zuordnung gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="44525-201">Once a mesh has been partitioned into individually-parameterized charts, the charts need to be packed efficiently into a single texture map.</span></span> <span data-ttu-id="44525-202">Dies wird als zweiter Schritt von D3DXUVAtlasCreate ausgeführt oder kann explizit durch Aufrufen von D3DXUVAtlasPack aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="44525-202">This is performed as the second step of D3DXUVAtlasCreate or can be invoked explicitly by calling D3DXUVAtlasPack.</span></span>

<span data-ttu-id="44525-203">Gepackte Diagramme werden durch eine benutzerdefinierte Breite getrennt.</span><span class="sxs-lookup"><span data-stu-id="44525-203">Packed charts are separated by a user-specified gutter width.</span></span> <span data-ttu-id="44525-204">Der bundgerbreite ist die Menge der Trennung zwischen Diagrammen und ermöglicht die bilineare Interpolations-und MIP-Zuordnung, um das Rendern von Artefakten an Diagramm Grenzen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="44525-204">The gutter width is the amount of separation between charts, and allows for bilinear interpolation and mip-mapping to avoid rendering artifacts at chart boundaries.</span></span> <span data-ttu-id="44525-205">D3DX stellt eine Schnittstelle zum automatischen Ausfüllen dieser Bundstege bereit. Weitere Informationen finden Sie unter [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="44525-205">D3DX provides an interface for automatically filling in these gutters - see [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) for more information.</span></span>

## <a name="integrating-uvatlas-into-your-pipeline"></a><span data-ttu-id="44525-206">Integrieren von uvatlas in ihre Pipeline</span><span class="sxs-lookup"><span data-stu-id="44525-206">Integrating UVAtlas Into Your Pipeline</span></span>

<span data-ttu-id="44525-207">Diese Funktionen können nicht nur vor dem Textur zeichnen, sondern auch in eine automatisierte Grafik Pipeline integriert werden.</span><span class="sxs-lookup"><span data-stu-id="44525-207">In addition to being artist-invoked prior to texture painting, these functions can be integrated into an automated art pipeline.</span></span> <span data-ttu-id="44525-208">Beispielsweise kann ein uvatlas-Befehl automatisch ausgegeben werden, nachdem ein Objekt aktualisiert wurde, bevor eine PRT-Simulation oder ein normaler Zuordnungs Durchlauf durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44525-208">For example, a UVAtlas call can be issued automatically after an asset is updated, prior to performing a PRT simulation or normal mapping pass.</span></span> <span data-ttu-id="44525-209">Dadurch wird vermieden, dass die UV-Zuordnung eines Objekts manuell repariert werden muss, wenn die Topologie des Netzes geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="44525-209">This avoids any need to manually manual repair of an object's UV mapping if the mesh's topology has been modified.</span></span>

<span data-ttu-id="44525-210">Eine Beispiel Verwendung der uvatlas-Funktionen finden Sie im [Command-Line Tool für UV-Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="44525-210">See the [UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx) for example usage of the UVAtlas functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44525-211">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="44525-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44525-212">Erweiterte Themen</span><span class="sxs-lookup"><span data-stu-id="44525-212">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
