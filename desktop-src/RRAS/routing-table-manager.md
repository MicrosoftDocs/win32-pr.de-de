---
title: Routingtabellen-Manager
description: Der Routingtabellen-Manager ist das zentrale Repository mit Routinginformationen für alle Routingprotokolle, die unter dem Routing- und RAS-Dienst (RRAS) ausgeführt werden.
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 850726cd2203eca85be33aea3bd33f1ed903ba2d197d102ff7de294c5e852626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787468"
---
# <a name="routing-table-manager"></a>Routingtabellen-Manager

Der Routingtabellen-Manager ist das zentrale Repository mit Routinginformationen für alle Routingprotokolle, die unter dem Routing- und RAS-Dienst (RRAS) ausgeführt werden. Clients werden benachrichtigt, wenn Änderungen vorgenommen wurden, und Clients können private Informationen austauschen.

Der Routingtabellen-Manager stellt Routinginformationen für alle interessierten Clients bereit, z. B. Routingprotokolle, Verwaltungsprogramme und Überwachungsprogramme. Der Routingtabellen-Manager bestimmt auch die beste Route zu jedem Zielnetzwerk, das den Routingprotokollen bekannt ist. Der Routingtabellen-Manager bestimmt diese Route basierend auf den Routingprotokollprioritäten und den den Routen zugeordneten Metriken. Die Person, die den Router verwaltet, kann routingprotokollprioritäten mithilfe der RRAS-Verwaltungskonsole konfigurieren.

Der Routingtabellen-Manager übergibt die Informationen für die beste Route an die Weiterleitungen (eine pro Adressfamilie oder eine pro Schnittstelle) und an alle interessierten Clients.

Jeder Client registriert sich beim Routingtabellen-Manager und empfängt im Gegenzug ein Handle, das der Client zum Hinzufügen oder Löschen von Routen verwendet. Clients können informationen abrufen, die in der Routingtabelle gespeichert sind. Darüber hinaus können sich Clients beim Routingtabellen-Manager registrieren, um Benachrichtigungen über Änderungen an der besten Route zu einem Ziel zu erhalten.

 

 




