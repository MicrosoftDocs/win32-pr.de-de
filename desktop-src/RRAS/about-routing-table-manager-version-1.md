---
title: Informationen zum Routing Table Manager Version 1
description: Der Routing Tabellen-Manager ist ein zentrales Repository mit Routing Informationen für alle Routing Protokolle, die unter Routing-und RAS-Dienst (RRAS) betrieben werden.
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- RRAS für den Routing-und RAS-Dienst, Routing-Tabellen-Manager Version 1
- RRAS für den Routing-und RAS-Dienst, Routing Table Manager Version 1, beschrieben
- Routing Tabellen-Manager, Version 1, RRAS
- Routing Table Manager Version 1 RRAS, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037085"
---
# <a name="about-routing-table-manager-version-1"></a>Informationen zum Routing Table Manager Version 1

**Windows Server 2003:** Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Neue Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.

Der Routing Tabellen-Manager ist ein zentrales Repository mit Routing Informationen für alle Routing Protokolle, die unter Routing-und RAS-Dienst (RRAS) betrieben werden. Der Routing Tabellen-Manager bietet Routing Informationen für alle interessierten Komponenten, z. b. Routing Protokolle, Verwaltungs-Agents und Überwachungs-Agents. Der Routing Tabellen-Manager bestimmt außerdem die beste Route zu jedem Zielnetzwerk, das den Routing Protokollen bekannt ist. Diese Route wird anhand von Routing Protokoll Prioritäten und Metriken, die den Routen zugeordnet sind, bestimmt. Beachten Sie, dass der Administrator Routing Protokoll Prioritäten konfigurieren kann. Der Routing Tabellen-Manager übergibt dann die Best-Route-Informationen an die Weiterleitungen und zurück zu den Routing Protokollen.

Jedes Routing Protokoll ruft [**rtmregisterclient**](rtmregisterclient.md) auf, um sich beim Routing Tabellen-Manager zu registrieren. **Rtmregisterclient** gibt ein Handle zurück, das vom Routing Protokoll verwendet wird, um Routen Einträge hinzuzufügen oder zu löschen. **Rtmregisterclient** ermöglicht auch dem Routing Protokoll das Registrieren eines Ereignis Objekts beim Routing Tabellen-Manager. Der Routing-Tabellen-Manager signalisiert diesem Ereignis Objekt, das Routing Protokoll über Änderungen an den Informationen über die beste Route zu benachrichtigen. Alle anderen Komponenten können mithilfe der Routen Enumeration Informationen abrufen, die im Routing Tabellen-Manager gespeichert sind.

 

 




