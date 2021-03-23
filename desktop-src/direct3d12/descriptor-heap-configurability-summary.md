---
title: Deskriptorheap-Konfigurations Zusammenfassung
description: In der folgenden Tabelle werden Informationen zur Unterstützung von Shader und nicht-Shader-sichtbarem Heap zusammengefasst.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ce6718e95b774f83d25a84476616643c77c119
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103571"
---
# <a name="descriptor-heap-configurability-summary"></a>Deskriptorheap-Konfigurations Zusammenfassung

In der folgenden Tabelle werden Informationen zur Unterstützung von Shader und nicht-Shader-sichtbarem Heap zusammengefasst.



|                               | Shader-sichtbarer deskriptorheap                                                 | Sichtbarer deskriptorheap für nicht-Shader                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Heap Typen          | CBV \_ SRV \_ UAV, Sampler                                                         | Alle                                                                                                                                                                                                                                                                                                                                                                 |
| Unterstützte CPU-Seiteneigenschaften | nicht \_ verfügbar, schreiben \_ kombinieren                                                 | \_Zurückschreiben                                                                                                                                                                                                                                                                                                                                                         |
| Residenz Verwaltung nach App   | Ja, App Verantwortlichkeit                                                           | Nicht zutreffend (nicht GPU-sichtbar).                                                                                                                                                                                                                                                                                                                                   |
| Unterstützung für deskriptorbearbeitung       | Nur Ziel kopieren, über die Befehlsliste aktualisieren und/oder CPU-Kopie, wenn CPU sichtbar ist. | Nur CPU-Lese-und Schreibvorgänge. Kein direkter GPU-Zugriff. Kann zum sofortigen Kopieren von CPU (als Quelle und Ziel) verwendet werden. Kann in einer Befehlsliste als Update Quelle verwendet werden – dadurch werden die Deskriptoren im Befehlslisten Daten Satz in den Befehlslisten Speicher kopiert. Bei der Ausführung wird die gespeicherte Kopie in das Ziel kopiert, bei dem es sich um einen für Shader sichtbaren Heap handeln muss. |



 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 




