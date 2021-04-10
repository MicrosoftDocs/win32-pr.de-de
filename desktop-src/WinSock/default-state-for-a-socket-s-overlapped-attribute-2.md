---
description: Die Socketfunktion erstellte Sockets mit dem überlappenden Attribut, das standardmäßig im ersten Wsock32.dll festgelegt ist, der 32-Bit-Version von Windows Sockets 1,1.
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: Standardzustand für das überlappende Attribut eines Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bc46fbf08731b0f73d841291f6815b43d02785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129204"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a><span data-ttu-id="8ad80-103">Standardzustand für das überlappende Attribut eines Sockets</span><span class="sxs-lookup"><span data-stu-id="8ad80-103">Default State for a Socket's Overlapped Attribute</span></span>

<span data-ttu-id="8ad80-104">Die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) erstellte Sockets mit dem überlappenden Attribut, das standardmäßig im ersten Wsock32.dll festgelegt ist, der 32-Bit-Version von Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="8ad80-104">The [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function created sockets with the overlapped attribute set by default in the first Wsock32.dll, the 32-bit version of Windows Sockets 1.1.</span></span> <span data-ttu-id="8ad80-105">Um die Abwärtskompatibilität mit aktuell bereitgestellten Wsock32.dll-Implementierungen sicherzustellen, ist dies auch bei Windows Sockets 2 der Fall.</span><span class="sxs-lookup"><span data-stu-id="8ad80-105">In order to ensure backward compatibility with currently deployed Wsock32.dll implementations, this will continue to be the case for Windows Sockets 2 as well.</span></span> <span data-ttu-id="8ad80-106">Das heißt, dass in Windows Sockets 2 Sockets, die mit der **Socket** -Funktion erstellt werden, über das überlappende Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="8ad80-106">That is, in Windows Sockets 2 sockets created with the **socket** function will have the overlapped attribute.</span></span> <span data-ttu-id="8ad80-107">Um jedoch kompatibler mit dem Rest der Windows-API zu sein, haben Sockets, die mit [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) erstellt werden, standardmäßig das überlappende Attribut.</span><span class="sxs-lookup"><span data-stu-id="8ad80-107">However, in order to be more compatible with the rest of the Windows API, sockets created with [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) will not, default, have the overlapped attribute.</span></span> <span data-ttu-id="8ad80-108">Dieses Attribut wird nur angewendet, wenn das überlappende WSA- \_ Flag \_ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8ad80-108">This attribute will only be applied if the WSA\_FLAG\_OVERLAPPED bit is set.</span></span>

 

 



