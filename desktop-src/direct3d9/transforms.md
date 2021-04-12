---
description: Der Teil von Direct3D, der die Geometrie über die Geometrie Pipeline mit fester Funktionsweise überträgt, ist die Transform-Engine.
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: Transformationen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f482ef12c88140c2eff4c61e634fd3297aeaf295
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392881"
---
# <a name="transforms-direct3d-9"></a><span data-ttu-id="37f32-103">Transformationen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="37f32-103">Transforms (Direct3D 9)</span></span>

<span data-ttu-id="37f32-104">Der Teil von Direct3D, der die Geometrie über die Geometrie Pipeline mit fester Funktionsweise überträgt, ist die Transform-Engine.</span><span class="sxs-lookup"><span data-stu-id="37f32-104">The part of Direct3D that pushes geometry through the fixed function geometry pipeline is the transform engine.</span></span> <span data-ttu-id="37f32-105">Er sucht das Modell und den Viewer auf der Welt, projiziert die Scheitel Punkte, die auf dem Bildschirm angezeigt werden, und schneidet Scheitel Punkte an den Viewport.</span><span class="sxs-lookup"><span data-stu-id="37f32-105">It locates the model and viewer in the world, projects vertices for display on the screen, and clips vertices to the viewport.</span></span> <span data-ttu-id="37f32-106">Die Transformations-Engine führt auch Beleuchtungsberechnungen durch, um die diffusen und Glanz Komponenten in jedem Scheitelpunkt zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="37f32-106">The transform engine also performs lighting computations to determine diffuse and specular components at each vertex.</span></span>

<span data-ttu-id="37f32-107">Die Geometrie Pipeline nimmt Vertices als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="37f32-107">The geometry pipeline takes vertices as input.</span></span> <span data-ttu-id="37f32-108">Die Transformations-Engine wendet die Transformationen "World", "View" und "Projection" auf die Scheitel Punkte an, schneidet das Ergebnis ab und übergibt alles an den Rasterizer.</span><span class="sxs-lookup"><span data-stu-id="37f32-108">The transform engine applies the world, view, and projection transforms to the vertices, clips the result, and passes everything to the rasterizer.</span></span>

<span data-ttu-id="37f32-109">Am Anfang der Pipeline werden die Vertices eines Modells relativ zu einem lokalen Koordinatensystem deklariert.</span><span class="sxs-lookup"><span data-stu-id="37f32-109">At the head of the pipeline, a model's vertices are declared relative to a local coordinate system.</span></span> <span data-ttu-id="37f32-110">Dies ist ein lokaler Ursprung und eine Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="37f32-110">This is a local origin and an orientation.</span></span> <span data-ttu-id="37f32-111">Diese Ausrichtung von Koordinaten wird häufig als Modellbereich bezeichnet, und einzelne Koordinaten werden als Modell Koordinaten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="37f32-111">This orientation of coordinates is often referred to as model space, and individual coordinates are called model coordinates.</span></span>

<span data-ttu-id="37f32-112">In der ersten Phase der Geometrie Pipeline werden die Scheitel Punkte eines Modells von Ihrem lokalen Koordinatensystem in ein Koordinatensystem transformiert, das von allen Objekten in einer Szene verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37f32-112">The first stage of the geometry pipeline transforms a model's vertices from their local coordinate system to a coordinate system that is used by all the objects in a scene.</span></span> <span data-ttu-id="37f32-113">Der Prozess der Umgestaltung der Scheitel Punkte wird als Welt Transformation bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="37f32-113">The process of reorienting the vertices is called the world transform.</span></span> <span data-ttu-id="37f32-114">Diese neue Ausrichtung wird häufig als Welt Raum bezeichnet, und jeder Scheitelpunkt im Raum wird mit Weltkoordinaten deklariert.</span><span class="sxs-lookup"><span data-stu-id="37f32-114">This new orientation is commonly referred to as world space, and each vertex in world space is declared using world coordinates.</span></span>

