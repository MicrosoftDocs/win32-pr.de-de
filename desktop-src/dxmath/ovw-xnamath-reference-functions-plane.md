---
description: Listet die von directxmath bereitgestellten Ebenenfunktionen auf.
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: Directxmath-Bibliotheks Ebenen-Funktionen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b3f450b4dbaa5ed1b4348ad8b090210c14e2022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356589"
---
# <a name="directxmath-library-plane-functions"></a><span data-ttu-id="34cbe-103">Directxmath-Bibliotheks Ebenen-Funktionen</span><span class="sxs-lookup"><span data-stu-id="34cbe-103">DirectXMath Library plane functions</span></span>

<span data-ttu-id="34cbe-104">Listet die von directxmath bereitgestellten Ebenenfunktionen auf.</span><span class="sxs-lookup"><span data-stu-id="34cbe-104">Lists the plane functions provided by DirectXMath.</span></span>

<span data-ttu-id="34cbe-105">Diese Funktionen verwenden einen xmvector 4-Vector zur Darstellung der Koeffizienten der ebenengleichung, AX + durch + CZ + D = 0, wobei die X-Komponente ist, die Y-Komponente B, die Z-Komponente C und die W-Komponente D ist.</span><span class="sxs-lookup"><span data-stu-id="34cbe-105">These functions use an XMVECTOR 4-vector to represent the coefficients of the plane equation, Ax+By+Cz+D = 0, where the X-component is A, the Y-component is B, the Z-component is C, and the W-component is D.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="34cbe-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="34cbe-106">In this section</span></span>



