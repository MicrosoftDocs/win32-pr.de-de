---
description: In diesem Abschnitt werden die grundlegenden Konzepte der Ansichts Transformation vorgestellt, und es wird erläutert, wie Sie eine Ansichts Transformationsmatrix in einer Direct3D-Anwendung einrichten.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Transformation anzeigen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf933db7424b2c3aeb5aa7c06a37b03782eaa6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521907"
---
# <a name="view-transform-direct3d-9"></a><span data-ttu-id="7c337-103">Transformation anzeigen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7c337-103">View Transform (Direct3D 9)</span></span>

<span data-ttu-id="7c337-104">In diesem Abschnitt werden die grundlegenden Konzepte der Ansichts Transformation vorgestellt, und es wird erläutert, wie Sie eine Ansichts Transformationsmatrix in einer Direct3D-Anwendung einrichten.</span><span class="sxs-lookup"><span data-stu-id="7c337-104">This section introduces the basic concepts of the view transform and provides details on how to set up a view transform matrix in a Direct3D application.</span></span>

<span data-ttu-id="7c337-105">Die Transformation "Ansicht" lokalisiert den Viewer im Raum und wandelt Vertices in den Kamerabereich um.</span><span class="sxs-lookup"><span data-stu-id="7c337-105">The view transform locates the viewer in world space, transforming vertices into camera space.</span></span> <span data-ttu-id="7c337-106">Im Kamerabereich befindet sich die Kamera oder der Viewer am Ursprung und sucht in der positiven z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="7c337-106">In camera space, the camera, or viewer, is at the origin, looking in the positive z-direction.</span></span> <span data-ttu-id="7c337-107">Denken Sie daran, dass Direct3D ein Links händiges Koordinatensystem verwendet, sodass z in einer Szene positiv ist.</span><span class="sxs-lookup"><span data-stu-id="7c337-107">Recall that Direct3D uses a left-handed coordinate system, so z is positive into a scene.</span></span> <span data-ttu-id="7c337-108">In der Sicht Matrix werden die Objekte weltweit um die Position einer Kamera, den Ursprung des Kamera Raums und die Ausrichtung, verschoben.</span><span class="sxs-lookup"><span data-stu-id="7c337-108">The view matrix relocates the objects in the world around a camera's position - the origin of camera space - and orientation.</span></span>

<span data-ttu-id="7c337-109">Es gibt viele Möglichkeiten, eine Ansichts Matrix zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7c337-109">There are many ways to create a view matrix.</span></span> <span data-ttu-id="7c337-110">In allen Fällen hat die Kamera eine logische Position und Orientierung im Raum der Welt, die als Ausgangspunkt verwendet wird, um eine Ansichts Matrix zu erstellen, die auf die Modelle in einer Szene angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c337-110">In all cases, the camera has some logical position and orientation in world space that is used as a starting point to create a view matrix that will be applied to the models in a scene.</span></span> <span data-ttu-id="7c337-111">Die Ansichts Matrix übersetzt und rotiert Objekte, um Sie in den Kamerabereich zu platzieren, in dem sich die Kamera am Ursprung befindet.</span><span class="sxs-lookup"><span data-stu-id="7c337-111">The view matrix translates and rotates objects to place them in camera space, where the camera is at the origin.</span></span> <span data-ttu-id="7c337-112">Eine Möglichkeit zum Erstellen einer Sicht Matrix besteht darin, eine Übersetzungs Matrix mit Rotations Matrizen für jede Achse zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="7c337-112">One way to create a view matrix is to combine a translation matrix with rotation matrices for each axis.</span></span> <span data-ttu-id="7c337-113">Bei dieser Vorgehensweise gilt die folgende allgemeine Matrix Gleichung.</span><span class="sxs-lookup"><span data-stu-id="7c337-113">In this approach, the following general matrix equation applies.</span></span>

![Gleichung der Ansichts Transformation](images/viewtran.png)

<span data-ttu-id="7c337-115">In dieser Formel ist V die Ansichts Matrix, die erstellt wird, T ist eine Übersetzungs Matrix, die Objekte der Welt neu positioniert, und r ₓ bis r<sub>z</sub> sind Rotations Matrizen, die Objekte entlang der x-, y-und z-Achse drehen.</span><span class="sxs-lookup"><span data-stu-id="7c337-115">In this formula, V is the view matrix being created, T is a translation matrix that repositions objects in the world, and Rₓ through R<sub>z</sub> are rotation matrices that rotate objects along the x-, y-, and z-axis.</span></span> <span data-ttu-id="7c337-116">Die Konvertierungs-und Rotations Matrizen basieren auf der logischen Position und Ausrichtung der Kamera im Raum.</span><span class="sxs-lookup"><span data-stu-id="7c337-116">The translation and rotation matrices are based on the camera's logical position and orientation in world space.</span></span> <span data-ttu-id="7c337-117">Wenn die logische Position der Kamera auf der Welt <10, 20100> ist, besteht das Ziel der Übersetzungs Matrix darin, Objekte-10 Einheiten entlang der x-Achse,-20 Einheiten entlang der y-Achse und-100-Einheiten entlang der z-Achse zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="7c337-117">So, if the camera's logical position in the world is <10,20,100>, the aim of the translation matrix is to move objects -10 units along the x-axis, -20 units along the y-axis, and -100 units along the z-axis.</span></span> <span data-ttu-id="7c337-118">Die Rotations Matrizen in der Formel basieren auf der Ausrichtung der Kamera, im Hinblick darauf, wie viel die Achsen des Kamera Raums aus der Ausrichtung mit dem Raum gedreht werden.</span><span class="sxs-lookup"><span data-stu-id="7c337-118">The rotation matrices in the formula are based on the camera's orientation, in terms of how much the axes of camera space are rotated out of alignment with world space.</span></span> <span data-ttu-id="7c337-119">Wenn z. b. die zuvor erwähnte Kamera gerade zeigt, ist die z-Achse 90 Grad (PI/2-Bogenmaß) außerhalb der Ausrichtung auf die z-Achse des Raum Raums, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7c337-119">For example, if the camera mentioned earlier is pointing straight down, its z-axis is 90 degrees (pi/2 radians) out of alignment with the z-axis of world space, as shown in the following illustration.</span></span>

