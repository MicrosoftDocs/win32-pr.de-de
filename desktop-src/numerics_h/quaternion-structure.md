---
title: Quaternion-Struktur (windowsnumerics. h)
description: Ein vierdimensionaler Vektor, der zum Darstellen einer Drehung verwendet wird.
ms.assetid: A6B25885-8ECB-4039-9DC6-41D5F3A02489
keywords:
- Quaternion-Struktur
topic_type:
- apiref
api_name:
- quaternion structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ae169232f83e6753505f9d5d07fffac09e67e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359796"
---
# <a name="quaternion-structure"></a><span data-ttu-id="79e72-104">Quaternion-Struktur</span><span class="sxs-lookup"><span data-stu-id="79e72-104">quaternion Structure</span></span>

<span data-ttu-id="79e72-105">Ein vierdimensionaler Vektor, der zum Darstellen einer Drehung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="79e72-105">A four dimensional vector, used to represent a rotation.</span></span>

<span data-ttu-id="79e72-106">Eine Quaternion kann ein Objekt über den (x, y, z) Vektor durch den Winkel der Spitze, wobei w = cos (-TA/2) effizient gedreht wird, effizient drehen.</span><span class="sxs-lookup"><span data-stu-id="79e72-106">A quaternion can efficiently rotate an object about the (x, y, z) vector by the angle theta, where w = cos(theta/2).</span></span> <span data-ttu-id="79e72-107">Quaternionen werden in der Regel für eine reibungslose interpolsierung zwischen zwei Winkeln verwendet, um das Problem bei der Gimbal-Sperre zu vermeiden, das in eulwinkels auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="79e72-107">Quaternions are typically used for smooth interpolation between two angles, and for avoiding the gimbal lock problem that can occur with Euler angles.</span></span>

