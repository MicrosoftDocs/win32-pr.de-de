---
title: Verwenden von Microsoft Locator
description: Microsoft Locator ist der Standardnamendienst. Die RPC-Laufzeitbibliothek verwendet sie, um Serverprogramme auf Serverhostsystemen zu suchen.
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- Remoteprozeduraufruf RPC , Tasks, mit Microsoft Locator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64a5c54c09ee344ffdba46f9f44a546ab866557bc861b206868ad6d3992896b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010738"
---
# <a name="using-microsoft-locator"></a>Verwenden von Microsoft Locator

Microsoft Locator ist der Standardnamendienst. Die RPC-Laufzeitbibliothek verwendet sie, um Serverprogramme auf Serverhostsystemen zu suchen.

**Hinweis**  Der Microsoft RPC-Locator wird in Windows Vista- und späteren Betriebssystemen nicht unterstützt.

Vor Windows 2000 hat Microsoft Locator keine Einträge für den Dienst mit persistenten Namen zur Verfügung gestellt. Alle Einträge im Namensdienst wurden in einem Speichercache auf dem Hostcomputer des Serverprogramms gespeichert. Der Locator hat einen Broadcastmechanismus verwendet, um den Von Clients angeforderten Speicherort von Servern zu ermitteln. Jedes Mal, wenn das Hostsystem heruntergefahren wird, sind alle Namensdiensteinträge verloren gegangen.

Ab der Veröffentlichung von Windows 2000 unterstützt Microsoft Locator jetzt Diensteinträge für persistente Namen. Zu diesem Zweck verwendet das System einen verteilten Verzeichnisdienst, um Namensdiensteinträge zu speichern. Dieser Mechanismus hat mehrere Vorteile:

-   **Persistenz.** Serverprogramme müssen ihre Bindungsinformationen nicht mehr jedes Mal, wenn sie gestartet werden, in den Namensdienst exportieren. Der Name-Dienst speichert jetzt die Informationen, bis das Serverprogramm auf dem Netzwerkadministrator sie explizit entfernt.
-   **Effizienz.** Durch die Beseitigung des Großteils der Übertragung für Namensdiensteinträge reduziert der Locator den Netzwerkdatenverkehr. Außerdem werden Namensdiensteinträge schneller gefunden.
-   **Domänenübergreifende Interoperabilität.** Clients können jetzt Namensdienstanforderungen über mehrere Domänen hinweg durchführen.

Aktuelle Versionen von Microsoft Locator sind abwärtskompatibel. Beispielsweise kann ein Serverhostsystem, auf dem der Locator ausgeführt wird, der mit Windows 2000 geliefert wird, ordnungsgemäß in einem Netzwerk ausgeführt werden, das Serverhostsysteme enthält, auf denen der Locator ausgeführt wird, der mit Windows NT 4.0 ausgeliefert wird.

Mit der Veröffentlichung von Windows 2000 unterstützt Microsoft Locator jetzt Namensdiensteinträge für Benutzergruppen. Außerdem können Sie Benutzerprofile erstellen.

Darüber hinaus unterstützt die aktuelle Version von Microsoft Locator die Verwendung von Access Control Listen in Namensdiensteinträgen. Diese Möglichkeit erhöht die Sicherheit des Netzwerks.

Plug & Play Unterstützung ist jetzt in Microsoft Locator enthalten. Daher kann es Plug & Play Ereignisse wie Domänenänderungen transparent verarbeiten. Weitere Informationen finden Sie unter [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) und [**RpcNsBindingUnexportPnP.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa)

 

 




