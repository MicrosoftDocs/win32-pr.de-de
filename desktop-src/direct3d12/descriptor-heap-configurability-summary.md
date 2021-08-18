---
title: Zusammenfassung der Deskriptorheap-Konfigurierbarkeit
description: In der folgenden Tabelle sind Informationen zur Unterstützung sichtbarer Shader- und Nicht-Shader-Heaps zusammengefasst.
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

In der folgenden Tabelle sind Informationen zur Unterstützung sichtbarer Shader- und Nicht-Shader-Heaps zusammengefasst.



|                               | Sichtbarer Shaderdeskriptorheap                                                 | Sichtbarer Deskriptorheap ohne Shader                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Unterstützte Heaptypen**          | CBV \_ SRV \_ UAV, Sampler                                                         | Alle                                                                                                                                                                                                                                                                                                                                                                 |
| **Unterstützte CPU-Seiteneigenschaften** | NICHT \_ VERFÜGBAR, WRITE \_ COMBINE                                                 | \_ZURÜCKSCHREIBEN                                                                                                                                                                                                                                                                                                                                                         |
| **Residency Management By App**   | Ja, app responsible                                                           | Nicht zutreffend (nicht GPU sichtbar).                                                                                                                                                                                                                                                                                                                                   |
| **Deskriptorbearbeitungsunterstützung**       | Nur Ziel kopieren, über Aktualisierung der Befehlsliste und/oder CPU-Kopie, wenn DIE CPU sichtbar ist. | Nur CPU-Lese- und -Schreibzugriff. Kein direkter GPU-Zugriff. Kann für das sofortige Kopieren der CPU (als Quelle und Ziel) verwendet werden. Kann als Updatequelle für eine Befehlsliste verwendet werden. Dadurch werden die Deskriptoren während des Befehlslistendatensatzes in den Befehlslistenspeicher kopiert. Bei der Ausführung wird die gespeicherte Kopie in das Ziel kopiert, das ein sichtbarer Shaderheap sein muss. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 




