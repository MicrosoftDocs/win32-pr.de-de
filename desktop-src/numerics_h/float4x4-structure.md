---
title: float4x4-Struktur (windowsnumerics. h)
description: Eine 4 x 4-Matrix, die für 3D-Transformationen verwendet wird.
ms.assetid: C0D2198A-B547-4153-AD02-9A47835FD272
keywords:
- float4x4-Struktur
topic_type:
- apiref
api_name:
- float4x4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71c91de5eef404db33eff118568540be912d551d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361489"
---
# <a name="float4x4-structure"></a>float4x4-Struktur

Eine 4 x 4-Matrix, die für 3D-Transformationen verwendet wird.

Dieser Matrixtyp verwendet ein Zeilen Vektor Layout. Die x, y und z des Übersetzungs Vektors dieser Matrix entsprechen den Feldern M41, M42, M43.

Dieser Typ ist nur in C++ verfügbar. Die .NET-Entsprechung ist [System. Numerics. Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).

## <a name="constructors"></a>Konstruktoren

| Name | BESCHREIBUNG |
|-|-|
| `float4x4()` | Erstellt ein nicht initialisiertes float4x4-. |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | Erstellt eine float4x4 mit den angegebenen Werten. |
| `explicit float4x4(float3x2 value)` | Erstellt ein float4x4 aus einem float3x2. |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | Konvertiert eine **Microsoft. Graphics. Canvas. Numerics. Matrix4x4** in eine float4x4. |

## <a name="functions"></a>Functions

| Name | BESCHREIBUNG |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | Erstellt ein sphärisches Billboard, das um eine angegebene Objektposition rotiert, mithilfe eines Rechts gerichteten Koordinatensystems. |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | Erstellt ein zylindrisches Billboard, das um eine angegebene Achse rotiert, wobei ein rechts händiges Koordinatensystem verwendet wird. |
| `float4x4 make_float4x4_translation(float3 const& position)` | Erstellt eine Translationsmatrix. |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | Erstellt eine Translationsmatrix. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | Erstellt eine Skalierungs Matrix, die auf dem Ursprung zentriert ist. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | Erstellt eine Skalierungs Matrix, die auf dem angegebenen Punkt zentriert ist. |
| `float4x4 make_float4x4_scale(float3 const& scales)` | Erstellt eine Skalierungs Matrix, die auf dem Ursprung zentriert ist. |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | Erstellt eine Skalierungs Matrix, die auf dem angegebenen Punkt zentriert ist. |
| `float4x4 make_float4x4_scale(float scale)` | Erstellt eine Skalierungs Matrix, die auf dem Ursprung zentriert ist. |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | Erstellt eine Skalierungs Matrix, die auf dem angegebenen Punkt zentriert ist. |
| `float4x4 make_float4x4_rotation_x(float radians)` | Erstellt eine Drehungs Matrix der x-Achse, die auf dem Ursprung zentriert ist. |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | Erstellt eine Drehungs Matrix der x-Achse, die auf dem angegebenen Punkt zentriert ist. |
| `float4x4 make_float4x4_rotation_y(float radians)` | Erstellt eine y-Achse-Rotations Matrix, die sich auf den Ursprung konzentriert. |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | Erstellt eine y-Achse-Rotations Matrix, die sich auf den angegebenen Punkt konzentriert. |
| `float4x4 make_float4x4_rotation_z(float radians)` | Erstellt eine z-Achsen-Rotations Matrix, die auf dem Ursprung zentriert ist. |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | Erstellt eine z-Achsen-Rotations Matrix, die auf den angegebenen Punkt zentriert ist. |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | Erstellt eine Matrix, die um einen beliebigen Vektor rotiert. |
| `float4x4 make_float4x4_?perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | Erstellt eine perspektivische Projektions Matrix basierend auf einem Sichtfeld mithilfe eines Rechts gerichteten Koordinatensystems. |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | Erstellt mithilfe eines Rechts gerichteten Koordinatensystems eine perspektivische Projektions Matrix. |
| `float4x4 make_float4x4_?perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | Erstellt mithilfe eines Rechts gerichteten Koordinatensystems eine angepasste perspektivische Projektions Matrix. |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | Erstellt eine orthografische Projektions Matrix mithilfe eines Rechts gerichteten Koordinatensystems. |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | Erstellt eine angepasste orthografische Projektions Matrix mithilfe eines Rechts gerichteten Koordinatensystems. |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | Erstellt eine Ansichts Matrix mithilfe eines Rechts gerichteten Koordinatensystems. |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | Erstellt eine Weltmatrix mithilfe eines Rechts gerichteten Koordinatensystems. Dies kann verwendet werden, um Objekte in 3D-Raum zu positionieren. |
| `float4x4 make_float4x4_?from_quaternion(quaternion const& quaternion)` | Erstellt eine Rotations Matrix aus einer Quaternion. |
| `float4x4 make_float4x4_?from_yaw_pitch_roll(float yaw, float pitch, float roll)` | Erstellt eine Rotations Matrix aus einem angegebenen Yaw, einer angegebenen Tonhöhe und einem angegebenen Rollout. |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | Erstellt eine Matrix, die Geometrie auf einer angegebenen Ebene flach darstellt, als ob eine angegebene Lichtquelle einen Schatten wirft. |
| `float4x4 make_float4x4_reflection(plane const& value)` | Erstellt eine Matrix, die das Koordinatensystem auf einer angegebenen Ebene wiedergibt. |
| `bool is_identity(float4x4 const& value)` | Überprüft, ob es sich um eine Identitätsmatrix handelt. |
| `float determinant(float4x4 const& value)` | Berechnet den Determinanten der Matrix. |
| `float3 translation(float4x4 const& value)` | Ruft den Übersetzungs Vektor der Matrix ab. |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | Berechnet den umgekehrten einer Matrix. Gibt true zurück, wenn die Matrix invertiert werden kann. andernfalls false. |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | Extrahiert die skalaren, Verschiebungs-und Rotations Komponenten aus einer 3D-Skala/Drehung/Übersetzung (SRT)-Matrix. Gibt true zurück, wenn die Matrix zerlegt werden kann. andernfalls false. |
| `float4x4 transform(float4x4 const& value, quaternion const& rotation)` | Transformiert eine Matrix durch Anwenden einer quaternionrotation. |
| `float4x4 transpose(float4x4 const& matrix)` | Vertauscht die Komponenten einer Matrix entlang der Diagonal. |
| `float4x4 lerp(float4x4 const& matrix1, float4x4 const& matrix2, float amount)` | Linearly interpoliert zwischen den entsprechenden Werten von zwei Matrizen. |

