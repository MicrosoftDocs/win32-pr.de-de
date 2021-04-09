---
title: Verwenden von Microsoft Locator
description: Microsoft Locator ist der Standard Namensdienst. Die RPC-Lauf Zeit Bibliothek verwendet diese für die Suche nach Serverprogrammen auf Server Hostsystemen.
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Verwendung von Microsoft Locator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236dce18b9286150581af925935222f3c9b3f862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856136"
---
# <a name="using-microsoft-locator"></a>Verwenden von Microsoft Locator

Microsoft Locator ist der Standard Namensdienst. Die RPC-Lauf Zeit Bibliothek verwendet diese für die Suche nach Serverprogrammen auf Server Hostsystemen.

**Hinweis**    Der Microsoft RPC-Serverlocatorpunkt wird in Windows Vista und höheren Betriebssystemen nicht unterstützt.

Vor Windows 2000 hat der Microsoft-Locator keine permanenten Namensdienst Einträge bereitgestellt. Alle Einträge im Name-Dienst wurden auf dem Host Computer des Server Programms in einem Arbeitsspeicher Cache gespeichert. Der Serverlocatorpunkt hat einen Broadcast Mechanismus verwendet, um den Standort der Server zu ermitteln, wie er von Clients angefordert wird. Wenn das Host System heruntergefahren wird, gingen alle Namensdienst Einträge verloren.

Ab der Veröffentlichung von Windows 2000 unterstützt der Microsoft-Locator nun persistente Namensdienst Einträge. Um dies zu erreichen, verwendet das System einen verteilten Verzeichnisdienst zum Speichern von Namensdienst Einträgen. Dieser Mechanismus bietet mehrere Vorteile:

-   **Persistenz.** Server Programme sind nicht mehr erforderlich, um die Bindungs Informationen bei jedem Start in den Namensdienst zu exportieren. Der Namensdienst speichert die Informationen jetzt, bis Sie vom Serverprogramm auf dem Netzwerkadministrator explizit entfernt werden.
-   **Leistung.** Der Serverlocatorpunkt reduziert den Netzwerk Datenverkehr, indem der Großteil der Broadcast Informationen für Namensdienst Einträge entfällt. Außerdem werden Namensdienst Einträge schneller gefunden.
-   **Domänen übergreifende Interoperabilität.** Clients können nun Namensdienst Anforderungen über mehrere Domänen hinweg erstellen.

Die aktuellen Versionen von Microsoft Locator sind abwärts kompatibel. Beispielsweise kann ein Server Host System mit dem Serverlocatorpunkt, der im Lieferumfang von Windows 2000 enthalten ist, ordnungsgemäß in einem Netzwerk ausgeführt werden, das Server Host Systeme mit dem Serverlocatorpunkt, der im Lieferumfang von Windows NT 4,0 ausgeführt wird.

Mit der Veröffentlichung von Windows 2000 unterstützt der Microsoft-Locator jetzt Namensdienst Einträge für Gruppen von Benutzern. Es bietet Ihnen auch die Möglichkeit, Benutzerprofile zu erstellen.

Außerdem unterstützt die aktuelle Version von Microsoft Locator die Verwendung von Access Control Listen in Namensdienst Einträgen. Diese Fähigkeit erhöht die Sicherheit des Netzwerks.

Die Plug & Play-Unterstützung ist jetzt in Microsoft Locator enthalten. Daher können Plug & Play Ereignisse wie z. b. Domänen Änderungen transparent behandelt werden. Weitere Informationen finden Sie unter [**rpcnsbindingexportpnp**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) und [**rpcnsbindingunexportpnp**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).

 

 




