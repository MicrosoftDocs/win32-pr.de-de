---
title: float3x2-Struktur (windowsnumerics. h)
description: Eine 3 x 2-Matrix, die für 2D-Transformationen verwendet wird.
ms.assetid: 5C2A4C30-3EC4-4DE9-A42A-6A19F96F8D69
keywords:
- float3x2-Struktur
topic_type:
- apiref
api_name:
- float3x2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9351fae9636ca2512825c7df5383eddf1558583e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367106"
---
# <a name="float3x2-structure"></a><span data-ttu-id="2a19f-104">float3x2-Struktur</span><span class="sxs-lookup"><span data-stu-id="2a19f-104">float3x2 structure</span></span>

<span data-ttu-id="2a19f-105">Eine 3 x 2-Matrix, die für 2D-Transformationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2a19f-105">A 3x2 matrix, used for 2D transforms.</span></span>

<span data-ttu-id="2a19f-106">Dieser Matrixtyp verwendet ein Zeilen Vektor Layout.</span><span class="sxs-lookup"><span data-stu-id="2a19f-106">This matrix type uses a row vector layout.</span></span> <span data-ttu-id="2a19f-107">Das x und y des Übersetzungs Vektors dieser Matrix entsprechen den Feldern M31, M32.</span><span class="sxs-lookup"><span data-stu-id="2a19f-107">The x and y of this matrix's translation vector correspond to the fields m31, m32.</span></span>

<span data-ttu-id="2a19f-108">Dieser Typ ist nur in C++ verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2a19f-108">This type is available only in C++.</span></span> <span data-ttu-id="2a19f-109">Die .NET-Entsprechung ist [System. Numerics. Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="2a19f-109">Its .NET equivalent is [System.Numerics.Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="2a19f-110">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="2a19f-110">Constructors</span></span>

| <span data-ttu-id="2a19f-111">Name</span><span class="sxs-lookup"><span data-stu-id="2a19f-111">Name</span></span> | <span data-ttu-id="2a19f-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a19f-112">Description</span></span> |
|-|-|
| `float3x2()` | <span data-ttu-id="2a19f-113">Erstellt ein nicht initialisiertes float3x2-.</span><span class="sxs-lookup"><span data-stu-id="2a19f-113">Creates an uninitialized float3x2.</span></span> |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | <span data-ttu-id="2a19f-114">Erstellt eine float3x2 mit den angegebenen Werten.</span><span class="sxs-lookup"><span data-stu-id="2a19f-114">Creates a float3x2 with the specified values.</span></span> |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | <span data-ttu-id="2a19f-115">Konvertiert eine **Microsoft. Graphics. Canvas. Numerics. Matrix3x2** in eine float3x2.</span><span class="sxs-lookup"><span data-stu-id="2a19f-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2** to a float3x2.</span></span> |

## <a name="functions"></a><span data-ttu-id="2a19f-116">Functions</span><span class="sxs-lookup"><span data-stu-id="2a19f-116">Functions</span></span>