![Darstellung des Anzeige Raums der Kamera im Vergleich zum Raum](images/camtop.png)

<span data-ttu-id="7c337-121">Die Rotations Matrizen wenden Drehungen von gleicher, aber umgekehrter Größe auf die Modelle in der Szene an.</span><span class="sxs-lookup"><span data-stu-id="7c337-121">The rotation matrices apply rotations of equal, but opposite, magnitude to the models in the scene.</span></span> <span data-ttu-id="7c337-122">Die Ansichts Matrix für diese Kamera umfasst eine Drehung von-90 Grad um die x-Achse.</span><span class="sxs-lookup"><span data-stu-id="7c337-122">The view matrix for this camera includes a rotation of -90 degrees around the x-axis.</span></span> <span data-ttu-id="7c337-123">Die Rotations Matrix wird mit der Übersetzungs Matrix kombiniert, um eine Ansichts Matrix zu erstellen, mit der die Position und Ausrichtung der Objekte in der Szene angepasst werden, sodass ihre Oberseite mit der Kamera verknüpft ist. Dadurch wird die Darstellung der Kamera oberhalb des Modells dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7c337-123">The rotation matrix is combined with the translation matrix to create a view matrix that adjusts the position and orientation of the objects in the scene so that their top is facing the camera, giving the appearance that the camera is above the model.</span></span>

## <a name="setting-up-a-view-matrix"></a><span data-ttu-id="7c337-124">Einrichten einer Ansichts Matrix</span><span class="sxs-lookup"><span data-stu-id="7c337-124">Setting Up a View Matrix</span></span>

<span data-ttu-id="7c337-125">Die Hilfsfunktionen [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) und [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) erstellen eine Ansichts Matrix basierend auf der Kameraposition und einem Blickpunkt.</span><span class="sxs-lookup"><span data-stu-id="7c337-125">The [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) and [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) helper functions create a view matrix based on the camera location and a look-at point.</span></span>

<span data-ttu-id="7c337-126">Im folgenden Beispiel wird eine Ansichts Matrix für Links gesteuerte Koordinaten erstellt.</span><span class="sxs-lookup"><span data-stu-id="7c337-126">The following example creates a view matrix for left-handed coordinates.</span></span>


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



<span data-ttu-id="7c337-127">Direct3D verwendet die "World"-und "View"-Matrizen zum Konfigurieren mehrerer interner Datenstrukturen.</span><span class="sxs-lookup"><span data-stu-id="7c337-127">Direct3D uses the world and view matrices to configure several internal data structures.</span></span> <span data-ttu-id="7c337-128">Jedes Mal, wenn Sie eine neue Welt-oder Sicht Matrix festlegen, berechnet das System die zugeordneten internen Strukturen neu.</span><span class="sxs-lookup"><span data-stu-id="7c337-128">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="7c337-129">Das häufige Festlegen dieser Matrizen ist Rechenzeit aufwändig.</span><span class="sxs-lookup"><span data-stu-id="7c337-129">Setting these matrices frequently is computationally time-consuming.</span></span> <span data-ttu-id="7c337-130">Sie können die Anzahl der erforderlichen Berechnungen minimieren, indem Sie Ihre Welt und Matrizen in einer World-View-Matrix verketten, die Sie als Weltmatrix festlegen, und dann die Ansichts Matrix auf die Identität festlegen.</span><span class="sxs-lookup"><span data-stu-id="7c337-130">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="7c337-131">Behalten Sie zwischengespeicherte Kopien der einzelnen Welt bei, und zeigen Sie Matrizen an, die Sie ändern, verketten und die World Matrix nach Bedarf zurücksetzen können.</span><span class="sxs-lookup"><span data-stu-id="7c337-131">Keep cached copies of individual world and view matrices that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="7c337-132">Aus Gründen der Übersichtlichkeit werden diese Optimierungen in den Beispielen selten eingesetzt.</span><span class="sxs-lookup"><span data-stu-id="7c337-132">For clarity, the samples rarely employ this optimization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c337-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7c337-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c337-134">Transformationen</span><span class="sxs-lookup"><span data-stu-id="7c337-134">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 



