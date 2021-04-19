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
# <a name="float2-structure"></a>float2-Struktur

Ein Vektor mit zwei Komponenten.

Dieser Typ ist nur in C++ verfügbar. Die .NET-Entsprechung ist [System. Numerics. Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).

## <a name="constructors"></a>Konstruktoren

| Name | BESCHREIBUNG |
|-|-|
| `float2()` | Erstellt ein nicht initialisiertes float2-. |
| `float2(float x, float y)` | Erstellt eine float2 mit den angegebenen Werten. |
| `explicit float2(float value)` | Erstellt eine float2, bei der alle Komponenten auf den angegebenen Wert festgelegt sind. |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | Konvertiert eine **Microsoft. Graphics. Canvas. Numerics. Vector2** in eine float2. |
| `float2(Windows::Foundation::Point const& value)` | Konvertiert ein [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point) in eine float2. |
| `float2(Windows::Foundation::Size const& value)` | Konvertiert eine [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size) in eine float2. |

## <a name="functions"></a>Functions

| Name | BESCHREIBUNG |
|-|-|
| `float length(float2 const& value)` | Berechnet die Länge des Vektors (bzw. euklidische Entfernung). |
| `float length_squared(float2 const& value)` | Berechnet die Länge oder den euklidischen Abstand des Vektor Quadrates. |
| `float distance(float2 const& value1, float2 const& value2)` | Berechnet den euklidischen Abstand zwischen zwei Vektoren. |
| `float distance_squared(float2 const& value1, float2 const& value2)` | Berechnet den euklidischen Abstand zwischen zwei quadratischen Vektoren. |
| `float dot(float2 const& value1, float2 const& value2)` | Berechnet das Punktprodukt von zwei Vektoren. |
| `float2 normalize(float2 const& value)` | Erstellt einen Einheits Vektor aus dem angegebenen Vektor. |
| `float2 reflect(float2 const& vector, float2 const& normal)` | Bestimmt den reflektionvektor des angegebenen Vektors und des normalen. |
| `float2 min(float2 const& value1, float2 const& value2)` | Gibt einen Vektor zurück, der den niedrigsten Wert aus jedem übereinstimmenden paar von Komponenten enthält. |
| `float2 max(float2 const& value1, float2 const& value2)` | Gibt einen Vektor zurück, der den höchsten Wert aus jedem übereinstimmenden paar von Komponenten enthält. |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | Schränkt einen Wert in einen angegebenen Bereich ein. |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | Führt eine lineare interpolung zwischen zwei Vektoren aus. |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | Wandelt den Vektor (x, y, 0, 1) um die angegebene Matrix um. |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | Wandelt den Vektor (x, y, 0, 1) um die angegebene Matrix um. |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | Wandelt den normalen Vektor (x, y, 0, 0) um die angegebene Matrix um. |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | Wandelt den normalen Vektor (x, y, 0, 0) um die angegebene Matrix um. |
| `float2 transform(float2 const& value, quaternion const& rotation)` | Transformiert eine float2 durch die angegebene Quaternion. |

## <a name="methods"></a>Methoden

| Name | BESCHREIBUNG |
|-|-|
| `static float2 zero()` | Gibt eine float2 zurück, deren Komponenten auf 0 (null) festgelegt sind. |
| `static float2 one()` | Gibt einen float2-Wert zurück, dessen Komponenten auf einen Wert festgelegt sind. |
| `static float2 unit_x()` | Gibt float2 (1, 0) zurück. |
| `static float2 unit_y()` | Gibt float2 (0,0) zurück. |

## <a name="operators"></a>Operatoren

| Name | BESCHREIBUNG |
|-|-|
| `operator Windows::Foundation::Point() const` | Konvertiert ein float2-Zeichen in einen [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point). |
| `operator Windows::Foundation::Size() const` | Konvertiert ein float2-in eine [**Windows. Foundation. size-Klasse**](/uwp/api/Windows.Foundation.Size). |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | Addiert zwei Vektoren. |
| `float2 operator- (float2 const& value1, float2 const& value2)` | Subtrahiert einen Vektor von einem Vektor. |
| `float2 operator* (float2 const& value1, float2 const& value2)` | Multipliziert die Komponenten von zwei Vektoren untereinander. |
| `float2 operator* (float2 const& value1, float value2)` | Multipliziert einen Vektor mit einem skalaren. |
| `float2 operator* (float value1, float2 const& value2)` | Multipliziert einen Vektor mit einem skalaren. |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | Dividiert die Komponenten eines Vektors durch die Komponenten eines anderen Vektors. |
| `float2 operator/ (float2 const& value1, float value2)` | Dividiert einen Vektor durch einen Skalarwert. |
| `float2 operator- (float2 const& value)` | Gibt einen Vektor zurück, der in umgekehrter Richtung zeigt. |
| `float2& operator+= (float2& value1, float2 const& value2)` | Direkt fügt zwei Vektoren hinzu. |
| `float2& operator-= (float2& value1, float2 const& value2)` | Direkt subtrahiert einen Vektor von einem Vektor. |
| `float2& operator*= (float2& value1, float2 const& value2)` | Direkt multipliziert die Komponenten von zwei Vektoren miteinander. |
| `float2& operator*= (float2& value1, float value2)` | Direkt multipliziert einen Vektor mit einem skalaren. |
| `float2& operator/= (float2& value1, float2 const& value2)` | Direkt dividiert die Komponenten eines Vektors durch die Komponenten eines anderen Vektors. |
| `float2& operator/= (float2& value1, float value2)` | Direkt unterteilt einen Vektor durch einen Skalarwert. |
| `bool operator== (float2 const& value1, float2 const& value2)` | Bestimmt, ob zwei Instanzen von float2 gleich sind. |
| `bool operator!= (float2 const& value1, float2 const& value2)` | Bestimmt, ob zwei Instanzen von float2 nicht gleich sind. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | Konvertiert ein float2-Zeichen in eine **Microsoft. Graphics. Canvas. Numerics. Vector2**. |

## <a name="fields"></a>Felder

| Name | BESCHREIBUNG |
|-|-|
| `float x` | X-Komponente des Vektors. |
| `float y` | Y-Komponente des Vektors. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Namespace | Windows:: Foundation:: Numerics |
| Header | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[windowsnumerics. h-APIs](windowsnumerics-h-apis-portal.md)