| <span data-ttu-id="2a19f-117">Name</span><span class="sxs-lookup"><span data-stu-id="2a19f-117">Name</span></span> | <span data-ttu-id="2a19f-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a19f-118">Description</span></span> |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | <span data-ttu-id="2a19f-119">Erstellt eine Translationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-119">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | <span data-ttu-id="2a19f-120">Erstellt eine Translationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-120">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | <span data-ttu-id="2a19f-121">Erstellt eine Skalierungs Matrix, die auf dem Ursprung zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="2a19f-121">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | <span data-ttu-id="2a19f-122">Erstellt eine Skalierungs Matrix, die auf dem angegebenen Punkt zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="2a19f-122">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales)` | <span data-ttu-id="2a19f-123">Erstellt eine Skalierungs Matrix, die auf dem Ursprung zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="2a19f-123">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | <span data-ttu-id="2a19f-124">Erstellt eine Skalierungs Matrix, die auf dem angegebenen Punkt zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="2a19f-124">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float scale)` | <span data-ttu-id="2a19f-125">Erstellt eine Skalierungs Matrix, die auf dem Ursprung zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="2a19f-125">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | <span data-ttu-id="2a19f-126">Erstellt eine Skalierungs Matrix, die auf dem angegebenen Punkt zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="2a19f-126">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | <span data-ttu-id="2a19f-127">Erstellt eine schiefe Matrix, die auf dem Ursprung zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="2a19f-127">Creates a skew matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | <span data-ttu-id="2a19f-128">Erstellt eine schiefe Matrix, die auf den angegebenen Punkt zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="2a19f-128">Creates a skew matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_rotation(float radians)` | <span data-ttu-id="2a19f-129">Erstellt eine Rotations Matrix, die auf dem Ursprung zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="2a19f-129">Creates a rotation matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | <span data-ttu-id="2a19f-130">Erstellt eine Rotations Matrix, die auf den angegebenen Punkt zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="2a19f-130">Creates a rotation matrix, centered on the specified point.</span></span> |
| `bool is_identity(float3x2 const& value)` | <span data-ttu-id="2a19f-131">Überprüft, ob es sich um eine Identitätsmatrix handelt.</span><span class="sxs-lookup"><span data-stu-id="2a19f-131">Checks whether this is an identity matrix.</span></span> |
| `float determinant(float3x2 const& value)` | <span data-ttu-id="2a19f-132">Berechnet den Determinanten der Matrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-132">Calculates the determinant of the matrix.</span></span> |
| `float2 translation(float3x2 const& value)` | <span data-ttu-id="2a19f-133">Ruft den Übersetzungs Vektor der Matrix ab.</span><span class="sxs-lookup"><span data-stu-id="2a19f-133">Gets the translation vector of the matrix.</span></span> |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | <span data-ttu-id="2a19f-134">Berechnet den umgekehrten einer Matrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-134">Calculates the inverse of a matrix.</span></span> <span data-ttu-id="2a19f-135">Gibt true zurück, wenn die Matrix invertiert werden kann. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="2a19f-135">Returns true if the matrix can be inverted; false otherwise.</span></span> |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | <span data-ttu-id="2a19f-136">Linearly interpoliert zwischen den entsprechenden Werten von zwei Matrizen.</span><span class="sxs-lookup"><span data-stu-id="2a19f-136">Linearly interpolates between the corresponding values of two matrices.</span></span> |

## <a name="methods"></a><span data-ttu-id="2a19f-137">Methoden</span><span class="sxs-lookup"><span data-stu-id="2a19f-137">Methods</span></span>

| <span data-ttu-id="2a19f-138">Name</span><span class="sxs-lookup"><span data-stu-id="2a19f-138">Name</span></span> | <span data-ttu-id="2a19f-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a19f-139">Description</span></span> |
|-|-|
| `static float3x2 identity()` | <span data-ttu-id="2a19f-140">Gibt eine Instanz der Identitätsmatrix zurück.</span><span class="sxs-lookup"><span data-stu-id="2a19f-140">Returns an instance of the identity matrix.</span></span> |

## <a name="operators"></a><span data-ttu-id="2a19f-141">Operatoren</span><span class="sxs-lookup"><span data-stu-id="2a19f-141">Operators</span></span>

| <span data-ttu-id="2a19f-142">Name</span><span class="sxs-lookup"><span data-stu-id="2a19f-142">Name</span></span> | <span data-ttu-id="2a19f-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a19f-143">Description</span></span> |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="2a19f-144">Fügt jede Komponente einer Matrix einer anderen Matrix hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a19f-144">Adds each component of a matrix to another matrix.</span></span> |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="2a19f-145">Subtrahiert jede Komponente einer Matrix von einer anderen Matrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-145">Subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="2a19f-146">Multipliziert eine Matrix mit einer anderen Matrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-146">Multiplies a matrix by another matrix.</span></span> <span data-ttu-id="2a19f-147">Dies hat den Effekt, dass zwei Transformationen verkettet werden.</span><span class="sxs-lookup"><span data-stu-id="2a19f-147">This has the effect of concatenating two transforms.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float value2)` | <span data-ttu-id="2a19f-148">Multipliziert jede Komponente einer Matrix mit einem skalaren Wert.</span><span class="sxs-lookup"><span data-stu-id="2a19f-148">Multiplies each component of a matrix by a scalar value.</span></span> |
| `float3x2 operator- (float3x2 const& value)` | <span data-ttu-id="2a19f-149">Negiert jede Komponente einer Matrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-149">Negates each component of a matrix.</span></span> |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="2a19f-150">Direkt fügt jede Komponente einer Matrix einer anderen Matrix hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a19f-150">In-place adds each component of a matrix to another matrix.</span></span> |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="2a19f-151">Direkt subtrahiert jede Komponente einer Matrix aus einer anderen Matrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-151">In-place subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="2a19f-152">Direkt multipliziert eine Matrix mit einer anderen Matrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-152">In-place multiplies a matrix by another matrix.</span></span> <span data-ttu-id="2a19f-153">Dies hat den Effekt, dass zwei Transformationen verkettet werden.</span><span class="sxs-lookup"><span data-stu-id="2a19f-153">This has the effect of concatenating two transforms.</span></span> |
| `float3x2& operator*= (float3x2& value1, float value2)` | <span data-ttu-id="2a19f-154">Direkt multipliziert jede Komponente einer Matrix mit einem skalaren Wert.</span><span class="sxs-lookup"><span data-stu-id="2a19f-154">In-place multiplies each component of a matrix by a scalar value.</span></span> |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="2a19f-155">Bestimmt, ob zwei Instanzen von float3x2 gleich sind.</span><span class="sxs-lookup"><span data-stu-id="2a19f-155">Determines whether two instances of float3x2 are equal.</span></span> |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="2a19f-156">Bestimmt, ob zwei Instanzen von float3x2 nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="2a19f-156">Determines whether two instances of float3x2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | <span data-ttu-id="2a19f-157">Konvertiert ein float3x2-Zeichen in eine **Microsoft. Graphics. Canvas. Numerics. Matrix3x2**.</span><span class="sxs-lookup"><span data-stu-id="2a19f-157">Converts a float3x2 to a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="2a19f-158">Felder</span><span class="sxs-lookup"><span data-stu-id="2a19f-158">Fields</span></span>