<span data-ttu-id="79e72-108">Dieser Typ ist nur in C++ verfügbar.</span><span class="sxs-lookup"><span data-stu-id="79e72-108">This type is available only in C++.</span></span> <span data-ttu-id="79e72-109">Die .NET-Entsprechung ist [System. Numerics. Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="79e72-109">Its .NET equivalent is [System.Numerics.Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="79e72-110">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="79e72-110">Constructors</span></span>

| <span data-ttu-id="79e72-111">Name</span><span class="sxs-lookup"><span data-stu-id="79e72-111">Name</span></span> | <span data-ttu-id="79e72-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79e72-112">Description</span></span> |
|-|-|
| `quaternion()` | <span data-ttu-id="79e72-113">Erstellt eine nicht initialisierte Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-113">Creates an uninitialized quaternion.</span></span> |
| `quaternion(float x, float y, float z, float w)` | <span data-ttu-id="79e72-114">Erstellt eine Quaternion mit den angegebenen Werten.</span><span class="sxs-lookup"><span data-stu-id="79e72-114">Creates a quaternion with the specified values.</span></span> |
| `quaternion(float3 vectorPart, float scalarPart)` | <span data-ttu-id="79e72-115">Erstellt eine Quaternion aus einem float3-und einem skalaren.</span><span class="sxs-lookup"><span data-stu-id="79e72-115">Creates a quaternion from a float3 and scalar.</span></span> |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | <span data-ttu-id="79e72-116">Konvertiert eine **Microsoft. Graphics. Canvas. Numerics. Quaternion** in eine Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Quaternion** to a quaternion.</span></span> |

## <a name="functions"></a><span data-ttu-id="79e72-117">Functions</span><span class="sxs-lookup"><span data-stu-id="79e72-117">Functions</span></span>

| <span data-ttu-id="79e72-118">Name</span><span class="sxs-lookup"><span data-stu-id="79e72-118">Name</span></span> | <span data-ttu-id="79e72-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79e72-119">Description</span></span> |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | <span data-ttu-id="79e72-120">Erstellt eine Quaternion aus einem Vektor und einen Winkel für die Drehung um den Vektor.</span><span class="sxs-lookup"><span data-stu-id="79e72-120">Creates a quaternion from a vector and an angle to rotate about the vector.</span></span> |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | <span data-ttu-id="79e72-121">Erstellt eine Quaternion aus den angegebenen Ecken, der angegebenen Tonhöhe und den angegebenen Roll Winkeln.</span><span class="sxs-lookup"><span data-stu-id="79e72-121">Creates a quaternion from specified yaw, pitch, and roll angles.</span></span> |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | <span data-ttu-id="79e72-122">Erstellt eine Quaternion aus einer Rotations Matrix.</span><span class="sxs-lookup"><span data-stu-id="79e72-122">Creates a quaternion from a rotation matrix.</span></span> |
| `bool is_identity(quaternion const& value)` | <span data-ttu-id="79e72-123">Überprüft, ob es sich um eine Identitäts-Quaternion (keine Drehung) handelt.</span><span class="sxs-lookup"><span data-stu-id="79e72-123">Checks whether this is an identity (no rotation) quaternion.</span></span> |
| `float length(quaternion const& value)` | <span data-ttu-id="79e72-124">Berechnet die Länge einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-124">Calculates the length of a quaternion.</span></span> |
| `float length_squared(quaternion const& value)` | <span data-ttu-id="79e72-125">Berechnet die Quadrat Länge einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-125">Calculates the length squared of a quaternion.</span></span> |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | <span data-ttu-id="79e72-126">Berechnet das Skalarprodukt von zwei Quaternionen.</span><span class="sxs-lookup"><span data-stu-id="79e72-126">Calculates the dot product of two quaternions.</span></span> |
| `quaternion normalize(quaternion const& value)` | <span data-ttu-id="79e72-127">Dividiert jede Komponente einer Quaternion durch die Länge der Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-127">Divides each component of a quaternion by the length of the quaternion.</span></span> |
| `quaternion conjugate(quaternion const& value)` | <span data-ttu-id="79e72-128">Berechnet die konjugierte einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-128">Calculates the conjugate of a quaternion.</span></span> |
| `quaternion inverse(quaternion const& value)` | <span data-ttu-id="79e72-129">Berechnet die Umkehrung einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-129">Calculates the inverse of a quaternion.</span></span> |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="79e72-130">Interpoliert zwischen zwei Quaternionen mit der Methode der sphärischen linearen Interpolation.</span><span class="sxs-lookup"><span data-stu-id="79e72-130">Interpolates between two quaternions, using spherical linear interpolation.</span></span> |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="79e72-131">Linearly interpoliert zwischen zwei Quaternionen.</span><span class="sxs-lookup"><span data-stu-id="79e72-131">Linearly interpolates between two quaternions.</span></span> |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="79e72-132">Verkettet zwei Quaternionen. Das Ergebnis stellt die erste Drehung, gefolgt von der zweiten Drehung, dar.</span><span class="sxs-lookup"><span data-stu-id="79e72-132">Concatenates two quaternions; the result represents the first rotation followed by the second rotation.</span></span> |

## <a name="methods"></a><span data-ttu-id="79e72-133">Methoden</span><span class="sxs-lookup"><span data-stu-id="79e72-133">Methods</span></span>

| <span data-ttu-id="79e72-134">Name</span><span class="sxs-lookup"><span data-stu-id="79e72-134">Name</span></span> | <span data-ttu-id="79e72-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79e72-135">Description</span></span> |
|-|-|
| `static quaternion identity()` | <span data-ttu-id="79e72-136">Gibt eine Instanz der Identitäts-Quaternion zurück.</span><span class="sxs-lookup"><span data-stu-id="79e72-136">Returns an instance of the identity quaternion.</span></span> |

## <a name="operators"></a><span data-ttu-id="79e72-137">Operatoren</span><span class="sxs-lookup"><span data-stu-id="79e72-137">Operators</span></span>

| <span data-ttu-id="79e72-138">Name</span><span class="sxs-lookup"><span data-stu-id="79e72-138">Name</span></span> | <span data-ttu-id="79e72-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79e72-139">Description</span></span> |
|-|-|
| `quaternion operator+ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="79e72-140">Addiert zwei Quaternionen.</span><span class="sxs-lookup"><span data-stu-id="79e72-140">Adds two quaternions.</span></span> |
| `quaternion operator- (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="79e72-141">Subtrahiert eine Quaternion von einer anderen Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-141">Subtracts a quaternion from another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="79e72-142">Multipliziert eine Quaternion mit einer anderen Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-142">Multiplies a quaternion by another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, float value2)` | <span data-ttu-id="79e72-143">Multipliziert eine Quaternion mit einem skalaren Wert.</span><span class="sxs-lookup"><span data-stu-id="79e72-143">Multiplies a quaternion by a scalar value.</span></span> |
| `quaternion operator/ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="79e72-144">Dividiert eine Quaternion durch eine andere Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-144">Divides a quaternion by another quaternion.</span></span> |
| `quaternion operator- (quaternion const& value)` | <span data-ttu-id="79e72-145">Flippt das Vorzeichen jeder Komponente der Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-145">Flips the sign of each component of the quaternion.</span></span> |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="79e72-146">Direkt fügt zwei Quaternionen hinzu.</span><span class="sxs-lookup"><span data-stu-id="79e72-146">In-place adds two quaternions.</span></span> |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="79e72-147">Direkt Subtrahiert eine Quaternion von einer anderen Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-147">In-place subtracts a quaternion from another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="79e72-148">Direkt multipliziert eine Quaternion von einer anderen Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-148">In-place multiplies a quaternion by another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, float value2)` | <span data-ttu-id="79e72-149">Direkte nulswerte sind eine Quaternion durch einen Skalarwert.</span><span class="sxs-lookup"><span data-stu-id="79e72-149">In-place nultiplies a quaternion by a scalar value.</span></span> |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="79e72-150">Direkte unterteilt eine Quaternion durch eine andere Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-150">In-place divides a quaternion by another quaternion.</span></span> |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="79e72-151">Bestimmt, ob zwei Instanzen von Quaternion gleich sind.</span><span class="sxs-lookup"><span data-stu-id="79e72-151">Determines whether two instances of quaternion are equal.</span></span> |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="79e72-152">Bestimmt, ob zwei Instanzen von Quaternion nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="79e72-152">Determines whether two instances of quaternion are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | <span data-ttu-id="79e72-153">Konvertiert eine Quaternion in eine **Microsoft. Graphics. Canvas. Numerics. Quaternion**.</span><span class="sxs-lookup"><span data-stu-id="79e72-153">Converts a quaternion to a **Microsoft.Graphics.Canvas.Numerics.Quaternion**.</span></span> |

## <a name="fields"></a><span data-ttu-id="79e72-154">Felder</span><span class="sxs-lookup"><span data-stu-id="79e72-154">Fields</span></span>

| <span data-ttu-id="79e72-155">Name</span><span class="sxs-lookup"><span data-stu-id="79e72-155">Name</span></span> | <span data-ttu-id="79e72-156">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79e72-156">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="79e72-157">Der X-Wert der Vektor Komponente der Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-157">X value of the vector component of the quaternion.</span></span> |
| `float y` | <span data-ttu-id="79e72-158">Der Y-Wert der Vektor Komponente der Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-158">Y value of the vector component of the quaternion.</span></span> |
| `float z` | <span data-ttu-id="79e72-159">Der Z-Wert der Vektor Komponente der Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-159">Z value of the vector component of the quaternion.</span></span> |
| `float w` | <span data-ttu-id="79e72-160">Die Rotations Komponente der Quaternion.</span><span class="sxs-lookup"><span data-stu-id="79e72-160">Rotation component of the quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="79e72-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79e72-161">Requirements</span></span>

| <span data-ttu-id="79e72-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79e72-162">Requirement</span></span> | <span data-ttu-id="79e72-163">Wert</span><span class="sxs-lookup"><span data-stu-id="79e72-163">Value</span></span> |
|-|-|
| <span data-ttu-id="79e72-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="79e72-164">Namespace</span></span> | <span data-ttu-id="79e72-165">Windows:: Foundation:: Numerics</span><span class="sxs-lookup"><span data-stu-id="79e72-165">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="79e72-166">Header</span><span class="sxs-lookup"><span data-stu-id="79e72-166">Header</span></span> | <dl> <span data-ttu-id="79e72-167"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="79e72-167"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="79e72-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79e72-168">See also</span></span>

[<span data-ttu-id="79e72-169">windowsnumerics. h-APIs</span><span class="sxs-lookup"><span data-stu-id="79e72-169">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
