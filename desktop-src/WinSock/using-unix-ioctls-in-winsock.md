---
description: Der von den meisten UNIX-Implementierungen bereitgestellte Befehl "siocgifconf" wird in Form von WSAIoctl-und wspioctl-Funktionen mit dem Befehl "sio \_ Get Interface List" unterstützt \_ \_ . Mit diesem Befehl wird die Liste der konfigurierten Schnittstellen und deren Parameter zurückgegeben.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Verwenden von UNIX IOCTLs in Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b52c311ea8c5f67dc374503f00c3ca16c5d053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362280"
---
# <a name="using-unix-ioctls-in-winsock"></a><span data-ttu-id="ac415-104">Verwenden von UNIX IOCTLs in Winsock</span><span class="sxs-lookup"><span data-stu-id="ac415-104">Using UNIX Ioctls in Winsock</span></span>

<span data-ttu-id="ac415-105">Der von den meisten UNIX-Implementierungen bereitgestellte Befehl " **siocgifconf** " wird in Form von [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -und [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) -Funktionen mit dem Befehl " **SIO \_ get \_ Interface \_ List**" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ac415-105">The **SIOCGIFCONF** command provided by most UNIX implementations is supported in the form of [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) and [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) functions with the command **SIO\_GET\_INTERFACE\_LIST**.</span></span> <span data-ttu-id="ac415-106">Mit diesem Befehl wird die Liste der konfigurierten Schnittstellen und deren Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ac415-106">This command returns the list of configured interfaces and their parameters.</span></span>

> [!Note]  
> <span data-ttu-id="ac415-107">Die Unterstützung dieses Befehls ist für Windows Sockets 2-kompatible TCP/IP-Dienstanbieter obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="ac415-107">Support of this command is mandatory for Windows Sockets 2-compliant TCP/IP service providers.</span></span>

 

<span data-ttu-id="ac415-108">Der *lpvoutbuffer* -Parameter verweist auf den Puffer, in dem [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) und [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) die Informationen über Schnittstellen speichern.</span><span class="sxs-lookup"><span data-stu-id="ac415-108">The parameter *lpvOutBuffer* points to the buffer in which [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) and [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) store the information about interfaces.</span></span> <span data-ttu-id="ac415-109">Die Anzahl der Schnittstellen (Anzahl der in *lpvoutbuffer* zurückgegebenen Strukturen) kann basierend auf der tatsächlichen Länge des Ausgabepuffers bestimmt werden, der in *lpcbbyteszurück* gegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ac415-109">The number of interfaces (number of structures returned in *lpvOutBuffer*) can be determined based on the actual length of the output buffer returned in *lpcbBytesReturned*.</span></span>

 

 
