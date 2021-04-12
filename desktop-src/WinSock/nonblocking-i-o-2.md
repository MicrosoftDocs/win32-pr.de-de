---
description: Wenn sich ein Socket im nicht blockierenden Modus befindet, muss jeder e/a-Vorgang entweder sofort abgeschlossen werden oder den Fehlercode "WSAEWOULDBLOCK" zurückgeben, der angibt, dass der Vorgang nicht sofort abgeschlossen werden kann.
ms.assetid: badd279b-ec71-4761-9066-d501aa2485c2
title: Nicht blockierende Eingabe/Ausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9f6fec896c8daf1998e71a20a23a296b7b5a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526129"
---
# <a name="nonblocking-inputoutput"></a><span data-ttu-id="7ab31-103">Nicht blockierende Eingabe/Ausgabe</span><span class="sxs-lookup"><span data-stu-id="7ab31-103">Nonblocking Input/Output</span></span>

<span data-ttu-id="7ab31-104">Wenn sich ein Socket im nicht blockierenden Modus befindet, muss jeder e/a-Vorgang entweder sofort abgeschlossen werden oder den Fehlercode "WSAEWOULDBLOCK" zurückgeben, der angibt, dass der Vorgang nicht sofort abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ab31-104">If a socket is in nonblocking mode, any I/O operation must either complete immediately or return the error code WSAEWOULDBLOCK indicating that the operation cannot be finished right away.</span></span> <span data-ttu-id="7ab31-105">Im letzteren Fall ist ein Mechanismus erforderlich, um zu ermitteln, wann es sinnvoll ist, den Vorgang erneut auszuführen, und es wird davon ausgegangen, dass der Vorgang erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ab31-105">In the latter case, a mechanism is needed to discover when it is appropriate to try the operation again with the expectation that the operation will succeed.</span></span> <span data-ttu-id="7ab31-106">Zu diesem Zweck wurde eine Gruppe von Netzwerk Ereignissen definiert.</span><span class="sxs-lookup"><span data-stu-id="7ab31-106">A set of network events has been defined for this purpose.</span></span> <span data-ttu-id="7ab31-107">Diese Ereignisse können mithilfe von [**wspselect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))abgerufen oder gewartet werden, oder Sie können für die asynchrone Übermittlung durch Aufrufen von [**wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) oder [**wspeventselect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))registriert werden.</span><span class="sxs-lookup"><span data-stu-id="7ab31-107">These events can be polled or waited on by using [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)), or they can be registered for asynchronous delivery by calling [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) or [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="7ab31-108">Weitere Informationen finden Sie [unter Benachrichtigung zu Netzwerk Ereignissen](notification-of-network-events-2.md) .</span><span class="sxs-lookup"><span data-stu-id="7ab31-108">See [Notification of Network Events](notification-of-network-events-2.md) for more information.</span></span>

 

 
