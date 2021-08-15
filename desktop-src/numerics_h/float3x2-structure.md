---
title: float3x2-Struktur (Windowsnumerics.h)
description: Eine 3x2-Matrix, die für 2D-Transformationen verwendet wird.
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
ms.openlocfilehash: 24d403446fa3544bdb001c065e9874f812a829680e19a5e6b526ed12276fd6e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971759"
---
# <a name="float3x2-structure"></a>float3x2-Struktur

Eine 3x2-Matrix, die für 2D-Transformationen verwendet wird.

Dieser Matrixtyp verwendet ein Zeilenvektorlayout. Das x und das y des Übersetzungsvektors dieser Matrix entsprechen den Feldern m31, m32.

Dieser Typ ist nur in C++ verfügbar. Die entsprechende .NET-Datei [ist System.Numerics.Matrix3x2.](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8)

## <a name="constructors"></a>Konstruktoren

| Name | BESCHREIBUNG |
|-|-|
| `float3x2()` | Erstellt ein nicht initialisiertes float3x2. |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | Erstellt einen float3x2-Wert mit den angegebenen Werten. |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | Konvertiert eine **Microsoft.Graphics.Canvas.Numerics.Matrix3x2** in eine float3x2. |

## <a name="functions"></a>Functions

| Name | BESCHREIBUNG |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | Erstellt eine Translationsmatrix. |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | Erstellt eine Translationsmatrix. |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | Erstellt eine Skalierungsmatrix, die auf dem Ursprung zentriert ist. |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | Erstellt eine Skalierungsmatrix, die auf dem angegebenen Punkt zentriert ist. |
| `float3x2 make_float3x2_scale(float2 const& scales)` | Erstellt eine Skalierungsmatrix, die auf dem Ursprung zentriert ist. |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | Erstellt eine Skalierungsmatrix, die auf dem angegebenen Punkt zentriert ist. |
| `float3x2 make_float3x2_scale(float scale)` | Erstellt eine Skalierungsmatrix, die auf dem Ursprung zentriert ist. |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | Erstellt eine Skalierungsmatrix, die auf dem angegebenen Punkt zentriert ist. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | Erstellt eine Schiefematrix, die auf dem Ursprung zentriert ist. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | Erstellt eine Schiefematrix, die auf dem angegebenen Punkt zentriert ist. |
| `float3x2 make_float3x2_rotation(float radians)` | Erstellt eine Drehungsmatrix, die auf dem Ursprung zentriert ist. |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | Erstellt eine Drehungsmatrix, die auf dem angegebenen Punkt zentriert ist. |
| `bool is_identity(float3x2 const& value)` | Überprüft, ob es sich um eine Identitätsmatrix handelt. |
| `float determinant(float3x2 const& value)` | Berechnet die Determinante der Matrix. |
| `float2 translation(float3x2 const& value)` | Ruft den Übersetzungsvektor der Matrix ab. |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | Berechnet die Umkehrung einer Matrix. Gibt TRUE zurück, wenn die Matrix invertiert werden kann. Andernfalls false. |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | Interpoliert linear zwischen den entsprechenden Werten von zwei Matrizen. |

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
| `float3x2 operator* (float3x2 const& value1, float value2)` | Multipliziert jede Komponente einer Matrix mit einem Skalarwert. |
| `float3x2 operator- (float3x2 const& value)` | Negiert jede Komponente einer Matrix. |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | Fügt jede Komponente einer Matrix einer anderen Matrix hinzu. |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | In-place subtrahiert jede Komponente einer Matrix von einer anderen Matrix. |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | In-place multipliziert eine Matrix mit einer anderen Matrix. Dies hat den Effekt, dass zwei Transformationen verkettet werden. |
| `float3x2& operator*= (float3x2& value1, float value2)` | In-place multipliziert jede Komponente einer Matrix mit einem Skalarwert. |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | Bestimmt, ob zwei Instanzen von float3x2 gleich sind. |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | Bestimmt, ob zwei Instanzen von float3x2 nicht gleich sind. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | Konvertiert float3x2 in **microsoft.Graphics.Canvas.Numerics.Matrix3x2**. |

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
| Namespace | Windows::Foundation::Numerics |
| Header | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Weitere Informationen

[windowsnumerics.h-APIs](windowsnumerics-h-apis-portal.md)
