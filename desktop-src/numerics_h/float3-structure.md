---
title: float3-Struktur (Windowsnumerics.h)
description: Ein Vektor mit drei Komponenten.
ms.assetid: CAA10ADA-C5A8-4B75-A0A9-5C5B3FDD9A07
keywords:
- float3-Struktur
topic_type:
- apiref
api_name:
- float3 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521c63f99c35e68f18d9a6c0a81118f647ff131effb0f6528e2ef3882c43e234
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939512"
---
# <a name="float3-structure"></a>float3-Struktur

Ein Vektor mit drei Komponenten.

Dieser Typ ist nur in C++ verfügbar. Seine .NET-Entsprechung ist [System.Numerics.Vector3.](/dotnet/api/system.numerics.vector3?view=netframework-4.8)

## <a name="constructors"></a>Konstruktoren

| Name | BESCHREIBUNG |
|-|-|
| `float3()` | Erstellt ein nicht initialisiertes float3. |
| `float3(float x, float y, float z)` | Erstellt einen float3-Wert mit den angegebenen Werten. |
| `float3(float2 value, float z)` | Erstellt eine float3-Datei mit x und y, die aus float2 plus dem angegebenen z-Wert kopiert wurden. |
| `explicit float3(float value)` | Erstellt einen float3-Wert, bei dem alle Komponenten auf den angegebenen Wert festgelegt sind. |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | Konvertiert **microsoft.Graphics.Canvas.Numerics.Vector3** in einen float3-Wert. |

## <a name="functions"></a>Funktionen

| Name | BESCHREIBUNG |
|-|-|
| `float length(float3 const& value)` | Berechnet die Länge oder euklidische Entfernung des Vektors. |
| `float length_squared(float3 const& value)` | Berechnet die Länge oder den euklidischen Abstand des vektorbasierten Quadrats. |
| `float distance(float3 const& value1, float3 const& value2)` | Berechnet den euklidischen Abstand zwischen zwei Vektoren. |
| `float distance_squared(float3 const& value1, float3 const& value2)` | Berechnet den euklidischen Abstand zwischen zwei Vektoren im Quadrat. |
| `float dot(float3 const& vector1, float3 const& vector2)` | Berechnet das Punktprodukt von zwei Vektoren. |
| `float3 normalize(float3 const& value)` | Erstellt einen Einheitenvektor aus dem angegebenen Vektor. |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | Berechnet das Kreuzprodukt zweier Vektoren. |
| `float3 reflect(float3 const& vector, float3 const& normal)` | Bestimmt den Reflektorvektor des angegebenen Vektors und normal. |
| `float3 min(float3 const& value1, float3 const& value2)` | Gibt einen Vektor zurück, der den niedrigsten Wert aus jedem übereinstimmenden Komponentenpaar enthält. |
| `float3 max(float3 const& value1, float3 const& value2)` | Gibt einen Vektor zurück, der den höchsten Wert aus jedem übereinstimmenden Komponentenpaar enthält. |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | Schränkt einen Wert ein, der innerhalb eines angegebenen Bereichs liegt. |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | Führt eine lineare Interpolation zwischen zwei Vektoren aus. |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | Transformiert den Vektor (x, y, z, 1) durch die angegebene Matrix. |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | Transformiert den normalen Vektor (x, y, z, 0) durch die angegebene Matrix. |
| `float3 transform(float3 const& value, quaternion const& rotation)` | Transformiert float3 um die gegebene Quaternion. |

## <a name="methods"></a>Methoden

| Name | BESCHREIBUNG |
|-|-|
| `static float3 zero()` | Gibt einen float3-Wert zurück, bei dem alle Komponenten auf 0 (null) festgelegt sind. |
| `static float3 one()` | Gibt einen float3-Wert zurück, bei dem alle Komponenten auf 1 festgelegt sind. |
| `static float3 unit_x()` | Gibt float3 (1, 0, 0) zurück. |
| `static float3 unit_y()` | Gibt float3 (0, 1, 0) zurück. |
| `static float3 unit_z()` | Gibt float3 (0, 0, 1) zurück. |

## <a name="operators"></a>Operatoren

| Name | BESCHREIBUNG |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | Fügt zwei Vektoren hinzu. |
| `float3 operator- (float3 const& value1, float3 const& value2)` | Subtrahiert einen Vektor von einem Vektor. |
| `float3 operator* (float3 const& value1, float3 const& value2)` | Multipliziert die Komponenten von zwei Vektoren miteinander. |
| `float3 operator* (float3 const& value1, float value2)` | Multipliziert einen Vektor mit einem Skalar. |
| `float3 operator* (float value1, float3 const& value2)` | Multipliziert einen Vektor mit einem Skalar. |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | Dividiert die Komponenten eines Vektors durch die Komponenten eines anderen Vektors. |
| `float3 operator/ (float3 const& value1, float value2)` | Dividiert einen Vektor durch einen Skalarwert. |
| `float3 operator- (float3 const& value)` | Gibt einen Vektor zurück, der in die entgegengesetzte Richtung zeigen soll. |
| `float3& operator+= (float3& value1, float3 const& value2)` | Fügt zwei Vektoren hinzu. |
| `float3& operator-= (float3& value1, float3 const& value2)` | In-place subtrahiert einen Vektor von einem Vektor. |
| `float3& operator*= (float3& value1, float3 const& value2)` | In-place multipliziert die Komponenten von zwei Vektoren miteinander. |
| `float3& operator*= (float3& value1, float value2)` | In-place multipliziert einen Vektor mit einem Skalar. |
| `float3& operator/= (float3& value1, float3 const& value2)` | In-place dividiert die Komponenten eines Vektors durch die Komponenten eines anderen Vektors. |
| `float3& operator/= (float3& value1, float value2)` | In-place dividiert einen Vektor durch einen Skalarwert. |
| `bool operator== (float3 const& value1, float3 const& value2)` | Bestimmt, ob zwei Instanzen von float3 gleich sind. |
| `bool operator!= (float3 const& value1, float3 const& value2)` | Bestimmt, ob zwei Instanzen von float3 nicht gleich sind. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | Konvertiert einen float3-Wert in **microsoft.Graphics.Canvas.Numerics.Vector3.** |

## <a name="fields"></a>Felder

| Name | BESCHREIBUNG |
|-|-|
| `float x` | X-Komponente des Vektors. |
| `float y` | Y-Komponente des Vektors. |
| `float z` | Z-Komponente des Vektors. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Namespace | Windows::Foundation::Numerics |
| Header | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[windowsnumerics.h-APIs](windowsnumerics-h-apis-portal.md)
