---
description: Eine Serveranwendung stellt Dienste für Clients bereit.
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: Client-/Server-Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c943d9d1e1f1cc5dcc405f49ab200aa30618f7eefb86c7f26342f005f23249fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782725"
---
# <a name="clientserver-access-control"></a>Client-/Server-Access Control

Eine Serveranwendung stellt Dienste für Clients bereit. Beispielsweise kann ein Server die folgenden Dienste im Auftrag eines Clients ausführen:

-   Speichern und Abrufen von Informationen aus einer privaten Datenbank
-   Zugreifen auf Netzwerkressourcen
-   Starten von [*Prozessen*](/windows/desktop/SecGloss/p-gly) im [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des Clients auf dem Computer des Servers

Ein geschützter Server steuert den Zugriff auf seine Dienste. Windows bietet Sicherheitsunterstützung, mit der ein Server folgende Schritte ausführen kann:

-   Nehmen Sie die Identität des [*Sicherheitskontexts*](/windows/desktop/SecGloss/s-gly)eines Clients an, wodurch das System die meisten Zugriffs- und [*Berechtigungsprüfungen*](/windows/desktop/SecGloss/p-gly) für das [*Zugriffstoken*](/windows/desktop/SecGloss/a-gly) des Clients und nicht für das des Servers durchführt.
-   Anmelden eines Clients beim Computer des Servers
-   Verbinden zu Netzwerkressourcen unter Verwendung des Sicherheitskontexts des Clients
-   Erstellen von [*Sicherheitsbeschreibungen*](/windows/desktop/SecGloss/s-gly) zum Schützen privater Objekte
-   Bestimmen, ob eine Sicherheitsbeschreibung den Zugriff auf einen Client zulässt
-   Bestimmen, ob ein Satz von Berechtigungen im Token eines Clients aktiviert ist
-   Generieren von Überwachungsmeldungen im Sicherheitsereignisprotokoll, um Versuche eines Clients aufzuzeichnen, auf Objekte zuzugreifen oder Berechtigungen zu verwenden

 

 
