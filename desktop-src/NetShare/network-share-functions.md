---
description: Die Netzwerkfreigabe Funktionen steuern freigegebene Ressourcen. Eine freigegebene Ressource ist eine lokale Ressource auf einem Server (z. b. ein Datenträger Verzeichnis, Druck Gerät oder Named Pipe), auf die von Benutzern und Anwendungen im Netzwerk zugegriffen werden kann.
ms.assetid: 14886bb0-e597-4728-a64f-bc16e82874da
title: Netzwerkfreigabe Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640dc877c9b482cb8ebdcef0d36e6dff562fcd8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356665"
---
# <a name="network-share-functions"></a><span data-ttu-id="4a895-104">Netzwerkfreigabe Funktionen</span><span class="sxs-lookup"><span data-stu-id="4a895-104">Network Share Functions</span></span>

<span data-ttu-id="4a895-105">Die Netzwerkfreigabe Funktionen steuern freigegebene Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4a895-105">The network share functions control shared resources.</span></span> <span data-ttu-id="4a895-106">Eine freigegebene Ressource ist eine lokale Ressource auf einem Server (z. b. ein Datenträger Verzeichnis, Druck Gerät oder Named Pipe), auf die von Benutzern und Anwendungen im Netzwerk zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4a895-106">A shared resource is a local resource on a server (for example, a disk directory, print device, or named pipe) that can be accessed by users and applications on the network.</span></span>

<span data-ttu-id="4a895-107">Die Freigabe Funktionen sind nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a895-107">The share functions are listed following.</span></span>



| <span data-ttu-id="4a895-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="4a895-108">Function</span></span>                                   | <span data-ttu-id="4a895-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a895-109">Description</span></span>                                                          |
|--------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="4a895-110">**NetShareAdd**</span><span class="sxs-lookup"><span data-stu-id="4a895-110">**NetShareAdd**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd)         | <span data-ttu-id="4a895-111">Gibt eine Ressource auf einem Server frei.</span><span class="sxs-lookup"><span data-stu-id="4a895-111">Shares a resource on a server.</span></span>                                       |
| [<span data-ttu-id="4a895-112">**Netsharecheck**</span><span class="sxs-lookup"><span data-stu-id="4a895-112">**NetShareCheck**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharecheck)     | <span data-ttu-id="4a895-113">Fragt ab, ob ein Server ein Gerät gemeinsam verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a895-113">Queries whether a server is sharing a device.</span></span>                        |
| [<span data-ttu-id="4a895-114">**Netsharedel**</span><span class="sxs-lookup"><span data-stu-id="4a895-114">**NetShareDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharedel)         | <span data-ttu-id="4a895-115">Löscht einen Freigabe Namen aus der Liste der freigegebenen Ressourcen eines Servers.</span><span class="sxs-lookup"><span data-stu-id="4a895-115">Deletes a share name from a server's list of shared resources.</span></span>       |
| [<span data-ttu-id="4a895-116">**Netshareaufumum**</span><span class="sxs-lookup"><span data-stu-id="4a895-116">**NetShareEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netshareenum)       | <span data-ttu-id="4a895-117">Ruft Freigabe Informationen zu den einzelnen freigegebenen Ressourcen auf einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="4a895-117">Retrieves share information about each shared resource on a server.</span></span>  |
| [<span data-ttu-id="4a895-118">**NetShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="4a895-118">**NetShareGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharegetinfo) | <span data-ttu-id="4a895-119">Ruft Informationen zu einer angegebenen freigegebenen Ressource auf einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="4a895-119">Retrieves information about a specified shared resource on a server.</span></span> |
| [<span data-ttu-id="4a895-120">**NetShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="4a895-120">**NetShareSetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo) | <span data-ttu-id="4a895-121">Legt die Parameter einer freigegebenen Ressource fest.</span><span class="sxs-lookup"><span data-stu-id="4a895-121">Sets a shared resource's parameters.</span></span>                                 |



 

<span data-ttu-id="4a895-122">Die [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) -Funktion ermöglicht es einem Benutzer oder einer Anwendung, mithilfe des angegebenen Freigabe namens eine Ressource eines bestimmten Typs freizugeben.</span><span class="sxs-lookup"><span data-stu-id="4a895-122">The [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) function allows a user or application to share a resource of a specific type using the specified share name.</span></span> <span data-ttu-id="4a895-123">Die Funktion **NetShareAdd** erfordert, dass der Freigabe Name und der Name des lokalen Geräts die Ressource freigeben.</span><span class="sxs-lookup"><span data-stu-id="4a895-123">The **NetShareAdd** function requires the share name and local device name to share the resource.</span></span> <span data-ttu-id="4a895-124">Ein Benutzer oder eine Anwendung muss über ein Konto auf dem Server verfügen, um auf die Ressource zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="4a895-124">A user or application must have an account on the server to access the resource.</span></span>

