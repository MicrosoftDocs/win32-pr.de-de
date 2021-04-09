---
description: Verwendung blockierender e/a-Vorgänge, nicht blockierende e/a-Vorgänge mit asynchroner Benachrichtigung über Netzwerkereignisse und überlappende e/a-Vorgänge mit Abschluss Angabe in Windows Sockets 2 (Winsock).
ms.assetid: 07f34177-72bc-4b2a-b655-57e53d1742b0
title: Socket-e/a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efcd325a0a379671dd39709f37e2c6d2133ca27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129117"
---
# <a name="socket-io"></a><span data-ttu-id="b69a0-103">Socket-e/a</span><span class="sxs-lookup"><span data-stu-id="b69a0-103">Socket I/O</span></span>

<span data-ttu-id="b69a0-104">Es gibt drei Hauptmethoden zum Ausführen von e/a-Vorgängen in Windows Sockets 2:</span><span class="sxs-lookup"><span data-stu-id="b69a0-104">There are three primary ways of doing I/O in Windows Sockets 2:</span></span>

-   <span data-ttu-id="b69a0-105">Blockierende e/a.</span><span class="sxs-lookup"><span data-stu-id="b69a0-105">Blocking I/O.</span></span>
-   <span data-ttu-id="b69a0-106">Nicht blockierende e/a-Vorgänge sowie asynchrone Benachrichtigungen von Netzwerk Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="b69a0-106">Nonblocking I/O along with asynchronous notification of network events.</span></span>
-   <span data-ttu-id="b69a0-107">Überlappende e/a-Vorgänge mit Abschluss Angabe.</span><span class="sxs-lookup"><span data-stu-id="b69a0-107">Overlapped I/O with completion indication.</span></span>

<span data-ttu-id="b69a0-108">In den folgenden Abschnitten werden die einzelnen Methoden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b69a0-108">We describe each method in the following sections.</span></span> <span data-ttu-id="b69a0-109">Blockierende e/a-Vorgänge sind das Standardverhalten, der nicht Blockierungs Modus kann für jeden Socket verwendet werden, der in den nicht blockierenden Modus versetzt wird. überlappende e/a-Vorgänge können nur bei Sockets auftreten, die mit dem überlappenden Attribut erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b69a0-109">Blocking I/O is the default behavior, nonblocking mode can be used on any socket that is placed into nonblocking mode, and overlapped I/O can only occur on sockets that are created with the overlapped attribute.</span></span> <span data-ttu-id="b69a0-110">Beachten Sie außerdem, dass die beiden Aufrufe zum Senden von: [**wspsend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) und [**wspsendto**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) und die beiden Aufrufe zum Empfangen von: [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) und [**wsprecvfrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) jeweils alle drei e/a-Methoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="b69a0-110">It is also interesting to note that the two calls for sending: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) and the two calls for receiving: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) each implement all three methods of I/O.</span></span> <span data-ttu-id="b69a0-111">Dienstanbieter bestimmen, wie der e/a-Vorgang auf der Grundlage von Socketmodi, Attributen und Eingabeparameter Werten durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b69a0-111">Service providers determine how to perform the I/O operation based on socket modes, attributes, and the input parameter values.</span></span>

 

 
