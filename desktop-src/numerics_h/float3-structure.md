---
title: float3-Struktur (windowsnumerics. h)
description: Ein Vektor mit drei Komponenten.
ms.assetid: CAA10ADA-C5A8-4B75-A0A9-5C5B3FDD9A07
keywords:
- float3-Struktur
topic_type:
- apiref
api_name:
- float3 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae524205c900c63438a50094dcd551a4903632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365657"
---
# <a name="float3-structure"></a><span data-ttu-id="ddf34-104">float3-Struktur</span><span class="sxs-lookup"><span data-stu-id="ddf34-104">float3 structure</span></span>

<span data-ttu-id="ddf34-105">Ein Vektor mit drei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="ddf34-105">A vector with three components.</span></span>

<span data-ttu-id="ddf34-106">Dieser Typ ist nur in C++ verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ddf34-106">This type is available only in C++.</span></span> <span data-ttu-id="ddf34-107">Die .NET-Entsprechung ist [System. Numerics. Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="ddf34-107">Its .NET equivalent is [System.Numerics.Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="ddf34-108">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="ddf34-108">Constructors</span></span>

| <span data-ttu-id="ddf34-109">Name</span><span class="sxs-lookup"><span data-stu-id="ddf34-109">Name</span></span> | <span data-ttu-id="ddf34-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddf34-110">Description</span></span> |
|-|-|
| `float3()` | <span data-ttu-id="ddf34-111">Erstellt ein nicht initialisiertes float3-.</span><span class="sxs-lookup"><span data-stu-id="ddf34-111">Creates an uninitialized float3.</span></span> |
| `float3(float x, float y, float z)` | <span data-ttu-id="ddf34-112">Erstellt eine float3 mit den angegebenen Werten.</span><span class="sxs-lookup"><span data-stu-id="ddf34-112">Creates a float3 with the specified values.</span></span> |
| `float3(float2 value, float z)` | <span data-ttu-id="ddf34-113">Erstellt ein float3 mit x und y, das aus einem float2 plus dem angegebenen z-Wert kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ddf34-113">Creates a float3 with x and y copied from a float2 plus the specified z value.</span></span> |
| `explicit float3(float value)` | <span data-ttu-id="ddf34-114">Erstellt eine float3, bei der alle Komponenten auf den angegebenen Wert festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="ddf34-114">Creates a float3 with all components set to the specified value.</span></span> |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | <span data-ttu-id="ddf34-115">Konvertiert eine **Microsoft. Graphics. Canvas. Numerics. Vector3** in eine float3.</span><span class="sxs-lookup"><span data-stu-id="ddf34-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector3** to a float3.</span></span> |

## <a name="functions"></a><span data-ttu-id="ddf34-116">Functions</span><span class="sxs-lookup"><span data-stu-id="ddf34-116">Functions</span></span>

