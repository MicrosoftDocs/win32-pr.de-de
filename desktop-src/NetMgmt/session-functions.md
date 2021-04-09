---
title: Sitzungs Funktionen (Netzwerkverwaltung)
description: Die Funktionen der Netzwerk Verwaltungssitzung Steuern Netzwerksitzungen, die zwischen Arbeitsstationen und Servern hergestellt werden. Die Funktionen erfordern, dass der Server Dienst auf dem Server gestartet wird.
ms.assetid: ef912cd9-be5c-4202-89aa-e60f275e8938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b1e0236881b50f0363a6c872394cfe42f44748
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858604"
---
# <a name="session-functions-network-management"></a><span data-ttu-id="f195a-104">Sitzungs Funktionen (Netzwerkverwaltung)</span><span class="sxs-lookup"><span data-stu-id="f195a-104">Session Functions (Network Management)</span></span>

<span data-ttu-id="f195a-105">Die Funktionen der Netzwerk Verwaltungssitzung Steuern Netzwerksitzungen, die zwischen Arbeitsstationen und Servern hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f195a-105">The network management session functions control network sessions established between workstations and servers.</span></span> <span data-ttu-id="f195a-106">Die Funktionen erfordern, dass der Server Dienst auf dem Server gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f195a-106">The functions require that the server service be started on the server.</span></span>

<span data-ttu-id="f195a-107">Die Sitzungs Funktionen sind nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f195a-107">The session functions are listed following.</span></span>



| <span data-ttu-id="f195a-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="f195a-108">Function</span></span>                                      | <span data-ttu-id="f195a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f195a-109">Description</span></span>                                                                                       |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f195a-110">**"Netzessiondel"**</span><span class="sxs-lookup"><span data-stu-id="f195a-110">**NetSessionDel**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)         | <span data-ttu-id="f195a-111">Löscht die aktuellen Verbindungen zwischen einer Arbeitsstation und einem Server. beendet die Netzwerksitzung.</span><span class="sxs-lookup"><span data-stu-id="f195a-111">Deletes the current connections between a workstation and server; terminates the network session.</span></span> |
| [<span data-ttu-id="f195a-112">**"Netzessionaufumum"**</span><span class="sxs-lookup"><span data-stu-id="f195a-112">**NetSessionEnum**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsessionenum)       | <span data-ttu-id="f195a-113">Gibt Informationen zu allen aktuellen Sitzungen zurück, die für einen Server eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="f195a-113">Returns information about all current sessions established for a server.</span></span>                          |
| [<span data-ttu-id="f195a-114">**"Netzessiongetinfo"**</span><span class="sxs-lookup"><span data-stu-id="f195a-114">**NetSessionGetInfo**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) | <span data-ttu-id="f195a-115">Gibt Informationen zu einer bestimmten Sitzung zurück.</span><span class="sxs-lookup"><span data-stu-id="f195a-115">Returns information about a particular session.</span></span>                                                   |



 

<span data-ttu-id="f195a-116">Eine *Sitzung* ist eine Verknüpfung zwischen einer Arbeitsstation und einem Server.</span><span class="sxs-lookup"><span data-stu-id="f195a-116">A *session* is a link between a workstation and a server.</span></span> <span data-ttu-id="f195a-117">Eine Sitzung wird erstellt, wenn eine Arbeitsstation zum ersten Mal eine Verbindung mit einer freigegebenen Ressource auf dem Server herstellt.</span><span class="sxs-lookup"><span data-stu-id="f195a-117">A session is established the first time a workstation makes a connection to a shared resource on the server.</span></span> <span data-ttu-id="f195a-118">Bis zum Ende der Sitzung sind alle weiteren Verbindungen zwischen der Arbeitsstation und dem Serverteil derselben Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f195a-118">Until the session ends, all further connections between the workstation and the server are part of the same session.</span></span> <span data-ttu-id="f195a-119">Um eine Sitzung zu beenden, ruft eine Anwendung auf dem Server Ende einer Verbindung die Funktion " [**netzessiondel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) " auf.</span><span class="sxs-lookup"><span data-stu-id="f195a-119">To end a session, an application on the server end of a connection calls the [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) function.</span></span>

<span data-ttu-id="f195a-120">Die Funktionen der Netzwerk Verwaltungssitzung verwalten die Informationen auf Benutzerbasis mit dem *username* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="f195a-120">The network management session functions manage information on a per-user basis with the *username* parameter.</span></span> <span data-ttu-id="f195a-121">Da mehrere Benutzer pro Sitzung vorhanden sein können, ist dieser Parameter erforderlich, um auf die benutzerspezifischen Informationen der Sitzung zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f195a-121">Because there can be multiple users per session, this parameter is necessary to access the user-specific information for the session.</span></span>

<span data-ttu-id="f195a-122">Sitzungs Funktionen sind auf den folgenden Informationsebenen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="f195a-122">Session functions are available at the following information levels:</span></span>

-   [<span data-ttu-id="f195a-123">**Sitzungs \_ Informationen \_ 0**</span><span class="sxs-lookup"><span data-stu-id="f195a-123">**SESSION\_INFO\_0**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_0)
-   [<span data-ttu-id="f195a-124">**Sitzungs \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f195a-124">**SESSION\_INFO\_1**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_1)
-   [<span data-ttu-id="f195a-125">**Sitzungs \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f195a-125">**SESSION\_INFO\_2**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_2)
-   [<span data-ttu-id="f195a-126">**Sitzungs \_ Informationen \_ 10**</span><span class="sxs-lookup"><span data-stu-id="f195a-126">**SESSION\_INFO\_10**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_10)
-   [<span data-ttu-id="f195a-127">**Sitzungs \_ Informationen \_ 502**</span><span class="sxs-lookup"><span data-stu-id="f195a-127">**SESSION\_INFO\_502**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-session_info_502)

<span data-ttu-id="f195a-128">Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Funktionen der Netzwerk Verwaltungssitzung erreichen können.</span><span class="sxs-lookup"><span data-stu-id="f195a-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions.</span></span> <span data-ttu-id="f195a-129">Weitere Informationen finden Sie unter [**iadssession**](/windows/desktop/api/iads/nn-iads-iadssession) und [**iadsfileserviceoperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="f195a-129">For more information, see [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
