---
title: float4-Struktur (Windowsnumerics.h)
description: Ein Vektor mit vier Komponenten.
ms.assetid: AC07C6D0-E7FD-4582-B40D-4838F49FB8B4
keywords:
- float4-Struktur
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
ms.openlocfilehash: 4eb1af9bee9a571abf58fb20539945effc3ff1ee81cbb48a4d90c1510aebcd4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825280"
---
# <a name="float4-structure"></a>float4-Struktur

Ein Vektor mit vier Komponenten.

Dieser Typ ist nur in C++ verfügbar. Die .NET-Entsprechung ist [System.Numerics.Vector4.](/dotnet/api/system.numerics.vector4?view=netframework-4.8)

## <a name="constructors"></a>Konstruktoren

| Name | BESCHREIBUNG |
|-|-|
| `float4()` | Erstellt einen nicht initialisierten float4. |
| `float4(float x, float y, float z, float w)` | Erstellt eine float4-Datei mit den angegebenen Werten. |
| `float4(float2 value, float z, float w)` | Erstellt eine float4-Datei mit x und y, die aus einem float2-Wert sowie den angegebenen z- und w-Werten kopiert wurden. |
| `float4(float3 value, float w)` | Erstellt eine float4-Datei mit x, y und z, die aus einem float3-Wert zuzüglich des angegebenen w-Werts kopiert wurden. |
| `explicit float4(float value)` | Erstellt eine float4-Datei, bei der alle com.ents auf den angegebenen Wert festgelegt sind. |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | Konvertiert **microsoft.Graphics.Canvas.Numerics.Vector4** in float4. |

## <a name="functions"></a>Funktionen

| Name | BESCHREIBUNG |
|-|-|
| `float length(float4 const& value)` | Berechnet die Länge (euklidischer Abstand) des Vektors. |
| `float length_squared(float4 const& value)` | Berechnet die Länge oder euklidische Entfernung des Vektors im Quadrat. |
| `float distance(float4 const& value1, float4 const& value2)` | Berechnet den euklidischen Abstand zwischen zwei Vektoren. |
| `float distance_squared(float4 const& value1, float4 const& value2)` | Berechnet den euklidischen Abstand zwischen zwei quadratischen Vektoren. |
| `float dot(float4 const& vector1, float4 const& vector2)` | Berechnet das Punktprodukt von zwei Vektoren. |
| `float4 normalize(float4 const& vector)` | Erstellt einen Einheitenvektor aus dem angegebenen Vektor. |
| `float4 min(float4 const& value1, float4 const& value2)` | Gibt einen Vektor zurück, der den niedrigsten Wert aus jedem übereinstimmenden Komponentenpaar enthält. |
| `float4 max(float4 const& value1, float4 const& value2)` | Gibt einen Vektor zurück, der den höchsten Wert aus jedem übereinstimmenden Komponentenpaar enthält. |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | Schränkt einen Wert auf einen angegebenen Bereich ein. |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | Führt eine lineare Interpolation zwischen zwei Vektoren aus. |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | Transformiert einen float4-Typ durch die angegebene Matrix. |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | Transformiert einen float3-Typ durch die angegebene Matrix und gibt einen float4-Typ zurück. |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | Transformiert ein float2 durch die angegebene Matrix und gibt einen float4 zurück. |
| `float4 transform(float4 const& value, quaternion const& rotation)` | Transformiert float4 durch die angegebene Quaternion. |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | Transformiert einen float3 durch die angegebene Quaternion und gibt float4 zurück. |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | Transformiert ein float2 durch die angegebene Quaternion und gibt float4 zurück. |

## <a name="methods"></a>Methoden

| Name | BESCHREIBUNG |
|-|-|
| `static float4 zero()` | Gibt float4 zurück, wobei alle zugehörigen Komponenten auf 0 (null) festgelegt sind. |
| `static float4 one()` | Gibt float4 zurück, wobei alle zugehörigen Komponenten auf eins festgelegt sind. |
| `static float4 unit_x()` | Gibt float4 (1, 0, 0, 0) zurück. |
| `static float4 unit_y()` | Gibt float4 (0, 1, 0, 0) zurück. |
| `static float4 unit_z()` | Gibt float4 (0, 0, 1, 0) zurück. |
| `static float4 unit_w()` | Gibt float4 (0, 0, 0, 1) zurück. |

## <a name="operators"></a>Operatoren

| Name | BESCHREIBUNG |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | Fügt zwei Vektoren hinzu. |
| `float4 operator- (float4 const& value1, float4 const& value2)` | Subtrahiert einen Vektor von einem Vektor. |
| `float4 operator* (float4 const& value1, float4 const& value2)` | Multipliziert die Komponenten von zwei Vektoren miteinander. |
| `float4 operator* (float4 const& value1, float value2)` | Multipliziert einen Vektor mit einem Skalar. |
| `float4 operator* (float value1, float4 const& value2)` | Multipliziert einen Vektor mit einem Skalar. |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | Dividiert die Komponenten eines Vektors durch die Komponenten eines anderen Vektors. |
| `float4 operator/ (float4 const& value1, float value2)` | Dividiert einen Vektor durch einen Skalarwert. |
| `float4 operator- (float4 const& value)` | Gibt einen Vektor zurück, der in entgegengesetzter Richtung verweist. |
| `float4& operator+= (float4& value1, float4 const& value2)` | In-Place fügt zwei Vektoren hinzu. |
| `float4& operator-= (float4& value1, float4 const& value2)` | In-Place subtrahiert einen Vektor von einem Vektor. |
| `float4& operator*= (float4& value1, float4 const& value2)` | In-Place multipliziert die Komponenten von zwei Vektoren miteinander. |
| `float4& operator*= (float4& value1, float value2)` | In-Place multipliziert einen Vektor mit einem Skalar. |
| `float4& operator/= (float4& value1, float4 const& value2)` | Die Komponenten eines Vektors werden durch die Komponenten eines anderen Vektors dividiert. |
| `float4& operator/= (float4& value1, float value2)` | In-Place dividiert einen Vektor durch einen Skalarwert. |
| `bool operator== (float4 const& value1, float4 const& value2)` | Bestimmt, ob zwei Instanzen von float4 gleich sind. |
| `bool operator!= (float4 const& value1, float4 const& value2)` | Bestimmt, ob zwei Instanzen von float4 ungleich sind. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | Konvertiert float4 in **microsoft.Graphics.Canvas.Numerics.Vector4.** |

## <a name="fields"></a>Felder

| Name | BESCHREIBUNG |
|-|-|
| `float x` | X-Komponente des Vektors. |
| `float y` | Y-Komponente des Vektors. |
| `float z` | Z-Komponente des Vektors. |
| `float w` | W-Komponente des Vektors. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Namespace | Windows::Foundation::Numerics |
| Header | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[windowsnumerics.h-APIs](windowsnumerics-h-apis-portal.md)
