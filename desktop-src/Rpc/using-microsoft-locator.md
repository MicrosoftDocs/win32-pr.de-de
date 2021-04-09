---
title: Verwenden von Microsoft Locator
description: Microsoft Locator ist der Standard Namensdienst. Die RPC-Lauf Zeit Bibliothek verwendet diese für die Suche nach Serverprogrammen auf Server Hostsystemen.
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Verwendung von Microsoft Locator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236dce18b9286150581af925935222f3c9b3f862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856136"
---
# <a name="using-microsoft-locator"></a><span data-ttu-id="a45f0-105">Verwenden von Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="a45f0-105">Using Microsoft Locator</span></span>

<span data-ttu-id="a45f0-106">Microsoft Locator ist der Standard Namensdienst.</span><span class="sxs-lookup"><span data-stu-id="a45f0-106">Microsoft Locator is the default name service.</span></span> <span data-ttu-id="a45f0-107">Die RPC-Lauf Zeit Bibliothek verwendet diese für die Suche nach Serverprogrammen auf Server Hostsystemen.</span><span class="sxs-lookup"><span data-stu-id="a45f0-107">The RPC run-time library uses it to find server programs on server host systems.</span></span>

<span data-ttu-id="a45f0-108">**Hinweis**    Der Microsoft RPC-Serverlocatorpunkt wird in Windows Vista und höheren Betriebssystemen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a45f0-108">**Note**  Microsoft RPC locator is not supported in Windows Vista and later operating systems.</span></span>

<span data-ttu-id="a45f0-109">Vor Windows 2000 hat der Microsoft-Locator keine permanenten Namensdienst Einträge bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a45f0-109">Prior to Windows 2000, Microsoft Locator did not provide persistent name service entries.</span></span> <span data-ttu-id="a45f0-110">Alle Einträge im Name-Dienst wurden auf dem Host Computer des Server Programms in einem Arbeitsspeicher Cache gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a45f0-110">All entries in the name service were stored in a memory cache on the server program's host computer.</span></span> <span data-ttu-id="a45f0-111">Der Serverlocatorpunkt hat einen Broadcast Mechanismus verwendet, um den Standort der Server zu ermitteln, wie er von Clients angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="a45f0-111">The locator used a broadcast mechanism to discover the location of servers as requested by clients.</span></span> <span data-ttu-id="a45f0-112">Wenn das Host System heruntergefahren wird, gingen alle Namensdienst Einträge verloren.</span><span class="sxs-lookup"><span data-stu-id="a45f0-112">Whenever the host system shut down, all name service entries were lost.</span></span>

<span data-ttu-id="a45f0-113">Ab der Veröffentlichung von Windows 2000 unterstützt der Microsoft-Locator nun persistente Namensdienst Einträge.</span><span class="sxs-lookup"><span data-stu-id="a45f0-113">Beginning with the release of Windows 2000, Microsoft Locator now supports persistent name service entries.</span></span> <span data-ttu-id="a45f0-114">Um dies zu erreichen, verwendet das System einen verteilten Verzeichnisdienst zum Speichern von Namensdienst Einträgen.</span><span class="sxs-lookup"><span data-stu-id="a45f0-114">To accomplish this, the system employs a distributed directory service to store name service entries.</span></span> <span data-ttu-id="a45f0-115">Dieser Mechanismus bietet mehrere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="a45f0-115">This mechanism has several advantages:</span></span>

