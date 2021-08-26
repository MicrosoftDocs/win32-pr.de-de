---
title: Abrufen des Änderungsstatus und Ignorieren von Änderungen
description: Der Client kann den Routingtabellen-Manager abfragen, um zu ermitteln, ob eine Benachrichtigung über eine Änderung an einem Ziel aussteht, indem er RtmGetChangeStatus aufruft. Diese Funktion gibt TRUE zurück, bis der Aufrufer diese Änderung durch Aufrufen von RtmGetChangedDests abruft.
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a117130ac939788a74aaa32092000e8f6f29aa6b34e697ca6066c9e13259b8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028060"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a>Abrufen des Änderungsstatus und Ignorieren von Änderungen

Der Client kann den Routingtabellen-Manager abfragen, um zu ermitteln, ob eine Benachrichtigung über eine Änderung an einem Ziel aussteht, indem [**rtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus)aufgerufen wird. Diese Funktion gibt **TRUE** zurück, bis der Aufrufer diese Änderung durch Aufrufen von [**RtmGetChangedDests abruft.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)

Ein Client kann diese Abfrage verwenden, um eine Aktion zu vermeiden, die rückgängig machen müsste, nachdem die Änderungsbenachrichtigung empfangen und verarbeitet wurde. Die Verwendung dieses Features ermöglicht es dem Client, effizient zu arbeiten, indem bestimmte Vorgänge auf einen späteren Zeitpunkt zurückgesetzt werden.

Der Client kann auch eine ausstehende Änderungsbenachrichtigung für ein Ziel ignorieren, indem [**er RtmIgnoreChangedDests aufruft.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests) Ein späterer Aufruf von [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) gibt dieses Ziel nur dann zurück, wenn nach dem Aufruf von [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)eine andere Änderung erfolgt.

 

 




