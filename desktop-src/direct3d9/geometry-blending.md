---
description: Direct3D ermöglicht es einer Anwendung, die Umsetzung ihrer Szenen zu steigern, indem segmentierte polygonale Objekte gerendert werden, insbesondere Zeichen, die über reibungslos gemischte Gelenke verfügen.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Geometrie Mischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19daa40f7d7d8193ae486640bc613dd7a666ec7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745384"
---
# <a name="geometry-blending-direct3d-9"></a><span data-ttu-id="83b22-103">Geometrie Mischung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="83b22-103">Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="83b22-104">Direct3D ermöglicht es einer Anwendung, die Umsetzung ihrer Szenen zu steigern, indem segmentierte polygonale Objekte gerendert werden, insbesondere Zeichen, die über reibungslos gemischte Gelenke verfügen.</span><span class="sxs-lookup"><span data-stu-id="83b22-104">Direct3D enables an application to increase the realism of its scenes by rendering segmented polygonal objects - especially characters - that have smoothly blended joints.</span></span> <span data-ttu-id="83b22-105">Diese Effekte werden häufig als "Skinning" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="83b22-105">These effects are often referred to as skinning.</span></span> <span data-ttu-id="83b22-106">Das System erreicht diesen Effekt, indem er zusätzliche Transformations Matrizen für die Welt auf einen einzelnen Satz von Vertices anwendet, um mehrere Ergebnisse zu erstellen, und dann eine lineare Mischung zwischen den resultierenden Scheitel Punkten durchführen, um einen einzelnen Satz von Geometrie für das Rendering zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="83b22-106">The system achieves this effect by applying additional world transformation matrices to a single set of vertices to create multiple results, and then performing a linear blend between the resultant vertices to create a single set of geometry for rendering.</span></span> <span data-ttu-id="83b22-107">Die folgende Abbildung einer Banane zeigt diesen Prozess.</span><span class="sxs-lookup"><span data-stu-id="83b22-107">The following illustration of a banana shows this process.</span></span>

![Abbildung des Prozesses zum Mischen von zwei Objekten mit der Bananen Textur](images/geometry-blend.png)

<span data-ttu-id="83b22-109">Die obige Abbildung zeigt, wie Sie sich den Geometry-Mischungs Prozess vorstellen können.</span><span class="sxs-lookup"><span data-stu-id="83b22-109">The preceding illustration shows how you might imagine the geometry-blending process.</span></span> <span data-ttu-id="83b22-110">Bei einem einzelnen Renderingbefehl übernimmt das System die Scheitel Punkte für die Banane, transformiert Sie zweimal, und zwar ohne Änderung und einmal mit einer einfachen Drehung, und kombiniert die Ergebnisse, um eine gekrümmten Banane zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="83b22-110">In a single rendering call, the system takes the vertices for the banana, transforms them twice - once without modification, and once with a simple rotation - and blends the results to create a bent banana.</span></span> <span data-ttu-id="83b22-111">Das System mischt die Scheitelpunkt Position sowie den Scheitelpunkt normal, wenn Beleuchtung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="83b22-111">The system blends the vertex position, as well as the vertex normal when lighting is enabled.</span></span> <span data-ttu-id="83b22-112">Anwendungen sind nicht auf zwei Mischungs Pfade beschränkt. Direct3D kann Geometrie zwischen bis zu vier Welt Matrizen, einschließlich der Standard-World Matrix, [**D3DTS \_ World**](d3dts-world.md), mischen.</span><span class="sxs-lookup"><span data-stu-id="83b22-112">Applications are not limited to two blending paths; Direct3D can blend geometry between as many as four world matrices, including the standard world matrix, [**D3DTS\_WORLD**](d3dts-world.md).</span></span>

> [!Note]
>
> <span data-ttu-id="83b22-113">Wenn Beleuchtung aktiviert ist, werden Vertex-Normale durch eine entsprechende inverse World-View-Matrix transformiert, die auf die gleiche Weise gewichtet wird wie die Berechnungen der Scheitelpunkt Position.</span><span class="sxs-lookup"><span data-stu-id="83b22-113">When lighting is enabled, vertex normals are transformed by a corresponding inverse world-view matrix, weighted in the same way as the vertex position computations.</span></span> <span data-ttu-id="83b22-114">Das System normalisiert den resultierenden normalen Vektor, wenn der D3DRS \_ normalizenormals-Rendering-Zustand auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="83b22-114">The system normalizes the resulting normal vector if the D3DRS\_NORMALIZENORMALS render state is set to **TRUE**.</span></span>

 