-   <span data-ttu-id="a45f0-116">**Persistenz.**</span><span class="sxs-lookup"><span data-stu-id="a45f0-116">**Persistence.**</span></span> <span data-ttu-id="a45f0-117">Server Programme sind nicht mehr erforderlich, um die Bindungs Informationen bei jedem Start in den Namensdienst zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="a45f0-117">Server programs are no longer required to export their binding information to the name service each time they start up.</span></span> <span data-ttu-id="a45f0-118">Der Namensdienst speichert die Informationen jetzt, bis Sie vom Serverprogramm auf dem Netzwerkadministrator explizit entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a45f0-118">The name service now stores the information until the server program on the network administrator explicitly removes it.</span></span>
-   <span data-ttu-id="a45f0-119">**Leistung.**</span><span class="sxs-lookup"><span data-stu-id="a45f0-119">**Efficiency.**</span></span> <span data-ttu-id="a45f0-120">Der Serverlocatorpunkt reduziert den Netzwerk Datenverkehr, indem der Großteil der Broadcast Informationen für Namensdienst Einträge entfällt.</span><span class="sxs-lookup"><span data-stu-id="a45f0-120">By eliminating the majority of broadcasting for name service entries, the locator reduces network traffic.</span></span> <span data-ttu-id="a45f0-121">Außerdem werden Namensdienst Einträge schneller gefunden.</span><span class="sxs-lookup"><span data-stu-id="a45f0-121">It also finds name service entries more rapidly.</span></span>
-   <span data-ttu-id="a45f0-122">**Domänen übergreifende Interoperabilität.**</span><span class="sxs-lookup"><span data-stu-id="a45f0-122">**Cross-Domain Interoperability.**</span></span> <span data-ttu-id="a45f0-123">Clients können nun Namensdienst Anforderungen über mehrere Domänen hinweg erstellen.</span><span class="sxs-lookup"><span data-stu-id="a45f0-123">Clients are now able to make name service requests across multiple domains.</span></span>

<span data-ttu-id="a45f0-124">Die aktuellen Versionen von Microsoft Locator sind abwärts kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a45f0-124">Current versions of Microsoft Locator are backward compatible.</span></span> <span data-ttu-id="a45f0-125">Beispielsweise kann ein Server Host System mit dem Serverlocatorpunkt, der im Lieferumfang von Windows 2000 enthalten ist, ordnungsgemäß in einem Netzwerk ausgeführt werden, das Server Host Systeme mit dem Serverlocatorpunkt, der im Lieferumfang von Windows NT 4,0 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a45f0-125">For instance, a server host system running the locator that ships with Windows 2000 can operate correctly on a network that contains server host systems running the locator that ships with Windows NT 4.0.</span></span>

<span data-ttu-id="a45f0-126">Mit der Veröffentlichung von Windows 2000 unterstützt der Microsoft-Locator jetzt Namensdienst Einträge für Gruppen von Benutzern.</span><span class="sxs-lookup"><span data-stu-id="a45f0-126">With the release of Windows 2000, Microsoft Locator now supports name service entries for groups of users.</span></span> <span data-ttu-id="a45f0-127">Es bietet Ihnen auch die Möglichkeit, Benutzerprofile zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a45f0-127">It also provides the ability for you to create user profiles.</span></span>

<span data-ttu-id="a45f0-128">Außerdem unterstützt die aktuelle Version von Microsoft Locator die Verwendung von Access Control Listen in Namensdienst Einträgen.</span><span class="sxs-lookup"><span data-stu-id="a45f0-128">In addition, the current version of Microsoft Locator supports the use of Access Control Lists in name service entries.</span></span> <span data-ttu-id="a45f0-129">Diese Fähigkeit erhöht die Sicherheit des Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="a45f0-129">This ability enhances the security of the network.</span></span>

<span data-ttu-id="a45f0-130">Die Plug & Play-Unterstützung ist jetzt in Microsoft Locator enthalten.</span><span class="sxs-lookup"><span data-stu-id="a45f0-130">Plug and Play support is now included in Microsoft Locator.</span></span> <span data-ttu-id="a45f0-131">Daher können Plug & Play Ereignisse wie z. b. Domänen Änderungen transparent behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="a45f0-131">Therefore, it can transparently handle Plug and Play events such as domain changes.</span></span> <span data-ttu-id="a45f0-132">Weitere Informationen finden Sie unter [**rpcnsbindingexportpnp**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) und [**rpcnsbindingunexportpnp**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).</span><span class="sxs-lookup"><span data-stu-id="a45f0-132">For more information, see [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) and [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).</span></span>

 

 