## <a name="methods"></a>Methoden

| Name | BESCHREIBUNG |
|-|-|
| `static float4x4 identity()` | Gibt eine Instanz der Identitätsmatrix zurück. |

## <a name="operators"></a>Operatoren

| Name | BESCHREIBUNG |
|-|-|
| `float4x4 operator+ (float4x4 const& value1, float4x4 const& value2)` | Fügt jede Komponente einer Matrix einer anderen Matrix hinzu. |
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | Subtrahiert jede Komponente einer Matrix von einer anderen Matrix. |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | Multipliziert eine Matrix mit einer anderen Matrix. Dies hat den Effekt, dass zwei Transformationen verkettet werden. |
| `float4x4 operator* (float4x4 const& value1, float value2)` | Multipliziert jede Komponente einer Matrix mit einem skalaren Wert. |
| `float4x4 operator- (float4x4 const& value)` | Negiert jede Komponente einer Matrix. |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | Direkt fügt jede Komponente einer Matrix einer anderen Matrix hinzu. |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | Direkt subtrahiert jede Komponente einer Matrix aus einer anderen Matrix. |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | Direkt multipliziert eine Matrix mit einer anderen Matrix. Dies hat den Effekt, dass zwei Transformationen verkettet werden. |
| `float4x4& operator*= (float4x4& value1, float value2)` | Direkt multipliziert jede Komponente einer Matrix mit einem skalaren Wert. |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | Bestimmt, ob zwei Instanzen von float4x4 gleich sind. |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | Bestimmt, ob zwei Instanzen von float4x4 nicht gleich sind. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | Konvertiert ein float4x4-Zeichen in eine **Microsoft. Graphics. Canvas. Numerics. Matrix4x4**. |

## <a name="fields"></a>Felder

| Name | BESCHREIBUNG |
|-|-|
| `float m11` | Wert in Zeile 1 Spalte 1 der Matrix. |
| `float m12` | Wert in Zeile 1 Spalte 2 der Matrix. |
| `float m13` | Wert in Zeile 1 Spalte 3 der Matrix. |
| `float m14` | Wert in Zeile 1 Spalte 4 der Matrix. |
| `float m21` | Wert in Zeile 2 Spalte 1 der Matrix. |
| `float m22` | Wert in Zeile 2 Spalte 2 der Matrix. |
| `float m23` | Wert in Zeile 2 Spalte 3 der Matrix. |
| `float m24` | Wert in Zeile 2 Spalte 4 der Matrix. |
| `float m31` | Wert in Zeile 3 Spalte 1 der Matrix. |
| `float m32` | Wert in Zeile 3 Spalte 2 der Matrix. |
| `float m33` | Wert in Zeile 3 Spalte 3 der Matrix. |
| `float m34` | Wert in Zeile 3 Spalte 4 der Matrix. |
| `float m41` | Wert in Zeile 4 Spalte 1 der Matrix. |
| `float m42` | Wert in Zeile 4 Spalte 2 der Matrix. |
| `float m43` | Wert in Zeile 4 Spalte 3 der Matrix. |
| `float m44` | Wert in Zeile 4 Spalte 4 der Matrix. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Namespace | Windows:: Foundation:: Numerics |
| Header | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[windowsnumerics. h-APIs](windowsnumerics-h-apis-portal.md)
