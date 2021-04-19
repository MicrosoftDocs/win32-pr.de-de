---
title: Plane-Struktur (windowsnumerics. h)
description: Diese Struktur stellt eine Ebene mit einem 3D-Vektor normal und einem Entfernungs Wert dar.
ms.assetid: 3C5A5EA0-8A51-4F9B-A84A-0C8E726CE3FD
keywords:
- Plane-Struktur
topic_type:
- apiref
api_name:
- plane structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d870e2769121b4aec542235081011406e439d579
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359797"
---
# <a name="plane-structure"></a><span data-ttu-id="2d663-104">Plane-Struktur</span><span class="sxs-lookup"><span data-stu-id="2d663-104">plane structure</span></span>

<span data-ttu-id="2d663-105">Diese Struktur stellt eine Ebene mit einem 3D-Vektor normal und einem Entfernungs Wert dar.</span><span class="sxs-lookup"><span data-stu-id="2d663-105">This structure represents a plane using a 3D vector normal and a distance value.</span></span>

<span data-ttu-id="2d663-106">Dieser Typ ist nur in C++ verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2d663-106">This type is available only in C++.</span></span> <span data-ttu-id="2d663-107">Die .NET-Entsprechung ist [System. Numerics. Plane](/dotnet/api/system.numerics.plane?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="2d663-107">Its .NET equivalent is [System.Numerics.Plane](/dotnet/api/system.numerics.plane?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="2d663-108">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="2d663-108">Constructors</span></span>

| <span data-ttu-id="2d663-109">Name</span><span class="sxs-lookup"><span data-stu-id="2d663-109">Name</span></span> | <span data-ttu-id="2d663-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d663-110">Description</span></span> |
|-|-|
| `plane()` | <span data-ttu-id="2d663-111">Erstellt eine nicht initialisierte Ebene.</span><span class="sxs-lookup"><span data-stu-id="2d663-111">Creates an uninitialized plane.</span></span> |
| `plane(float x, float y, float z, float d)` | <span data-ttu-id="2d663-112">Erstellt eine Ebene mit den angegebenen Werten.</span><span class="sxs-lookup"><span data-stu-id="2d663-112">Creates a plane with the specified values.</span></span> |
| `plane(float3 normal, float d)` | <span data-ttu-id="2d663-113">Erstellt eine Ebene aus einem float3 und einer Entfernung.</span><span class="sxs-lookup"><span data-stu-id="2d663-113">Creates a plane from a float3 and a distance.</span></span> |
| `explicit plane(float4 value)` | <span data-ttu-id="2d663-114">Erstellt eine Ebene aus einer float4.</span><span class="sxs-lookup"><span data-stu-id="2d663-114">Creates a plane from a float4.</span></span> |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | <span data-ttu-id="2d663-115">Konvertiert eine **Microsoft. Graphics. Canvas. Numerics. Plane** in eine Ebene.</span><span class="sxs-lookup"><span data-stu-id="2d663-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Plane** to a plane.</span></span> |

## <a name="functions"></a><span data-ttu-id="2d663-116">Functions</span><span class="sxs-lookup"><span data-stu-id="2d663-116">Functions</span></span>

