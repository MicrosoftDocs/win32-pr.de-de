---
description: Verwenden von Comrepl
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Verwenden von Comrepl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb39640998b3b27ac25cbab2ae60948418d6cee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748640"
---
# <a name="using-comrepl"></a>Verwenden von Comrepl

Führen Sie die folgenden Schritte aus, um das Befehlszeilen-Hilfsprogramm Comrepl zu starten:

1.  Fügen Sie% windir% \\ system32 \\ com zum Standard Umgebungs Pfad hinzu, indem Sie in der Eingabeaufforderung Folgendes eingeben:

    **Legen Sie path =% path%;% windir% \\ system32 com fest. \\**

2.  Geben Sie den folgenden Comrepl-Befehl ein:

    **Comrepl** *sourcecomputer* *targetcomputerlist* **\[ /n \[ /v \] \]**

    Dabei gilt:

    -   *sourcecomputer* ist der Computername der Quelle.

    -   *targetcomputerlist* ist die Computernamen der Ziele, die durch Leerzeichen getrennt sind.

    -   **/n** unterdrückt Bestätigungsaufforderung vor dem Starten der Replikation

    -   **/v** gibt die Protokolldatei Ausgabe an die Konsole aus.

## <a name="notes"></a>Notizen

-   Da com+ nicht repliziert wird (nur Konfigurationsdaten und Anwendungen), muss com+ auf allen Ziel Computern bereits installiert sein.
-   Der Benutzer muss sowohl auf dem Quell-als auch auf dem Zielcomputer Rollen Überprüfungen für die Systemanwendung übergeben.
-   Keine lokalen Computer Konten, die von Rollen verwendet werden können, werden repliziert.
-   Der Zielcomputer muss online sein.
-   Der Benutzer ist dafür verantwortlich, alle nicht-com-Daten (z. b. Datenbanktabellen, Datendateien usw.) auf den Ziel Computern zu replizieren.
-   Cluster können an der Replikation teilnehmen, aber beachten Sie, dass Comrepl nur auf benannte Computer repliziert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateiverwaltung](file-management.md)
</dt> <dt>

[Protokollierung und Fehlerberichterstattung](logging-and-error-reporting.md)
</dt> <dt>

[Replikations Phasen](replication-phases.md)
</dt> <dt>

[Was wird repliziert?](what-gets-replicated.md)
</dt> </dl>

 

 



