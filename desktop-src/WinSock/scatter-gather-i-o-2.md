---
description: Die Funktionen "WSARecv", "WSARecvFrom", "wsarecvmsg", "wsasend", "wsasendmsg" und "WSASendTo" nehmen ein Array von Anwendungs Puffern als Eingabeparameter an und können für die e/a-Vorgänge vom Typ "Scatter/Gather" (oder "VEC
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: Scatter/Gather-e/a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c572892a75b3532d68a39e2fabdcc971f0a3327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355641"
---
# <a name="scattergather-io"></a><span data-ttu-id="f9baf-103">Scatter/Gather-e/a</span><span class="sxs-lookup"><span data-stu-id="f9baf-103">Scatter/Gather I/O</span></span>

<span data-ttu-id="f9baf-104">Die Funktionen " [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)", " [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)", " [**LPFN_WSARECVMSG" (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), " [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)", " [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)" und " [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) " nehmen ein Array von Anwendungs Puffern als Eingabeparameter an und können für die e/a-Vorgänge für Punkt/Erfassung (oder Vektoren) verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f9baf-104">The [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg), and [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) functions all take an array of application buffers as input parameters and can be used for scatter/gather (or vectored) I/O.</span></span> <span data-ttu-id="f9baf-105">Dies kann sehr nützlich sein, wenn Teile jeder übermittelten Nachricht zusätzlich zum Nachrichtentext aus einer oder mehreren Header Komponenten fester Länge bestehen.</span><span class="sxs-lookup"><span data-stu-id="f9baf-105">This can be very useful in instances where portions of each message being transmitted consist of one or more fixed-length header components in addition to the message body.</span></span> <span data-ttu-id="f9baf-106">Diese Header Komponenten müssen von der Anwendung nicht in einem einzelnen zusammenhängenden Puffer vor dem Senden verkettet werden.</span><span class="sxs-lookup"><span data-stu-id="f9baf-106">Such header components need not be concatenated by the application into a single contiguous buffer prior to sending.</span></span> <span data-ttu-id="f9baf-107">Beim Empfang von können die Header Komponenten automatisch in separate Puffer aufgeteilt werden, sodass der Nachrichtentext selbst nicht mehr angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f9baf-107">Likewise on receiving, the header components can be automatically split off into separate buffers, leaving the message body by itself.</span></span>

<span data-ttu-id="f9baf-108">Beim Empfang in mehrere Puffer erfolgt der Abschluss, wenn Daten aus dem Netzwerk eintreffen, unabhängig davon, ob alle angegebenen Puffer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9baf-108">When receiving into multiple buffers, completion occurs as data arrives from the network, regardless of whether all the supplied buffers are utilized.</span></span>

 

 
