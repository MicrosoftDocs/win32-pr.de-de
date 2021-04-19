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
# <a name="float4-structure"></a>FLOAT4-Struktur

Ein Vektor mit vier Komponenten.

Dieser Typ ist nur in C++ verfügbar. Die .NET-Entsprechung ist [System. Numerics. Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).

## <a name="constructors"></a>Konstruktoren

| Name | BESCHREIBUNG |
|-|-|
| `float4()` | Erstellt ein nicht initialisiertes float4-. |
| `float4(float x, float y, float z, float w)` | Erstellt eine float4 mit den angegebenen Werten. |
| `float4(float2 value, float z, float w)` | Erstellt ein float4 mit x und y, das aus einem float2 plus den angegebenen z-und w-Werten kopiert wurde. |
| `float4(float3 value, float w)` | Erstellt ein float4 mit x, y und z, das aus einem float3 plus dem angegebenen w-Wert kopiert wurde. |
| `explicit float4(float value)` | Erstellt ein float4-Wert, bei dem alle com. ents auf den angegebenen Wert festgelegt sind. |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | Konvertiert eine **Microsoft. Graphics. Canvas. Numerics. Vector4** in eine float4. |

## <a name="functions"></a>Functions

| Name | BESCHREIBUNG |
|-|-|
| `float length(float4 const& value)` | Berechnet die Länge des Vektors (bzw. euklidische Entfernung). |
| `float length_squared(float4 const& value)` | Berechnet die Länge oder den euklidischen Abstand des Vektor Quadrates. |
| `float distance(float4 const& value1, float4 const& value2)` | Berechnet den euklidischen Abstand zwischen zwei Vektoren. |
| `float distance_squared(float4 const& value1, float4 const& value2)` | Berechnet den euklidischen Abstand zwischen zwei quadratischen Vektoren. |
| `float dot(float4 const& vector1, float4 const& vector2)` | Berechnet das Punktprodukt von zwei Vektoren. |
| `float4 normalize(float4 const& vector)` | Erstellt einen Einheits Vektor aus dem angegebenen Vektor. |
| `float4 min(float4 const& value1, float4 const& value2)` | Gibt einen Vektor zurück, der den niedrigsten Wert aus jedem übereinstimmenden paar von Komponenten enthält. |
| `float4 max(float4 const& value1, float4 const& value2)` | Gibt einen Vektor zurück, der den höchsten Wert aus jedem übereinstimmenden paar von Komponenten enthält. |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | Schränkt einen Wert in einen angegebenen Bereich ein. |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | Führt eine lineare interpolung zwischen zwei Vektoren aus. |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | Transformiert eine float4 durch die angegebene Matrix. |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | Transformiert eine float3 durch die angegebene Matrix und gibt eine float4 zurück. |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | Transformiert eine float2 durch die angegebene Matrix und gibt eine float4 zurück. |
| `float4 transform(float4 const& value, quaternion const& rotation)` | Transformiert eine float4 durch die angegebene Quaternion. |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | Transformiert eine float3 durch die angegebene Quaternion und gibt eine float4 zurück. |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | Transformiert eine float2 durch die angegebene Quaternion und gibt eine float4 zurück. |

## <a name="methods"></a>Methoden

| Name | BESCHREIBUNG |
|-|-|
| `static float4 zero()` | Gibt eine float4 zurück, deren Komponenten auf 0 (null) festgelegt sind. |
| `static float4 one()` | Gibt einen float4-Wert zurück, dessen Komponenten auf einen Wert festgelegt sind. |
| `static float4 unit_x()` | Gibt FLOAT4 (1, 0, 0, 0) zurück. |
| `static float4 unit_y()` | Gibt FLOAT4 (0, 1, 0, 0) zurück. |
| `static float4 unit_z()` | Gibt FLOAT4 (0,0) zurück. |
| `static float4 unit_w()` | Gibt FLOAT4 (0,0) zurück. |

## <a name="operators"></a>Operatoren

| Name | BESCHREIBUNG |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | Addiert zwei Vektoren. |
| `float4 operator- (float4 const& value1, float4 const& value2)` | Subtrahiert einen Vektor von einem Vektor. |
| `float4 operator* (float4 const& value1, float4 const& value2)` | Multipliziert die Komponenten von zwei Vektoren untereinander. |
| `float4 operator* (float4 const& value1, float value2)` | Multipliziert einen Vektor mit einem skalaren. |
| `float4 operator* (float value1, float4 const& value2)` | Multipliziert einen Vektor mit einem skalaren. |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | Dividiert die Komponenten eines Vektors durch die Komponenten eines anderen Vektors. |
| `float4 operator/ (float4 const& value1, float value2)` | Dividiert einen Vektor durch einen Skalarwert. |
| `float4 operator- (float4 const& value)` | Gibt einen Vektor zurück, der in umgekehrter Richtung zeigt. |
| `float4& operator+= (float4& value1, float4 const& value2)` | Direkt fügt zwei Vektoren hinzu. |
| `float4& operator-= (float4& value1, float4 const& value2)` | Direkt subtrahiert einen Vektor von einem Vektor. |
| `float4& operator*= (float4& value1, float4 const& value2)` | Direkt multipliziert die Komponenten von zwei Vektoren miteinander. |
| `float4& operator*= (float4& value1, float value2)` | Direkt multipliziert einen Vektor mit einem skalaren. |
| `float4& operator/= (float4& value1, float4 const& value2)` | Direkt dividiert die Komponenten eines Vektors durch die Komponenten eines anderen Vektors. |
| `float4& operator/= (float4& value1, float value2)` | Direkt unterteilt einen Vektor durch einen Skalarwert. |
| `bool operator== (float4 const& value1, float4 const& value2)` | Bestimmt, ob zwei Instanzen von float4 gleich sind. |
| `bool operator!= (float4 const& value1, float4 const& value2)` | Bestimmt, ob zwei Instanzen von float4 nicht gleich sind. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | Konvertiert ein float4-Zeichen in eine **Microsoft. Graphics. Canvas. Numerics. Vector4**. |

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
| Namespace | Windows:: Foundation:: Numerics |
| Header | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[windowsnumerics. h-APIs](windowsnumerics-h-apis-portal.md)
