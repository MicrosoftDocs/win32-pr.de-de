---
title: Zusammenfassung der Deskriptorheap-Konfigurierbarkeit
description: In der folgenden Tabelle sind Informationen zur Unterstützung von shader- und nicht shader-sichtbaren Heaps zusammengefasst.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c974516a09552fc5e3b301ca3ef91a3aea3d1752d0177f34d5fc94928ee8f293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530552"
---
# <a name="descriptor-heap-configurability-summary"></a>Zusammenfassung der Deskriptorheap-Konfigurierbarkeit

In der folgenden Tabelle sind Informationen zur Unterstützung von shader- und nicht shader-sichtbaren Heaps zusammengefasst.



|                               | Shader Visible Descriptor Heap                                                 | Nicht shader sichtbarer Deskriptor-Heap                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Unterstützte Heaptypen**          | CBV \_ SRV \_ UAV, Sampler                                                         | Alle                                                                                                                                                                                                                                                                                                                                                                 |
| **Unterstützte CPU-Seiteneigenschaften** | NICHT \_ VERFÜGBAR, WRITE \_ COMBINE                                                 | \_ZURÜCKSCHREIBEN                                                                                                                                                                                                                                                                                                                                                         |
| **Verwaltung von Residencys nach App**   | Ja, app responsible                                                           | Nicht zutreffend (nicht gpu-sichtbar).                                                                                                                                                                                                                                                                                                                                   |
| **Unterstützung für Deskriptorbearbeitung**       | Nur Ziel kopieren, über Befehlslistenaktualisierung und/oder CPU-Kopie, wenn CPU sichtbar ist. | Nur CPU-Lese- und -Schreibzugriff. Kein direkter GPU-Zugriff. Kann zum sofortigen Kopieren von CPUs (als Quelle und Ziel) verwendet werden. Kann als Updatequelle für eine Befehlsliste verwendet werden. Dadurch werden die Deskriptoren während des Befehlslisten-Datensatzes in den Befehlslistenspeicher kopiert. Bei der Ausführung wird die gespeicherte Kopie in das Ziel kopiert, bei dem es sich um einen shader sichtbaren Heap geben muss. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 




