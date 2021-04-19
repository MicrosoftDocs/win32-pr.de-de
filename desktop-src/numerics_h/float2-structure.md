---
title: float2-Struktur (windowsnumerics. h)
description: Ein Vektor mit zwei Komponenten.
ms.assetid: 1A23C1E3-F34F-4249-80EA-92A13CD4B34F
keywords:
- float2-Struktur
topic_type:
- apiref
api_name:
- float2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72398bdc087e0f7a0845703a2cefea40b5465b21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361490"
---
# <a name="float2-structure"></a><span data-ttu-id="a497d-104">float2-Struktur</span><span class="sxs-lookup"><span data-stu-id="a497d-104">float2 structure</span></span>

<span data-ttu-id="a497d-105">Ein Vektor mit zwei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="a497d-105">A vector with two components.</span></span>

<span data-ttu-id="a497d-106">Dieser Typ ist nur in C++ verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a497d-106">This type is available only in C++.</span></span> <span data-ttu-id="a497d-107">Die .NET-Entsprechung ist [System. Numerics. Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="a497d-107">Its .NET equivalent is [System.Numerics.Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="a497d-108">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="a497d-108">Constructors</span></span>

| <span data-ttu-id="a497d-109">Name</span><span class="sxs-lookup"><span data-stu-id="a497d-109">Name</span></span> | <span data-ttu-id="a497d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a497d-110">Description</span></span> |
|-|-|
| `float2()` | <span data-ttu-id="a497d-111">Erstellt ein nicht initialisiertes float2-.</span><span class="sxs-lookup"><span data-stu-id="a497d-111">Creates an uninitialized float2.</span></span> |
| `float2(float x, float y)` | <span data-ttu-id="a497d-112">Erstellt eine float2 mit den angegebenen Werten.</span><span class="sxs-lookup"><span data-stu-id="a497d-112">Creates a float2 with the specified values.</span></span> |
| `explicit float2(float value)` | <span data-ttu-id="a497d-113">Erstellt eine float2, bei der alle Komponenten auf den angegebenen Wert festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="a497d-113">Creates a float2 with all components set to the specified value.</span></span> |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | <span data-ttu-id="a497d-114">Konvertiert eine **Microsoft. Graphics. Canvas. Numerics. Vector2** in eine float2.</span><span class="sxs-lookup"><span data-stu-id="a497d-114">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector2** to a float2.</span></span> |
| `float2(Windows::Foundation::Point const& value)` | <span data-ttu-id="a497d-115">Konvertiert ein [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point) in eine float2.</span><span class="sxs-lookup"><span data-stu-id="a497d-115">Converts a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point) to a float2.</span></span> |
| `float2(Windows::Foundation::Size const& value)` | <span data-ttu-id="a497d-116">Konvertiert eine [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size) in eine float2.</span><span class="sxs-lookup"><span data-stu-id="a497d-116">Converts a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size) to a float2.</span></span> |

## <a name="functions"></a><span data-ttu-id="a497d-117">Functions</span><span class="sxs-lookup"><span data-stu-id="a497d-117">Functions</span></span>

