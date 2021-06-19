---
title: Direct3D 12-Raytracing, HLSL-Systemwertinterna
description: Hier finden Sie Links zu Artikeln, in denen systeminterne HlSL-Systemwertfunktionen (High-Level Shader Language, Shadersprache) beschrieben werden, die die Direct3D 12-Raytracingpipeline unterstützen.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2790cf5df42f64071db3ca51a35e58ee9afcd5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396435"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a>Direct3D 12-Raytracing, HLSL-Systemwertinterna

Systemwerte werden mithilfe spezieller intrinsischer Funktionen abgerufen, anstatt Parameter mit spezieller Semantik in Ihre Shaderfunktionssignatur ein- und zu übernehmen. 

## <a name="in-this-section"></a>In diesem Abschnitt

### <a name="ray-dispatch-system-values"></a>Ray Dispatch-Systemwerte

| Thema | Beschreibung |
|-|-|
| [**DispatchRaysIndex**](dispatchraysindex.md) | Ruft die aktuelle x- und y-Position innerhalb der Breite und Höhe ab, die mit dem **systeminternen DispatchRaysDimensions-Systemwert** ermittelt wird. |
| [**DispatchRaysDimensions**](dispatchraysdimensions.md) | Die Werte für Breite, Höhe und Tiefe der **D3D12 \_ DISPATCH \_ RAY \_ DESC-Struktur,** die im ursprünglichen **DispatchRays-Aufruf angegeben** sind. |

### <a name="ray-system-values"></a>Ray-Systemwerte

| Thema | Beschreibung |
|-|-|
| [**WorldRayOrigin**](worldrayorigin.md) | Der Ursprung des aktuellen Strahls in der Welt. |
| [**WorldRayDirection**](worldraydirection.md) | Die Weltraumrichtung für den aktuellen Strahl. |
| [**RayTMin**](raytmin.md) | Ein Gleitkommawert, der den aktuellen parametrischen Ausgangspunkt für den Strahl darstellt. |
| [**RayTCurrent**](raytcurrent.md) | Ein Gleitkommawert, der den aktuellen parametrischen Endpunkt für den Strahl darstellt.  |
| [**RayFlags**](rayflags.md) | Eine ganze Zahl ohne Vorzeichen, die die aktuellen **ray_flag** enthält. |

### <a name="primitiveobject-space-system-values"></a>Primitive/Objektraum-Systemwerte

| Thema | Beschreibung |
|-|-|
| [**InstanceIndex**](instanceindex.md) | Der automatisch generierte Index der aktuellen Instanz in der Raytracingbeschleunigungsstruktur der obersten Ebene. |
| [**Instanceid**](instanceid.md) | Der vom Benutzer bereitgestellte Bezeichner für die -Instanz in der Instanz der Beschleunigungsstruktur auf unterer Ebene innerhalb der Struktur der obersten Ebene. |
| [**PrimitiveIndex**](primitiveindex.md) | Der automatisch generierte Index des Primitiven innerhalb der Geometrie innerhalb der Instanz der Beschleunigungsstruktur auf unterer Ebene. |
| [**ObjectRayOrigin**](objectrayorigin.md) | Der Objektraum-Ursprung für den aktuellen Strahl. |
| [**ObjectRayDirection**](objectraydirection.md) | Die Objektraumrichtung für den aktuellen Strahl. |
| [**ObjectToWorld3x4**](objecttoworld3x4.md) | Eine Matrix für die Transformation von Objektraum in Raum. |
| [**ObjectToWorld4x3**](objecttoworld4x3.md) | Eine Matrix für die Transformation von Objektraum in Raum. |
| [**WorldToObject3x4**](worldtoobject3x4.md) | Eine Matrix für die Transformation vom Raum in den Objektraum |
| [**WorldToObject4x3**](worldtoobject4x3.md) | Eine Matrix für die Transformation vom Raum in den Objektraum |
### <a name="hit-specific-system-values"></a>Trefferspezifische Systemwerte

| Thema | Beschreibung |
|-|-|
| [**HitKind**](hitkind.md) | Gibt den Wert zurück, der als **HitKind-Parameter** an [**ReportHit übergeben wird.**](reporthit-function.md) |

## <a name="related-topics"></a>Zugehörige Themen

* [Kernreferenz](direct3d-12-core-reference.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)
