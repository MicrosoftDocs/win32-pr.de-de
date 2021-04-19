---
title: Routing Tabellen-Manager
description: Der Routing Tabellen-Manager ist das zentrale Repository von Routing Informationen für alle Routing Protokolle, die unter dem Routing-und RAS-Dienst (RRAS) betrieben werden.
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98094eb34c8575e0c24854813fc7458c98749568
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341838"
---
# <a name="routing-table-manager"></a>Routing Tabellen-Manager

Der Routing Tabellen-Manager ist das zentrale Repository von Routing Informationen für alle Routing Protokolle, die unter dem Routing-und RAS-Dienst (RRAS) betrieben werden. Clients werden benachrichtigt, wenn Änderungen aufgetreten sind, und Clients können private Informationen austauschen.

Der Routing Tabellen-Manager bietet Routing Informationen für alle interessierten Clients, z. b. Routing Protokolle, Verwaltungsprogramme und Überwachungsprogramme. Der Routing Tabellen-Manager bestimmt außerdem die beste Route zu jedem Zielnetzwerk, das den Routing Protokollen bekannt ist. Der Routing Tabellen-Manager bestimmt diese Route basierend auf den Prioritäten des Routing Protokolls und den Metriken, die den Routen zugeordnet sind. Die Person, die den Router verwaltet, kann Routing Protokoll Prioritäten mithilfe der RRAS-Verwaltungskonsole konfigurieren.

Der Routing Tabellen-Manager übergibt die Informationen der besten Route an die Weiterleitungen (eine pro Adressfamilie oder eine pro Schnittstelle) und an alle interessierten Clients.

Jeder Client wird beim Routing Tabellen-Manager registriert, und in Return wird ein Handle empfangen, das der Client zum Hinzufügen oder Löschen von Routen verwendet. Clients können in der Routing Tabelle gespeicherte Informationen abrufen. Darüber hinaus können sich Clients beim Routing Tabellen-Manager registrieren, um Benachrichtigungen über Änderungen an der optimalen Route zu einem Ziel zu erhalten.

 

 