<span data-ttu-id="83b22-115">Ohne Geometrie Mischung werden dynamische artikulierte Modelle häufig in Segmenten gerendert.</span><span class="sxs-lookup"><span data-stu-id="83b22-115">Without geometry blending, dynamic articulated models are often rendered in segments.</span></span> <span data-ttu-id="83b22-116">Stellen Sie sich beispielsweise ein 3D-Modell der menschlichen Arm vor.</span><span class="sxs-lookup"><span data-stu-id="83b22-116">For instance, consider a 3D model of the human arm.</span></span> <span data-ttu-id="83b22-117">In der einfachsten Ansicht besteht ein Arm aus zwei Teilen: dem oberen Arm, der mit dem Text verbunden ist, und dem unteren Arm, der eine Verbindung mit der Hand herstellt.</span><span class="sxs-lookup"><span data-stu-id="83b22-117">In the simplest view, an arm has two parts: the upper arm which connects to the body, and the lower arm, which connects to the hand.</span></span> <span data-ttu-id="83b22-118">Beide sind am-Bogen angeschlossen, und der untere Arm dreht sich an diesem Punkt.</span><span class="sxs-lookup"><span data-stu-id="83b22-118">The two are connected at the elbow, and the lower arm rotates at that point.</span></span> <span data-ttu-id="83b22-119">Eine Anwendung, die einen Arm rendert, behält möglicherweise Scheitelpunkt Daten für den oberen und unteren Arm bei, jeweils mit einer separaten Welt Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="83b22-119">An application that renders an arm might retain vertex data for the upper and lower arm, each with a separate world transformation matrix.</span></span> <span data-ttu-id="83b22-120">Dies wird im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="83b22-120">The following code example illustrates this.</span></span>


```
typedef struct _Arm
{
    VERTEX upper_arm_verts[200];
    D3DMATRIX matWorld_Upper;

    VERTEX lower_arm_verts[200];
    D3DMATRIX matWorld_Lower;
} ARM, *LPARM;

ARM MyArm; // This needs to be initialized.
```



<span data-ttu-id="83b22-121">Um den Arm zu rendern, werden zwei renderingaufrufe durchgeführt, wie im folgenden Code dargestellt.</span><span class="sxs-lookup"><span data-stu-id="83b22-121">To render the arm, two rendering calls are made, as shown in the following code.</span></span>


```
// Render the upper arm.
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Upper );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );

// Render the lower arm, updating its world matrix to articulate
// the arm by pi/4 radians (45 degrees) at the elbow.
MyArm.matWorld_Lower = RotateMyArm(MyArm.matWorld, pi/4);
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Lower );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );
```



<span data-ttu-id="83b22-122">Die folgende Abbildung stellt eine Banane dar, die zur Verwendung dieser Technik geändert wird.</span><span class="sxs-lookup"><span data-stu-id="83b22-122">The following illustration is a banana, modified to use this technique.</span></span>

![Abbildung einer gemischten Banane ohne Geometrie Mischung](images/noblend.png)

<span data-ttu-id="83b22-124">Die Unterschiede zwischen der gemischten Geometrie und der nicht gemischten Geometrie sind offensichtlich.</span><span class="sxs-lookup"><span data-stu-id="83b22-124">The differences between the blended geometry and the nonblended geometry are obvious.</span></span> <span data-ttu-id="83b22-125">Dieses Beispiel ist ziemlich extrem.</span><span class="sxs-lookup"><span data-stu-id="83b22-125">This example is somewhat extreme.</span></span> <span data-ttu-id="83b22-126">In einer realen Anwendung werden die Gelenke segmentierter Modelle so entworfen, dass die Nähte nicht so offensichtlich sind.</span><span class="sxs-lookup"><span data-stu-id="83b22-126">In a real-world application, the joints of segmented models are designed so that seams are not as obvious.</span></span> <span data-ttu-id="83b22-127">Allerdings sind die Nähte manchmal sichtbar, was eine Konstante Herausforderung für Modell Designer darstellt.</span><span class="sxs-lookup"><span data-stu-id="83b22-127">However, seams are visible at times, which presents constant challenges for model designers.</span></span>

