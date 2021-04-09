---
description: IP-Hilfsobjekte bieten Informations Abruf Funktionen, die für die Netzwerkverwaltung des lokalen Computers nützlich sind.
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: Abrufen von Informationen über das Internetprotokoll und das Internet Control Message-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b2768ff591b53db79bbbfb38fc2c6c2596ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958681"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a><span data-ttu-id="aba5f-103">Abrufen von Informationen über das Internetprotokoll und das Internet Control Message-Protokoll</span><span class="sxs-lookup"><span data-stu-id="aba5f-103">Retrieving Information on the Internet Protocol and the Internet Control Message Protocol</span></span>

<span data-ttu-id="aba5f-104">IP-Hilfsobjekte bieten Informations Abruf Funktionen, die für die Netzwerkverwaltung des lokalen Computers nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="aba5f-104">IP Helper provides information retrieval capabilities that are useful for the network administration of the local computer.</span></span> <span data-ttu-id="aba5f-105">Die folgenden Funktionen rufen Statistiken für das Internetprotokoll (IP) und das Internet Control Message-Protokoll (ICMP) ab.</span><span class="sxs-lookup"><span data-stu-id="aba5f-105">The following functions retrieve statistics for the Internet Protocol (IP) and the Internet Control Message Protocol (ICMP).</span></span> <span data-ttu-id="aba5f-106">Sie können diese Funktionen auch verwenden, um bestimmte Konfigurationsparameter für IP festzulegen.</span><span class="sxs-lookup"><span data-stu-id="aba5f-106">You can also use these functions to set certain configuration parameters for IP.</span></span>

<span data-ttu-id="aba5f-107">Die [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) -Funktion Ruft die aktuellen IP-Statistiken für den lokalen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="aba5f-107">The [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function retrieves the current IP statistics for the local computer.</span></span> <span data-ttu-id="aba5f-108">Codebeispiele mit **GetIpStatistics** finden [Sie unter Abrufen von Informationen mithilfe von GetIpStatistics](retrieving-information-using-getipstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="aba5f-108">For code samples involving **GetIpStatistics** see [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md).</span></span>

<span data-ttu-id="aba5f-109">Die [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) -Funktion Ruft die aktuellen ICMP-Statistiken ab.</span><span class="sxs-lookup"><span data-stu-id="aba5f-109">The [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) function retrieves the current ICMP statistics.</span></span>

<span data-ttu-id="aba5f-110">Verwenden Sie [**die Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) "Funktion", um die IP-Weiterleitung zu aktivieren oder zu deaktivieren</span><span class="sxs-lookup"><span data-stu-id="aba5f-110">Use the [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) function to enable or disable IP forwarding.</span></span> <span data-ttu-id="aba5f-111">Mit dieser Funktion können Sie auch die Standard Gültigkeitsdauer (Time-to-Live, TTL) für IP-Datagramme festlegen.</span><span class="sxs-lookup"><span data-stu-id="aba5f-111">This function also makes it possible for you to set the default time-to-live (TTL) for IP datagrams.</span></span> <span data-ttu-id="aba5f-112">Alternativ können Sie die Gültigkeitsdauer mithilfe der Funktion " [**setipttl**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="aba5f-112">Alternatively, you can set the TTL by using the [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) function.</span></span>

 

 