<span data-ttu-id="4a895-125">Sie können auch eine Sicherheits Beschreibung angeben, die einer Freigabe zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a895-125">You can also specify a security descriptor to be associated with a share.</span></span> <span data-ttu-id="4a895-126">Sicherheits Deskriptoren geben an, welche Benutzer über die Freigabe auf Dateien zugreifen dürfen und mit welchem Zugriffstyp.</span><span class="sxs-lookup"><span data-stu-id="4a895-126">Security descriptors specify which users are allowed to access files through the share, and with what type of access.</span></span> <span data-ttu-id="4a895-127">Geben Sie [**eine Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) mit der Informationsebene [**Freigabe \_ Info \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) an, wenn [**Sie NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) oder [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4a895-127">Specify a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) with the [**SHARE\_INFO\_502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) information level when calling [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) or [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo).</span></span> <span data-ttu-id="4a895-128">**NetShareSetInfo** unterstützt die Informationsebene [**Freigabe \_ Info \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) .</span><span class="sxs-lookup"><span data-stu-id="4a895-128">**NetShareSetInfo** supports the [**SHARE\_INFO\_1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) information level.</span></span> <span data-ttu-id="4a895-129">Weitere Informationen zu Sicherheits Beschreibungen finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="4a895-129">For more information about security descriptors, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="4a895-130">Die Netzwerk Verwaltungsfunktionen verwenden die folgenden speziellen Freigabe Namen für die prozessübergreifende Kommunikation (prozessübergreifende Communication, IPC) und die Remote Verwaltung des-Servers:</span><span class="sxs-lookup"><span data-stu-id="4a895-130">The network management functions use the following special share names for interprocess communication (IPC) and remote administration of the server:</span></span>

-   <span data-ttu-id="4a895-131">IPC $, für prozessübergreifende Kommunikation reserviert</span><span class="sxs-lookup"><span data-stu-id="4a895-131">IPC$, reserved for interprocess communication</span></span>
-   <span data-ttu-id="4a895-132">ADMIN $, für Remote Verwaltung reserviert</span><span class="sxs-lookup"><span data-stu-id="4a895-132">ADMIN$, reserved for remote administration</span></span>
-   <span data-ttu-id="4a895-133">A $, B $, C $ (und andere lokale Datenträger Namen, gefolgt von einem Dollarzeichen), die lokalen Datenträgern zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="4a895-133">A$, B$, C$ (and other local disk names followed by a dollar sign), assigned to local disk devices</span></span>

<span data-ttu-id="4a895-134">Um alle Verbindungen aufzulisten, die mit einer freigegebenen Ressource auf einem Server hergestellt wurden, oder um alle Verbindungen aufzulisten, die von einem bestimmten Computer hergestellt wurden, nennen Sie die [**netconnectionenum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4a895-134">To list all connections made to a shared resource on a server, or to list all connections established from a particular computer, call the [**NetConnectionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) function.</span></span> <span data-ttu-id="4a895-135">Sie können **netconnectionenum** auf den Informationsebenen [**Connection \_ Info \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) und [**Connection \_ Info \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4a895-135">You can call **NetConnectionEnum** at the [**CONNECTION\_INFO\_0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) and [**CONNECTION\_INFO\_1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) information levels.</span></span>

<span data-ttu-id="4a895-136">Freigabe Funktionen sind auf den folgenden Informationsebenen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="4a895-136">Share functions are available at the following information levels:</span></span>

<dl>

[<span data-ttu-id="4a895-137">**Freigabe \_ Informationen \_ 0**</span><span class="sxs-lookup"><span data-stu-id="4a895-137">**SHARE\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_0)  
[<span data-ttu-id="4a895-138">**Freigabe \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4a895-138">**SHARE\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1)  
[<span data-ttu-id="4a895-139">**Freigabe \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4a895-139">**SHARE\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_2)  
[<span data-ttu-id="4a895-140">**Freigabe \_ Informationen \_ 501**</span><span class="sxs-lookup"><span data-stu-id="4a895-140">**SHARE\_INFO\_501**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_501)  
[<span data-ttu-id="4a895-141">**Freigabe \_ Informationen \_ 502**</span><span class="sxs-lookup"><span data-stu-id="4a895-141">**SHARE\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502)  
[<span data-ttu-id="4a895-142">**Freigabe \_ Informationen \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="4a895-142">**SHARE\_INFO\_1005**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1005)  
</dl>

<span data-ttu-id="4a895-143">Die folgenden Informationsebenen sind nur für [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo)gültig:</span><span class="sxs-lookup"><span data-stu-id="4a895-143">The following information levels are valid only for [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):</span></span>

<dl>

[<span data-ttu-id="4a895-144">**Freigabe \_ Informationen \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="4a895-144">**SHARE\_INFO\_1004**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1004)  
[<span data-ttu-id="4a895-145">**Freigabe \_ Informationen \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="4a895-145">**SHARE\_INFO\_1006**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1006)  
[<span data-ttu-id="4a895-146">**Freigabe \_ Informationen \_ 1501**</span><span class="sxs-lookup"><span data-stu-id="4a895-146">**SHARE\_INFO\_1501**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501)  
</dl>

<span data-ttu-id="4a895-147">Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Funktionen der Netzwerk Verwaltungs Freigabe erreichen können.</span><span class="sxs-lookup"><span data-stu-id="4a895-147">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions.</span></span> <span data-ttu-id="4a895-148">Weitere Informationen finden Sie unter [**iadsfileshare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).</span><span class="sxs-lookup"><span data-stu-id="4a895-148">For more information, see [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).</span></span>

 

 
