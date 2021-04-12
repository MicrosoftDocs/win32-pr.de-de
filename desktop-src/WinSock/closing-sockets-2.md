---
description: Wspclosesocket gibt den socketdeskriptor frei, sodass alle ausstehenden Vorgänge in allen Threads desselben Prozesses abgebrochen werden, und jeder weitere Verweis darauf schlägt fehl.
ms.assetid: 658d0c35-05d4-4b51-a4d3-a3b441a2c735
title: Schließen von Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d0c877767925f67e07427a77dc8ec8445f30c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526189"
---
# <a name="closing-sockets"></a><span data-ttu-id="d770f-103">Schließen von Sockets</span><span class="sxs-lookup"><span data-stu-id="d770f-103">Closing Sockets</span></span>

<span data-ttu-id="d770f-104">[**Wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) gibt den socketdeskriptor frei, sodass alle ausstehenden Vorgänge in allen Threads desselben Prozesses abgebrochen werden, und jeder weitere Verweis darauf schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="d770f-104">[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) releases the socket descriptor so that any pending operations in any threads of the same process will be aborted, and any further reference to it will fail.</span></span> <span data-ttu-id="d770f-105">Beachten Sie, dass ein Verweis Zähler für freigegebene Sockets verwendet werden sollte. wenn es sich hierbei um den letzten Verweis auf einen zugrunde liegenden Socket handelt, sollten die diesem Socket zugeordneten Informationen verworfen werden, wenn ein ordnungsgemäßes schließen nicht angefordert wird (d. h., dass \_ DontLinger nicht festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="d770f-105">Note that a reference count should be employed for shared sockets, and only if this is the last reference to an underlying socket, should the information associated with this socket be discarded, provided graceful close is not requested (that is, SO\_DONTLINGER is not set).</span></span> <span data-ttu-id="d770f-106">Im Fall der \_ Festlegung von DontLinger werden alle Daten, die für die Übertragung in die Warteschlange eingereiht werden, nach Möglichkeit gesendet, bevor dem Socket zugeordnete Informationen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d770f-106">In the case of SO\_DONTLINGER being set, any data queued for transmission will be sent, if possible, before information associated with the socket is released.</span></span> <span data-ttu-id="d770f-107">Weitere Informationen finden Sie unter **wspclosesocket** .</span><span class="sxs-lookup"><span data-stu-id="d770f-107">See **WSPCloseSocket** for more information.</span></span>

<span data-ttu-id="d770f-108">Für nonifs-Dienstanbieter muss [**wpuclosesockethandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) aufgerufen werden, um den Sockethandle zurück zur Windows Sockets 2-dll freizugeben.</span><span class="sxs-lookup"><span data-stu-id="d770f-108">For nonIFS service providers, [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) must be invoked to release the socket handle back to the Windows Sockets 2 DLL.</span></span>

 

 
