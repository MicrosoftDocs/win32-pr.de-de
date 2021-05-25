---
title: Für den Shader nicht sichtbare Deskriptorheaps
description: Auf einige Deskriptorheaps kann von Shadern nicht über Deskriptortabellen verwiesen werden, sie sind jedoch entweder vorhanden, um die App beim Staging der Deskriptoren vor der Aufzeichnung einer Befehlsliste zu unterstützen, oder weil kein shader-sichtbarer Heap erforderlich ist.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51d30c7a99250ee0842b79d76ccebb6150bcf9a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343455"
---
# <a name="non-shader-visible-descriptor-heaps"></a>Für den Shader nicht sichtbare Deskriptorheaps

Auf einige Deskriptorheaps kann von Shadern nicht über Deskriptortabellen verwiesen werden, sie sind jedoch entweder vorhanden, um die App beim Staging der Deskriptoren vor der Aufzeichnung einer Befehlsliste zu unterstützen, oder weil kein shader-sichtbarer Heap erforderlich ist.

-   [Nicht sichtbare Ansichten](#non-visible-views)
-   [Zusammenfassung](#summary)
-   [Verwandte Themen](#related-topics)

## <a name="non-visible-views"></a>Nicht sichtbare Ansichten

Alle Deskriptorheaps, einschließlich der zuvor beschriebenen Shader-Deskriptorheaps, können von den CPU- und/oder Befehlslisten abhängig vom Arbeitsspeicherpool und den CPU-Zugriffseigenschaften bearbeitet werden, die die Anwendung für einen Deskriptorheap auswählt.

Für [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md)ist der offensichtliche Grund, shader den Zugriff auf diese Deskriptorheaps zu verweigern, während sie ge staget werden. Anschließend werden diese Heaps als Shader sichtbar gemacht und über Deskriptortabellen bei der Ausführung der Befehlsliste aufgerufen. Es ist jedoch nicht erforderlich, für Shader sichtbare Heaps zu stagen, da sie direkt aufgefüllt werden können.

Andere Deskriptoren werden an die Pipeline gebunden, indem ihre Inhalte direkt in der Befehlsliste aufgezeichnet werden. Diese Deskriptoren dienen nur dazu, die Ansichtsparameter zum Zeitpunkt des Befehlslisten-Datensatzes zu übersetzen. Diese Heaps sind immer nicht als Shader sichtbar und enthalten Folgendes.

-   Renderzielansichten (RTVs)
-   Tiefenschablonenansichten (DSVs)

Indexpuffersichten (IBVs), Vertexpuffersichten (VBVs) und Streamausgabesichten (Stream Output Views, SOVs) werden direkt an API-Methoden übergeben und weisen keine bestimmten Heaptypen auf.

Nach der Aufzeichnung in der Befehlsliste (z. B. mit einem Aufruf wie [**OMSetRenderTargets)**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)steht der Arbeitsspeicher, der zum Speichern der Deskriptoren für diesen Aufruf verwendet wird, sofort zur erneuten Verwendung nach dem Aufruf zur Verfügung.

Selbst Deskriptortabellen verfügen über Optionen, bei denen eine App es der Implementierung ermöglichen kann, den Tabelleninhalt bei der Befehlslistenaufzeichnung aufzuzeichnen (anstatt den Tabellenzeiger bei der Ausführung zu dereferenzieren).

## <a name="summary"></a>Zusammenfassung



|                   | Shader sichtbar, nur CPU-Schreibzugriff                                   | Nicht-Shader sichtbar, CPU-Lese-/Schreibzugriff                                       |
|-------------------|------------------------------------|----------------------------------------|
| **CBV, SRV, UAV** | Ja                                | Ja                                    |
| **Sampler**       | Ja                                | Ja                                    |
| **RTV**           | nein                                 | Ja                                    |
| **Dsv**           | nein                                 | Ja                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 




