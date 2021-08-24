---
description: Verwenden von COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Verwenden von COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501cca8d32383e23fc636669e32a80cfdfe96dd658717e41c1618244fc5af81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853880"
---
# <a name="using-comrepl"></a>Verwenden von COMREPL

Führen Sie die folgenden Schritte aus, um das Befehlszeilenprogramm COMREPL zu starten:

1.  Fügen Sie %windir% system32 Com zum Standardumgebungspfad hinzu, indem Sie An \\ \\ der Eingabeaufforderung Folgendes eingeben:

    **set path = %PATH%;%windir% \\ system32 \\ Com**

2.  Geben Sie den folgenden COMREPL-Befehl ein:

    **COMREPL-QuelleComputerzielComputerList**   **\[ /n \[ /v \] \]**

    Dabei gilt:

    -   *sourceComputer* ist der Computername der Quelle.

    -   *targetComputerList* sind die Computernamen der Ziele, die durch Leerzeichen getrennt sind.

    -   **/n unterdrückt** die Bestätigungsaufforderung vor dem Starten der Replikation.

    -   **/v gibt** die Protokolldateiausgabe an die Konsole weiter.

## <a name="notes"></a>Hinweise

-   Da COM+ nicht repliziert wird (nur Konfigurationsdaten und Anwendungen), muss com+ auf allen Zielcomputern bereits installiert sein.
-   Der Benutzer muss rollenüberprüfungen für die Systemanwendung sowohl auf dem Quell- als auch auf dem Zielcomputer bestehen.
-   Es werden keine Konten lokaler Computer repliziert, die von Rollen verwendet werden können.
-   Die Zielcomputer müssen online sein.
-   Der Benutzer ist dafür verantwortlich, alle Nicht-COM+-Daten (z. B. Datenbanktabellen, Datendateien usw.) auf die Zielcomputer zu replizieren.
-   Cluster können an der Replikation teilnehmen. Beachten Sie jedoch, dass COMREPL nur auf benannte Computer repliziert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateiverwaltung](file-management.md)
</dt> <dt>

[Protokollierung und Fehlerberichterstattung](logging-and-error-reporting.md)
</dt> <dt>

[Replikationsphasen](replication-phases.md)
</dt> <dt>

[Was wird repliziert?](what-gets-replicated.md)
</dt> </dl>

 

 



