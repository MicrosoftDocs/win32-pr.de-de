---
description: Comrepl funktioniert in drei Phasen.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Replikations Phasen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc180e7864f05eb1be60262ee54dd4b71df53bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346455"
---
# <a name="replication-phases"></a>Replikations Phasen

Comrepl funktioniert in drei Phasen. Der Replikationsprozess wird aus den folgenden zwei Gründen in verschiedene Phasen unterteilt:

-   So trennen Sie die Arbeit, die für die Vorbereitung der Quelle auf den einzelnen Zielen erledigt ist
-   So verzögern Sie die Änderung des Ziels, bis alle Daten aus der Quelle abgerufen wurden

Die Replikations Phasen lauten wie folgt.



| Phase         | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorbereitungsphase | Exportiert alle installierten Anwendungen lokal auf den Quellcomputer. In dieser Phase wird die Konfiguration von Zielen nicht berücksichtigt.                                                                                                                                                                                                                                                                                                                                                                                                           |
| Kopier Phase    | Kopiert Daten auf einen Bereitstellungs Zielcomputer. Alle Anwendungen, die auf der Quelle exportiert werden, werden in das Ziel kopiert. Dabei handelt es sich um einen Datei Kopiervorgang. (Weitere Informationen finden Sie unter [Dateiverwaltung](file-management.md).) Bei diesem Schritt werden auch einige Daten vom Quellcomputer angefordert, die nicht in exportierten Anwendungs Dateien (z. b. Anwendungs Identitäten) gekapselt sind. Diese Daten werden im Arbeitsspeicher in Comrepl gespeichert. In dieser Phase wird die Konfiguration von Ziel Computern nicht berührt.                                                                               |
| Installationsphase | Installiert den Quell Katalog auf einem Bereitstellungs Zielcomputer. Wenn dieser Schritt initiiert wird, befinden sich alle zum Neukonfigurieren des Ziels erforderlichen Daten innerhalb der Anwendungs Dateien im Dateisystem des Ziels oder befinden sich in Comrepl als Instanzdaten. In dieser Phase werden alle installierten Anwendungen auf dem Ziel gelöscht (außer den in [was replizierten](what-gets-replicated.md)Anwendungen), bevor die aus der Quelle kopierten Anwendungen installiert werden. Comrepl wird gleichzeitig auf mehreren Zielen installiert, indem ein Installations Thread pro Ziel verwendet wird. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateiverwaltung](file-management.md)
</dt> <dt>

[Protokollierung und Fehlerberichterstattung](logging-and-error-reporting.md)
</dt> <dt>

[Verwenden von Comrepl](using-comrepl.md)
</dt> <dt>

[Was wird repliziert?](what-gets-replicated.md)
</dt> </dl>

 

 



