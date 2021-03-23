---
title: Nicht Shader sichtbare deskriptorheaps
description: Auf einige deskriptorheaps kann nicht durch Shader durch deskriptortabellen verwiesen werden. Sie ist jedoch entweder vorhanden, um der APP das Staging der Deskriptoren vor dem Aufzeichnen einer Befehlsliste zu unterstützen, oder weil kein Shader-sichtbarer Heap erforderlich ist.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894640cde142f1241b088518ba7140ffb9405152
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548665"
---
# <a name="non-shader-visible-descriptor-heaps"></a>Nicht Shader sichtbare deskriptorheaps

Auf einige deskriptorheaps kann nicht durch Shader durch deskriptortabellen verwiesen werden. Sie ist jedoch entweder vorhanden, um der APP das Staging der Deskriptoren vor dem Aufzeichnen einer Befehlsliste zu unterstützen, oder weil kein Shader-sichtbarer Heap erforderlich ist.

-   [Nicht sichtbare Sichten](#non-visible-views)
-   [Zusammenfassung](#summary)
-   [Verwandte Themen](#related-topics)

## <a name="non-visible-views"></a>Nicht sichtbare Sichten

Alle deskriptorheaps, einschließlich der zuvor beschriebenen deskriptorheaps für Shader, können je nach Arbeitsspeicher Pool und den CPU-Zugriffs Eigenschaften, die von der Anwendung für einen deskriptorheap ausgewählt werden, von der CPU-und/oder der Befehlsliste bearbeitet werden.

Für [Shader sichtbare deskriptorheaps](shader-visible-descriptor-heaps.md)ist der offensichtliche Grund, den Shader-Zugriff auf diese deskriptorheaps zu verweigern, während Sie bereitgestellt werden. Anschließend werden diese Heaps in den Shader-sichtbar umgewandelt, und der Zugriff erfolgt über deskriptortabellen bei der Ausführung der Befehlsliste. Es ist jedoch nicht erforderlich, für Shader sichtbare Heaps bereitzustellen. Sie können direkt ausgefüllt werden.

Andere Deskriptoren werden an die Pipeline gebunden, indem ihre Inhalte direkt in der Befehlsliste aufgezeichnet werden. Diese Deskriptoren dienen nur zur Übersetzung der Ansichts Parameter in der Befehlslisten-Daten Satz Zeit. Diese Heaps sind immer nicht-Shader sichtbar und enthalten Folgendes:

-   Renderzielsichten (rtvs)
-   Tiefen Schablonen Ansichten (DSVs)

Index Puffer Sichten (ibvs), Vertex-Puffer Sichten (vbvs) und Stream-Ausgabe Sichten (sovs) werden direkt an API-Methoden übermittelt, verfügen nicht über bestimmte Heap Typen.

Nach dem aufzeichnen in der Befehlsliste (z. b. mit einem-Befehl wie z. b. [**omstrendertargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)) steht der Arbeitsspeicher, der zum Speichern der Deskriptoren für diesen Befehl verwendet wurde, sofort zur erneuten Verwendung nach dem-Befehl zur Verfügung.

Auch deskriptortabellen haben Optionen, bei denen eine APP es der Implementierung ermöglicht, den Tabelleninhalt bei der Aufzeichnung der Befehlsliste aufzuzeichnen (anstatt den Tabellen Zeiger bei der Ausführung zu dereferenzieren).

## <a name="summary"></a>Zusammenfassung



|                   |                                    |                                        |
|-------------------|------------------------------------|----------------------------------------|
|                   | **Shader sichtbar, nur CPU-Schreibvorgänge** | **nicht-Shader sichtbar, CPU-Lese-/Schreibzugriff** |
| **CBV, SRV, UAV** | ja                                | ja                                    |
| **Sammel**       | ja                                | ja                                    |
| **RTV**           | Nein                                 | ja                                    |
| **DSV**           | Nein                                 | ja                                    |



 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 