<span data-ttu-id="83b22-128">Geometrie Mischung in Direct3D stellt eine Alternative zum klassischen segmentierten Modellierungs Szenario dar.</span><span class="sxs-lookup"><span data-stu-id="83b22-128">Geometry blending in Direct3D presents an alternative to the classic segmented-modeling scenario.</span></span> <span data-ttu-id="83b22-129">Die verbesserte visuelle Qualität segmentierter Objekte ergibt sich jedoch aus den Kosten der Mischungs Berechnungen während des Renderings.</span><span class="sxs-lookup"><span data-stu-id="83b22-129">However, the improved visual quality of segmented objects comes at the cost of the blending computations during rendering.</span></span> <span data-ttu-id="83b22-130">Um die Auswirkungen dieser zusätzlichen Vorgänge zu minimieren, wird die Direct3D Geometry-Pipeline optimiert, um Geometrie mit dem geringstmöglichen Verwaltungsaufwand zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="83b22-130">To minimize the impact of these additional operations, the Direct3D geometry pipeline is optimized to blend geometry with the least possible overhead.</span></span> <span data-ttu-id="83b22-131">Anwendungen, die die von Direct3D angebotenen Geometrie-Mischungs Dienste Intelligent verwenden, können den Realismus ihrer Zeichen verbessern und gleichzeitig ernsthafte Auswirkungen auf die Leistung vermeiden.</span><span class="sxs-lookup"><span data-stu-id="83b22-131">Applications that intelligently use the geometry blending services offered by Direct3D can improve the realism of their characters while avoiding serious performance repercussions.</span></span>

## <a name="blending-transform-and-render-states"></a><span data-ttu-id="83b22-132">Mischen von Transformations-und renderzuständen</span><span class="sxs-lookup"><span data-stu-id="83b22-132">Blending Transform and Render States</span></span>

