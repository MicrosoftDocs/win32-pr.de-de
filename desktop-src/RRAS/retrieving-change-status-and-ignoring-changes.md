---
title: Abrufen des Änderungs Status und ignorieren von Änderungen
description: Der Client kann den Routing Tabellen-Manager Abfragen, um zu ermitteln, ob eine Benachrichtigung über eine Änderung an einem Ziel durch Aufrufen von rtmgetchangestatus aussteht. Diese Funktion gibt true zurück, bis der Aufrufer diese Änderung durch Aufrufen von rtmgetchangeddests abruft.
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a339cbf9ba4e97dfef25b2ebc2020ff94f8e20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709102"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a>Abrufen des Änderungs Status und ignorieren von Änderungen

Der Client kann den Routing Tabellen-Manager Abfragen, um zu ermitteln, ob eine Benachrichtigung über eine Änderung an einem Ziel durch Aufrufen von [**rtmgetchangestatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus)aussteht. Diese Funktion gibt **true** zurück, bis der Aufrufer diese Änderung durch Aufrufen von [**rtmgetchangeddests abruft**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).

Ein Client kann diese Abfrage verwenden, um die Ausführung einer Aktion zu vermeiden, die rückgängig gemacht werden müsste, nachdem die Änderungs Benachrichtigung empfangen und verarbeitet wurde. Mit dieser Funktion kann der Client effizient arbeiten, indem bestimmte Vorgänge auf einen späteren Zeitpunkt verschoben werden.

Der Client kann auch eine ausstehende Änderungs Benachrichtigung für ein Ziel ignorieren, indem er [**rtmignorechangeddests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)aufrufen. Ein späterer Befehl von [**rtmgetchangeddebug**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) gibt dieses Ziel nicht zurück, es sei denn, nach dem Aufrufen von [**rtmignorechangedentsts**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)wird eine andere Änderung vorgenommen.

 

 




