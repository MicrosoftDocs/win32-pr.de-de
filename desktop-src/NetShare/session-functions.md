---
description: Grundlegendes zu Sitzungsfunktionen in der Verwaltung von Netzwerkfreigaben. Diese Funktionen steuern Netzwerksitzungen, die zwischen Arbeitsstationen und Servern eingerichtet wurden.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Sitzungsfunktionen (Netzwerkfreigabeverwaltung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdde451eb2942171569b24c36aae5d5742208e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409723"
---
# <a name="session-functions-network-share-management"></a><span data-ttu-id="948a6-104">Sitzungsfunktionen (Netzwerkfreigabeverwaltung)</span><span class="sxs-lookup"><span data-stu-id="948a6-104">Session Functions (Network Share Management)</span></span>

<span data-ttu-id="948a6-105">Die Netzwerkverwaltungssitzungsfunktionen steuern Netzwerksitzungen, die zwischen Arbeitsstationen und Servern eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="948a6-105">The network management session functions control network sessions established between workstations and servers.</span></span> <span data-ttu-id="948a6-106">Die Funktionen erfordern, dass der Serverdienst auf dem Server gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="948a6-106">The functions require that the server service be started on the server.</span></span>

<span data-ttu-id="948a6-107">Die Sitzungsfunktionen sind im Folgenden aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="948a6-107">The session functions are listed following.</span></span>



| <span data-ttu-id="948a6-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="948a6-108">Function</span></span>                                       | <span data-ttu-id="948a6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="948a6-109">Description</span></span>                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="948a6-110">**NetSessionDel**</span><span class="sxs-lookup"><span data-stu-id="948a6-110">**NetSessionDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | <span data-ttu-id="948a6-111">Löscht die aktuellen Verbindungen zwischen einer Arbeitsstation und einem Server. beendet die Netzwerksitzung.</span><span class="sxs-lookup"><span data-stu-id="948a6-111">Deletes the current connections between a workstation and server; terminates the network session.</span></span> |
| [<span data-ttu-id="948a6-112">**NetSessionEnum**</span><span class="sxs-lookup"><span data-stu-id="948a6-112">**NetSessionEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | <span data-ttu-id="948a6-113">Gibt Informationen zu allen aktuellen Sitzungen zurück, die für einen Server eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="948a6-113">Returns information about all current sessions established for a server.</span></span>                          |
| [<span data-ttu-id="948a6-114">**NetSessionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="948a6-114">**NetSessionGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | <span data-ttu-id="948a6-115">Gibt Informationen zu einer bestimmten Sitzung zurück.</span><span class="sxs-lookup"><span data-stu-id="948a6-115">Returns information about a particular session.</span></span>                                                   |



 

<span data-ttu-id="948a6-116">Eine *Sitzung* ist eine Verknüpfung zwischen einer Arbeitsstation und einem Server.</span><span class="sxs-lookup"><span data-stu-id="948a6-116">A *session* is a link between a workstation and a server.</span></span> <span data-ttu-id="948a6-117">Wenn eine Arbeitsstation zum ersten Mal eine Verbindung mit einer freigegebenen Ressource auf dem Server herstellen soll, wird eine Sitzung eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="948a6-117">A session is established the first time a workstation makes a connection to a shared resource on the server.</span></span> <span data-ttu-id="948a6-118">Bis zum Ende der Sitzung sind alle weiteren Verbindungen zwischen der Arbeitsstation und dem Server Teil derselben Sitzung.</span><span class="sxs-lookup"><span data-stu-id="948a6-118">Until the session ends, all further connections between the workstation and the server are part of the same session.</span></span> <span data-ttu-id="948a6-119">Um eine Sitzung zu beenden, ruft eine Anwendung auf dem Serverende einer Verbindung die [**NetSessionDel-Funktion**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) auf.</span><span class="sxs-lookup"><span data-stu-id="948a6-119">To end a session, an application on the server end of a connection calls the [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) function.</span></span>

<span data-ttu-id="948a6-120">Die Netzwerkverwaltungssitzungsfunktionen verwalten Informationen pro Benutzer mit dem *Parameter username.*</span><span class="sxs-lookup"><span data-stu-id="948a6-120">The network management session functions manage information on a per-user basis with the *username* parameter.</span></span> <span data-ttu-id="948a6-121">Da es mehrere Benutzer pro Sitzung geben kann, ist dieser Parameter erforderlich, um auf die benutzerspezifischen Informationen für die Sitzung zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="948a6-121">Because there can be multiple users per session, this parameter is necessary to access the user-specific information for the session.</span></span>

<span data-ttu-id="948a6-122">Sitzungsfunktionen sind auf fünf Informationsebenen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="948a6-122">Session functions are available at five information levels:</span></span>

<dl>

[<span data-ttu-id="948a6-123">**\_SITZUNGSINFORMATIONEN \_ 0**</span><span class="sxs-lookup"><span data-stu-id="948a6-123">**SESSION\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[<span data-ttu-id="948a6-124">**\_SITZUNGSINFORMATIONEN \_ 1**</span><span class="sxs-lookup"><span data-stu-id="948a6-124">**SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[<span data-ttu-id="948a6-125">**\_SITZUNGSINFORMATIONEN \_ 2**</span><span class="sxs-lookup"><span data-stu-id="948a6-125">**SESSION\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[<span data-ttu-id="948a6-126">**\_SITZUNGSINFORMATIONEN \_ 10**</span><span class="sxs-lookup"><span data-stu-id="948a6-126">**SESSION\_INFO\_10**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[<span data-ttu-id="948a6-127">**\_SITZUNGSINFORMATIONEN \_ 502**</span><span class="sxs-lookup"><span data-stu-id="948a6-127">**SESSION\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

<span data-ttu-id="948a6-128">Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte ADSI-Methoden (Active Directory Service Interface) aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Netzwerkverwaltungssitzungsfunktionen erreichen können.</span><span class="sxs-lookup"><span data-stu-id="948a6-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions.</span></span> <span data-ttu-id="948a6-129">Weitere Informationen finden Sie unter [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) und [**IADsFileServiceOperations.**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)</span><span class="sxs-lookup"><span data-stu-id="948a6-129">For more information, see [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
