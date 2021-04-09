---
description: .
ms.assetid: a85fe46c-ce5f-4978-aa37-a3666560426b
title: Peer-to-Peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3fe029d8d6e4c6e6d9759283ec5b73996fc7b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867460"
---
# <a name="peer-to-peer"></a><span data-ttu-id="a6579-103">Peer-to-Peer</span><span class="sxs-lookup"><span data-stu-id="a6579-103">Peer-to-Peer</span></span>

## <a name="purpose"></a><span data-ttu-id="a6579-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="a6579-104">Purpose</span></span>

<span data-ttu-id="a6579-105">Peer-to-Peer-Technologien werden verwendet, um die Echtzeitkommunikation und Zusammenarbeit in verteilten Netzwerken zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a6579-105">Peer-to-peer technologies are used to facilitate real-time communication and collaboration across distributed networks.</span></span>

<span data-ttu-id="a6579-106">Im Peer-to-Peer-Modell, ohne Internet Server zu verwenden, kann jeder PC-Benutzer folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="a6579-106">In the peer-to-peer model, without using Internet servers, each PC user can do the following:</span></span>

-   <span data-ttu-id="a6579-107">Austauschen von Daten</span><span class="sxs-lookup"><span data-stu-id="a6579-107">Exchange data</span></span>
-   <span data-ttu-id="a6579-108">Freigeben von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a6579-108">Share resources</span></span>
-   <span data-ttu-id="a6579-109">Andere Benutzer suchen</span><span class="sxs-lookup"><span data-stu-id="a6579-109">Locate other users</span></span>
-   <span data-ttu-id="a6579-110">Kommunizieren</span><span class="sxs-lookup"><span data-stu-id="a6579-110">Communicate</span></span>
-   <span data-ttu-id="a6579-111">Direkte Zusammenarbeit in Echtzeit</span><span class="sxs-lookup"><span data-stu-id="a6579-111">Collaborate directly in real time</span></span>

<span data-ttu-id="a6579-112">Durch die Verwendung von Peer-to-Peer-Technologien können Anwendungen, die die Verwendung von Computer-CPU-Zyklen und-Speicher koordinieren, Ressourcen zwischen kleinen oder großen Gruppen von Computern gemeinsam nutzen, die mit dem Internet verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="a6579-112">By using peer-to-peer technologies, applications that coordinate the use of computer CPU cycles and storage can share resources among small or large groups of computers connected to the Internet.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="a6579-113">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="a6579-113">Where applicable</span></span>

<span data-ttu-id="a6579-114">Entwickler können die Peer Infrastruktur verwenden, um eine große Bandbreite von verteilten Ad-hoc-und Peer-to-Peer-Anwendungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a6579-114">Developers can use the Peer Infrastructure to create a wide range of distributed, ad-hoc, and peer-to-peer applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a6579-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="a6579-115">Developer audience</span></span>

<span data-ttu-id="a6579-116">Entwickler, die die Peer Infrastruktur verwenden, sollten mit C-Programmier Konzepten vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="a6579-116">Developers using the Peer Infrastructure should be familiar with C programming concepts.</span></span> <span data-ttu-id="a6579-117">Entwickler, die den PNRP-Winsock-Namespace Anbieter verwenden, sollten mit der Winsock-API vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="a6579-117">Developers using the PNRP Winsock Namespace Provider should be familiar with the Winsock API.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a6579-118">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="a6579-118">Run-time requirements</span></span>

<span data-ttu-id="a6579-119">Die Peer Infrastruktur wird in Windows Vista, Windows XP mit Service Pack 2 (SP2) und höher unterstützt. Außerdem ist das erweiterte Netzwerk Paket für Windows XP verfügbar, das für Windows XP mit Service Pack 1 (SP1) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a6579-119">The Peer Infrastructure is supported in Windows Vista, Windows XP with Service Pack 2 (SP2) and later as well the Advanced Networking Pack for Windows XP available for Windows XP with Service Pack 1 (SP1).</span></span> <span data-ttu-id="a6579-120">Die Peer-to-Peer-Infrastruktur erfordert, dass IPv6 installiert und initiiert wird, damit Peer Netzwerkanwendungen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="a6579-120">The Peer-to-Peer Infrastructure requires that IPv6 be installed and initiated to allow peer networking applications to function.</span></span> <span data-ttu-id="a6579-121">Die Verwendung der Peer-zu-Peer-Zusammenarbeit wird nur in Windows Vista unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6579-121">Use of Peer-to-Peer Collaboration is only supported in Windows Vista .</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a6579-122">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a6579-122">In this section</span></span>