<span data-ttu-id="37f32-115">In der nächsten Phase sind die Scheitel Punkte, die Ihre 3D-Welt beschreiben, in Bezug auf eine Kamera orientiert.</span><span class="sxs-lookup"><span data-stu-id="37f32-115">In the next stage, the vertices that describe your 3D world are oriented with respect to a camera.</span></span> <span data-ttu-id="37f32-116">Das heißt, Ihre Anwendung wählt eine Sicht Ansicht für die Szene aus, und die Raumkoordinaten der Welt werden verschoben und um die Ansicht der Kamera gedreht. Dadurch wird der Raum in den Kamerabereich verwandelt.</span><span class="sxs-lookup"><span data-stu-id="37f32-116">That is, your application chooses a point-of-view for the scene, and world space coordinates are relocated and rotated around the camera's view, turning world space into camera space.</span></span> <span data-ttu-id="37f32-117">Dies ist die Ansichts Transformation.</span><span class="sxs-lookup"><span data-stu-id="37f32-117">This is the view transform.</span></span>

<span data-ttu-id="37f32-118">Die nächste Phase ist die Projektions Transformation.</span><span class="sxs-lookup"><span data-stu-id="37f32-118">The next stage is the projection transform.</span></span> <span data-ttu-id="37f32-119">In diesem Teil der Pipeline werden Objekte in der Regel auf die Entfernung des Viewers skaliert, um die Illusion von Tiefe an eine Szene zu vermitteln. Close-Objekte werden so erstellt, dass Sie größer als entfernte Objekte sind usw.</span><span class="sxs-lookup"><span data-stu-id="37f32-119">In this part of the pipeline, objects are usually scaled with relation to their distance from the viewer in order to give the illusion of depth to a scene; close objects are made to appear larger than distant objects, and so on.</span></span> <span data-ttu-id="37f32-120">Der Einfachheit halber bezieht sich diese Dokumentation auf den Raum, in dem Scheitel Punkte nach der Projektions Transformation als Projektionsraum vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="37f32-120">For simplicity, this documentation refers to the space in which vertices exist after the projection transform as projection space.</span></span> <span data-ttu-id="37f32-121">In einigen Grafik Büchern wird der Projektionsraum möglicherweise als homogener Perspektiven Raum bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="37f32-121">Some graphics books might refer to projection space as post-perspective homogeneous space.</span></span> <span data-ttu-id="37f32-122">Nicht alle Projektions Transformationen Skalieren die Größe von Objekten in einer Szene.</span><span class="sxs-lookup"><span data-stu-id="37f32-122">Not all projection transforms scale the size of objects in a scene.</span></span> <span data-ttu-id="37f32-123">Eine Projektion wie diese wird mitunter als affine oder orthogonale Projektion bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="37f32-123">A projection such as this is sometimes called an affine or orthogonal projection.</span></span>

<span data-ttu-id="37f32-124">Im letzten Teil der Pipeline werden alle Scheitel Punkte, die auf dem Bildschirm nicht sichtbar sind, entfernt, sodass der Raster nicht mehr die Zeit zum Berechnen der Farben und Schattierung für etwas hat, das nie angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="37f32-124">In the final part of the pipeline, any vertices that will not be visible on the screen are removed, so that the rasterizer doesn't take the time to calculate the colors and shading for something that will never be seen.</span></span> <span data-ttu-id="37f32-125">Dieser Vorgang wird als Clipping bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="37f32-125">This process is called clipping.</span></span> <span data-ttu-id="37f32-126">Nach dem Clipping werden die verbleibenden Scheitel Punkte entsprechend den viewportparametern skaliert und in Bildschirm Koordinaten konvertiert.</span><span class="sxs-lookup"><span data-stu-id="37f32-126">After clipping, the remaining vertices are scaled according to the viewport parameters and converted into screen coordinates.</span></span> <span data-ttu-id="37f32-127">Die resultierenden Scheitel Punkte, die auf dem Bildschirm angezeigt werden, wenn die Szene rasteriert ist, sind im Bildschirmbereich vorhanden.</span><span class="sxs-lookup"><span data-stu-id="37f32-127">The resulting vertices, seen on the screen when the scene is rasterized, exist in screen space.</span></span>

