---
title: Plane-Struktur (windowsnumerics. h)
description: Diese Struktur stellt eine Ebene mit einem 3D-Vektor normal und einem Entfernungs Wert dar.
ms.assetid: 3C5A5EA0-8A51-4F9B-A84A-0C8E726CE3FD
keywords:
- Plane-Struktur
topic_type:
- apiref
api_name:
- plane structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d870e2769121b4aec542235081011406e439d579
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359797"
---
# <a name="plane-structure"></a>Plane-Struktur

Diese Struktur stellt eine Ebene mit einem 3D-Vektor normal und einem Entfernungs Wert dar.

Dieser Typ ist nur in C++ verfügbar. Die .NET-Entsprechung ist [System. Numerics. Plane](/dotnet/api/system.numerics.plane?view=netframework-4.8).

## <a name="constructors"></a>Konstruktoren

| Name | BESCHREIBUNG |
|-|-|
| `plane()` | Erstellt eine nicht initialisierte Ebene. |
| `plane(float x, float y, float z, float d)` | Erstellt eine Ebene mit den angegebenen Werten. |
| `plane(float3 normal, float d)` | Erstellt eine Ebene aus einem float3 und einer Entfernung. |
| `explicit plane(float4 value)` | Erstellt eine Ebene aus einer float4. |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | Konvertiert eine **Microsoft. Graphics. Canvas. Numerics. Plane** in eine Ebene. |

## <a name="functions"></a>Functions

| Name | BESCHREIBUNG |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | Erstellt eine Ebene aus einem Satz von drei Scheitelpunkt Positionen, die sich alle unterscheiden und sich nicht in einer geraden Linie befinden müssen. |
| `plane normalize(plane const& value)` | Ändert die Koeffizienten des normalen Vektors einer Ebene, um diese auf die Einheitslänge zu legen. |
| `plane transform(plane const& plane, float4x4 const& matrix)` | Transformiert eine normalisierte Ebene durch eine Matrix. |
| `plane transform(plane const& plane, quaternion const& rotation)` | Transformiert eine normalisierte Ebene durch eine quaternionrotation. |
| `float dot(plane const& plane, float4 const& value)` | Berechnet das Punktprodukt einer Ebene mit einem Vektor. |
| `float dot_coordinate(plane const& plane, float3 const& value)` | Berechnet das Punktprodukt einer Ebene mit einer float3-Koordinate. Anders als bei Punkt \_ Normal umfasst diese Berechnung den Wert der Ebene d. |
| `float dot_normal(plane const& plane, float3 const& value)` | Berechnet das Punktprodukt einer Ebene mit einer float3 normal. Anders als bei \_ der Punkt Koordinate ignoriert diese Berechnung den Wert der Ebene d. |

## <a name="operators"></a>Operatoren

| Name | BESCHREIBUNG |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | Bestimmt, ob zwei Instanzen der Ebene gleich sind. |
| `bool operator!= (plane const& value1, plane const& value2)` | Bestimmt, ob zwei Instanzen der Ebene nicht gleich sind. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | Konvertiert eine Ebene in eine **Microsoft. Graphics. Canvas. Numerics. Plane**. |

## <a name="fields"></a>Felder

| Name | BESCHREIBUNG |
|-|-|
| `float3 normal` | Normaler Vektor der Ebene. |
| `float d` | Abstand der Ebene entlang ihrer normalen vom Ursprung. |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Namespace | Windows:: Foundation:: Numerics |
| Header | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[windowsnumerics. h-APIs](windowsnumerics-h-apis-portal.md)
