---
description: In Direct3D beschreiben Vertices Position und Ausrichtung. Jeder Scheitelpunkt in einem primitiven wird durch einen Vektor beschrieben, der seine Position, Farbe, Texturkoordinaten und einen normalen Vektor übergibt, der seine Ausrichtung ermöglicht.
ms.assetid: f18b235c-97ff-4779-8584-8e96b62c7ca3
title: Vektoren, Vertices und Quaternionen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c2e6e6e316b633359205ffd24a64aa349eeec74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521163"
---
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a><span data-ttu-id="91517-104">Vektoren, Vertices und Quaternionen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="91517-104">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>

<span data-ttu-id="91517-105">In Direct3D beschreiben Vertices Position und Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="91517-105">Throughout Direct3D, vertices describe position and orientation.</span></span> <span data-ttu-id="91517-106">Jeder Scheitelpunkt in einem primitiven wird durch einen Vektor beschrieben, der seine Position, Farbe, Texturkoordinaten und einen normalen Vektor übergibt, der seine Ausrichtung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="91517-106">Each vertex in a primitive is described by a vector that gives its position, color, texture coordinates, and a normal vector that gives its orientation.</span></span>

<span data-ttu-id="91517-107">Quaternionen fügen ein viertes Element zu den \[ x-, y-, z- \] Werten hinzu, die einen drei komponentenvektor definieren.</span><span class="sxs-lookup"><span data-stu-id="91517-107">Quaternions add a fourth element to the \[x, y, z\] values that define a three-component-vector.</span></span> <span data-ttu-id="91517-108">Quaternionen stellen eine Alternative zu den Matrix Methoden dar, die in der Regel für 3D-Drehungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91517-108">Quaternions are an alternative to the matrix methods that are typically used for 3D rotations.</span></span> <span data-ttu-id="91517-109">Eine Quaternion stellt eine Achse im 3D-Raum und eine Drehung um diese Achse dar.</span><span class="sxs-lookup"><span data-stu-id="91517-109">A quaternion represents an axis in 3D space and a rotation around that axis.</span></span> <span data-ttu-id="91517-110">Beispielsweise kann eine Quaternion eine (1, 1, 2) Achse und eine Drehung von einem Radian darstellen.</span><span class="sxs-lookup"><span data-stu-id="91517-110">For example, a quaternion might represent a (1,1,2) axis and a rotation of 1 radian.</span></span> <span data-ttu-id="91517-111">Quaternions enthalten wertvolle Informationen, aber ihre wahre Leistung ergibt sich aus den beiden Vorgängen, die Sie ausführen können: Komposition und interpolung.</span><span class="sxs-lookup"><span data-stu-id="91517-111">Quaternions carry valuable information, but their true power comes from the two operations that you can perform on them: composition and interpolation.</span></span>

<span data-ttu-id="91517-112">Das Durchführen der Komposition in Quaternionen ähnelt dem kombinieren.</span><span class="sxs-lookup"><span data-stu-id="91517-112">Performing composition on quaternions is similar to combining them.</span></span> <span data-ttu-id="91517-113">Die Komposition von zwei Quaternionen ist wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="91517-113">The composition of two quaternions is notated like the following illustration.</span></span>

![Abbildung der Quaternion-Notation](images/quateq.png)

<span data-ttu-id="91517-115">Die Komposition von zwei Quaternionen, die auf eine Geometrie angewendet werden, bedeutet "Drehen der Geometrie um die Achse" durch Drehung, und drehen Sie Sie um die Achse ₁ durch Drehung ₁. "</span><span class="sxs-lookup"><span data-stu-id="91517-115">The composition of two quaternions applied to a geometry means "rotate the geometry around axis₂ by rotation₂, then rotate it around axis₁ by rotation₁."</span></span> <span data-ttu-id="91517-116">In diesem Fall stellt q eine Drehung um eine einzelne Achse dar, die das Ergebnis der Anwendung von q-Wert ist, und dann q ₁ auf die Geometrie.</span><span class="sxs-lookup"><span data-stu-id="91517-116">In this case, Q represents a rotation around a single axis that is the result of applying q₂, then q₁ to the geometry.</span></span>

<span data-ttu-id="91517-117">Mithilfe der Quaternion-interpolung kann eine Anwendung einen Smooth-und einen angemessenen Pfad von einer Achse und eine Ausrichtung auf eine andere berechnen.</span><span class="sxs-lookup"><span data-stu-id="91517-117">Using quaternion interpolation, an application can calculate a smooth and reasonable path from one axis and orientation to another.</span></span> <span data-ttu-id="91517-118">Aus diesem Grund bietet die Interpolationsmethode zwischen q ₁ und q-CO2 eine einfache Möglichkeit, um von einer Ausrichtung zu einer anderen zu animieren.</span><span class="sxs-lookup"><span data-stu-id="91517-118">Therefore, interpolation between q₁ and q₂ provides a simple way to animate from one orientation to another.</span></span>

