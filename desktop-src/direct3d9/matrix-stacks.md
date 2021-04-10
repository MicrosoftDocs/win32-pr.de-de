---
description: Die D3DX Utility Library stellt die ID3DXMATRIXStack-Schnittstelle bereit.
ms.assetid: e3cfb29e-4ef6-4b48-ad6b-f0371f526507
title: Matrix Stapel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d535307fb99d8743b910f2f3f8c6d55e197748e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860318"
---
# <a name="matrix-stacks-direct3d-9"></a><span data-ttu-id="6a62a-103">Matrix Stapel (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6a62a-103">Matrix Stacks (Direct3D 9)</span></span>

<span data-ttu-id="6a62a-104">Die D3DX Utility Library stellt die [**ID3DXMATRIXStack**](id3dxmatrixstack.md) -Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="6a62a-104">The D3DX utility library provides the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span> <span data-ttu-id="6a62a-105">Es stellt einen Mechanismus bereit, mit dem Matrizen auf einem Matrix Stapel abgelegt und aus diesem entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="6a62a-105">It supplies a mechanism to enable matrices to be pushed onto and popped off of a matrix stack.</span></span> <span data-ttu-id="6a62a-106">Das Implementieren eines Matrix Stapels ist eine effiziente Möglichkeit zum Nachverfolgen von Matrizen beim Durchlaufen einer Transformations Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="6a62a-106">Implementing a matrix stack is an efficient way to track matrices while traversing a transform hierarchy.</span></span>

