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
# <a name="float3x2-structure"></a>float3x2-Struktur

Eine 3 x 2-Matrix, die für 2D-Transformationen verwendet wird.

Dieser Matrixtyp verwendet ein Zeilen Vektor Layout. Das x und y des Übersetzungs Vektors dieser Matrix entsprechen den Feldern M31, M32.

Dieser Typ ist nur in C++ verfügbar. Die .NET-Entsprechung ist [System. Numerics. Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).

## <a name="constructors"></a>Konstruktoren

| Name | BESCHREIBUNG |
|-|-|
| `float3x2()` | Erstellt ein nicht initialisiertes float3x2-. |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | Erstellt eine float3x2 mit den angegebenen Werten. |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | Konvertiert eine **Microsoft. Graphics. Canvas. Numerics. Matrix3x2** in eine float3x2. |

## <a name="functions"></a>Functions

| Name | BESCHREIBUNG |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | Erstellt eine Translationsmatrix. |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | Erstellt eine Translationsmatrix. |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | Erstellt eine Skalierungs Matrix, die auf dem Ursprung zentriert ist. |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | Erstellt eine Skalierungs Matrix, die auf dem angegebenen Punkt zentriert ist. |
| `float3x2 make_float3x2_scale(float2 const& scales)` | Erstellt eine Skalierungs Matrix, die auf dem Ursprung zentriert ist. |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | Erstellt eine Skalierungs Matrix, die auf dem angegebenen Punkt zentriert ist. |
| `float3x2 make_float3x2_scale(float scale)` | Erstellt eine Skalierungs Matrix, die auf dem Ursprung zentriert ist. |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | Erstellt eine Skalierungs Matrix, die auf dem angegebenen Punkt zentriert ist. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | Erstellt eine schiefe Matrix, die auf dem Ursprung zentriert ist. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | Erstellt eine schiefe Matrix, die auf den angegebenen Punkt zentriert ist. |
| `float3x2 make_float3x2_rotation(float radians)` | Erstellt eine Rotations Matrix, die auf dem Ursprung zentriert ist. |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | Erstellt eine Rotations Matrix, die auf den angegebenen Punkt zentriert ist. |
| `bool is_identity(float3x2 const& value)` | Überprüft, ob es sich um eine Identitätsmatrix handelt. |
| `float determinant(float3x2 const& value)` | Berechnet den Determinanten der Matrix. |
| `float2 translation(float3x2 const& value)` | Ruft den Übersetzungs Vektor der Matrix ab. |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | Berechnet den umgekehrten einer Matrix. Gibt true zurück, wenn die Matrix invertiert werden kann. andernfalls false. |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | Linearly interpoliert zwischen den entsprechenden Werten von zwei Matrizen. |

## <a name="methods"></a>Methoden

| Name | BESCHREIBUNG |
|-|-|
| `static float3x2 identity()` | Gibt eine Instanz der Identitätsmatrix zurück. |

## <a name="operators"></a>Operatoren

| Name | BESCHREIBUNG |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | Fügt jede Komponente einer Matrix einer anderen Matrix hinzu. |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | Subtrahiert jede Komponente einer Matrix von einer anderen Matrix. |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | Multipliziert eine Matrix mit einer anderen Matrix. Dies hat den Effekt, dass zwei Transformationen verkettet werden. |
| `float3x2 operator* (float3x2 const& value1, float value2)` | Multipliziert jede Komponente einer Matrix mit einem skalaren Wert. |
| `float3x2 operator- (float3x2 const& value)` | Negiert jede Komponente einer Matrix. |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | Direkt fügt jede Komponente einer Matrix einer anderen Matrix hinzu. |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | Direkt subtrahiert jede Komponente einer Matrix aus einer anderen Matrix. |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | Direkt multipliziert eine Matrix mit einer anderen Matrix. Dies hat den Effekt, dass zwei Transformationen verkettet werden. |
| `float3x2& operator*= (float3x2& value1, float value2)` | Direkt multipliziert jede Komponente einer Matrix mit einem skalaren Wert. |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | Bestimmt, ob zwei Instanzen von float3x2 gleich sind. |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | Bestimmt, ob zwei Instanzen von float3x2 nicht gleich sind. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | Konvertiert ein float3x2-Zeichen in eine **Microsoft. Graphics. Canvas. Numerics. Matrix3x2**. |

## <a name="fields"></a>Felder

| Name | BESCHREIBUNG |
|-|-|
| `float m11` | Wert in Zeile 1 Spalte 1 der Matrix. |
| `float m12` | Wert in Zeile 1 Spalte 2 der Matrix. |
| `float m21` | Wert in Zeile 2 Spalte 1 der Matrix. |
| `float m22` | Wert in Zeile 2 Spalte 2 der Matrix. |
| `float m31` | Wert in Zeile 3 Spalte 1 der Matrix. |
| `float m32` | Wert in Zeile 3 Spalte 2 der Matrix. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Namespace | Windows:: Foundation:: Numerics |
| Header | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[windowsnumerics. h-APIs](windowsnumerics-h-apis-portal.md)
