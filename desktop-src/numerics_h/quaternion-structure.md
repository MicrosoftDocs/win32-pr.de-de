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
# <a name="quaternion-structure"></a>Quaternion-Struktur

Ein vierdimensionaler Vektor, der zum Darstellen einer Drehung verwendet wird.

Eine Quaternion kann ein Objekt über den (x, y, z) Vektor durch den Winkel der Spitze, wobei w = cos (-TA/2) effizient gedreht wird, effizient drehen. Quaternionen werden in der Regel für eine reibungslose interpolsierung zwischen zwei Winkeln verwendet, um das Problem bei der Gimbal-Sperre zu vermeiden, das in eulwinkels auftreten kann.

Dieser Typ ist nur in C++ verfügbar. Die .NET-Entsprechung ist [System. Numerics. Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).

## <a name="constructors"></a>Konstruktoren

| Name | BESCHREIBUNG |
|-|-|
| `quaternion()` | Erstellt eine nicht initialisierte Quaternion. |
| `quaternion(float x, float y, float z, float w)` | Erstellt eine Quaternion mit den angegebenen Werten. |
| `quaternion(float3 vectorPart, float scalarPart)` | Erstellt eine Quaternion aus einem float3-und einem skalaren. |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | Konvertiert eine **Microsoft. Graphics. Canvas. Numerics. Quaternion** in eine Quaternion. |

## <a name="functions"></a>Functions

| Name | BESCHREIBUNG |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | Erstellt eine Quaternion aus einem Vektor und einen Winkel für die Drehung um den Vektor. |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | Erstellt eine Quaternion aus den angegebenen Ecken, der angegebenen Tonhöhe und den angegebenen Roll Winkeln. |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | Erstellt eine Quaternion aus einer Rotations Matrix. |
| `bool is_identity(quaternion const& value)` | Überprüft, ob es sich um eine Identitäts-Quaternion (keine Drehung) handelt. |
| `float length(quaternion const& value)` | Berechnet die Länge einer Quaternion. |
| `float length_squared(quaternion const& value)` | Berechnet die Quadrat Länge einer Quaternion. |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | Berechnet das Skalarprodukt von zwei Quaternionen. |
| `quaternion normalize(quaternion const& value)` | Dividiert jede Komponente einer Quaternion durch die Länge der Quaternion. |
| `quaternion conjugate(quaternion const& value)` | Berechnet die konjugierte einer Quaternion. |
| `quaternion inverse(quaternion const& value)` | Berechnet die Umkehrung einer Quaternion. |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | Interpoliert zwischen zwei Quaternionen mit der Methode der sphärischen linearen Interpolation. |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | Linearly interpoliert zwischen zwei Quaternionen. |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | Verkettet zwei Quaternionen. Das Ergebnis stellt die erste Drehung, gefolgt von der zweiten Drehung, dar. |

## <a name="methods"></a>Methoden

| Name | BESCHREIBUNG |
|-|-|
| `static quaternion identity()` | Gibt eine Instanz der Identitäts-Quaternion zurück. |

## <a name="operators"></a>Operatoren

| Name | BESCHREIBUNG |
|-|-|
| `quaternion operator+ (quaternion const& value1, quaternion const& value2)` | Addiert zwei Quaternionen. |
| `quaternion operator- (quaternion const& value1, quaternion const& value2)` | Subtrahiert eine Quaternion von einer anderen Quaternion. |
| `quaternion operator* (quaternion const& value1, quaternion const& value2)` | Multipliziert eine Quaternion mit einer anderen Quaternion. |
| `quaternion operator* (quaternion const& value1, float value2)` | Multipliziert eine Quaternion mit einem skalaren Wert. |
| `quaternion operator/ (quaternion const& value1, quaternion const& value2)` | Dividiert eine Quaternion durch eine andere Quaternion. |
| `quaternion operator- (quaternion const& value)` | Flippt das Vorzeichen jeder Komponente der Quaternion. |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | Direkt fügt zwei Quaternionen hinzu. |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | Direkt Subtrahiert eine Quaternion von einer anderen Quaternion. |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | Direkt multipliziert eine Quaternion von einer anderen Quaternion. |
| `quaternion& operator*= (quaternion& value1, float value2)` | Direkte nulswerte sind eine Quaternion durch einen Skalarwert. |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | Direkte unterteilt eine Quaternion durch eine andere Quaternion. |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | Bestimmt, ob zwei Instanzen von Quaternion gleich sind. |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | Bestimmt, ob zwei Instanzen von Quaternion nicht gleich sind. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | Konvertiert eine Quaternion in eine **Microsoft. Graphics. Canvas. Numerics. Quaternion**. |

## <a name="fields"></a>Felder

| Name | BESCHREIBUNG |
|-|-|
| `float x` | Der X-Wert der Vektor Komponente der Quaternion. |
| `float y` | Der Y-Wert der Vektor Komponente der Quaternion. |
| `float z` | Der Z-Wert der Vektor Komponente der Quaternion. |
| `float w` | Die Rotations Komponente der Quaternion. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Namespace | Windows:: Foundation:: Numerics |
| Header | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[windowsnumerics. h-APIs](windowsnumerics-h-apis-portal.md)