| <span data-ttu-id="2d663-117">Name</span><span class="sxs-lookup"><span data-stu-id="2d663-117">Name</span></span> | <span data-ttu-id="2d663-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d663-118">Description</span></span> |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | <span data-ttu-id="2d663-119">Erstellt eine Ebene aus einem Satz von drei Scheitelpunkt Positionen, die sich alle unterscheiden und sich nicht in einer geraden Linie befinden müssen.</span><span class="sxs-lookup"><span data-stu-id="2d663-119">Creates a plane from a set of three vertex positions, which must all be different and not in a straight line.</span></span> |
| `plane normalize(plane const& value)` | <span data-ttu-id="2d663-120">Ändert die Koeffizienten des normalen Vektors einer Ebene, um diese auf die Einheitslänge zu legen.</span><span class="sxs-lookup"><span data-stu-id="2d663-120">Changes the coefficients of the normal vector of a plane to make it of unit length.</span></span> |
| `plane transform(plane const& plane, float4x4 const& matrix)` | <span data-ttu-id="2d663-121">Transformiert eine normalisierte Ebene durch eine Matrix.</span><span class="sxs-lookup"><span data-stu-id="2d663-121">Transforms a normalized plane by a matrix.</span></span> |
| `plane transform(plane const& plane, quaternion const& rotation)` | <span data-ttu-id="2d663-122">Transformiert eine normalisierte Ebene durch eine quaternionrotation.</span><span class="sxs-lookup"><span data-stu-id="2d663-122">Transforms a normalized plane by a quaternion rotation.</span></span> |
| `float dot(plane const& plane, float4 const& value)` | <span data-ttu-id="2d663-123">Berechnet das Punktprodukt einer Ebene mit einem Vektor.</span><span class="sxs-lookup"><span data-stu-id="2d663-123">Calculates the dot product of a plane with a vector.</span></span> |
| `float dot_coordinate(plane const& plane, float3 const& value)` | <span data-ttu-id="2d663-124">Berechnet das Punktprodukt einer Ebene mit einer float3-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="2d663-124">Calculates the dot product of a plane with a float3 coordinate.</span></span> <span data-ttu-id="2d663-125">Anders als bei Punkt \_ Normal umfasst diese Berechnung den Wert der Ebene d.</span><span class="sxs-lookup"><span data-stu-id="2d663-125">Unlike dot\_normal, this computation includes the plane d value.</span></span> |
| `float dot_normal(plane const& plane, float3 const& value)` | <span data-ttu-id="2d663-126">Berechnet das Punktprodukt einer Ebene mit einer float3 normal.</span><span class="sxs-lookup"><span data-stu-id="2d663-126">Calculates the dot product of a plane with a float3 normal.</span></span> <span data-ttu-id="2d663-127">Anders als bei \_ der Punkt Koordinate ignoriert diese Berechnung den Wert der Ebene d.</span><span class="sxs-lookup"><span data-stu-id="2d663-127">Unlike dot\_coordinate, this computation ignores the plane d value.</span></span> |

## <a name="operators"></a><span data-ttu-id="2d663-128">Operatoren</span><span class="sxs-lookup"><span data-stu-id="2d663-128">Operators</span></span>

| <span data-ttu-id="2d663-129">Name</span><span class="sxs-lookup"><span data-stu-id="2d663-129">Name</span></span> | <span data-ttu-id="2d663-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d663-130">Description</span></span> |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | <span data-ttu-id="2d663-131">Bestimmt, ob zwei Instanzen der Ebene gleich sind.</span><span class="sxs-lookup"><span data-stu-id="2d663-131">Determines whether two instances of plane are equal.</span></span> |
| `bool operator!= (plane const& value1, plane const& value2)` | <span data-ttu-id="2d663-132">Bestimmt, ob zwei Instanzen der Ebene nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="2d663-132">Determines whether two instances of plane are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | <span data-ttu-id="2d663-133">Konvertiert eine Ebene in eine **Microsoft. Graphics. Canvas. Numerics. Plane**.</span><span class="sxs-lookup"><span data-stu-id="2d663-133">Converts a plane to a **Microsoft.Graphics.Canvas.Numerics.Plane**.</span></span> |

## <a name="fields"></a><span data-ttu-id="2d663-134">Felder</span><span class="sxs-lookup"><span data-stu-id="2d663-134">Fields</span></span>

| <span data-ttu-id="2d663-135">Name</span><span class="sxs-lookup"><span data-stu-id="2d663-135">Name</span></span> | <span data-ttu-id="2d663-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d663-136">Description</span></span> |
|-|-|
| `float3 normal` | <span data-ttu-id="2d663-137">Normaler Vektor der Ebene.</span><span class="sxs-lookup"><span data-stu-id="2d663-137">Normal vector of the plane.</span></span> |
| `float d` | <span data-ttu-id="2d663-138">Abstand der Ebene entlang ihrer normalen vom Ursprung.</span><span class="sxs-lookup"><span data-stu-id="2d663-138">Distance of the plane along its normal from the origin.</span></span> |

## <a name="requirements"></a><span data-ttu-id="2d663-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d663-139">Requirements</span></span>

| <span data-ttu-id="2d663-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d663-140">Requirement</span></span> | <span data-ttu-id="2d663-141">Wert</span><span class="sxs-lookup"><span data-stu-id="2d663-141">Value</span></span> |
|-|-|
| <span data-ttu-id="2d663-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d663-142">Namespace</span></span> | <span data-ttu-id="2d663-143">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="2d663-143">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="2d663-144">Header</span><span class="sxs-lookup"><span data-stu-id="2d663-144">Header</span></span> | <dl> <span data-ttu-id="2d663-145"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d663-145"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="2d663-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d663-146">See also</span></span>

[<span data-ttu-id="2d663-147">windowsnumerics. h-APIs</span><span class="sxs-lookup"><span data-stu-id="2d663-147">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