<span data-ttu-id="37f32-128">Transformationen werden verwendet, um die Objekt Geometrie von einem Koordinaten Bereich in einen anderen zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="37f32-128">Transforms are used to convert object geometry from one coordinate space to another.</span></span> <span data-ttu-id="37f32-129">Direct3D verwendet Matrizen, um 3D-Transformationen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="37f32-129">Direct3D uses matrices to perform 3D transforms.</span></span> <span data-ttu-id="37f32-130">In diesem Abschnitt wird erläutert, wie Matrizen 3D-Transformationen erstellen, einige gängige Verwendungsmöglichkeiten für Transformationen beschreiben und wie Sie Matrizen kombinieren können, um eine einzelne Matrix zu erstellen, die mehrere Transformationen umfasst.</span><span class="sxs-lookup"><span data-stu-id="37f32-130">This section explains how matrices create 3D transforms, describes some common uses for transforms, and details how you can combine matrices to produce a single matrix that encompasses multiple transforms.</span></span>

-   <span data-ttu-id="37f32-131">[World Transform (Direct3D 9)](world-transform.md) : Konvertieren vom Modellbereich in den Raum</span><span class="sxs-lookup"><span data-stu-id="37f32-131">[World Transform (Direct3D 9)](world-transform.md) - convert from model space to world space</span></span>
-   <span data-ttu-id="37f32-132">[Transformation anzeigen (Direct3D 9)](view-transform.md) -Konvertieren von Welt Raum zum Anzeigen von Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="37f32-132">[View Transform (Direct3D 9)](view-transform.md) - convert from world space to view space</span></span>
-   <span data-ttu-id="37f32-133">[Projektions Transformation (Direct3D 9)](projection-transform.md) -Konvertieren von Sichtbereich in Projektionsraum</span><span class="sxs-lookup"><span data-stu-id="37f32-133">[Projection Transform (Direct3D 9)](projection-transform.md) - convert from view space to projection space</span></span>

## <a name="matrix-transforms"></a><span data-ttu-id="37f32-134">Matrixtransformationen</span><span class="sxs-lookup"><span data-stu-id="37f32-134">Matrix Transforms</span></span>

<span data-ttu-id="37f32-135">In Anwendungen, die mit 3D-Grafiken funktionieren, können Sie mithilfe geometrischer Transformationen folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="37f32-135">In applications that work with 3D graphics, you can use geometrical transforms to do the following:</span></span>

-   <span data-ttu-id="37f32-136">Gibt den Speicherort eines Objekts relativ zu einem anderen Objekt an.</span><span class="sxs-lookup"><span data-stu-id="37f32-136">Express the location of an object relative to another object.</span></span>
-   <span data-ttu-id="37f32-137">Drehen und Größe von Objekten.</span><span class="sxs-lookup"><span data-stu-id="37f32-137">Rotate and size objects.</span></span>
-   <span data-ttu-id="37f32-138">Ändern der Anzeige von Positionen, Richtungen und Perspektiven.</span><span class="sxs-lookup"><span data-stu-id="37f32-138">Change viewing positions, directions, and perspectives.</span></span>