<span data-ttu-id="83b22-133">Die [**IDirect3DDevice9:: setTransform**](/windows/desktop/api) -Methode erkennt die Makros [**D3DTS \_ World**](d3dts-world.md) und [**D3DTS \_ worldn**](d3dts-worldn.md) , die den Werten entsprechen, die vom [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) -Makro definiert werden können.</span><span class="sxs-lookup"><span data-stu-id="83b22-133">The [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method recognizes the [**D3DTS\_WORLD**](d3dts-world.md) and [**D3DTS\_WORLDn**](d3dts-worldn.md) macros, which correspond to values that can be defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro.</span></span> <span data-ttu-id="83b22-134">Diese Makros werden verwendet, um die Matrizen zu identifizieren, zwischen denen die Geometrie gemischt wird.</span><span class="sxs-lookup"><span data-stu-id="83b22-134">These macros are used to identify the matrices between which geometry will be blended.</span></span>

<span data-ttu-id="83b22-135">Der [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) -Enumerationstyp enthält den D3DRS \_ vertexblend-Rendering-Zustand zum Aktivieren und Steuern der Geometrie Mischung.</span><span class="sxs-lookup"><span data-stu-id="83b22-135">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes the D3DRS\_VERTEXBLEND render state to enable and control geometry blending.</span></span> <span data-ttu-id="83b22-136">Gültige Werte für diesen Rendering-Zustand werden durch den [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) -enumerierten Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="83b22-136">Valid values for this render state are defined by the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="83b22-137">Wenn Geometrie Mischung aktiviert ist, muss das Scheitelpunkt Format die entsprechende Anzahl von Mischungs Gewichtungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="83b22-137">If geometry blending is enabled, the vertex format must include the appropriate number of blending weights.</span></span>

## <a name="blending-weights"></a><span data-ttu-id="83b22-138">Mischen von Gewichtungen</span><span class="sxs-lookup"><span data-stu-id="83b22-138">Blending Weights</span></span>

<span data-ttu-id="83b22-139">Ein Mischungs Gewicht, manchmal auch als Beta-Gewichtung bezeichnet, steuert, in welchem Ausmaß eine bestimmte Weltmatrix auf einen Scheitelpunkt wirkt.</span><span class="sxs-lookup"><span data-stu-id="83b22-139">A blending weight, sometimes called a beta weight, controls the extent to which a given world matrix affects a vertex.</span></span> <span data-ttu-id="83b22-140">Beim Mischen von Gewichtungen handelt es sich um Gleit Komma Werte zwischen 0,0 und 1,0, die im Vertex-Format codiert sind. der Wert 0,0 bedeutet, dass der Scheitelpunkt nicht mit dieser Matrix gemischt ist, und 1,0 bedeutet, dass der Scheitelpunkt vollständig von der Matrix betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="83b22-140">Blending weights are floating-point values that range from 0.0 to 1.0, encoded in the vertex format, where a value of 0.0 means the vertex is not blended with that matrix, and 1.0 means that the vertex is affected in full by the matrix.</span></span>

<span data-ttu-id="83b22-141">Geometrie-Mischungs Gewichtungen werden im Vertex-Format codiert und unmittelbar nach der Position der einzelnen Scheitel Punkte angezeigt, wie in [Fixed Function f VF Codes (Direct3D 9)](fixed-function-fvf-codes.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="83b22-141">Geometry blending weights are encoded in the vertex format, appearing immediately after the position for each vertex, as described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span> <span data-ttu-id="83b22-142">Sie geben die Anzahl der Mischungs Gewichtungen im Vertex-Format an, indem Sie eine der [FVF-Konstanten](d3dfvf.md) in die vertexbeschreibung einschließen, die Sie den Renderingmethoden bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="83b22-142">You communicate the number of blending weights in the vertex format by including one of the [FVF constants](d3dfvf.md) in the vertex description that you provide to the rendering methods.</span></span>

<span data-ttu-id="83b22-143">Das System führt eine lineare Mischung zwischen den gewichteten Ergebnissen der Blend-Matrizen aus.</span><span class="sxs-lookup"><span data-stu-id="83b22-143">The system performs a linear blend between the weighted results of the blend matrices.</span></span> <span data-ttu-id="83b22-144">Die folgende Gleichung ist die komplette Mischungs Formel.</span><span class="sxs-lookup"><span data-stu-id="83b22-144">The following equation is the complete blending formula.</span></span>

![Gleichung linearer Mischungs-, using World Transformation Matrizen](images/vert-blend-formula.png)

<span data-ttu-id="83b22-146">In der vorangehenden Gleichung ist vblend der Ausgabe Scheitelpunkt. die v-Elemente sind die Scheitel Punkte, die von der angewendeten Weltmatrix ([**D3DTS \_ worldn**](d3dts-worldn.md)) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="83b22-146">In the preceding equation, vBlend is the output vertex, the v-elements are the vertices produced by the applied world matrix ([**D3DTS\_WORLDn**](d3dts-worldn.md)).</span></span> <span data-ttu-id="83b22-147">Die W-Elemente sind die entsprechenden Gewichtungswerte im Scheitelpunkt Format.</span><span class="sxs-lookup"><span data-stu-id="83b22-147">The W elements are the corresponding weight values within the vertex format.</span></span> <span data-ttu-id="83b22-148">Ein Scheitelpunkt zwischen n Matrizen kann-1 enthalten, der Gewichtungswerte für jede Mischungs Matrix (mit Ausnahme des letzten) kombiniert.</span><span class="sxs-lookup"><span data-stu-id="83b22-148">A vertex blended between n matrices can have - 1 blending weight values, one for each blending matrix, except the last.</span></span> <span data-ttu-id="83b22-149">Das System generiert automatisch die Gewichtung für die letzte Weltmatrix, sodass die Summe aller Gewichtungen 1,0 ist, ausgedrückt in Sigma-Notation.</span><span class="sxs-lookup"><span data-stu-id="83b22-149">The system automatically generates the weight for the last world matrix so that the sum of all weights is 1.0, expressed in sigma notation here.</span></span> <span data-ttu-id="83b22-150">Diese Formel kann für jeden der von Direct3D unterstützten Fällen vereinfacht werden, was in den folgenden Gleichungen gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="83b22-150">This formula can be simplified for each of the cases supported by Direct3D, which is shown in the following equations.</span></span>

![Gleichungen linearer Blending für drei Mischungs Fälle](images/vert-blend-formulas-simple.png)

<span data-ttu-id="83b22-152">Dies sind die vereinfachten Formen der kompletten Mischungs Formel für die zwei, drei und vier Blend Matrix Fälle.</span><span class="sxs-lookup"><span data-stu-id="83b22-152">These are the simplified forms of the complete blending formula for the two, three, and four blend matrix cases.</span></span>

> [!Note]  
> <span data-ttu-id="83b22-153">Obwohl Direct3D FVF-Deskriptoren enthält, um Vertices zu definieren, die bis zu fünf Mischungs Gewichtungen enthalten, können in dieser Version von DirectX nur drei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83b22-153">Although Direct3D includes FVF descriptors to define vertices that contain up to five blending weights, only three can be used in this release of DirectX.</span></span>

 

<span data-ttu-id="83b22-154">Weitere Informationen finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="83b22-154">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="83b22-155">Verwenden von Geometrie Mischung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="83b22-155">Using Geometry Blending (Direct3D 9)</span></span>](using-geometry-blending.md)
-   [<span data-ttu-id="83b22-156">Indiziertes Vertex-Blending (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="83b22-156">Indexed Vertex Blending (Direct3D 9)</span></span>](indexed-vertex-blending.md)
-   [<span data-ttu-id="83b22-157">Vertex-Tweening (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="83b22-157">Vertex Tweening (Direct3D 9)</span></span>](vertex-tweening.md)

## <a name="related-topics"></a><span data-ttu-id="83b22-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="83b22-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83b22-159">Scheitelpunkt Pipeline</span><span class="sxs-lookup"><span data-stu-id="83b22-159">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