| <span data-ttu-id="34cbe-107">Thema</span><span class="sxs-lookup"><span data-stu-id="34cbe-107">Topic</span></span>                                                               | <span data-ttu-id="34cbe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34cbe-108">Description</span></span>                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34cbe-109">**Xmplanedot**</span><span class="sxs-lookup"><span data-stu-id="34cbe-109">**XMPlaneDot**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | <span data-ttu-id="34cbe-110">Berechnet das Punktprodukt zwischen einer Eingabe Ebene und einem 4D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="34cbe-110">Calculates the dot product between an input plane and a 4D vector.</span></span><br/>                                    |
| [<span data-ttu-id="34cbe-111">**Xmplanedotcoord**</span><span class="sxs-lookup"><span data-stu-id="34cbe-111">**XMPlaneDotCoord**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | <span data-ttu-id="34cbe-112">Berechnet das Punktprodukt zwischen einer Eingabe Ebene und einem 3D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="34cbe-112">Calculates the dot product between an input plane and a 3D vector.</span></span><br/>                                    |
| [<span data-ttu-id="34cbe-113">**Xmplanedotnormal**</span><span class="sxs-lookup"><span data-stu-id="34cbe-113">**XMPlaneDotNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | <span data-ttu-id="34cbe-114">Berechnet das Punktprodukt zwischen dem normalen Vektor einer Ebene und einem 3D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="34cbe-114">Calculates the dot product between the normal vector of a plane and a 3D vector.</span></span><br/>                      |
| [<span data-ttu-id="34cbe-115">**Xmplaneequal**</span><span class="sxs-lookup"><span data-stu-id="34cbe-115">**XMPlaneEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | <span data-ttu-id="34cbe-116">Bestimmt, ob zwei Ebenen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="34cbe-116">Determines if two planes are equal.</span></span><br/>                                                                   |
| [<span data-ttu-id="34cbe-117">**Xmplanefrompointnormal**</span><span class="sxs-lookup"><span data-stu-id="34cbe-117">**XMPlaneFromPointNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | <span data-ttu-id="34cbe-118">Berechnet die Gleichung einer Ebene, die von einem Punkt in der Ebene und einem normalen Vektor erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="34cbe-118">Computes the equation of a plane constructed from a point in the plane and a normal vector.</span></span><br/>           |
| [<span data-ttu-id="34cbe-119">**Xmplanefrompoints**</span><span class="sxs-lookup"><span data-stu-id="34cbe-119">**XMPlaneFromPoints**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | <span data-ttu-id="34cbe-120">Berechnet die Gleichung einer Ebene, die aus drei Punkten in der Ebene erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="34cbe-120">Computes the equation of a plane constructed from three points in the plane.</span></span><br/>                          |
| [<span data-ttu-id="34cbe-121">**Xmplaneintersectline**</span><span class="sxs-lookup"><span data-stu-id="34cbe-121">**XMPlaneIntersectLine**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | <span data-ttu-id="34cbe-122">Sucht die Schnittmenge zwischen einer Ebene und einer Linie.</span><span class="sxs-lookup"><span data-stu-id="34cbe-122">Finds the intersection between a plane and a line.</span></span><br/>                                                    |
| [<span data-ttu-id="34cbe-123">**Xmplaneingabe tersectplane**</span><span class="sxs-lookup"><span data-stu-id="34cbe-123">**XMPlaneIntersectPlane**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | <span data-ttu-id="34cbe-124">Sucht die Schnittmenge von zwei Ebenen.</span><span class="sxs-lookup"><span data-stu-id="34cbe-124">Finds the intersection of two planes.</span></span><br/>                                                                 |
| [<span data-ttu-id="34cbe-125">**Xmplaneisinfinite**</span><span class="sxs-lookup"><span data-stu-id="34cbe-125">**XMPlaneIsInfinite**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | <span data-ttu-id="34cbe-126">Testet, ob eine der Koeffizienten einer Ebene positiv oder minus unendlich ist.</span><span class="sxs-lookup"><span data-stu-id="34cbe-126">Tests whether any of the coefficients of a plane is positive or negative infinity.</span></span><br/>                    |
| [<span data-ttu-id="34cbe-127">**Xmplaneisnan**</span><span class="sxs-lookup"><span data-stu-id="34cbe-127">**XMPlaneIsNaN**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | <span data-ttu-id="34cbe-128">Testet, ob eine der Koeffizienten einer Ebene ein NaN ist.</span><span class="sxs-lookup"><span data-stu-id="34cbe-128">Tests whether any of the coefficients of a plane is a NaN.</span></span><br/>                                            |
| [<span data-ttu-id="34cbe-129">**Xmplanenearequal**</span><span class="sxs-lookup"><span data-stu-id="34cbe-129">**XMPlaneNearEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | <span data-ttu-id="34cbe-130">Bestimmt, ob zwei Ebenen fast gleich sind.</span><span class="sxs-lookup"><span data-stu-id="34cbe-130">Determines whether two planes are nearly equal.</span></span><br/>                                                       |
| [<span data-ttu-id="34cbe-131">**XMPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="34cbe-131">**XMPlaneNormalize**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | <span data-ttu-id="34cbe-132">Normalisiert die Koeffizienten einer Ebene, sodass Koeffizienten von x, y und z einen Einheiten normalen Vektor bilden.</span><span class="sxs-lookup"><span data-stu-id="34cbe-132">Normalizes the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/> |
| [<span data-ttu-id="34cbe-133">**XMPlaneNormalizeEst**</span><span class="sxs-lookup"><span data-stu-id="34cbe-133">**XMPlaneNormalizeEst**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | <span data-ttu-id="34cbe-134">Schätzt die Koeffizienten einer Ebene, sodass Koeffizienten von x, y und z einen Einheiten normalen Vektor bilden.</span><span class="sxs-lookup"><span data-stu-id="34cbe-134">Estimates the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/>  |
| [<span data-ttu-id="34cbe-135">**Xmplanenotequal**</span><span class="sxs-lookup"><span data-stu-id="34cbe-135">**XMPlaneNotEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | <span data-ttu-id="34cbe-136">Bestimmt, ob zwei Ebenen ungleich sind.</span><span class="sxs-lookup"><span data-stu-id="34cbe-136">Determines if two planes are unequal.</span></span><br/>                                                                 |
| [<span data-ttu-id="34cbe-137">**Xmplanetransform**</span><span class="sxs-lookup"><span data-stu-id="34cbe-137">**XMPlaneTransform**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | <span data-ttu-id="34cbe-138">Transformiert eine Ebene um eine bestimmte Matrix.</span><span class="sxs-lookup"><span data-stu-id="34cbe-138">Transforms a plane by a given matrix.</span></span><br/>                                                                 |
| [<span data-ttu-id="34cbe-139">**Xmplanetransformstream**</span><span class="sxs-lookup"><span data-stu-id="34cbe-139">**XMPlaneTransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | <span data-ttu-id="34cbe-140">Transformiert einen Datenstrom von Ebenen durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="34cbe-140">Transforms a stream of planes by a given matrix.</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="34cbe-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34cbe-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34cbe-142">Directxmath-Bibliotheksfunktionen</span><span class="sxs-lookup"><span data-stu-id="34cbe-142">DirectXMath Library Functions</span></span>](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
