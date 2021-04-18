---
title: Direct3D 12-Raytracing, HLSL-Systemwertinterna
description: Die folgenden HLSL-Shader unterstützen die Direct3D 12-Raytracing-Pipeline.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a20282e7bc0e9e4898fd361b0959cd6b6f32253
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2020
ms.locfileid: "106338100"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a>Direct3D 12-Raytracing, HLSL-Systemwertinterna

System Werte werden mithilfe spezieller intrinsischer Funktionen abgerufen, anstatt Parameter mit spezieller Semantik in die Signatur der Shaderfunktionen einzuschließen. 

## <a name="in-this-section"></a>In diesem Abschnitt

### <a name="ray-dispatch-system-values"></a>System Werte von Ray Dispatch

| Thema | BESCHREIBUNG |
|-|-|
| [**Dispatchraysindex**](dispatchraysindex.md) | Ruft die aktuelle x-und y-Position innerhalb der Breite und Höhe ab, die mit dem systeminternen **dispatchraysdimensions** -System Wert abgerufen wird. |
| [**DispatchRaysDimensions**](dispatchraysdimensions.md) | Die Werte für Breite, Höhe und Tiefe der **D3D12 \_ Dispatch \_ Rays \_** -Struktur, die in den ursprünglichen **dispatchrays** -aufrufen angegeben sind. |

### <a name="ray-system-values"></a>Ray-System Werte

| Thema | BESCHREIBUNG |
|-|-|
| [**Worldrayorigin**](worldrayorigin.md) | Der Welt Raum Ursprung des aktuellen Strahls. |
| [**Worldraydirection**](worldraydirection.md) | Die Welt Raum Richtung für das aktuelle Ray. |
| [**Raytmin**](raytmin.md) | Ein float-Wert, der den aktuellen parametrischen Anfangspunkt für den Strahl darstellt. |
| [**Raycurrent**](raytcurrent.md) | Ein float-Wert, der den aktuellen parametrischen Endpunkt für den Strahl darstellt.  |
| [**Rayflags**](rayflags.md) | Eine ganze Zahl ohne Vorzeichen, die die aktuellen **ray_flag** Flags enthält. |

### <a name="primitiveobject-space-system-values"></a>Primitive/Objekt Raum System Werte

| Thema | BESCHREIBUNG |
|-|-|
| [**Instanceingedex**](instanceindex.md) | Der automatisch generierte Index der aktuellen Instanz in der Raytracing-Beschleunigungs Struktur der obersten Ebene. |
| [**InstanceId**](instanceid.md) | Der vom Benutzer bereitgestellte Bezeichner für die-Instanz auf der unteren Ebene der Beschleunigungs Struktur Instanz innerhalb der Struktur der obersten Ebene. |
| [**Primitiveingedex**](primitiveindex.md) | Der automatisch generierte Index des primitiven innerhalb der Geometrie innerhalb der Beschleunigung der Beschleunigung-Struktur der untersten Ebene. |
| [**Objectrayorigin**](objectrayorigin.md) | Der Objekt Raum Ursprung für das aktuelle Ray. |
| [**Objectraydirection**](objectraydirection.md) | Die Richtung des Objekt Raums für das aktuelle Ray. |
| [**ObjectToWorld3x4**](objecttoworld3x4.md) | Eine Matrix zum Transformieren von Objekt Raum in Raum. |
| [**ObjectToWorld4x3**](objecttoworld4x3.md) | Eine Matrix zum Transformieren von Objekt Raum in Raum. |
| [**WorldToObject3x4**](worldtoobject3x4.md) | Eine Matrix zum Transformieren von Welt Raum zu Objekt Raum |
| [**WorldToObject4x3**](worldtoobject4x3.md) | Eine Matrix zum Transformieren von Welt Raum zu Objekt Raum |
### <a name="hit-specific-system-values"></a>Treffer spezifische System Werte

| Thema | BESCHREIBUNG |
|-|-|
| [**Hitkind**](hitkind.md) | Gibt den Wert zurück, der als **hitkind** -Parameter an Report [**Thread**](reporthit-function.md)übergeben wird. |

## <a name="related-topics"></a>Zugehörige Themen

* [Kern Referenz](direct3d-12-core-reference.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)