| <span data-ttu-id="a6579-123">Thema</span><span class="sxs-lookup"><span data-stu-id="a6579-123">Topic</span></span>                                                     | <span data-ttu-id="a6579-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6579-124">Description</span></span>                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6579-125">Peer Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="a6579-125">Peer Infrastructure</span></span>](peer-infrastructure.md)<br/> | <span data-ttu-id="a6579-126">Informationen zur Peer Infrastruktur und zum Peer Name Resolution-Protokoll (PNRP).</span><span class="sxs-lookup"><span data-stu-id="a6579-126">Information about the Peer Infrastructure and the Peer Name Resolution Protocol (PNRP).</span></span> <br/> |
| [<span data-ttu-id="a6579-127">Peer Zusammenarbeit</span><span class="sxs-lookup"><span data-stu-id="a6579-127">Peer Collaboration</span></span>](peer-collaboration.md)<br/>   | <span data-ttu-id="a6579-128">Informationen und Referenzmaterial speziell für die Peer Kollaborations-API.</span><span class="sxs-lookup"><span data-stu-id="a6579-128">Information and reference material specific to the Peer Collaboration API.</span></span><br/>               |
| [<span data-ttu-id="a6579-129">Peer Verteilung</span><span class="sxs-lookup"><span data-stu-id="a6579-129">Peer Distribution</span></span>](peer-distribution.md)<br/>     | <span data-ttu-id="a6579-130">Informationen und Referenzmaterial speziell für die Peer Distribution-API.</span><span class="sxs-lookup"><span data-stu-id="a6579-130">Information and reference material specific to the Peer Distribution API.</span></span><br/>                |



 

## <a name="additional-resources"></a><span data-ttu-id="a6579-131">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a6579-131">Additional resources</span></span>

<span data-ttu-id="a6579-132">Weitere Informationen zu Peer-to-Peer-Technologien finden Sie unter den folgenden Speicherorten:</span><span class="sxs-lookup"><span data-stu-id="a6579-132">Further information regarding Peer-to-Peer technologies can be found at the following locations:</span></span>

|                                                                                                           |                                                                                                                |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6579-133">Windows-Peer-Netzwerkressourcen</span><span class="sxs-lookup"><span data-stu-id="a6579-133">Windows Peer Networking Resources</span></span>](https://www.microsoft.com/p2p)                       | <span data-ttu-id="a6579-134">Greifen Sie auf veröffentlichte Whitepaper, Beispiele und Präsentationen zu, die die Peer-Netzwerktechnologie erläutern.</span><span class="sxs-lookup"><span data-stu-id="a6579-134">Access published white-papers, samples, and presentations detailing the Peer Networking technology.</span></span><br/> |
| [<span data-ttu-id="a6579-135">Blog zu Microsoft-Peer Netzwerken</span><span class="sxs-lookup"><span data-stu-id="a6579-135">Microsoft Peer Networking Blog</span></span>](/archive/blogs/p2p/)                          | <span data-ttu-id="a6579-136">Lesen Sie die neuesten Blogeinträge des Peer Networking Teams von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a6579-136">Read the latest blog entries from Microsoft's Peer Networking Team.</span></span><br/>                                 |
| [<span data-ttu-id="a6579-137">MSDN-Peer Netzwerk Forum</span><span class="sxs-lookup"><span data-stu-id="a6579-137">MSDN Peer Networking Forum</span></span>](https://social.msdn.microsoft.com/forums/peertopeer/threads/)                              | <span data-ttu-id="a6579-138">Diskutieren Sie Peer Technologien, und arbeiten Sie mit anderen Entwicklern zusammen.</span><span class="sxs-lookup"><span data-stu-id="a6579-138">Discuss Peer technologies and collaborate with other developers.</span></span><br/>                                    |
| [<span data-ttu-id="a6579-139">TechNet-Peer-Netzwerkressourcen für IT-Experten</span><span class="sxs-lookup"><span data-stu-id="a6579-139">TechNet Peer Networking Resources for IT Professionals</span></span>](https://technet.microsoft.com/library/bb742623.aspx) | <span data-ttu-id="a6579-140">Eine Übersicht über konzeptionelle Peer Netzwerke sowie Anleitungen, die für die IT-professionelle Rolle spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="a6579-140">A conceptual Peer Networking overview, as well as guidance, specific to the IT Professional role.</span></span> <br/>  |



 

 

