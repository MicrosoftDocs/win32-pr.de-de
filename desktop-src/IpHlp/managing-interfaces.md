---
description: IP Helper erweitert ihre Fähigkeiten zum Verwalten von Netzwerkschnittstellen. Zwischen den Schnittstellen und Adaptern eines bestimmten Computers besteht eine eins-zu-eins-Entsprechung. Eine Schnittstelle ist eine Abstraktion auf IP-Ebene, während ein Adapter eine Abstraktion auf DataLink-Ebene ist.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Verwalten von Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d79d46ec1ba7606cbc7e79b4312432984239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215919"
---
# <a name="managing-interfaces"></a><span data-ttu-id="f8d21-105">Verwalten von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f8d21-105">Managing Interfaces</span></span>

<span data-ttu-id="f8d21-106">IP Helper erweitert ihre Fähigkeiten zum Verwalten von Netzwerkschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="f8d21-106">IP Helper extends your abilities to manage network interfaces.</span></span> <span data-ttu-id="f8d21-107">Zwischen den Schnittstellen und Adaptern eines bestimmten Computers besteht eine eins-zu-eins-Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="f8d21-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="f8d21-108">Eine Schnittstelle ist eine Abstraktion auf IP-Ebene, während ein Adapter eine Abstraktion auf DataLink-Ebene ist.</span><span class="sxs-lookup"><span data-stu-id="f8d21-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="f8d21-109">Verwenden Sie die Funktionen, die in den folgenden Abschnitten beschrieben werden, um Schnittstellen auf dem lokalen Computer zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="f8d21-109">Use the functions described in the following paragraphs to manage interfaces on the local computer.</span></span>

<span data-ttu-id="f8d21-110">Die [**getnumofinterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) -Funktion gibt die Anzahl der Schnittstellen auf dem lokalen Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="f8d21-110">The [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) function returns the number of interfaces on the local computer.</span></span>

<span data-ttu-id="f8d21-111">Die [**getinterfakeinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) -Funktion gibt eine Tabelle zurück, die die Namen und die entsprechenden Indizes für die Schnittstellen auf dem lokalen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="f8d21-111">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function returns a table that contains the names and corresponding indexes for the interfaces on the local computer.</span></span> <span data-ttu-id="f8d21-112">Codebeispiele, die **getinterfacetten Info** betreffen, finden [Sie unter Verwalten von Schnittstellen mithilfe von getinterfacetten](managing-interfaces-using-getinterfaceinfo.md)Info.</span><span class="sxs-lookup"><span data-stu-id="f8d21-112">For code samples involving **GetInterfaceInfo** see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="f8d21-113">Die [**getfriendlyifindex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) -Funktion nimmt einen Schnittstellen Index an und gibt einen abwärts kompatiblen Schnittstellen Index zurück, d. h. einen, der nur die unteren 24 Bits verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8d21-113">The [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) function takes an interface index and returns a backward-compatible interface index, that is, one that uses only the lower 24 bits.</span></span> <span data-ttu-id="f8d21-114">Dieser Indextyp wird manchmal als "benutzerfreundlicher" Schnittstellen Index bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f8d21-114">This type of index is sometimes referred to as a "friendly" interface index.</span></span>

<span data-ttu-id="f8d21-115">Die [**getif Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) -Funktion gibt eine [**MIB- \_ ifrow**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) -Struktur zurück, die Informationen zu einer bestimmten Schnittstelle auf dem lokalen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="f8d21-115">The [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) function returns a [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) structure that contains information about a particular interface on the local computer.</span></span> <span data-ttu-id="f8d21-116">Diese Funktion erfordert, dass der Aufrufer den Index der-Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f8d21-116">This function requires the caller to supply the index of the interface.</span></span>

<span data-ttu-id="f8d21-117">Die [**getiftable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) -Funktion gibt eine Tabelle mit [**MIB \_ ifrow**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) -Einträgen zurück, eine für jede Schnittstelle auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="f8d21-117">The [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) function returns a table of [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) entries, one for each interface on the computer.</span></span>

<span data-ttu-id="f8d21-118">Verwenden Sie [**die Funktion "**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) -Funktion", um die Konfiguration einer bestimmten Schnittstelle zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f8d21-118">Use the [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) function to modify the configuration of a particular interface.</span></span>

 

 
