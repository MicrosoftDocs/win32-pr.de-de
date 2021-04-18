---
description: Eine Serveranwendung stellt Dienste für Clients bereit.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Client/Server-Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b1d349abb2d55f00b9801c9bb493437fa858eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368156"
---
# <a name="clientserver-access-control"></a>Client/Server-Access Control

Eine Serveranwendung stellt Dienste für Clients bereit. Beispielsweise könnte ein Server die folgenden Dienste im Auftrag eines Clients ausführen:

-   Speichern und Abrufen von Informationen aus einer privaten Datenbank
-   Zugreifen auf Netzwerkressourcen
-   Starten von [*Prozessen*](/windows/desktop/SecGloss/p-gly) im [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des Clients auf dem Computer des Servers

Ein geschützter Server steuert den Zugriff auf seine Dienste. Windows bietet Sicherheitsunterstützung, die es einem Server ermöglicht, folgende Aufgaben durchzuführen:

-   Nimmt die Identität des [*Sicherheits Kontexts*](/windows/desktop/SecGloss/s-gly)eines Clients an. Dies bewirkt, dass das System die meisten Zugriffs-und [*Berechtigungs*](/windows/desktop/SecGloss/p-gly) Prüfungen für das [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) des Clients anstelle des Servers durchführt.
-   Anmelden eines Clients auf dem Computer des Servers
-   Herstellen einer Verbindung mit Netzwerkressourcen über den Sicherheitskontext des Clients
-   Erstellen von [*Sicherheits Deskriptoren*](/windows/desktop/SecGloss/s-gly) zum Schutz privater Objekte
-   Bestimmen, ob eine Sicherheits Beschreibung den Zugriff auf einen Client zulässt
-   Bestimmen, ob ein Berechtigungs Satz im Token eines Clients aktiviert ist
-   Generieren von Überwachungs Meldungen im Sicherheits Ereignisprotokoll zum Aufzeichnen von versuchen eines Clients, auf Objekte zuzugreifen oder Berechtigungen zu verwenden

 

 