<span data-ttu-id="37f32-139">Sie können beliebige Punkte (x, y, z) mit einer 4 x 4-Matrix in einen anderen Punkt (x ", y", z ") umwandeln, wie in der folgenden Gleichung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="37f32-139">You can transform any point (x,y,z) into another point (x', y', z') by using a 4x4 matrix, as shown in the following equation.</span></span>

![Gleichung der Umwandlung eines Punkts in einen anderen Punkt](images/matmult.png)

<span data-ttu-id="37f32-141">Führen Sie die folgenden Gleichungen für (x, y, z) und die Matrix aus, um den Punkt (x ', y ', z ') zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="37f32-141">Perform the following equations on (x, y, z) and the matrix to produce the point (x', y', z').</span></span>

![Gleichungen für den neuen Punkt](images/matexpnd.png)

<span data-ttu-id="37f32-143">Die gängigsten Transformationen sind Übersetzung, Drehung und Skalierung.</span><span class="sxs-lookup"><span data-stu-id="37f32-143">The most common transforms are translation, rotation, and scaling.</span></span> <span data-ttu-id="37f32-144">Sie können die Matrizen, die diese Effekte erzeugen, in einer einzelnen Matrix kombinieren, um mehrere Transformationen gleichzeitig zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="37f32-144">You can combine the matrices that produce these effects into a single matrix to calculate several transforms at once.</span></span> <span data-ttu-id="37f32-145">Beispielsweise können Sie eine einzelne Matrix erstellen, um eine Reihe von Punkten zu übersetzen und zu drehen.</span><span class="sxs-lookup"><span data-stu-id="37f32-145">For example, you can build a single matrix to translate and rotate a series of points.</span></span>

<span data-ttu-id="37f32-146">Matrizen werden in der Reihenfolge der Zeilen Spalten geschrieben.</span><span class="sxs-lookup"><span data-stu-id="37f32-146">Matrices are written in row-column order.</span></span> <span data-ttu-id="37f32-147">Eine Matrix, die Scheitel Punkte entlang jeder Achse gleichmäßig skaliert, die als einheitliche Skalierung bezeichnet wird, wird durch die folgende Matrix mithilfe der mathematischen Notation dargestellt.</span><span class="sxs-lookup"><span data-stu-id="37f32-147">A matrix that evenly scales vertices along each axis, known as uniform scaling, is represented by the following matrix using mathematical notation.</span></span>

![Gleichung einer Matrix für die einheitliche Skalierung](images/matrix.png)

<span data-ttu-id="37f32-149">In C++ deklariert Direct3D Matrizen als zweidimensionales Array mit der [**D3DMATRIX**](d3dmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="37f32-149">In C++, Direct3D declares matrices as a two-dimensional array, using the [**D3DMATRIX**](d3dmatrix.md) structure.</span></span> <span data-ttu-id="37f32-150">Im folgenden Beispiel wird gezeigt, wie eine **D3DMATRIX** -Struktur initialisiert wird, die als einheitliche Skalierungs Matrix fungiert.</span><span class="sxs-lookup"><span data-stu-id="37f32-150">The following example shows how to initialize a **D3DMATRIX** structure to act as a uniform scaling matrix.</span></span>


```
// In this example, s is a variable of type float.

D3DMATRIX scale = {
    s,               0.0f,            0.0f,            0.0f,
    0.0f,            s,               0.0f,            0.0f,
    0.0f,            0.0f,            s,               0.0f,
    0.0f,            0.0f,            0.0f,            1.0f
};
```



## <a name="translate"></a><span data-ttu-id="37f32-151">Translate</span><span class="sxs-lookup"><span data-stu-id="37f32-151">Translate</span></span>

<span data-ttu-id="37f32-152">Mit der folgenden Gleichung wird der Punkt (x, y, z) in einen neuen Punkt (x ", y", z ") übersetzt.</span><span class="sxs-lookup"><span data-stu-id="37f32-152">The following equation translates the point (x, y, z) to a new point (x', y', z').</span></span>

![Gleichung einer Übersetzungs Matrix für einen neuen Punkt](images/transl8.png)

<span data-ttu-id="37f32-154">Sie können eine Übersetzungs Matrix in C++ manuell erstellen.</span><span class="sxs-lookup"><span data-stu-id="37f32-154">You can manually create a translation matrix in C++.</span></span> <span data-ttu-id="37f32-155">Das folgende Beispiel zeigt den Quellcode für eine Funktion, die eine Matrix erstellt, um Vertices zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="37f32-155">The following example shows the source code for a function that creates a matrix to translate vertices.</span></span>


```
D3DXMATRIX Translate(const float dx, const float dy, const float dz) {
    D3DXMATRIX ret;

    D3DXMatrixIdentity(&ret);
    ret(3, 0) = dx;
    ret(3, 1) = dy;
    ret(3, 2) = dz;
    return ret;
}    // End of Translate
```



<span data-ttu-id="37f32-156">Zur einfacheren bereitstellt die D3DX Utility Library die [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) -Funktion bereit.</span><span class="sxs-lookup"><span data-stu-id="37f32-156">For convenience, the D3DX utility library supplies the [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) function.</span></span>

## <a name="scale"></a><span data-ttu-id="37f32-157">Skalieren</span><span class="sxs-lookup"><span data-stu-id="37f32-157">Scale</span></span>

<span data-ttu-id="37f32-158">Die folgende Gleichung skaliert den Punkt (x, y, z) um beliebige Werte in der x-, y-und z-Richtung zu einem neuen Punkt (x ', y ', z ').</span><span class="sxs-lookup"><span data-stu-id="37f32-158">The following equation scales the point (x, y, z) by arbitrary values in the x-, y-, and z-directions to a new point (x', y', z').</span></span>

![Gleichung einer Skalierungs Matrix für einen neuen Punkt](images/matscale.png)

## <a name="rotate"></a><span data-ttu-id="37f32-160">Rotate</span><span class="sxs-lookup"><span data-stu-id="37f32-160">Rotate</span></span>

<span data-ttu-id="37f32-161">Die hier beschriebenen Transformationen gelten für Links gesteuerte Koordinatensysteme und können sich daher von Transformations Matrizen unterscheiden, die Sie an anderer Stelle gesehen haben.</span><span class="sxs-lookup"><span data-stu-id="37f32-161">The transforms described here are for left-handed coordinate systems, and so may be different from transform matrices that you have seen elsewhere.</span></span>

<span data-ttu-id="37f32-162">Die folgende Gleichung dreht den Punkt (x, y, z) um die x-Achse und erzeugt einen neuen Punkt (x ', y ', z ').</span><span class="sxs-lookup"><span data-stu-id="37f32-162">The following equation rotates the point (x, y, z) around the x-axis, producing a new point (x', y', z').</span></span>

![Gleichung einer x-Rotations Matrix für einen neuen Punkt](images/matxrot.png)

<span data-ttu-id="37f32-164">Die folgende Gleichung dreht den Punkt um die y-Achse.</span><span class="sxs-lookup"><span data-stu-id="37f32-164">The following equation rotates the point around the y-axis.</span></span>

![Gleichung einer y-Rotations Matrix für einen neuen Punkt](images/matyrot.png)

<span data-ttu-id="37f32-166">Die folgende Gleichung dreht den Punkt um die z-Achse.</span><span class="sxs-lookup"><span data-stu-id="37f32-166">The following equation rotates the point around the z-axis.</span></span>

![Gleichung einer z-Rotations Matrix für einen neuen Punkt](images/matzrot.png)

<span data-ttu-id="37f32-168">In diesen Beispiel Matrizen steht der griechische Buchstabe der TA für den Drehwinkel im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="37f32-168">In these example matrices, the Greek letter theta stands for the angle of rotation, in radians.</span></span> <span data-ttu-id="37f32-169">Winkel werden im Uhrzeigersinn gemessen, wenn Sie entlang der Drehungs Achse zum Ursprung suchen.</span><span class="sxs-lookup"><span data-stu-id="37f32-169">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

<span data-ttu-id="37f32-170">Verwenden Sie in einer C++-Anwendung die [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md)-, [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)-und [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) -Funktionen, die von der D3DX Utility Library bereitgestellt werden, um Rotations Matrizen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="37f32-170">In a C++ application, use the [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md), and [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) functions supplied by the D3DX utility library to create rotation matrices.</span></span> <span data-ttu-id="37f32-171">Im folgenden finden Sie den Code für die **D3DXMatrixRotationX** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="37f32-171">The following is the code for the **D3DXMatrixRotationX** function.</span></span>


```
D3DXMATRIX* WINAPI D3DXMatrixRotationX
    ( D3DXMATRIX *pOut, float angle )
{
#if DBG
    if(!pOut)
        return NULL;
#endif

    float sin, cos;
    sincosf(angle, &sin, &cos);  // Determine sin and cos of angle

    pOut->_11 = 1.0f; pOut->_12 =  0.0f;   pOut->_13 = 0.0f; pOut->_14 = 0.0f;
    pOut->_21 = 0.0f; pOut->_22 =  cos;    pOut->_23 = sin;  pOut->_24 = 0.0f;
    pOut->_31 = 0.0f; pOut->_32 = -sin;    pOut->_33 = cos;  pOut->_34 = 0.0f;
    pOut->_41 = 0.0f; pOut->_42 =  0.0f;   pOut->_43 = 0.0f; pOut->_44 = 1.0f;

    return pOut;
}
```



## <a name="concatenating-matrices"></a><span data-ttu-id="37f32-172">Verketten von Matrizen</span><span class="sxs-lookup"><span data-stu-id="37f32-172">Concatenating Matrices</span></span>

<span data-ttu-id="37f32-173">Ein Vorteil der Verwendung von Matrizen besteht darin, dass Sie die Auswirkungen von zwei oder mehr Matrizen kombinieren können, indem Sie diese multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="37f32-173">One advantage of using matrices is that you can combine the effects of two or more matrices by multiplying them.</span></span> <span data-ttu-id="37f32-174">Dies bedeutet, dass Sie keine zwei Matrizen anwenden müssen, um ein Modell zu drehen und es dann an einen Speicherort zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="37f32-174">This means that, to rotate a model and then translate it to some location, you don't need to apply two matrices.</span></span> <span data-ttu-id="37f32-175">Stattdessen multiplizieren Sie die Drehung und die Übersetzungs Matrizen, um eine zusammengesetzte Matrix zu erzeugen, die all ihre Auswirkungen enthält.</span><span class="sxs-lookup"><span data-stu-id="37f32-175">Instead, you multiply the rotation and translation matrices to produce a composite matrix that contains all their effects.</span></span> <span data-ttu-id="37f32-176">Dieser Prozess, der als Matrix Verkettung bezeichnet wird, kann mit der folgenden Gleichung geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="37f32-176">This process, called matrix concatenation, can be written with the following equation.</span></span>

![Gleichung der Matrix Verkettung](images/matrxcat.png)

<span data-ttu-id="37f32-178">In dieser Gleichung ist C die zusammengesetzte Matrix, die erstellt wird, und M ₁ bis MN sind die einzelnen Matrizen.</span><span class="sxs-lookup"><span data-stu-id="37f32-178">In this equation, C is the composite matrix being created, and M₁ through Mₙ are the individual matrices.</span></span> <span data-ttu-id="37f32-179">In den meisten Fällen werden nur zwei oder drei Matrizen verkettet, aber es gibt keine Begrenzung.</span><span class="sxs-lookup"><span data-stu-id="37f32-179">In most cases, only two or three matrices are concatenated, but there is no limit.</span></span>

<span data-ttu-id="37f32-180">Verwenden Sie die [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) -Funktion, um die Matrix Multiplikation auszuführen.</span><span class="sxs-lookup"><span data-stu-id="37f32-180">Use the [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) function to perform matrix multiplication.</span></span>

<span data-ttu-id="37f32-181">Die Reihenfolge, in der die Matrix Multiplikation durchgeführt wird, ist entscheidend.</span><span class="sxs-lookup"><span data-stu-id="37f32-181">The order in which the matrix multiplication is performed is crucial.</span></span> <span data-ttu-id="37f32-182">Die vorangehende Formel reflektiert die Regel von links nach rechts der Matrix Verkettung.</span><span class="sxs-lookup"><span data-stu-id="37f32-182">The preceding formula reflects the left-to-right rule of matrix concatenation.</span></span> <span data-ttu-id="37f32-183">Das heißt, die sichtbaren Auswirkungen der Matrizen, die Sie zum Erstellen einer zusammengesetzten Matrix verwenden, treten in der Reihenfolge von links nach rechts auf.</span><span class="sxs-lookup"><span data-stu-id="37f32-183">That is, the visible effects of the matrices that you use to create a composite matrix occur in left-to-right order.</span></span> <span data-ttu-id="37f32-184">Im folgenden Beispiel wird eine typische Weltmatrix gezeigt.</span><span class="sxs-lookup"><span data-stu-id="37f32-184">A typical world matrix is shown in the following example.</span></span> <span data-ttu-id="37f32-185">Stellen Sie sich vor, dass Sie die Weltmatrix für einen Stereo typischen Flugtyp erstellen.</span><span class="sxs-lookup"><span data-stu-id="37f32-185">Imagine that you are creating the world matrix for a stereotypical flying saucer.</span></span> <span data-ttu-id="37f32-186">Vielleicht möchten Sie den fliegenden Schlauch um seine Mitte drehen, die y-Achse des Modell Raums, und ihn an eine andere Stelle in Ihrer Szene übersetzen.</span><span class="sxs-lookup"><span data-stu-id="37f32-186">You would probably want to spin the flying saucer around its center - the y-axis of model space - and translate it to some other location in your scene.</span></span> <span data-ttu-id="37f32-187">Um diesen Effekt zu erreichen, erstellen Sie zunächst eine Rotations Matrix und multiplizieren Sie dann mit einer Übersetzungs Matrix, wie in der folgenden Gleichung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="37f32-187">To accomplish this effect, you first create a rotation matrix, and then multiply it by a translation matrix, as shown in the following equation.</span></span>

![Gleichung der Drehung basierend auf einer Rotations Matrix und einer Übersetzungs Matrix](images/wrldexpl.png)

<span data-ttu-id="37f32-189">In dieser Formel ist R<sub>y</sub> eine Matrix für die Drehung der y-Achse, und T<sub>w</sub> ist eine Übersetzung an eine Position in globalen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="37f32-189">In this formula, R<sub>y</sub> is a matrix for rotation about the y-axis, and T<sub>w</sub> is a translation to some position in world coordinates.</span></span>

<span data-ttu-id="37f32-190">Die Reihenfolge, in der Sie die Matrizen multiplizieren, ist wichtig, da im Gegensatz zu multiplizieren zweier Skalarwerte die Matrix Multiplikation nicht commutativ ist.</span><span class="sxs-lookup"><span data-stu-id="37f32-190">The order in which you multiply the matrices is important because, unlike multiplying two scalar values, matrix multiplication is not commutative.</span></span> <span data-ttu-id="37f32-191">Das Multiplizieren der Matrizen in umgekehrter Reihenfolge hat den visuellen Effekt, dass der fliegende Unterbereich in seine Welt Raum Position übersetzt und dann um den Ursprung der Welt gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="37f32-191">Multiplying the matrices in the opposite order has the visual effect of translating the flying saucer to its world space position, and then rotating it around the world origin.</span></span>

<span data-ttu-id="37f32-192">Unabhängig von der Art der Matrix, die Sie erstellen, merken Sie sich die Regel von links nach rechts, um sicherzustellen, dass Sie die erwarteten Auswirkungen erzielen.</span><span class="sxs-lookup"><span data-stu-id="37f32-192">No matter what type of matrix you are creating, remember the left-to-right rule to ensure that you achieve the expected effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37f32-193">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="37f32-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37f32-194">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="37f32-194">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



