---
description: Da duplizieren die socketdeskriptoren und nicht die zugrunde liegenden Sockets sind, werden alle Zustände, die einem Socket zugeordnet sind, in allen Deskriptoren gemeinsam gespeichert.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Mehrere Handles für einen einzelnen Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2356f24a69d132f87e0f6543f61509ff12acba5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360035"
---
# <a name="multiple-handles-to-a-single-socket"></a><span data-ttu-id="76279-103">Mehrere Handles für einen einzelnen Socket</span><span class="sxs-lookup"><span data-stu-id="76279-103">Multiple Handles to a Single Socket</span></span>

<span data-ttu-id="76279-104">Da duplizieren die socketdeskriptoren und nicht die zugrunde liegenden Sockets sind, werden alle Zustände, die einem Socket zugeordnet sind, in allen Deskriptoren gemeinsam gespeichert.</span><span class="sxs-lookup"><span data-stu-id="76279-104">Since what are duplicated are the socket descriptors and not the underlying sockets, all of the states associated with a socket are held in common across all the descriptors.</span></span> <span data-ttu-id="76279-105">Beispielsweise wird ein [**wspsetsockopt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) -Vorgang, der mit einem Deskriptor ausgeführt wird, anschließend mithilfe von [**wspgetsockopt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) von einem beliebigen oder allen Deskriptoren sichtbar.</span><span class="sxs-lookup"><span data-stu-id="76279-105">For example a [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) operation performed using one descriptor is subsequently visible using a [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) from any or all descriptors.</span></span>

<span data-ttu-id="76279-106">Benachrichtigungen zu freigegebenen Sockets unterliegen den üblichen Einschränkungen von [**wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) und [**wspeventselect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76279-106">Notification on shared sockets is subject to the usual constraints of [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) and [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="76279-107">Wenn Sie einen dieser Aufrufe mit einem der freigegebenen Deskriptoren ausgeben, werden alle vorherigen Ereignis Registrierungen für den Socket abgebrochen, unabhängig davon, welcher Deskriptor für die Registrierung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="76279-107">Issuing either of these calls using any of the shared descriptors cancels any previous event registration for the socket, regardless of which descriptor was used to make that registration.</span></span> <span data-ttu-id="76279-108">Folglich wäre es z. B. nicht möglich, den Prozess A Receive FD \_ -Lese Ereignisse und Process B-Receive-Write-Ereignisse zu verarbeiten \_ .</span><span class="sxs-lookup"><span data-stu-id="76279-108">Thus, for example, it would not be possible to have process A receive FD\_READ events and process B receive FD\_WRITE events.</span></span> <span data-ttu-id="76279-109">In Situationen, in denen eine solche strenge Koordination erforderlich ist, wird empfohlen, dass Entwickler anstelle von separaten Prozessen die Verwendung von Threads in Erwägung gezogen werden.</span><span class="sxs-lookup"><span data-stu-id="76279-109">For situations when such tight coordination is required, it is suggested that developers consider using threads instead of separate processes.</span></span>

 

 
