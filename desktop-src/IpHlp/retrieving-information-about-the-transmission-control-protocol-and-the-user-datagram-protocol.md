---
description: IP-Hilfsobjekte ermöglichen den Zugriff auf Informationen zu Netzwerkprotokollen, die auf dem lokalen Computer verwendet werden.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Abrufen von Informationen über das Transmission Control-Protokoll und das User Datagram-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760843"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a><span data-ttu-id="ef4a8-103">Abrufen von Informationen über das Transmission Control-Protokoll und das User Datagram-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ef4a8-103">Retrieving Information About the Transmission Control Protocol and the User Datagram Protocol</span></span>

<span data-ttu-id="ef4a8-104">IP-Hilfsobjekte ermöglichen den Zugriff auf Informationen zu Netzwerkprotokollen, die auf dem lokalen Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef4a8-104">IP Helper makes it possible to access information about network protocols that are used on the local computer.</span></span> <span data-ttu-id="ef4a8-105">Verwenden Sie die Funktionen, die in den folgenden Abschnitten beschrieben werden, um Informationen über das Transmission Control Protocol (TCP) und das User Datagram-Protokoll (UDP) auf dem lokalen Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ef4a8-105">Use the functions described in the following paragraphs to retrieve information about the Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) on the local computer.</span></span>

<span data-ttu-id="ef4a8-106">Die [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) -Funktion Ruft die aktuellen Statistiken für TCP ab.</span><span class="sxs-lookup"><span data-stu-id="ef4a8-106">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function retrieves the current statistics for TCP.</span></span> <span data-ttu-id="ef4a8-107">Codebeispiele, die **GetTcpStatistics** betreffen, finden [Sie unter Abrufen von Informationen mithilfe von GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="ef4a8-107">For code samples involving **GetTcpStatistics** see [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).</span></span>

<span data-ttu-id="ef4a8-108">Die [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) -Funktion Ruft die aktuellen Statistiken für UDP ab.</span><span class="sxs-lookup"><span data-stu-id="ef4a8-108">The [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) function retrieves the current statistics for UDP.</span></span>

<span data-ttu-id="ef4a8-109">Die [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) -Funktion Ruft die TCP-Verbindungstabelle ab.</span><span class="sxs-lookup"><span data-stu-id="ef4a8-109">The [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) function retrieves the TCP connection table.</span></span> <span data-ttu-id="ef4a8-110">Die [**getudptable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) Ruft die UDP-listenertabelle ab.</span><span class="sxs-lookup"><span data-stu-id="ef4a8-110">The [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) retrieves the UDP listener table.</span></span>

<span data-ttu-id="ef4a8-111">Mithilfe der [**settcpentry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) -Funktion kann ein Entwickler den Zustand einer angegebenen TCP-Verbindung auf den MIB- \_ TCP- \_ Status \_ Delete \_ TCB festlegen.</span><span class="sxs-lookup"><span data-stu-id="ef4a8-111">The [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) function enables a developer to set the state of a specified TCP connection to MIB\_TCP\_STATE\_DELETE\_TCB.</span></span>

 

 



