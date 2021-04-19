---
title: FLOAT4-Struktur (windowsnumerics. h)
description: Ein Vektor mit vier Komponenten.
ms.assetid: AC07C6D0-E7FD-4582-B40D-4838F49FB8B4
keywords:
- FLOAT4-Struktur
topic_type:
- apiref
api_name:
- float4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4a2a4721e3ab7e5520545b42367d2432ba967f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372726"
---
# <a name="float4-structure"></a><span data-ttu-id="10bee-104">FLOAT4-Struktur</span><span class="sxs-lookup"><span data-stu-id="10bee-104">float4 structure</span></span>

<span data-ttu-id="10bee-105">Ein Vektor mit vier Komponenten.</span><span class="sxs-lookup"><span data-stu-id="10bee-105">A vector with four components.</span></span>

<span data-ttu-id="10bee-106">Dieser Typ ist nur in C++ verfügbar.</span><span class="sxs-lookup"><span data-stu-id="10bee-106">This type is available only in C++.</span></span> <span data-ttu-id="10bee-107">Die .NET-Entsprechung ist [System. Numerics. Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="10bee-107">Its .NET equivalent is [System.Numerics.Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="10bee-108">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="10bee-108">Constructors</span></span>

| <span data-ttu-id="10bee-109">Name</span><span class="sxs-lookup"><span data-stu-id="10bee-109">Name</span></span> | <span data-ttu-id="10bee-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10bee-110">Description</span></span> |
|-|-|
| `float4()` | <span data-ttu-id="10bee-111">Erstellt ein nicht initialisiertes float4-.</span><span class="sxs-lookup"><span data-stu-id="10bee-111">Creates an uninitialized float4.</span></span> |
| `float4(float x, float y, float z, float w)` | <span data-ttu-id="10bee-112">Erstellt eine float4 mit den angegebenen Werten.</span><span class="sxs-lookup"><span data-stu-id="10bee-112">Creates a float4 with the specified values.</span></span> |
| `float4(float2 value, float z, float w)` | <span data-ttu-id="10bee-113">Erstellt ein float4 mit x und y, das aus einem float2 plus den angegebenen z-und w-Werten kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="10bee-113">Creates a float4 with x and y copied from a float2 plus the specified z and w values.</span></span> |
| `float4(float3 value, float w)` | <span data-ttu-id="10bee-114">Erstellt ein float4 mit x, y und z, das aus einem float3 plus dem angegebenen w-Wert kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="10bee-114">Creates a float4 with x, y and z copied from a float3 plus the specified w value.</span></span> |
| `explicit float4(float value)` | <span data-ttu-id="10bee-115">Erstellt ein float4-Wert, bei dem alle com. ents auf den angegebenen Wert festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="10bee-115">Creates a float4 with all com.ents set to the specified value.</span></span> |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | <span data-ttu-id="10bee-116">Konvertiert eine **Microsoft. Graphics. Canvas. Numerics. Vector4** in eine float4.</span><span class="sxs-lookup"><span data-stu-id="10bee-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector4** to a float4.</span></span> |

## <a name="functions"></a><span data-ttu-id="10bee-117">Functions</span><span class="sxs-lookup"><span data-stu-id="10bee-117">Functions</span></span>

| <span data-ttu-id="10bee-118">Name</span><span class="sxs-lookup"><span data-stu-id="10bee-118">Name</span></span> | <span data-ttu-id="10bee-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10bee-119">Description</span></span> |
|-|-|
| `float length(float4 const& value)` | <span data-ttu-id="10bee-120">Berechnet die Länge des Vektors (bzw. euklidische Entfernung).</span><span class="sxs-lookup"><span data-stu-id="10bee-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float4 const& value)` | <span data-ttu-id="10bee-121">Berechnet die Länge oder den euklidischen Abstand des Vektor Quadrates.</span><span class="sxs-lookup"><span data-stu-id="10bee-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float4 const& value1, float4 const& value2)` | <span data-ttu-id="10bee-122">Berechnet den euklidischen Abstand zwischen zwei Vektoren.</span><span class="sxs-lookup"><span data-stu-id="10bee-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float4 const& value1, float4 const& value2)` | <span data-ttu-id="10bee-123">Berechnet den euklidischen Abstand zwischen zwei quadratischen Vektoren.</span><span class="sxs-lookup"><span data-stu-id="10bee-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float4 const& vector1, float4 const& vector2)` | <span data-ttu-id="10bee-124">Berechnet das Punktprodukt von zwei Vektoren.</span><span class="sxs-lookup"><span data-stu-id="10bee-124">Calculates the dot product of two vectors.</span></span> |
| `float4 normalize(float4 const& vector)` | <span data-ttu-id="10bee-125">Erstellt einen Einheits Vektor aus dem angegebenen Vektor.</span><span class="sxs-lookup"><span data-stu-id="10bee-125">Creates a unit vector from the specified vector.</span></span> |
| `float4 min(float4 const& value1, float4 const& value2)` | <span data-ttu-id="10bee-126">Gibt einen Vektor zurück, der den niedrigsten Wert aus jedem übereinstimmenden paar von Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="10bee-126">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float4 max(float4 const& value1, float4 const& value2)` | <span data-ttu-id="10bee-127">Gibt einen Vektor zurück, der den höchsten Wert aus jedem übereinstimmenden paar von Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="10bee-127">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | <span data-ttu-id="10bee-128">Schränkt einen Wert in einen angegebenen Bereich ein.</span><span class="sxs-lookup"><span data-stu-id="10bee-128">Restricts a value to be within a specified range.</span></span> |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | <span data-ttu-id="10bee-129">Führt eine lineare interpolung zwischen zwei Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="10bee-129">Performs a linear interpolation between two vectors.</span></span> |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | <span data-ttu-id="10bee-130">Transformiert eine float4 durch die angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="10bee-130">Transforms a float4 by the given matrix.</span></span> |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="10bee-131">Transformiert eine float3 durch die angegebene Matrix und gibt eine float4 zurück.</span><span class="sxs-lookup"><span data-stu-id="10bee-131">Transforms a float3 by the given matrix, returning a float4.</span></span> |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="10bee-132">Transformiert eine float2 durch die angegebene Matrix und gibt eine float4 zurück.</span><span class="sxs-lookup"><span data-stu-id="10bee-132">Transforms a float2 by the given matrix, returning a float4.</span></span> |
| `float4 transform(float4 const& value, quaternion const& rotation)` | <span data-ttu-id="10bee-133">Transformiert eine float4 durch die angegebene Quaternion.</span><span class="sxs-lookup"><span data-stu-id="10bee-133">Transforms a float4 by the given quaternion.</span></span> |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="10bee-134">Transformiert eine float3 durch die angegebene Quaternion und gibt eine float4 zurück.</span><span class="sxs-lookup"><span data-stu-id="10bee-134">Transforms a float3 by the given quaternion, returning a float4.</span></span> |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="10bee-135">Transformiert eine float2 durch die angegebene Quaternion und gibt eine float4 zurück.</span><span class="sxs-lookup"><span data-stu-id="10bee-135">Transforms a float2 by the given quaternion, returning a float4.</span></span> |

## <a name="methods"></a><span data-ttu-id="10bee-136">Methoden</span><span class="sxs-lookup"><span data-stu-id="10bee-136">Methods</span></span>

| <span data-ttu-id="10bee-137">Name</span><span class="sxs-lookup"><span data-stu-id="10bee-137">Name</span></span> | <span data-ttu-id="10bee-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10bee-138">Description</span></span> |
|-|-|
| `static float4 zero()` | <span data-ttu-id="10bee-139">Gibt eine float4 zurück, deren Komponenten auf 0 (null) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="10bee-139">Returns a float4 with all of its components set to zero.</span></span> |
| `static float4 one()` | <span data-ttu-id="10bee-140">Gibt einen float4-Wert zurück, dessen Komponenten auf einen Wert festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="10bee-140">Returns a float4 with all of its components set to one.</span></span> |
| `static float4 unit_x()` | <span data-ttu-id="10bee-141">Gibt FLOAT4 (1, 0, 0, 0) zurück.</span><span class="sxs-lookup"><span data-stu-id="10bee-141">Returns the float4 (1, 0, 0, 0).</span></span> |
| `static float4 unit_y()` | <span data-ttu-id="10bee-142">Gibt FLOAT4 (0, 1, 0, 0) zurück.</span><span class="sxs-lookup"><span data-stu-id="10bee-142">Returns the float4 (0, 1, 0, 0).</span></span> |
| `static float4 unit_z()` | <span data-ttu-id="10bee-143">Gibt FLOAT4 (0,0) zurück.</span><span class="sxs-lookup"><span data-stu-id="10bee-143">Returns the float4 (0, 0, 1, 0).</span></span> |
| `static float4 unit_w()` | <span data-ttu-id="10bee-144">Gibt FLOAT4 (0,0) zurück.</span><span class="sxs-lookup"><span data-stu-id="10bee-144">Returns the float4 (0, 0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="10bee-145">Operatoren</span><span class="sxs-lookup"><span data-stu-id="10bee-145">Operators</span></span>

| <span data-ttu-id="10bee-146">Name</span><span class="sxs-lookup"><span data-stu-id="10bee-146">Name</span></span> | <span data-ttu-id="10bee-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10bee-147">Description</span></span> |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="10bee-148">Addiert zwei Vektoren.</span><span class="sxs-lookup"><span data-stu-id="10bee-148">Adds two vectors.</span></span> |
| `float4 operator- (float4 const& value1, float4 const& value2)` | <span data-ttu-id="10bee-149">Subtrahiert einen Vektor von einem Vektor.</span><span class="sxs-lookup"><span data-stu-id="10bee-149">Subtracts a vector from a vector.</span></span> |
| `float4 operator* (float4 const& value1, float4 const& value2)` | <span data-ttu-id="10bee-150">Multipliziert die Komponenten von zwei Vektoren untereinander.</span><span class="sxs-lookup"><span data-stu-id="10bee-150">Multiplies the components of two vectors by each other.</span></span> |
| `float4 operator* (float4 const& value1, float value2)` | <span data-ttu-id="10bee-151">Multipliziert einen Vektor mit einem skalaren.</span><span class="sxs-lookup"><span data-stu-id="10bee-151">Multiplies a vector by a scalar.</span></span> |
| `float4 operator* (float value1, float4 const& value2)` | <span data-ttu-id="10bee-152">Multipliziert einen Vektor mit einem skalaren.</span><span class="sxs-lookup"><span data-stu-id="10bee-152">Multiplies a vector by a scalar.</span></span> |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="10bee-153">Dividiert die Komponenten eines Vektors durch die Komponenten eines anderen Vektors.</span><span class="sxs-lookup"><span data-stu-id="10bee-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float4 operator/ (float4 const& value1, float value2)` | <span data-ttu-id="10bee-154">Dividiert einen Vektor durch einen Skalarwert.</span><span class="sxs-lookup"><span data-stu-id="10bee-154">Divides a vector by a scalar value.</span></span> |
| `float4 operator- (float4 const& value)` | <span data-ttu-id="10bee-155">Gibt einen Vektor zurück, der in umgekehrter Richtung zeigt.</span><span class="sxs-lookup"><span data-stu-id="10bee-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float4& operator+= (float4& value1, float4 const& value2)` | <span data-ttu-id="10bee-156">Direkt fügt zwei Vektoren hinzu.</span><span class="sxs-lookup"><span data-stu-id="10bee-156">In-place adds two vectors.</span></span> |
| `float4& operator-= (float4& value1, float4 const& value2)` | <span data-ttu-id="10bee-157">Direkt subtrahiert einen Vektor von einem Vektor.</span><span class="sxs-lookup"><span data-stu-id="10bee-157">In-place subtracts a vector from a vector.</span></span> |
| `float4& operator*= (float4& value1, float4 const& value2)` | <span data-ttu-id="10bee-158">Direkt multipliziert die Komponenten von zwei Vektoren miteinander.</span><span class="sxs-lookup"><span data-stu-id="10bee-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float4& operator*= (float4& value1, float value2)` | <span data-ttu-id="10bee-159">Direkt multipliziert einen Vektor mit einem skalaren.</span><span class="sxs-lookup"><span data-stu-id="10bee-159">In-place multiplies a vector by a scalar.</span></span> |
| `float4& operator/= (float4& value1, float4 const& value2)` | <span data-ttu-id="10bee-160">Direkt dividiert die Komponenten eines Vektors durch die Komponenten eines anderen Vektors.</span><span class="sxs-lookup"><span data-stu-id="10bee-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float4& operator/= (float4& value1, float value2)` | <span data-ttu-id="10bee-161">Direkt unterteilt einen Vektor durch einen Skalarwert.</span><span class="sxs-lookup"><span data-stu-id="10bee-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float4 const& value1, float4 const& value2)` | <span data-ttu-id="10bee-162">Bestimmt, ob zwei Instanzen von float4 gleich sind.</span><span class="sxs-lookup"><span data-stu-id="10bee-162">Determines whether two instances of float4 are equal.</span></span> |
| `bool operator!= (float4 const& value1, float4 const& value2)` | <span data-ttu-id="10bee-163">Bestimmt, ob zwei Instanzen von float4 nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="10bee-163">Determines whether two instances of float4 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | <span data-ttu-id="10bee-164">Konvertiert ein float4-Zeichen in eine **Microsoft. Graphics. Canvas. Numerics. Vector4**.</span><span class="sxs-lookup"><span data-stu-id="10bee-164">Converts a float4 to a **Microsoft.Graphics.Canvas.Numerics.Vector4**.</span></span> |

## <a name="fields"></a><span data-ttu-id="10bee-165">Felder</span><span class="sxs-lookup"><span data-stu-id="10bee-165">Fields</span></span>

| <span data-ttu-id="10bee-166">Name</span><span class="sxs-lookup"><span data-stu-id="10bee-166">Name</span></span> | <span data-ttu-id="10bee-167">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10bee-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="10bee-168">X-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="10bee-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="10bee-169">Y-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="10bee-169">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="10bee-170">Z-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="10bee-170">Z component of the vector.</span></span> |
| `float w` | <span data-ttu-id="10bee-171">W-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="10bee-171">W component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="10bee-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10bee-172">Requirements</span></span>

| <span data-ttu-id="10bee-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10bee-173">Requirement</span></span> | <span data-ttu-id="10bee-174">Wert</span><span class="sxs-lookup"><span data-stu-id="10bee-174">Value</span></span> |
|-|-|
| <span data-ttu-id="10bee-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="10bee-175">Namespace</span></span> | <span data-ttu-id="10bee-176">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="10bee-176">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="10bee-177">Header</span><span class="sxs-lookup"><span data-stu-id="10bee-177">Header</span></span> | <dl> <span data-ttu-id="10bee-178"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="10bee-178"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="10bee-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10bee-179">See also</span></span>

[<span data-ttu-id="10bee-180">windowsnumerics. h-APIs</span><span class="sxs-lookup"><span data-stu-id="10bee-180">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
