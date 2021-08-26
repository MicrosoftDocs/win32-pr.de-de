---
description: COMREPL führt seine Arbeit in drei Phasen aus.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Replikationsphasen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d1924b85e2681854fe8de604fea1fe59a022fa97843051457677905048dd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990420"
---
# <a name="replication-phases"></a>Replikationsphasen

COMREPL führt seine Arbeit in drei Phasen aus. Der Replikationsprozess ist aus den folgenden beiden Gründen in unterschiedliche Phasen unterteilt:

-   So trennen Sie die Arbeit zur Vorbereitung der Quelle von der Arbeit, die auf jedem Ziel durchgeführt wird
-   So verzögern Sie die Änderung des Ziels, bis alle Daten aus der Quelle erfasst wurden

Die Replikationsphasen lauten wie folgt.



| Phase         | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorbereitungsphase | Exportiert alle installierten Anwendungen lokal auf dem Quellcomputer. Diese Phase wirkt sich nicht auf die Konfiguration von Zielen aus.                                                                                                                                                                                                                                                                                                                                                                                                           |
| Kopierphase    | Kopiert Daten auf einen Zielcomputer. Alle anwendungen, die in die Quelle exportiert werden, werden in das Ziel kopiert. Dies ist ein Dateikopiervorgang. (Siehe [Dateiverwaltung](file-management.md).) In diesem Schritt werden auch einige Daten vom Quellcomputer erhalten, die nicht in exportierten Anwendungsdateien (z. B. Anwendungsidentitäten) gekapselt sind. Diese Daten werden in COMREPL im Arbeitsspeicher gespeichert. Diese Phase wirkt sich nicht auf die Konfiguration von Zielcomputern aus.                                                                               |
| Installationsphase | Installiert den Quellkatalog auf einem Zielcomputer. Wenn dieser Schritt initiiert wird, werden alle Daten, die zum Neukonfigurieren des Ziels erforderlich sind, in Anwendungsdateien im Dateisystem des Ziels oder als Instanzdaten in COMREPL gespeichert. In dieser Phase werden alle installierten Anwendungen auf dem Ziel gelöscht (mit Ausnahme der unter [Was](what-gets-replicated.md)wird repliziert? beschriebenen Anwendungen), bevor die aus der Quelle kopierten Anwendungen installiert werden. COMREPL wird auf mehreren Zielen gleichzeitig mithilfe eines Installationsthreads pro Ziel installiert. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateiverwaltung](file-management.md)
</dt> <dt>

[Protokollierung und Fehlerberichterstattung](logging-and-error-reporting.md)
</dt> <dt>

[Verwenden von COMREPL](using-comrepl.md)
</dt> <dt>

[Was wird repliziert?](what-gets-replicated.md)
</dt> </dl>

 

 