<span data-ttu-id="91517-119">Wenn Sie Komposition und Interpolationen zusammen verwenden, bieten Sie eine einfache Möglichkeit, um eine Geometrie auf eine komplexe Weise zu manipulieren.</span><span class="sxs-lookup"><span data-stu-id="91517-119">When you use composition and interpolation together, they provide you with a simple way to manipulate a geometry in a manner that appears complex.</span></span> <span data-ttu-id="91517-120">Stellen Sie sich beispielsweise vor, dass Sie über eine Geometrie verfügen, die Sie zu einer bestimmten Ausrichtung drehen möchten.</span><span class="sxs-lookup"><span data-stu-id="91517-120">For example, imagine that you have a geometry that you want to rotate to a given orientation.</span></span> <span data-ttu-id="91517-121">Sie wissen, dass Sie die r-Grad-um-Achse um die Achse umdrehen und dann den Wert r ₁ Grad um Achse ₁ drehen möchten, aber die endgültige Quaternion ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="91517-121">You know that you want to rotate it r₂ degrees around axis₂, then rotate it r₁ degrees around axis₁, but you don't know the final quaternion.</span></span> <span data-ttu-id="91517-122">Mithilfe der Komposition können Sie die beiden Rotationen der Geometrie kombinieren, um eine einzelne Quaternion zu erhalten, die das Ergebnis ist.</span><span class="sxs-lookup"><span data-stu-id="91517-122">By using composition, you could combine the two rotations on the geometry to get a single quaternion that is the result.</span></span> <span data-ttu-id="91517-123">Anschließend könnten Sie von der ursprünglichen zur zusammengesetzten Quaternion interpolieren, um einen reibungslosen Übergang von einem zum anderen zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="91517-123">Then, you could interpolate from the original to the composed quaternion to achieve a smooth transition from one to the other.</span></span>

