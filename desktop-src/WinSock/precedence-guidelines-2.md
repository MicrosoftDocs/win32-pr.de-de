---
description: Die zwei (oder mehr) Deskriptoren, die auf einen freigegebenen Socket verweisen, können unabhängig von der e/a-Leistung unabhängig verwendet werden.
ms.assetid: 25252552-4b62-441a-b564-e7f4a77cf68a
title: Rang folgen Richtlinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c2086b2d640e2968c56082c2d8dfff99546fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129137"
---
# <a name="precedence-guidelines"></a><span data-ttu-id="2d235-103">Rang folgen Richtlinien</span><span class="sxs-lookup"><span data-stu-id="2d235-103">Precedence Guidelines</span></span>

<span data-ttu-id="2d235-104">Die zwei (oder mehr) Deskriptoren, die auf einen freigegebenen Socket verweisen, können unabhängig von der e/a-Leistung unabhängig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d235-104">The two (or more) descriptors that reference a shared socket may be used independently as far as I/O is concerned.</span></span> <span data-ttu-id="2d235-105">Die Windows Sockets-Schnittstelle implementiert jedoch keinen Zugriffs Steuerungstyp, d. h., es geht um die Prozesse, die zum koordinieren ihrer Vorgänge auf einem freigegebenen Socket beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="2d235-105">However, the Windows Sockets interface does not implement any type of access control, so it is up to the processes involved to coordinate their operations on a shared socket.</span></span> <span data-ttu-id="2d235-106">Eine typische Verwendung von freigegebenen Sockets besteht darin, dass ein Prozess, der für das Erstellen von Sockets und das Einrichten von Verbindungen zuständig ist, die Sockets an andere Prozesse übergibt, die für den Informationsaustausch zuständig sind.</span><span class="sxs-lookup"><span data-stu-id="2d235-106">A typical use for shared sockets is to have one process that is responsible for creating sockets and establishing connections hand off sockets to other processes that are responsible for information exchange.</span></span>

<span data-ttu-id="2d235-107">Die allgemeine Richtlinie zur Unterstützung mehrerer ausstehender Vorgänge für freigegebene Sockets besteht darin, dass ein Dienstanbieter alle gleichzeitigen Vorgänge für freigegebene Sockets berücksichtigen muss, insbesondere den letzten Vorgang für ein Socketobjekt.</span><span class="sxs-lookup"><span data-stu-id="2d235-107">The general guideline for supporting multiple outstanding operations on shared sockets is that a service provider is encouraged to honor all simultaneous operations on shared sockets, especially the most recent operation on a socket object.</span></span> <span data-ttu-id="2d235-108">Wenn dies erforderlich ist, kann dies auf Kosten der Ausführung einiger vorheriger, aber noch ausstehender Vorgänge auftreten, die in diesem Fall "WSAEINTR" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2d235-108">If need be, this may occur at the expense of canceling some of the previous but still pending operations, which will return WSAEINTR in this case.</span></span>

 

 



