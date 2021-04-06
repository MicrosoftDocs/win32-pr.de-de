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
# <a name="retrieving-change-status-and-ignoring-changes"></a><span data-ttu-id="cfe52-104">Abrufen des Änderungs Status und ignorieren von Änderungen</span><span class="sxs-lookup"><span data-stu-id="cfe52-104">Retrieving Change Status and Ignoring Changes</span></span>

<span data-ttu-id="cfe52-105">Der Client kann den Routing Tabellen-Manager Abfragen, um zu ermitteln, ob eine Benachrichtigung über eine Änderung an einem Ziel durch Aufrufen von [**rtmgetchangestatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus)aussteht.</span><span class="sxs-lookup"><span data-stu-id="cfe52-105">The client can query the routing table manager to find out if a notification of a change to a destination is pending by calling [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus).</span></span> <span data-ttu-id="cfe52-106">Diese Funktion gibt **true** zurück, bis der Aufrufer diese Änderung durch Aufrufen von [**rtmgetchangeddests abruft**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span><span class="sxs-lookup"><span data-stu-id="cfe52-106">This function returns **TRUE** until the caller retrieves this change by calling [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span></span>

<span data-ttu-id="cfe52-107">Ein Client kann diese Abfrage verwenden, um die Ausführung einer Aktion zu vermeiden, die rückgängig gemacht werden müsste, nachdem die Änderungs Benachrichtigung empfangen und verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="cfe52-107">A client can use this query to avoid performing an action that would have to be undone after the change notification is received and processed.</span></span> <span data-ttu-id="cfe52-108">Mit dieser Funktion kann der Client effizient arbeiten, indem bestimmte Vorgänge auf einen späteren Zeitpunkt verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="cfe52-108">Using this feature allows the client to work efficiently by deferring certain operations to a later time.</span></span>

<span data-ttu-id="cfe52-109">Der Client kann auch eine ausstehende Änderungs Benachrichtigung für ein Ziel ignorieren, indem er [**rtmignorechangeddests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cfe52-109">The client can also ignore a pending change notification for a destination by calling [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span> <span data-ttu-id="cfe52-110">Ein späterer Befehl von [**rtmgetchangeddebug**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) gibt dieses Ziel nicht zurück, es sei denn, nach dem Aufrufen von [**rtmignorechangedentsts**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)wird eine andere Änderung vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="cfe52-110">A later call to [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) does not return this destination unless another change occurs after the call to [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span>

 

 




