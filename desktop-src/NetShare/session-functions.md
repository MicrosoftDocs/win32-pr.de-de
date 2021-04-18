---
description: Die Funktionen der Netzwerk Verwaltungssitzung Steuern Netzwerksitzungen, die zwischen Arbeitsstationen und Servern hergestellt werden. Die Funktionen erfordern, dass der Server Dienst auf dem Server gestartet wird.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Sitzungs Funktionen (Netzwerkfreigabe Verwaltung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c672abd7c976cb9f83fa4f387dd40d175879dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354643"
---
# <a name="session-functions-network-share-management"></a><span data-ttu-id="c7082-104">Sitzungs Funktionen (Netzwerkfreigabe Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="c7082-104">Session Functions (Network Share Management)</span></span>

<span data-ttu-id="c7082-105">Die Funktionen der Netzwerk Verwaltungssitzung Steuern Netzwerksitzungen, die zwischen Arbeitsstationen und Servern hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c7082-105">The network management session functions control network sessions established between workstations and servers.</span></span> <span data-ttu-id="c7082-106">Die Funktionen erfordern, dass der Server Dienst auf dem Server gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c7082-106">The functions require that the server service be started on the server.</span></span>

<span data-ttu-id="c7082-107">Die Sitzungs Funktionen sind nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7082-107">The session functions are listed following.</span></span>



| <span data-ttu-id="c7082-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="c7082-108">Function</span></span>                                       | <span data-ttu-id="c7082-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7082-109">Description</span></span>                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7082-110">**"Netzessiondel"**</span><span class="sxs-lookup"><span data-stu-id="c7082-110">**NetSessionDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | <span data-ttu-id="c7082-111">Löscht die aktuellen Verbindungen zwischen einer Arbeitsstation und einem Server. beendet die Netzwerksitzung.</span><span class="sxs-lookup"><span data-stu-id="c7082-111">Deletes the current connections between a workstation and server; terminates the network session.</span></span> |
| [<span data-ttu-id="c7082-112">**"Netzessionaufumum"**</span><span class="sxs-lookup"><span data-stu-id="c7082-112">**NetSessionEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | <span data-ttu-id="c7082-113">Gibt Informationen zu allen aktuellen Sitzungen zurück, die für einen Server eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="c7082-113">Returns information about all current sessions established for a server.</span></span>                          |
| [<span data-ttu-id="c7082-114">**"Netzessiongetinfo"**</span><span class="sxs-lookup"><span data-stu-id="c7082-114">**NetSessionGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | <span data-ttu-id="c7082-115">Gibt Informationen zu einer bestimmten Sitzung zurück.</span><span class="sxs-lookup"><span data-stu-id="c7082-115">Returns information about a particular session.</span></span>                                                   |



 

<span data-ttu-id="c7082-116">Eine *Sitzung* ist eine Verknüpfung zwischen einer Arbeitsstation und einem Server.</span><span class="sxs-lookup"><span data-stu-id="c7082-116">A *session* is a link between a workstation and a server.</span></span> <span data-ttu-id="c7082-117">Eine Sitzung wird erstellt, wenn eine Arbeitsstation zum ersten Mal eine Verbindung mit einer freigegebenen Ressource auf dem Server herstellt.</span><span class="sxs-lookup"><span data-stu-id="c7082-117">A session is established the first time a workstation makes a connection to a shared resource on the server.</span></span> <span data-ttu-id="c7082-118">Bis zum Ende der Sitzung sind alle weiteren Verbindungen zwischen der Arbeitsstation und dem Serverteil derselben Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c7082-118">Until the session ends, all further connections between the workstation and the server are part of the same session.</span></span> <span data-ttu-id="c7082-119">Um eine Sitzung zu beenden, ruft eine Anwendung auf dem Server Ende einer Verbindung die Funktion " [**netzessiondel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) " auf.</span><span class="sxs-lookup"><span data-stu-id="c7082-119">To end a session, an application on the server end of a connection calls the [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) function.</span></span>

<span data-ttu-id="c7082-120">Die Funktionen der Netzwerk Verwaltungssitzung verwalten die Informationen auf Benutzerbasis mit dem *username* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="c7082-120">The network management session functions manage information on a per-user basis with the *username* parameter.</span></span> <span data-ttu-id="c7082-121">Da mehrere Benutzer pro Sitzung vorhanden sein können, ist dieser Parameter erforderlich, um auf die benutzerspezifischen Informationen der Sitzung zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c7082-121">Because there can be multiple users per session, this parameter is necessary to access the user-specific information for the session.</span></span>

<span data-ttu-id="c7082-122">Sitzungs Funktionen sind auf fünf Informationsebenen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="c7082-122">Session functions are available at five information levels:</span></span>

<dl>

[<span data-ttu-id="c7082-123">**Sitzungs \_ Informationen \_ 0**</span><span class="sxs-lookup"><span data-stu-id="c7082-123">**SESSION\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[<span data-ttu-id="c7082-124">**Sitzungs \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c7082-124">**SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[<span data-ttu-id="c7082-125">**Sitzungs \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c7082-125">**SESSION\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[<span data-ttu-id="c7082-126">**Sitzungs \_ Informationen \_ 10**</span><span class="sxs-lookup"><span data-stu-id="c7082-126">**SESSION\_INFO\_10**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[<span data-ttu-id="c7082-127">**Sitzungs \_ Informationen \_ 502**</span><span class="sxs-lookup"><span data-stu-id="c7082-127">**SESSION\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

<span data-ttu-id="c7082-128">Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Funktionen der Netzwerk Verwaltungssitzung erreichen können.</span><span class="sxs-lookup"><span data-stu-id="c7082-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions.</span></span> <span data-ttu-id="c7082-129">Weitere Informationen finden Sie unter [**iadssession**](/windows/desktop/api/iads/nn-iads-iadssession) und [**iadsfileserviceoperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="c7082-129">For more information, see [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