| <span data-ttu-id="a497d-118">Name</span><span class="sxs-lookup"><span data-stu-id="a497d-118">Name</span></span> | <span data-ttu-id="a497d-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a497d-119">Description</span></span> |
|-|-|
| `float length(float2 const& value)` | <span data-ttu-id="a497d-120">Berechnet die Länge des Vektors (bzw. euklidische Entfernung).</span><span class="sxs-lookup"><span data-stu-id="a497d-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float2 const& value)` | <span data-ttu-id="a497d-121">Berechnet die Länge oder den euklidischen Abstand des Vektor Quadrates.</span><span class="sxs-lookup"><span data-stu-id="a497d-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float2 const& value1, float2 const& value2)` | <span data-ttu-id="a497d-122">Berechnet den euklidischen Abstand zwischen zwei Vektoren.</span><span class="sxs-lookup"><span data-stu-id="a497d-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float2 const& value1, float2 const& value2)` | <span data-ttu-id="a497d-123">Berechnet den euklidischen Abstand zwischen zwei quadratischen Vektoren.</span><span class="sxs-lookup"><span data-stu-id="a497d-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float2 const& value1, float2 const& value2)` | <span data-ttu-id="a497d-124">Berechnet das Punktprodukt von zwei Vektoren.</span><span class="sxs-lookup"><span data-stu-id="a497d-124">Calculates the dot product of two vectors.</span></span> |
| `float2 normalize(float2 const& value)` | <span data-ttu-id="a497d-125">Erstellt einen Einheits Vektor aus dem angegebenen Vektor.</span><span class="sxs-lookup"><span data-stu-id="a497d-125">Creates a unit vector from the specified vector.</span></span> |
| `float2 reflect(float2 const& vector, float2 const& normal)` | <span data-ttu-id="a497d-126">Bestimmt den reflektionvektor des angegebenen Vektors und des normalen.</span><span class="sxs-lookup"><span data-stu-id="a497d-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float2 min(float2 const& value1, float2 const& value2)` | <span data-ttu-id="a497d-127">Gibt einen Vektor zurück, der den niedrigsten Wert aus jedem übereinstimmenden paar von Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="a497d-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float2 max(float2 const& value1, float2 const& value2)` | <span data-ttu-id="a497d-128">Gibt einen Vektor zurück, der den höchsten Wert aus jedem übereinstimmenden paar von Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="a497d-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | <span data-ttu-id="a497d-129">Schränkt einen Wert in einen angegebenen Bereich ein.</span><span class="sxs-lookup"><span data-stu-id="a497d-129">Restricts a value to be within a specified range.</span></span> |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | <span data-ttu-id="a497d-130">Führt eine lineare interpolung zwischen zwei Vektoren aus.</span><span class="sxs-lookup"><span data-stu-id="a497d-130">Performs a linear interpolation between two vectors.</span></span> |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | <span data-ttu-id="a497d-131">Wandelt den Vektor (x, y, 0, 1) um die angegebene Matrix um.</span><span class="sxs-lookup"><span data-stu-id="a497d-131">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="a497d-132">Wandelt den Vektor (x, y, 0, 1) um die angegebene Matrix um.</span><span class="sxs-lookup"><span data-stu-id="a497d-132">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | <span data-ttu-id="a497d-133">Wandelt den normalen Vektor (x, y, 0, 0) um die angegebene Matrix um.</span><span class="sxs-lookup"><span data-stu-id="a497d-133">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | <span data-ttu-id="a497d-134">Wandelt den normalen Vektor (x, y, 0, 0) um die angegebene Matrix um.</span><span class="sxs-lookup"><span data-stu-id="a497d-134">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="a497d-135">Transformiert eine float2 durch die angegebene Quaternion.</span><span class="sxs-lookup"><span data-stu-id="a497d-135">Transforms a float2 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="a497d-136">Methoden</span><span class="sxs-lookup"><span data-stu-id="a497d-136">Methods</span></span>

| <span data-ttu-id="a497d-137">Name</span><span class="sxs-lookup"><span data-stu-id="a497d-137">Name</span></span> | <span data-ttu-id="a497d-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a497d-138">Description</span></span> |
|-|-|
| `static float2 zero()` | <span data-ttu-id="a497d-139">Gibt eine float2 zurück, deren Komponenten auf 0 (null) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="a497d-139">Returns a float2 with all of its components set to zero.</span></span> |
| `static float2 one()` | <span data-ttu-id="a497d-140">Gibt einen float2-Wert zurück, dessen Komponenten auf einen Wert festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="a497d-140">Returns a float2 with all of its components set to one.</span></span> |
| `static float2 unit_x()` | <span data-ttu-id="a497d-141">Gibt float2 (1, 0) zurück.</span><span class="sxs-lookup"><span data-stu-id="a497d-141">Returns the float2 (1, 0).</span></span> |
| `static float2 unit_y()` | <span data-ttu-id="a497d-142">Gibt float2 (0,0) zurück.</span><span class="sxs-lookup"><span data-stu-id="a497d-142">Returns the float2 (0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="a497d-143">Operatoren</span><span class="sxs-lookup"><span data-stu-id="a497d-143">Operators</span></span>

| <span data-ttu-id="a497d-144">Name</span><span class="sxs-lookup"><span data-stu-id="a497d-144">Name</span></span> | <span data-ttu-id="a497d-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a497d-145">Description</span></span> |
|-|-|
| `operator Windows::Foundation::Point() const` | <span data-ttu-id="a497d-146">Konvertiert ein float2-Zeichen in einen [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point).</span><span class="sxs-lookup"><span data-stu-id="a497d-146">Converts a float2 to a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point).</span></span> |
| `operator Windows::Foundation::Size() const` | <span data-ttu-id="a497d-147">Konvertiert ein float2-in eine [**Windows. Foundation. size-Klasse**](/uwp/api/Windows.Foundation.Size).</span><span class="sxs-lookup"><span data-stu-id="a497d-147">Converts a float2 to a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size).</span></span> |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="a497d-148">Addiert zwei Vektoren.</span><span class="sxs-lookup"><span data-stu-id="a497d-148">Adds two vectors.</span></span> |
| `float2 operator- (float2 const& value1, float2 const& value2)` | <span data-ttu-id="a497d-149">Subtrahiert einen Vektor von einem Vektor.</span><span class="sxs-lookup"><span data-stu-id="a497d-149">Subtracts a vector from a vector.</span></span> |
| `float2 operator* (float2 const& value1, float2 const& value2)` | <span data-ttu-id="a497d-150">Multipliziert die Komponenten von zwei Vektoren untereinander.</span><span class="sxs-lookup"><span data-stu-id="a497d-150">Multiplies the components of two vectors by each other.</span></span> |
| `float2 operator* (float2 const& value1, float value2)` | <span data-ttu-id="a497d-151">Multipliziert einen Vektor mit einem skalaren.</span><span class="sxs-lookup"><span data-stu-id="a497d-151">Multiplies a vector by a scalar.</span></span> |
| `float2 operator* (float value1, float2 const& value2)` | <span data-ttu-id="a497d-152">Multipliziert einen Vektor mit einem skalaren.</span><span class="sxs-lookup"><span data-stu-id="a497d-152">Multiplies a vector by a scalar.</span></span> |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="a497d-153">Dividiert die Komponenten eines Vektors durch die Komponenten eines anderen Vektors.</span><span class="sxs-lookup"><span data-stu-id="a497d-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float2 operator/ (float2 const& value1, float value2)` | <span data-ttu-id="a497d-154">Dividiert einen Vektor durch einen Skalarwert.</span><span class="sxs-lookup"><span data-stu-id="a497d-154">Divides a vector by a scalar value.</span></span> |
| `float2 operator- (float2 const& value)` | <span data-ttu-id="a497d-155">Gibt einen Vektor zurück, der in umgekehrter Richtung zeigt.</span><span class="sxs-lookup"><span data-stu-id="a497d-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float2& operator+= (float2& value1, float2 const& value2)` | <span data-ttu-id="a497d-156">Direkt fügt zwei Vektoren hinzu.</span><span class="sxs-lookup"><span data-stu-id="a497d-156">In-place adds two vectors.</span></span> |
| `float2& operator-= (float2& value1, float2 const& value2)` | <span data-ttu-id="a497d-157">Direkt subtrahiert einen Vektor von einem Vektor.</span><span class="sxs-lookup"><span data-stu-id="a497d-157">In-place subtracts a vector from a vector.</span></span> |
| `float2& operator*= (float2& value1, float2 const& value2)` | <span data-ttu-id="a497d-158">Direkt multipliziert die Komponenten von zwei Vektoren miteinander.</span><span class="sxs-lookup"><span data-stu-id="a497d-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float2& operator*= (float2& value1, float value2)` | <span data-ttu-id="a497d-159">Direkt multipliziert einen Vektor mit einem skalaren.</span><span class="sxs-lookup"><span data-stu-id="a497d-159">In-place multiplies a vector by a scalar.</span></span> |
| `float2& operator/= (float2& value1, float2 const& value2)` | <span data-ttu-id="a497d-160">Direkt dividiert die Komponenten eines Vektors durch die Komponenten eines anderen Vektors.</span><span class="sxs-lookup"><span data-stu-id="a497d-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float2& operator/= (float2& value1, float value2)` | <span data-ttu-id="a497d-161">Direkt unterteilt einen Vektor durch einen Skalarwert.</span><span class="sxs-lookup"><span data-stu-id="a497d-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float2 const& value1, float2 const& value2)` | <span data-ttu-id="a497d-162">Bestimmt, ob zwei Instanzen von float2 gleich sind.</span><span class="sxs-lookup"><span data-stu-id="a497d-162">Determines whether two instances of float2 are equal.</span></span> |
| `bool operator!= (float2 const& value1, float2 const& value2)` | <span data-ttu-id="a497d-163">Bestimmt, ob zwei Instanzen von float2 nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="a497d-163">Determines whether two instances of float2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | <span data-ttu-id="a497d-164">Konvertiert ein float2-Zeichen in eine **Microsoft. Graphics. Canvas. Numerics. Vector2**.</span><span class="sxs-lookup"><span data-stu-id="a497d-164">Converts a float2 to a **Microsoft.Graphics.Canvas.Numerics.Vector2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="a497d-165">Felder</span><span class="sxs-lookup"><span data-stu-id="a497d-165">Fields</span></span>

| <span data-ttu-id="a497d-166">Name</span><span class="sxs-lookup"><span data-stu-id="a497d-166">Name</span></span> | <span data-ttu-id="a497d-167">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a497d-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="a497d-168">X-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="a497d-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="a497d-169">Y-Komponente des Vektors.</span><span class="sxs-lookup"><span data-stu-id="a497d-169">Y component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="a497d-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a497d-170">Requirements</span></span>

| <span data-ttu-id="a497d-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a497d-171">Requirement</span></span> | <span data-ttu-id="a497d-172">Wert</span><span class="sxs-lookup"><span data-stu-id="a497d-172">Value</span></span> |
|-|-|
| <span data-ttu-id="a497d-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="a497d-173">Namespace</span></span> | <span data-ttu-id="a497d-174">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="a497d-174">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="a497d-175">Header</span><span class="sxs-lookup"><span data-stu-id="a497d-175">Header</span></span> | <dl> <span data-ttu-id="a497d-176"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="a497d-176"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="a497d-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a497d-177">See also</span></span>

[<span data-ttu-id="a497d-178">windowsnumerics. h-APIs</span><span class="sxs-lookup"><span data-stu-id="a497d-178">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