<span data-ttu-id="6a62a-107">Die D3DX Utility Library verwendet einen Matrix Stapel zum Speichern von Transformationen als Matrizen.</span><span class="sxs-lookup"><span data-stu-id="6a62a-107">The D3DX utility library uses a matrix stack to store transformations as matrices.</span></span> <span data-ttu-id="6a62a-108">Die verschiedenen Methoden der [**ID3DXMATRIXStack**](id3dxmatrixstack.md) -Schnittstelle befassen sich mit der aktuellen Matrix oder der Matrix, die sich über dem Stapel befindet.</span><span class="sxs-lookup"><span data-stu-id="6a62a-108">The various methods of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface deal with the current matrix, or the matrix located on top of the stack.</span></span> <span data-ttu-id="6a62a-109">Sie können die aktuelle Matrix mit der [**ID3DXMATRIXStack:: loadidentity**](id3dxmatrixstack--loadidentity.md) -Methode löschen.</span><span class="sxs-lookup"><span data-stu-id="6a62a-109">You can clear the current matrix with the [**ID3DXMATRIXStack::LoadIdentity**](id3dxmatrixstack--loadidentity.md) method.</span></span> <span data-ttu-id="6a62a-110">Um explizit eine bestimmte Matrix anzugeben, die als aktuelle Transformationsmatrix geladen werden soll, verwenden Sie die [**ID3DXMATRIXStack:: loadmatrix**](id3dxmatrixstack--loadmatrix.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6a62a-110">To explicitly specify a certain matrix to load as the current transformation matrix, use the [**ID3DXMATRIXStack::LoadMatrix**](id3dxmatrixstack--loadmatrix.md) method.</span></span> <span data-ttu-id="6a62a-111">Anschließend können Sie entweder die [**ID3DXMATRIXStack:: mehrtmatrix**](id3dxmatrixstack--multmatrix.md) -Methode oder die [**ID3DXMATRIXStack:: multmatrixlocal**](id3dxmatrixstack--multmatrixlocal.md) -Methode aufzurufen, um die aktuelle Matrix mit der angegebenen Matrix zu multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="6a62a-111">Then you can call either the [**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md) method or the [**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) method to multiply the current matrix by the specified matrix.</span></span>

<span data-ttu-id="6a62a-112">Die [**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md) -Methode ermöglicht es Ihnen, zur vorherigen Transformationsmatrix zurückzukehren, und die [**ID3DXMATRIXStack::P USH**](id3dxmatrixstack--push.md) -Methode fügt dem Stapel eine Transformationsmatrix hinzu.</span><span class="sxs-lookup"><span data-stu-id="6a62a-112">The [**ID3DXMATRIXStack::Pop**](id3dxmatrixstack--pop.md) method enables you to return to the previous transformation matrix and the [**ID3DXMATRIXStack::Push**](id3dxmatrixstack--push.md) method adds a transformation matrix to the stack.</span></span>

<span data-ttu-id="6a62a-113">Die einzelnen Matrizen im Matrix Stapel werden als 4 x 4-Matrizen dargestellt, die von der D3DX Utility Library [**D3DXMATRIX**](d3dxmatrix.md) -Struktur definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6a62a-113">The individual matrices on the matrix stack are represented as 4x4 homogeneous matrices, defined by the D3DX utility library [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

<span data-ttu-id="6a62a-114">Die D3DX Utility Library bietet einen Matrix Stapel über ein COM-Objekt (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="6a62a-114">The D3DX utility library provides a matrix stack through a component object model (COM) object.</span></span>

## <a name="implementing-a-scene-hierarchy"></a><span data-ttu-id="6a62a-115">Implementieren einer Szenen Hierarchie</span><span class="sxs-lookup"><span data-stu-id="6a62a-115">Implementing a Scene Hierarchy</span></span>

<span data-ttu-id="6a62a-116">Ein Matrix Stapel vereinfacht die Erstellung von hierarchischen Modellen, in denen komplizierte Objekte aus einer Reihe von einfacheren Objekten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6a62a-116">A matrix stack simplifies the construction of hierarchical models, in which complicated objects are constructed from a series of simpler objects.</span></span>

<span data-ttu-id="6a62a-117">Eine Szene-oder Transformations Hierarchie wird normalerweise durch eine Strukturdaten Struktur dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6a62a-117">A scene, or transform, hierarchy is usually represented by a tree data structure.</span></span> <span data-ttu-id="6a62a-118">Jeder Knoten in der Strukturdaten Struktur enthält eine Matrix.</span><span class="sxs-lookup"><span data-stu-id="6a62a-118">Each node in the tree data structure contains a matrix.</span></span> <span data-ttu-id="6a62a-119">Eine bestimmte Matrix stellt die Änderung in Koordinatensystemen zwischen dem übergeordneten Knoten des Knotens und dem Knoten dar.</span><span class="sxs-lookup"><span data-stu-id="6a62a-119">A particular matrix represents the change in coordinate systems from the node's parent to the node.</span></span> <span data-ttu-id="6a62a-120">Wenn Sie z. b. eine menschliche Arm modellieren, können Sie die Hierarchie implementieren, die in der folgenden Abbildung dargestellt ist.</span><span class="sxs-lookup"><span data-stu-id="6a62a-120">For example, if you are modeling a human arm, you might implement the hierarchy that is shown in the following diagram.</span></span>

![Diagramm der Hierarchie einer menschlichen Arm](images/stack1.png)

<span data-ttu-id="6a62a-122">In dieser Hierarchie platziert die Text Matrix den Text der Welt.</span><span class="sxs-lookup"><span data-stu-id="6a62a-122">In this hierarchy, the Body matrix places the body in the world.</span></span> <span data-ttu-id="6a62a-123">Die Upperarm-Matrix enthält die Drehung der Schulter, die lowerarm-Matrix enthält die Drehung des Bogens, und die Hand Matrix enthält die Drehung des Handgelenks.</span><span class="sxs-lookup"><span data-stu-id="6a62a-123">The UpperArm matrix contains the rotation of the shoulder, the LowerArm matrix contains the rotation of the elbow, and the Hand matrix contains the rotation of the wrist.</span></span> <span data-ttu-id="6a62a-124">Um zu ermitteln, wo sich die Hand in Bezug auf die Welt befindet, Multiplizieren Sie alle Matrizen vom Text nach unten.</span><span class="sxs-lookup"><span data-stu-id="6a62a-124">To determine where the hand is relative to the world, you multiply all the matrices from Body down through Hand together.</span></span>

<span data-ttu-id="6a62a-125">Die vorherige Hierarchie ist übermäßig simpel, da jeder Knoten nur über ein untergeordnetes Element verfügt.</span><span class="sxs-lookup"><span data-stu-id="6a62a-125">The previous hierarchy is overly simplistic, because each node has only one child.</span></span> <span data-ttu-id="6a62a-126">Wenn Sie die Hand ausführlicher modellieren, werden Sie wahrscheinlich Finger und ein Thumb-Steuer Punkt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6a62a-126">If you begin to model the hand in more detail, you will probably add fingers and a thumb.</span></span> <span data-ttu-id="6a62a-127">Jede Ziffer kann der Hierarchie als untergeordnete Elemente hinzugefügt werden, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6a62a-127">Each digit can be added to the hierarchy as children of Hand, as shown in the following diagram.</span></span>

![Diagramm der Hierarchie einer Menschenhand](images/stack2.png)

<span data-ttu-id="6a62a-129">Wenn Sie das vollständige Diagramm des Arm-nach-oben-nach-unten-Reihenfolge durchlaufen, bevor Sie mit dem nächsten Pfad fortfahren, um die Szene zu zeichnen, führen Sie eine Sequenz segmentierter Rendering aus.</span><span class="sxs-lookup"><span data-stu-id="6a62a-129">If you traverse the complete graph of the arm in depth-first order - traversing as far down one path as possible before moving on to the next path - to draw the scene, you perform a sequence of segmented rendering.</span></span> <span data-ttu-id="6a62a-130">Um z. b. die Hand und die Finger zu erzeugen, implementieren Sie das folgende Muster.</span><span class="sxs-lookup"><span data-stu-id="6a62a-130">For example, to render the hand and fingers, you implement the following pattern.</span></span>

1.  <span data-ttu-id="6a62a-131">Überträgt die Hand Matrix auf den Matrix Stapel.</span><span class="sxs-lookup"><span data-stu-id="6a62a-131">Push the Hand matrix onto the matrix stack.</span></span>
2.  <span data-ttu-id="6a62a-132">Zeichnen Sie die Hand.</span><span class="sxs-lookup"><span data-stu-id="6a62a-132">Draw the hand.</span></span>
3.  <span data-ttu-id="6a62a-133">Übertragung der Ziehpunkt Matrix auf den Matrix Stapel.</span><span class="sxs-lookup"><span data-stu-id="6a62a-133">Push the Thumb matrix onto the matrix stack.</span></span>
4.  <span data-ttu-id="6a62a-134">Ziehen Sie den Ziehpunkt.</span><span class="sxs-lookup"><span data-stu-id="6a62a-134">Draw the thumb.</span></span>
5.  <span data-ttu-id="6a62a-135">Blättern Sie die Ziehpunkt Matrix aus dem Stapel.</span><span class="sxs-lookup"><span data-stu-id="6a62a-135">Pop the Thumb matrix off the stack.</span></span>
6.  <span data-ttu-id="6a62a-136">Übertragung der Finger 1-Matrix auf den Matrix Stapel.</span><span class="sxs-lookup"><span data-stu-id="6a62a-136">Push the Finger 1 matrix onto the matrix stack.</span></span>
7.  <span data-ttu-id="6a62a-137">Zeichnen Sie den ersten Finger.</span><span class="sxs-lookup"><span data-stu-id="6a62a-137">Draw the first finger.</span></span>
8.  <span data-ttu-id="6a62a-138">Schalten Sie die Finger 1-Matrix aus dem Stapel.</span><span class="sxs-lookup"><span data-stu-id="6a62a-138">Pop the Finger 1 matrix off the stack.</span></span>
9.  <span data-ttu-id="6a62a-139">Übertragung der Finger 2-Matrix auf den Matrix Stapel.</span><span class="sxs-lookup"><span data-stu-id="6a62a-139">Push the Finger 2 matrix onto the matrix stack.</span></span> <span data-ttu-id="6a62a-140">Sie werden auf diese Weise fortgesetzt, bis alle Finger und Thumb gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="6a62a-140">You continue in this manner until all the fingers and thumb are rendered.</span></span>

<span data-ttu-id="6a62a-141">Nachdem Sie das Rendering der Finger abgeschlossen haben, würden Sie die Hand Matrix aus dem Stapel aufklappen.</span><span class="sxs-lookup"><span data-stu-id="6a62a-141">After you have completed rendering the fingers, you would pop the Hand matrix off the stack.</span></span>

<span data-ttu-id="6a62a-142">Sie können diesen grundlegenden Prozess in Code mit den folgenden Beispielen ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a62a-142">You can follow this basic process in code with the following examples.</span></span> <span data-ttu-id="6a62a-143">Wenn während der tiefen Suche der Strukturdaten Struktur ein Knoten angezeigt wird, verschieben Sie die Matrix an den oberen Rand des Matrix Stapels.</span><span class="sxs-lookup"><span data-stu-id="6a62a-143">When you encounter a node during the depth-first search of the tree data structure, push the matrix onto the top of the matrix stack.</span></span>


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



<span data-ttu-id="6a62a-144">Wenn Sie mit einem Knoten fertig sind, können Sie die Matrix am oberen Rand des Matrix Stapels aufklappen.</span><span class="sxs-lookup"><span data-stu-id="6a62a-144">When you are finished with a node, pop the matrix off the top of the matrix stack.</span></span>


```
MatrixStack->Pop();
```



<span data-ttu-id="6a62a-145">Auf diese Weise stellt die Matrix am Anfang des Stapels immer die weltweite Transformation des aktuellen Knotens dar.</span><span class="sxs-lookup"><span data-stu-id="6a62a-145">In this way, the matrix on the top of the stack always represents the world-transform of the current node.</span></span> <span data-ttu-id="6a62a-146">Vor dem Zeichnen der einzelnen Knoten sollten Sie daher die Direct3D-Matrix festlegen.</span><span class="sxs-lookup"><span data-stu-id="6a62a-146">Therefore, before drawing each node, you should set the Direct3D matrix.</span></span>


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



<span data-ttu-id="6a62a-147">Weitere Informationen zu den spezifischen Methoden, die Sie für einen D3DX-Matrix Stapel ausführen können, finden Sie im [**ID3DXMATRIXStack**](id3dxmatrixstack.md) Reference Topic.</span><span class="sxs-lookup"><span data-stu-id="6a62a-147">For more information about the specific methods that you can perform on a D3DX matrix stack, see the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) reference topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a62a-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6a62a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a62a-149">Scheitelpunkt Pipeline</span><span class="sxs-lookup"><span data-stu-id="6a62a-149">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 



