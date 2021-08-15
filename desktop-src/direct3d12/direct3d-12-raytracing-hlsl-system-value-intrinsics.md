---
title: Direct3D 12-Raytracing, HLSL-Systemwertinterna
description: Sehen Sie sich Links zu Artikeln an, in denen systeminterne HlSL-Systemwertfunktionen (High-Level Shader Language) beschrieben werden, die die Direct3D 12-Raytracingpipeline unterstützen.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b2a2cbd870da41df94ee0389757a1d1ec7cd5e4549a3abd32dbaaf6a7c8e8e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045558"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a>Direct3D 12-Raytracing, HLSL-Systemwertinterna

Systemwerte werden mithilfe spezieller systeminterner Funktionen abgerufen, anstatt Parameter mit spezieller Semantik in ihre Shaderfunktionssignatur zu einschließen. 

## <a name="in-this-section"></a>In diesem Abschnitt

### <a name="ray-dispatch-system-values"></a>Ray Dispatch-Systemwerte

| Thema | BESCHREIBUNG |
|-|-|
| [**DispatchRaysIndex**](dispatchraysindex.md) | Ruft die aktuelle x- und y-Position innerhalb der Breite und Höhe ab, die mit dem **systeminternen DispatchRaysDimensions-Systemwert** abgerufen werden. |
| [**DispatchRaysDimensions**](dispatchraysdimensions.md) | Die Im ursprünglichen **DispatchRays-Aufruf** angegebenen Werte für Breite, Höhe und Tiefe aus der **D3D12 \_ DISPATCH RAY \_ \_ DESC-Struktur.** |

### <a name="ray-system-values"></a>Raysystemwerte

| Thema | BESCHREIBUNG |
|-|-|
| [**WorldRayOrigin**](worldrayorigin.md) | Der Ursprung des aktuellen Strahls im Raum. |
| [**WorldRayDirection**](worldraydirection.md) | Die Weltraumrichtung für den aktuellen Strahl. |
| [**RayTMin**](raytmin.md) | Ein gleitkommawert, der den aktuellen parametrischen Startpunkt für den Strahl darstellt. |
| [**RayTCurrent**](raytcurrent.md) | Ein Gleitkommawert, der den aktuellen parametrischen Endpunkt für den Strahl darstellt.  |
| [**RayFlags**](rayflags.md) | Eine ganze Zahl ohne Vorzeichen, die die aktuellen **ray_flag** Flags enthält. |

### <a name="primitiveobject-space-system-values"></a>Systemwerte für primitiven/Objektbereich

| Thema | BESCHREIBUNG |
|-|-|
| [**InstanceIndex**](instanceindex.md) | Der automatisch generierte Index der aktuellen Instanz in der Raytracingbeschleunigungsstruktur der obersten Ebene. |
| [**InstanceID**](instanceid.md) | Der vom Benutzer bereitgestellte Bezeichner für die Instanz in der Beschleunigungsstrukturinstanz der unteren Ebene innerhalb der Struktur der obersten Ebene. |
| [**PrimitiveIndex**](primitiveindex.md) | Der automatisch generierte Index des Primitiven innerhalb der Geometrie innerhalb der Beschleunigungsstrukturinstanz der unteren Ebene. |
| [**ObjectRayOrigin**](objectrayorigin.md) | Der Objektraumursprung für den aktuellen Strahl. |
| [**ObjectRayDirection**](objectraydirection.md) | Die Objektraumrichtung für den aktuellen Strahl. |
| [**ObjectToWorld3x4**](objecttoworld3x4.md) | Eine Matrix zum Transformieren vom Objektraum in den Weltraum. |
| [**ObjectToWorld4x3**](objecttoworld4x3.md) | Eine Matrix zum Transformieren vom Objektraum in den Weltraum. |
| [**WorldToObject3x4**](worldtoobject3x4.md) | Eine Matrix zum Transformieren vom Weltraum in den Objektraum |
| [**WorldToObject4x3**](worldtoobject4x3.md) | Eine Matrix zum Transformieren vom Weltraum in den Objektraum |
### <a name="hit-specific-system-values"></a>Trefferspezifische Systemwerte

| Thema | BESCHREIBUNG |
|-|-|
| [**HitKind**](hitkind.md) | Gibt den Wert zurück, der als **HitKind-Parameter** an [**ReportHit**](reporthit-function.md)übergeben wird. |

## <a name="related-topics"></a>Zugehörige Themen

* [Kernreferenz](direct3d-12-core-reference.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)
