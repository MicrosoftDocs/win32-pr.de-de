---
description: IP-Hilfsprogramm bietet Funktionen zum Verwalten von Netzwerkadaptern. Zwischen den Schnittstellen und Adaptern eines bestimmten Computers besteht eine eins-zu-eins-Entsprechung. Eine Schnittstelle ist eine Abstraktion auf IP-Ebene, während ein Adapter eine Abstraktion auf DataLink-Ebene ist.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Verwalten von Netzwerkadaptern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8f42cf1499ee7873d13334d0edbc9f954794f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525892"
---
# <a name="managing-network-adapters"></a><span data-ttu-id="c4f7d-105">Verwalten von Netzwerkadaptern</span><span class="sxs-lookup"><span data-stu-id="c4f7d-105">Managing Network Adapters</span></span>

<span data-ttu-id="c4f7d-106">IP-Hilfsprogramm bietet Funktionen zum Verwalten von Netzwerkadaptern.</span><span class="sxs-lookup"><span data-stu-id="c4f7d-106">IP Helper provides capabilities for managing network adapters.</span></span> <span data-ttu-id="c4f7d-107">Zwischen den Schnittstellen und Adaptern eines bestimmten Computers besteht eine eins-zu-eins-Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="c4f7d-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="c4f7d-108">Eine Schnittstelle ist eine Abstraktion auf IP-Ebene, während ein Adapter eine Abstraktion auf DataLink-Ebene ist.</span><span class="sxs-lookup"><span data-stu-id="c4f7d-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="c4f7d-109">Verwenden Sie die Funktionen, die in den folgenden Abschnitten beschrieben werden, um Informationen zu den Netzwerkadaptern auf dem lokalen Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c4f7d-109">Use the functions described in the following paragraphs to retrieve information about the network adapters in the local computer.</span></span>

<span data-ttu-id="c4f7d-110">Die [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) -Funktion gibt ein Array von [**IP- \_ Adapter \_ Informations**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) Strukturen zurück, eines für jeden Adapter auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="c4f7d-110">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns an array of [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structures, one for each adapter in the local computer.</span></span> <span data-ttu-id="c4f7d-111">Die [**getperadapterinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) -Funktion gibt zusätzliche Informationen zu einem bestimmten Adapter zurück.</span><span class="sxs-lookup"><span data-stu-id="c4f7d-111">The [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) function returns additional information about a specific adapter.</span></span> <span data-ttu-id="c4f7d-112">Die **getperadapterinfo** -Funktion erfordert, dass der Aufrufer den Index des Adapters angibt.</span><span class="sxs-lookup"><span data-stu-id="c4f7d-112">The **GetPerAdapterInfo** function requires the caller to specify the index of the adapter.</span></span> <span data-ttu-id="c4f7d-113">Verwenden Sie die [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) -Funktion, um den Adapter Index aus dem Adapter Namen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c4f7d-113">To obtain the adapter index from the adapter name, use the [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) function.</span></span>

<span data-ttu-id="c4f7d-114">Einige Anwendungen verwenden Adapter, die Datagramme empfangen, jedoch nicht übertragen können.</span><span class="sxs-lookup"><span data-stu-id="c4f7d-114">Some applications use adapters that receive datagrams, but cannot transmit them.</span></span> <span data-ttu-id="c4f7d-115">Zum Abrufen von Informationen zu diesen Adaptern verwenden Sie die [**getunidirectionaladapterinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c4f7d-115">To obtain information about these adapters, use the [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) function.</span></span>

<span data-ttu-id="c4f7d-116">Mit der Funktion " [**getadaptersadressen**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) " können Sie die einem bestimmten Adapter zugeordneten IP-Adressen abrufen.</span><span class="sxs-lookup"><span data-stu-id="c4f7d-116">The [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) function enables you to retrieve the IP addresses associated with a particular adapter.</span></span> <span data-ttu-id="c4f7d-117">Diese Funktion unterstützt sowohl IPv4-als auch IPv6-Adressierung.</span><span class="sxs-lookup"><span data-stu-id="c4f7d-117">This function supports both IPv4 and IPv6 addressing.</span></span>

-   <span data-ttu-id="c4f7d-118">Codebeispiele, die [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) betreffen, finden [Sie unter Verwalten von Netzwerkadaptern mithilfe von getadaptersinfo](managing-network-adapters-using-getadaptersinfo.md).</span><span class="sxs-lookup"><span data-stu-id="c4f7d-118">For code samples involving [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

 

 



