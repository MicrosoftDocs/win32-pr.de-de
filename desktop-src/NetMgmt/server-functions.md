---
title: Server Funktionen (Netzwerkverwaltung)
description: Die Netzwerk Management Server Funktionen führen administrative Aufgaben auf einem lokalen Server oder Remote Server aus. Die Serverfunktionen sind nachfolgend aufgeführt.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43758fa822ce60d484418431941a386681bb77d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104040008"
---
# <a name="server-functions-network-management"></a><span data-ttu-id="f2895-104">Server Funktionen (Netzwerkverwaltung)</span><span class="sxs-lookup"><span data-stu-id="f2895-104">Server Functions (Network Management)</span></span>

<span data-ttu-id="f2895-105">Die Netzwerk Management Server Funktionen führen administrative Aufgaben auf einem lokalen Server oder Remote Server aus.</span><span class="sxs-lookup"><span data-stu-id="f2895-105">The network management server functions perform administrative tasks on a local or remote server.</span></span> <span data-ttu-id="f2895-106">Die Serverfunktionen sind nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2895-106">The server functions are listed following.</span></span>



| <span data-ttu-id="f2895-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="f2895-107">Function</span></span>                                       | <span data-ttu-id="f2895-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2895-108">Description</span></span>                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2895-109">**Netserverdiskerum**</span><span class="sxs-lookup"><span data-stu-id="f2895-109">**NetServerDiskEnum**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | <span data-ttu-id="f2895-110">Gibt eine Liste lokaler Laufwerke auf einem Server zurück.</span><span class="sxs-lookup"><span data-stu-id="f2895-110">Returns a list of local disk drives on a server.</span></span>                                   |
| [<span data-ttu-id="f2895-111">**NetServerEnum**</span><span class="sxs-lookup"><span data-stu-id="f2895-111">**NetServerEnum**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | <span data-ttu-id="f2895-112">Listet alle sichtbaren Server eines bestimmten Typs (oder Typen) in der angegebenen Domäne auf.</span><span class="sxs-lookup"><span data-stu-id="f2895-112">Lists all visible servers of a particular type (or types) in the specified domain.</span></span> |
| [<span data-ttu-id="f2895-113">**NetServerGetInfo**</span><span class="sxs-lookup"><span data-stu-id="f2895-113">**NetServerGetInfo**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | <span data-ttu-id="f2895-114">Gibt Konfigurationsinformationen zu einem angegebenen Server zurück.</span><span class="sxs-lookup"><span data-stu-id="f2895-114">Returns configuration information about a specified server.</span></span>                        |
| [<span data-ttu-id="f2895-115">**Netserverabfo**</span><span class="sxs-lookup"><span data-stu-id="f2895-115">**NetServerSetInfo**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | <span data-ttu-id="f2895-116">Legt die Betriebsparameter für einen Server fest.</span><span class="sxs-lookup"><span data-stu-id="f2895-116">Sets the operating parameters for a server.</span></span>                                        |



 

<span data-ttu-id="f2895-117">Nur ein Benutzer oder eine Anwendung mit Administrator Gruppenmitgliedschaft auf einem lokalen Server oder einem Remote Server kann administrative Aufgaben auf diesem Server ausführen, um den Betrieb des Servers, den Benutzer Zugriff und die Ressourcen Freigabe zu steuern.</span><span class="sxs-lookup"><span data-stu-id="f2895-117">Only a user or application with admin group membership on a local or remote server can perform administrative tasks on that server to control the server's operation, user access, and resource sharing.</span></span> <span data-ttu-id="f2895-118">Die Parameter auf niedriger Ebene, die sich auf den Vorgang eines Servers auswirken, können durch Aufrufen der Funktionen [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) und [**netserversetinfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) überprüft und geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f2895-118">The low-level parameters that affect a server's operation can be examined and modified by calling the [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) and [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) functions.</span></span> <span data-ttu-id="f2895-119">Diese Parameter werden in der LANMAN.INI Datei des Servers definiert.</span><span class="sxs-lookup"><span data-stu-id="f2895-119">These parameters are defined in the server's LANMAN.INI file.</span></span>

<span data-ttu-id="f2895-120">Die meisten Netzwerk Management Server Funktionen werden nur auf einem Remote Server ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2895-120">Most network management server functions execute only on a remote server.</span></span> <span data-ttu-id="f2895-121">Die [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) -Funktion wird entweder auf einer lokalen Arbeitsstation oder auf einem Remote Server ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2895-121">The [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) function executes on either a local workstation or a remote server.</span></span> <span data-ttu-id="f2895-122">Wenn Sie versuchen, andere Serverfunktionen auf einer lokalen Arbeitsstation auszuführen, geben die Funktionen den Fehler NERR \_ RemoteOnly zurück.</span><span class="sxs-lookup"><span data-stu-id="f2895-122">If you attempt to execute other server functions on a local workstation, the functions return the error NERR\_RemoteOnly.</span></span>

<span data-ttu-id="f2895-123">Server spezifische Informationen sind auf folgenden Ebenen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="f2895-123">Server-specific information is available at the following levels:</span></span>

-   [<span data-ttu-id="f2895-124">**Server \_ Informationen \_ 100**</span><span class="sxs-lookup"><span data-stu-id="f2895-124">**SERVER\_INFO\_100**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [<span data-ttu-id="f2895-125">**Server \_ Informationen \_ 101**</span><span class="sxs-lookup"><span data-stu-id="f2895-125">**SERVER\_INFO\_101**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [<span data-ttu-id="f2895-126">**Server \_ Informationen \_ 102**</span><span class="sxs-lookup"><span data-stu-id="f2895-126">**SERVER\_INFO\_102**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [<span data-ttu-id="f2895-127">**Server \_ Informationen \_ 402**</span><span class="sxs-lookup"><span data-stu-id="f2895-127">**SERVER\_INFO\_402**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [<span data-ttu-id="f2895-128">**Server \_ Informationen \_ 403**</span><span class="sxs-lookup"><span data-stu-id="f2895-128">**SERVER\_INFO\_403**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [<span data-ttu-id="f2895-129">**Server \_ Informationen \_ 1501**</span><span class="sxs-lookup"><span data-stu-id="f2895-129">**SERVER\_INFO\_1501**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [<span data-ttu-id="f2895-130">**Server \_ Informationen \_ 1502**</span><span class="sxs-lookup"><span data-stu-id="f2895-130">**SERVER\_INFO\_1502**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [<span data-ttu-id="f2895-131">**Server \_ Informationen \_ 1503**</span><span class="sxs-lookup"><span data-stu-id="f2895-131">**SERVER\_INFO\_1503**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [<span data-ttu-id="f2895-132">**Server \_ Informationen \_ 1506**</span><span class="sxs-lookup"><span data-stu-id="f2895-132">**SERVER\_INFO\_1506**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [<span data-ttu-id="f2895-133">**Server \_ Informationen \_ 1509**</span><span class="sxs-lookup"><span data-stu-id="f2895-133">**SERVER\_INFO\_1509**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [<span data-ttu-id="f2895-134">**Server \_ Informationen \_ 1510**</span><span class="sxs-lookup"><span data-stu-id="f2895-134">**SERVER\_INFO\_1510**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [<span data-ttu-id="f2895-135">**Server \_ Informationen \_ 1511**</span><span class="sxs-lookup"><span data-stu-id="f2895-135">**SERVER\_INFO\_1511**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [<span data-ttu-id="f2895-136">**Server \_ Informationen \_ 1512**</span><span class="sxs-lookup"><span data-stu-id="f2895-136">**SERVER\_INFO\_1512**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [<span data-ttu-id="f2895-137">**Server \_ Informationen \_ 1513**</span><span class="sxs-lookup"><span data-stu-id="f2895-137">**SERVER\_INFO\_1513**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [<span data-ttu-id="f2895-138">**Server \_ Informationen \_ 1515**</span><span class="sxs-lookup"><span data-stu-id="f2895-138">**SERVER\_INFO\_1515**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [<span data-ttu-id="f2895-139">**Server \_ Informationen \_ 1516**</span><span class="sxs-lookup"><span data-stu-id="f2895-139">**SERVER\_INFO\_1516**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [<span data-ttu-id="f2895-140">**Server \_ Informationen \_ 1518**</span><span class="sxs-lookup"><span data-stu-id="f2895-140">**SERVER\_INFO\_1518**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [<span data-ttu-id="f2895-141">**Server \_ Informationen \_ 1523**</span><span class="sxs-lookup"><span data-stu-id="f2895-141">**SERVER\_INFO\_1523**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [<span data-ttu-id="f2895-142">**Server \_ Informationen \_ 1528**</span><span class="sxs-lookup"><span data-stu-id="f2895-142">**SERVER\_INFO\_1528**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [<span data-ttu-id="f2895-143">**Server \_ Informationen \_ 1529**</span><span class="sxs-lookup"><span data-stu-id="f2895-143">**SERVER\_INFO\_1529**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [<span data-ttu-id="f2895-144">**Server \_ Informationen \_ 1530**</span><span class="sxs-lookup"><span data-stu-id="f2895-144">**SERVER\_INFO\_1530**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [<span data-ttu-id="f2895-145">**Server \_ Informationen \_ 1533**</span><span class="sxs-lookup"><span data-stu-id="f2895-145">**SERVER\_INFO\_1533**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [<span data-ttu-id="f2895-146">**Server \_ Informationen \_ 1536**</span><span class="sxs-lookup"><span data-stu-id="f2895-146">**SERVER\_INFO\_1536**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [<span data-ttu-id="f2895-147">**Server \_ Informationen \_ 1538**</span><span class="sxs-lookup"><span data-stu-id="f2895-147">**SERVER\_INFO\_1538**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [<span data-ttu-id="f2895-148">**Server \_ Informationen \_ 1539**</span><span class="sxs-lookup"><span data-stu-id="f2895-148">**SERVER\_INFO\_1539**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [<span data-ttu-id="f2895-149">**Server \_ Informationen \_ 1540**</span><span class="sxs-lookup"><span data-stu-id="f2895-149">**SERVER\_INFO\_1540**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [<span data-ttu-id="f2895-150">**Server \_ Informationen \_ 1541**</span><span class="sxs-lookup"><span data-stu-id="f2895-150">**SERVER\_INFO\_1541**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [<span data-ttu-id="f2895-151">**Server \_ Informationen \_ 1542**</span><span class="sxs-lookup"><span data-stu-id="f2895-151">**SERVER\_INFO\_1542**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [<span data-ttu-id="f2895-152">**Server \_ Informationen \_ 1544**</span><span class="sxs-lookup"><span data-stu-id="f2895-152">**SERVER\_INFO\_1544**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [<span data-ttu-id="f2895-153">**Server \_ Informationen \_ 1550**</span><span class="sxs-lookup"><span data-stu-id="f2895-153">**SERVER\_INFO\_1550**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [<span data-ttu-id="f2895-154">**Server \_ Informationen \_ 1552**</span><span class="sxs-lookup"><span data-stu-id="f2895-154">**SERVER\_INFO\_1552**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

<span data-ttu-id="f2895-155">Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Network Management Server-Funktionen erreichen können.</span><span class="sxs-lookup"><span data-stu-id="f2895-155">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management server functions.</span></span> <span data-ttu-id="f2895-156">Weitere Informationen finden Sie unter [**iadscomputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).</span><span class="sxs-lookup"><span data-stu-id="f2895-156">For more information, see [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).</span></span>

<span data-ttu-id="f2895-157">Weitere Informationen finden Sie unter [Server-und Arbeitsstations-Transport Funktionen](server-and-workstation-transport-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f2895-157">For more information, see the [Server and Workstation Transport Functions](server-and-workstation-transport-functions.md).</span></span>

 

 