| <span data-ttu-id="2a19f-159">Name</span><span class="sxs-lookup"><span data-stu-id="2a19f-159">Name</span></span> | <span data-ttu-id="2a19f-160">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a19f-160">Description</span></span> |
|-|-|
| `float m11` | <span data-ttu-id="2a19f-161">Wert in Zeile 1 Spalte 1 der Matrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-161">Value at row 1 column 1 of the matrix.</span></span> |
| `float m12` | <span data-ttu-id="2a19f-162">Wert in Zeile 1 Spalte 2 der Matrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-162">Value at row 1 column 2 of the matrix.</span></span> |
| `float m21` | <span data-ttu-id="2a19f-163">Wert in Zeile 2 Spalte 1 der Matrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-163">Value at row 2 column 1 of the matrix.</span></span> |
| `float m22` | <span data-ttu-id="2a19f-164">Wert in Zeile 2 Spalte 2 der Matrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-164">Value at row 2 column 2 of the matrix.</span></span> |
| `float m31` | <span data-ttu-id="2a19f-165">Wert in Zeile 3 Spalte 1 der Matrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-165">Value at row 3 column 1 of the matrix.</span></span> |
| `float m32` | <span data-ttu-id="2a19f-166">Wert in Zeile 3 Spalte 2 der Matrix.</span><span class="sxs-lookup"><span data-stu-id="2a19f-166">Value at row 3 column 2 of the matrix.</span></span> |

## <a name="requirements"></a><span data-ttu-id="2a19f-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a19f-167">Requirements</span></span>

| <span data-ttu-id="2a19f-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a19f-168">Requirement</span></span> | <span data-ttu-id="2a19f-169">Wert</span><span class="sxs-lookup"><span data-stu-id="2a19f-169">Value</span></span> |
|-|-|
| <span data-ttu-id="2a19f-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a19f-170">Namespace</span></span> | <span data-ttu-id="2a19f-171">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="2a19f-171">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="2a19f-172">Header</span><span class="sxs-lookup"><span data-stu-id="2a19f-172">Header</span></span> | <dl> <span data-ttu-id="2a19f-173"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a19f-173"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="2a19f-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a19f-174">See also</span></span>

[<span data-ttu-id="2a19f-175">windowsnumerics. h-APIs</span><span class="sxs-lookup"><span data-stu-id="2a19f-175">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