<span data-ttu-id="91517-124">Die D3DX Utility Library enthält Funktionen, die Ihnen bei der Arbeit mit Quaternionen helfen.</span><span class="sxs-lookup"><span data-stu-id="91517-124">The D3DX utility library includes functions that help you work with quaternions.</span></span> <span data-ttu-id="91517-125">Die [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) -Funktion fügt z. b. einen Rotations Wert zu einem Vektor hinzu, der eine Achse der Drehung definiert, und gibt das Ergebnis in einer Quaternion zurück, die durch eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur definiert ist.</span><span class="sxs-lookup"><span data-stu-id="91517-125">For example, the [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) function adds a rotation value to a vector that defines an axis of rotation, and returns the result in a quaternion defined by a [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span> <span data-ttu-id="91517-126">Außerdem führt die [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) -Funktion Quaternionen aus, und [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) führt eine sphärische lineare interpolung zwischen zwei Quaternionen aus.</span><span class="sxs-lookup"><span data-stu-id="91517-126">Additionally, the [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) function composes quaternions and the [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) performs spherical linear interpolation between two quaternions.</span></span>

<span data-ttu-id="91517-127">Direct3D-Anwendungen können die folgenden Funktionen verwenden, um die Arbeit mit Quaternionen zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="91517-127">Direct3D applications can use the following functions to simplify the task of working with quaternions.</span></span>

-   [<span data-ttu-id="91517-128">**D3DXQuaternionBaryCentric**</span><span class="sxs-lookup"><span data-stu-id="91517-128">**D3DXQuaternionBaryCentric**</span></span>](d3dxquaternionbarycentric.md)
-   [<span data-ttu-id="91517-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="91517-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
-   [<span data-ttu-id="91517-130">**D3DXQuaternionDot**</span><span class="sxs-lookup"><span data-stu-id="91517-130">**D3DXQuaternionDot**</span></span>](d3dxquaterniondot.md)
-   [<span data-ttu-id="91517-131">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="91517-131">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
-   [<span data-ttu-id="91517-132">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="91517-132">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
-   [<span data-ttu-id="91517-133">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="91517-133">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
-   [<span data-ttu-id="91517-134">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="91517-134">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
-   [<span data-ttu-id="91517-135">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="91517-135">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
-   [<span data-ttu-id="91517-136">**D3DXQuaternionLengthSq**</span><span class="sxs-lookup"><span data-stu-id="91517-136">**D3DXQuaternionLengthSq**</span></span>](d3dxquaternionlengthsq.md)
-   [<span data-ttu-id="91517-137">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="91517-137">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
-   [<span data-ttu-id="91517-138">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="91517-138">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
-   [<span data-ttu-id="91517-139">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="91517-139">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
-   [<span data-ttu-id="91517-140">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="91517-140">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
-   [<span data-ttu-id="91517-141">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="91517-141">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
-   [<span data-ttu-id="91517-142">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="91517-142">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
-   [<span data-ttu-id="91517-143">**D3DXQuaternionSlerp**</span><span class="sxs-lookup"><span data-stu-id="91517-143">**D3DXQuaternionSlerp**</span></span>](d3dxquaternionslerp.md)
-   [<span data-ttu-id="91517-144">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="91517-144">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
-   [<span data-ttu-id="91517-145">**D3DXQuaternionToAxisAngle**</span><span class="sxs-lookup"><span data-stu-id="91517-145">**D3DXQuaternionToAxisAngle**</span></span>](d3dxquaterniontoaxisangle.md)

<span data-ttu-id="91517-146">Direct3D-Anwendungen können die folgenden Funktionen verwenden, um die Aufgabe der Arbeit mit drei-Komponenten-Vektoren zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="91517-146">Direct3D applications can use the following functions to simplify the task of working with three-component-vectors.</span></span>

-   [<span data-ttu-id="91517-147">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="91517-147">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
-   [<span data-ttu-id="91517-148">**D3DXVec3BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="91517-148">**D3DXVec3BaryCentric**</span></span>](d3dxvec3barycentric.md)
-   [<span data-ttu-id="91517-149">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="91517-149">**D3DXVec3CatmullRom**</span></span>](d3dxvec3catmullrom.md)
-   [<span data-ttu-id="91517-150">**D3DXVec3Cross**</span><span class="sxs-lookup"><span data-stu-id="91517-150">**D3DXVec3Cross**</span></span>](d3dxvec3cross.md)
-   [<span data-ttu-id="91517-151">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="91517-151">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
-   [<span data-ttu-id="91517-152">**D3DXVec3Hermite**</span><span class="sxs-lookup"><span data-stu-id="91517-152">**D3DXVec3Hermite**</span></span>](d3dxvec3hermite.md)
-   [<span data-ttu-id="91517-153">**D3DXVec3Length**</span><span class="sxs-lookup"><span data-stu-id="91517-153">**D3DXVec3Length**</span></span>](d3dxvec3length.md)
-   [<span data-ttu-id="91517-154">**D3DXVec3LengthSq**</span><span class="sxs-lookup"><span data-stu-id="91517-154">**D3DXVec3LengthSq**</span></span>](d3dxvec3lengthsq.md)
-   [<span data-ttu-id="91517-155">**D3DXVec3Lerp**</span><span class="sxs-lookup"><span data-stu-id="91517-155">**D3DXVec3Lerp**</span></span>](d3dxvec3lerp.md)
-   [<span data-ttu-id="91517-156">**D3DXVec3Maximize**</span><span class="sxs-lookup"><span data-stu-id="91517-156">**D3DXVec3Maximize**</span></span>](d3dxvec3maximize.md)
-   [<span data-ttu-id="91517-157">**D3DXVec3Minimize**</span><span class="sxs-lookup"><span data-stu-id="91517-157">**D3DXVec3Minimize**</span></span>](d3dxvec3minimize.md)
-   [<span data-ttu-id="91517-158">**D3DXVec3Normalize**</span><span class="sxs-lookup"><span data-stu-id="91517-158">**D3DXVec3Normalize**</span></span>](d3dxvec3normalize.md)
-   [<span data-ttu-id="91517-159">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="91517-159">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
-   [<span data-ttu-id="91517-160">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="91517-160">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
-   [<span data-ttu-id="91517-161">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="91517-161">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
-   [<span data-ttu-id="91517-162">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="91517-162">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
-   [<span data-ttu-id="91517-163">**D3DXVec3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="91517-163">**D3DXVec3TransformCoord**</span></span>](d3dxvec3transformcoord.md)
-   [<span data-ttu-id="91517-164">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="91517-164">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
-   [<span data-ttu-id="91517-165">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="91517-165">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)

<span data-ttu-id="91517-166">Viele zusätzliche Funktionen, die Aufgaben mit zwei-und vier-Komponenten-Vektoren vereinfachen, sind in den [mathematischen Funktionen](dx9-graphics-reference-d3dx-functions-math.md) enthalten, die von der D3DX Utility Library bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="91517-166">Many additional functions that simplify tasks using two- and four-component-vectors are included among the [Math Functions](dx9-graphics-reference-d3dx-functions-math.md) supplied by the D3DX utility library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91517-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="91517-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91517-168">Koordinatensysteme und Geometrie</span><span class="sxs-lookup"><span data-stu-id="91517-168">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



