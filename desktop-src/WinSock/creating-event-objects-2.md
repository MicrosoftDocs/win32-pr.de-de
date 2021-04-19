---
description: Die Ws2 \_ -32.dll bietet Funktionen für die Erstellung von Ereignis Objekten für Anwendungen und Dienstanbieter, obwohl in den meisten Fällen Ereignis Objekte von Anwendungen erstellt werden.
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: Erstellen von Ereignis Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec202f8f17790ed85979a8287005aa65374a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344441"
---
# <a name="creating-event-objects"></a><span data-ttu-id="8019c-103">Erstellen von Ereignis Objekten</span><span class="sxs-lookup"><span data-stu-id="8019c-103">Creating Event Objects</span></span>

<span data-ttu-id="8019c-104">Die Ws2 \_ -32.dll bietet Funktionen für die Erstellung von Ereignis Objekten für Anwendungen und Dienstanbieter, obwohl in den meisten Fällen Ereignis Objekte von Anwendungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8019c-104">The Ws2\_32.dll provides facilities for event object creation to both applications and service providers, although in most instances event objects will be created by applications.</span></span> <span data-ttu-id="8019c-105">Ereignis Objekt Dienste werden für Windows Sockets-Dienstanbieter über [**wpudeateevent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) bereitgestellt. Dies ist einfach als Hilfsmechanismus für jegliche interne Verarbeitung, die vom gleichen profitieren können.</span><span class="sxs-lookup"><span data-stu-id="8019c-105">Event object services are made available to Windows Sockets service providers through [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) simply as a convenience mechanism for any internal processing that may benefit from same.</span></span> <span data-ttu-id="8019c-106">Beachten Sie, dass das Ereignis Objekt Handle nur im Kontext des aufrufenden Prozesses gültig ist.</span><span class="sxs-lookup"><span data-stu-id="8019c-106">Note that the event object handle is only valid in the context of the calling process.</span></span> <span data-ttu-id="8019c-107">In Windows-Umgebungen erfolgt die Realisierung von Ereignis Objekten über die systemeigenen Ereignis Dienste, die vom Betriebssystem bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8019c-107">In Windows environments the realization of event objects is through the native event services provided by the operating system.</span></span>

 

 