| <span data-ttu-id="ddf34-117">Name</span><span class="sxs-lookup"><span data-stu-id="ddf34-117">Name</span></span> | <span data-ttu-id="ddf34-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddf34-118">Description</span></span> |
|-|-|
| `float length(float3 const& value)` | <span data-ttu-id="ddf34-119">Berechnet die Länge des Vektors (bzw. euklidische Entfernung).</span><span class="sxs-lookup"><span data-stu-id="ddf34-119">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float3 const& value)` | <span data-ttu-id="ddf34-120">Berechnet die Länge oder den euklidischen Abstand des Vektor Quadrates.</span><span class="sxs-lookup"><span data-stu-id="ddf34-120">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float3 const& value1, float3 const& value2)` | <span data-ttu-id="ddf34-121">Berechnet den euklidischen Abstand zwischen zwei Vektoren.</span><span class="sxs-lookup"><span data-stu-id="ddf34-121">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float3 const& value1, float3 const& value2)` | <span data-ttu-id="ddf34-122">Berechnet den euklidischen Abstand zwischen zwei quadratischen Vektoren.</span><span class="sxs-lookup"><span data-stu-id="ddf34-122">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="ddf34-123">Berechnet das Punktprodukt von zwei Vektoren.</span><span class="sxs-lookup"><span data-stu-id="ddf34-123">Calculates the dot product of two vectors.</span></span> |
| `float3 normalize(float3 const& value)` | <span data-ttu-id="ddf34-124">Erstellt einen Einheits Vektor aus dem angegebenen Vektor.</span><span class="sxs-lookup"><span data-stu-id="ddf34-124">Creates a unit vector from the specified vector.</span></span> |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="ddf34-125">Berechnet das Kreuzprodukt zweier Vektoren.</span><span class="sxs-lookup"><span data-stu-id="ddf34-125">Calculates the cross product of two vectors.</span></span> |
| `float3 reflect(float3 const& vector, float3 const& normal)` | <span data-ttu-id="ddf34-126">Bestimmt den reflektionvektor des angegebenen Vektors und des normalen.</span><span class="sxs-lookup"><span data-stu-id="ddf34-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float3 min(float3 const& value1, float3 const& value2)` | <span data-ttu-id="ddf34-127">Gibt einen Vektor zurück, der den niedrigsten Wert aus jedem übereinstimmenden paar von Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="ddf34-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float3 max(float3 const& value1, float3 const& value2)` | <span data-ttu-id="ddf34-128">Gibt einen Vektor zurück, der den höchsten Wert aus jedem übereinstimmenden paar von Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="ddf34-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | <span data-ttu-id="ddf34-129">Schränkt einen Wert in einen angegebenen Bereich ein.</span><span class="sxs-lookup"><span data-stu-id="ddf34-129">Restricts a value to be within a specified range.</span></span> |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | <span data-ttu-id="ddf34-130">Führt eine lineare interpolung zwischen zwei Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="ddf34-130">Performs a linear interpolation between two vectors.</span></span> |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="ddf34-131">Transformiert den Vektor (x, y, z, 1) um die angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="ddf34-131">Transforms the vector (x, y, z, 1) by the specified matrix.</span></span> |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | <span data-ttu-id="ddf34-132">Wandelt den normalen Vektor (x, y, z, 0) um die angegebene Matrix um.</span><span class="sxs-lookup"><span data-stu-id="ddf34-132">Transforms the normal vector (x, y, z, 0) by the specified matrix.</span></span> |
| `float3 transform(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="ddf34-133">Transformiert eine float3 durch die angegebene Quaternion.</span><span class="sxs-lookup"><span data-stu-id="ddf34-133">Transforms a float3 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="ddf34-134">Methoden</span><span class="sxs-lookup"><span data-stu-id="ddf34-134">Methods</span></span>

| <span data-ttu-id="ddf34-135">Name</span><span class="sxs-lookup"><span data-stu-id="ddf34-135">Name</span></span> | <span data-ttu-id="ddf34-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddf34-136">Description</span></span> |
|-|-|
| `static float3 zero()` | <span data-ttu-id="ddf34-137">Gibt eine float3 zurück, deren Komponenten auf 0 (null) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="ddf34-137">Returns a float3 with all of its components set to zero.</span></span> |
| `static float3 one()` | <span data-ttu-id="ddf34-138">Gibt einen float3-Wert zurück, dessen Komponenten auf einen Wert festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="ddf34-138">Returns a float3 with all of its components set to one.</span></span> |
| `static float3 unit_x()` | <span data-ttu-id="ddf34-139">Gibt float3 (1, 0, 0) zurück.</span><span class="sxs-lookup"><span data-stu-id="ddf34-139">Returns the float3 (1, 0, 0).</span></span> |
| `static float3 unit_y()` | <span data-ttu-id="ddf34-140">Gibt float3 (0, 1, 0) zurück.</span><span class="sxs-lookup"><span data-stu-id="ddf34-140">Returns the float3 (0, 1, 0).</span></span> |
| `static float3 unit_z()` | <span data-ttu-id="ddf34-141">Gibt float3 (0,0) zurück.</span><span class="sxs-lookup"><span data-stu-id="ddf34-141">Returns the float3 (0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="ddf34-142">Operatoren</span><span class="sxs-lookup"><span data-stu-id="ddf34-142">Operators</span></span>

| <span data-ttu-id="ddf34-143">Name</span><span class="sxs-lookup"><span data-stu-id="ddf34-143">Name</span></span> | <span data-ttu-id="ddf34-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddf34-144">Description</span></span> |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="ddf34-145">Addiert zwei Vektoren.</span><span class="sxs-lookup"><span data-stu-id="ddf34-145">Adds two vectors.</span></span> |
| `float3 operator- (float3 const& value1, float3 const& value2)` | <span data-ttu-id="ddf34-146">Subtrahiert einen Vektor von einem Vektor.</span><span class="sxs-lookup"><span data-stu-id="ddf34-146">Subtracts a vector from a vector.</span></span> |
| `float3 operator* (float3 const& value1, float3 const& value2)` | <span data-ttu-id="ddf34-147">Multipliziert die Komponenten von zwei Vektoren untereinander.</span><span class="sxs-lookup"><span data-stu-id="ddf34-147">Multiplies the components of two vectors by each other.</span></span> |
| `float3 operator* (float3 const& value1, float value2)` | <span data-ttu-id="ddf34-148">Multipliziert einen Vektor mit einem skalaren.</span><span class="sxs-lookup"><span data-stu-id="ddf34-148">Multiplies a vector by a scalar.</span></span> |
| `float3 operator* (float value1, float3 const& value2)` | <span data-ttu-id="ddf34-149">Multipliziert einen Vektor mit einem skalaren.</span><span class="sxs-lookup"><span data-stu-id="ddf34-149">Multiplies a vector by a scalar.</span></span> |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="ddf34-150">Dividiert die Komponenten eines Vektors durch die Komponenten eines anderen Vektors.</span><span class="sxs-lookup"><span data-stu-id="ddf34-150">Divides the components of a vector by the components of another vector.</span></span> |
| `float3 operator/ (float3 const& value1, float value2)` | <span data-ttu-id="ddf34-151">Dividiert einen Vektor durch einen Skalarwert.</span><span class="sxs-lookup"><span data-stu-id="ddf34-151">Divides a vector by a scalar value.</span></span> |
| `float3 operator- (float3 const& value)` | <span data-ttu-id="ddf34-152">Gibt einen Vektor zurück, der in umgekehrter Richtung zeigt.</span><span class="sxs-lookup"><span data-stu-id="ddf34-152">Returns a vector pointing in the opposite direction.</span></span> |
| `float3& operator+= (float3& value1, float3 const& value2)` | <span data-ttu-id="ddf34-153">Direkt fügt zwei Vektoren hinzu.</span><span class="sxs-lookup"><span data-stu-id="ddf34-153">In-place adds two vectors.</span></span> |
| `float3& operator-= (float3& value1, float3 const& value2)` | <span data-ttu-id="ddf34-154">Direkt subtrahiert einen Vektor von einem Vektor.</span><span class="sxs-lookup"><span data-stu-id="ddf34-154">In-place subtracts a vector from a vector.</span></span> |
| `float3& operator*= (float3& value1, float3 const& value2)` | <span data-ttu-id="ddf34-155">Direkt multipliziert die Komponenten von zwei Vektoren miteinander.</span><span class="sxs-lookup"><span data-stu-id="ddf34-155">In-place multiplies the components of two vectors by each other.</span></span> |
| `float3& operator*= (float3& value1, float value2)` | <span data-ttu-id="ddf34-156">Direkt multipliziert einen Vektor mit einem skalaren.</span><span class="sxs-lookup"><span data-stu-id="ddf34-156">In-place multiplies a vector by a scalar.</span></span> |
| `float3& operator/= (float3& value1, float3 const& value2)` | <span data-ttu-id="ddf34-157">Direkt dividiert die Komponenten eines Vektors durch die Komponenten eines anderen Vektors.</span><span class="sxs-lookup"><span data-stu-id="ddf34-157">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float3& operator/= (float3& value1, float value2)` | <span data-ttu-id="ddf34-158">Direkt unterteilt einen Vektor durch einen Skalarwert.</span><span class="sxs-lookup"><span data-stu-id="ddf34-158">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float3 const& value1, float3 const& value2)` | <span data-ttu-id="ddf34-159">Bestimmt, ob zwei Instanzen von float3 gleich sind.</span><span class="sxs-lookup"><span data-stu-id="ddf34-159">Determines whether two instances of float3 are equal.</span></span> |
| `bool operator!= (float3 const& value1, float3 const& value2)` | <span data-ttu-id="ddf34-160">Bestimmt, ob zwei Instanzen von float3 nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="ddf34-160">Determines whether two instances of float3 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | <span data-ttu-id="ddf34-161">Konvertiert ein float3-Zeichen in eine **Microsoft. Graphics. Canvas. Numerics. Vector3**.</span><span class="sxs-lookup"><span data-stu-id="ddf34-161">Converts a float3 to a **Microsoft.Graphics.Canvas.Numerics.Vector3**.</span></span> |

## <a name="fields"></a><span data-ttu-id="ddf34-162">Felder</span><span class="sxs-lookup"><span data-stu-id="ddf34-162">Fields</span></span>

| <span data-ttu-id="ddf34-163">Name</span><span class="sxs-lookup"><span data-stu-id="ddf34-163">Name</span></span> | <span data-ttu-id="ddf34-164">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddf34-164">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="ddf34-165">X-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="ddf34-165">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="ddf34-166">Y-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="ddf34-166">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="ddf34-167">Z-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="ddf34-167">Z component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="ddf34-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ddf34-168">Requirements</span></span>

| <span data-ttu-id="ddf34-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddf34-169">Requirement</span></span> | <span data-ttu-id="ddf34-170">Wert</span><span class="sxs-lookup"><span data-stu-id="ddf34-170">Value</span></span> |
|-|-|
| <span data-ttu-id="ddf34-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="ddf34-171">Namespace</span></span> | <span data-ttu-id="ddf34-172">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="ddf34-172">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="ddf34-173">Header</span><span class="sxs-lookup"><span data-stu-id="ddf34-173">Header</span></span> | <dl> <span data-ttu-id="ddf34-174"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddf34-174"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="ddf34-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddf34-175">See also</span></span>

[<span data-ttu-id="ddf34-176">windowsnumerics. h-APIs</span><span class="sxs-lookup"><span data-stu-id="ddf34-176">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
