---
description: Peer-zu-Peer
ms.assetid: a85fe46c-ce5f-4978-aa37-a3666560426b
title: Peer-zu-Peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62469eee79fbc501da911a60d8e21e3c6e94452
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094558"
---
# <a name="peer-to-peer"></a><span data-ttu-id="265e5-103">Peer-zu-Peer</span><span class="sxs-lookup"><span data-stu-id="265e5-103">Peer-to-Peer</span></span>

## <a name="purpose"></a><span data-ttu-id="265e5-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="265e5-104">Purpose</span></span>

<span data-ttu-id="265e5-105">Peer-to-Peer-Technologien werden verwendet, um die Kommunikation und Zusammenarbeit in Echtzeit über verteilte Netzwerke hinweg zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="265e5-105">Peer-to-peer technologies are used to facilitate real-time communication and collaboration across distributed networks.</span></span>

<span data-ttu-id="265e5-106">Im Peer-zu-Peer-Modell kann jeder PC-Benutzer ohne Verwendung von Internetservern Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="265e5-106">In the peer-to-peer model, without using Internet servers, each PC user can do the following:</span></span>

-   <span data-ttu-id="265e5-107">Austauschen von Daten</span><span class="sxs-lookup"><span data-stu-id="265e5-107">Exchange data</span></span>
-   <span data-ttu-id="265e5-108">Freigeben von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="265e5-108">Share resources</span></span>
-   <span data-ttu-id="265e5-109">Suchen nach anderen Benutzern</span><span class="sxs-lookup"><span data-stu-id="265e5-109">Locate other users</span></span>
-   <span data-ttu-id="265e5-110">Kommunizieren</span><span class="sxs-lookup"><span data-stu-id="265e5-110">Communicate</span></span>
-   <span data-ttu-id="265e5-111">Direktes Zusammenarbeiten in Echtzeit</span><span class="sxs-lookup"><span data-stu-id="265e5-111">Collaborate directly in real time</span></span>

<span data-ttu-id="265e5-112">Durch die Verwendung von Peer-zu-Peer-Technologien können Anwendungen, die die Verwendung von Computer-CPU-Zyklen und Speicher koordinieren, Ressourcen für kleine oder große Gruppen von Computern freigeben, die mit dem Internet verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="265e5-112">By using peer-to-peer technologies, applications that coordinate the use of computer CPU cycles and storage can share resources among small or large groups of computers connected to the Internet.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="265e5-113">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="265e5-113">Where applicable</span></span>

<span data-ttu-id="265e5-114">Entwickler können die Peerinfrastruktur verwenden, um eine Vielzahl verteilter, Ad-hoc- und Peer-zu-Peer-Anwendungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="265e5-114">Developers can use the Peer Infrastructure to create a wide range of distributed, ad-hoc, and peer-to-peer applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="265e5-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="265e5-115">Developer audience</span></span>

<span data-ttu-id="265e5-116">Entwickler, die die Peerinfrastruktur verwenden, sollten mit C-Programmierkonzepten vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="265e5-116">Developers using the Peer Infrastructure should be familiar with C programming concepts.</span></span> <span data-ttu-id="265e5-117">Entwickler, die den PNRP Winsock-Namespaceanbieter verwenden, sollten mit der Winsock-API vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="265e5-117">Developers using the PNRP Winsock Namespace Provider should be familiar with the Winsock API.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="265e5-118">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="265e5-118">Run-time requirements</span></span>

<span data-ttu-id="265e5-119">Die Peerinfrastruktur wird in Windows Vista, Windows XP mit Service Pack 2 (SP2) und höher sowie dem Advanced Networking Pack für Windows XP unterstützt, das für Windows XP mit Service Pack 1 (SP1) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="265e5-119">The Peer Infrastructure is supported in Windows Vista, Windows XP with Service Pack 2 (SP2) and later as well the Advanced Networking Pack for Windows XP available for Windows XP with Service Pack 1 (SP1).</span></span> <span data-ttu-id="265e5-120">Die Peer-zu-Peer-Infrastruktur erfordert, dass IPv6 installiert und initiiert wird, damit Peernetzwerkanwendungen funktionieren können.</span><span class="sxs-lookup"><span data-stu-id="265e5-120">The Peer-to-Peer Infrastructure requires that IPv6 be installed and initiated to allow peer networking applications to function.</span></span> <span data-ttu-id="265e5-121">Die Verwendung der Peer-zu-Peer-Zusammenarbeit wird nur in Windows Vista unterstützt.</span><span class="sxs-lookup"><span data-stu-id="265e5-121">Use of Peer-to-Peer Collaboration is only supported in Windows Vista .</span></span>

## <a name="in-this-section"></a><span data-ttu-id="265e5-122">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="265e5-122">In this section</span></span>



| <span data-ttu-id="265e5-123">Thema</span><span class="sxs-lookup"><span data-stu-id="265e5-123">Topic</span></span>                                                     | <span data-ttu-id="265e5-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="265e5-124">Description</span></span>                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="265e5-125">Peerinfrastruktur</span><span class="sxs-lookup"><span data-stu-id="265e5-125">Peer Infrastructure</span></span>](peer-infrastructure.md)<br/> | <span data-ttu-id="265e5-126">Informationen zur Peerinfrastruktur und zum PeerNamensauflösungsprotokoll (PNRP).</span><span class="sxs-lookup"><span data-stu-id="265e5-126">Information about the Peer Infrastructure and the Peer Name Resolution Protocol (PNRP).</span></span> <br/> |
| [<span data-ttu-id="265e5-127">Peerzusammenarbeit</span><span class="sxs-lookup"><span data-stu-id="265e5-127">Peer Collaboration</span></span>](peer-collaboration.md)<br/>   | <span data-ttu-id="265e5-128">Informationen und Referenzmaterial speziell für die Peerzusammenarbeits-API.</span><span class="sxs-lookup"><span data-stu-id="265e5-128">Information and reference material specific to the Peer Collaboration API.</span></span><br/>               |
| [<span data-ttu-id="265e5-129">Peerverteilung</span><span class="sxs-lookup"><span data-stu-id="265e5-129">Peer Distribution</span></span>](peer-distribution.md)<br/>     | <span data-ttu-id="265e5-130">Informationen und Referenzmaterial speziell für die Peerverteilungs-API.</span><span class="sxs-lookup"><span data-stu-id="265e5-130">Information and reference material specific to the Peer Distribution API.</span></span><br/>                |



 

## <a name="additional-resources"></a><span data-ttu-id="265e5-131">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="265e5-131">Additional resources</span></span>

<span data-ttu-id="265e5-132">Weitere Informationen zu Peer-zu-Peer-Technologien finden Sie an den folgenden Speicherorten:</span><span class="sxs-lookup"><span data-stu-id="265e5-132">Further information regarding Peer-to-Peer technologies can be found at the following locations:</span></span>

|                                                                                                           |                                                                                                                |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="265e5-133">Windows-Peernetzwerkressourcen</span><span class="sxs-lookup"><span data-stu-id="265e5-133">Windows Peer Networking Resources</span></span>](https://www.microsoft.com/p2p)                       | <span data-ttu-id="265e5-134">Greifen Sie auf veröffentlichte Whitepaper, Beispiele und Präsentationen zu, die die Peernetzwerktechnologie detailliert beschreiben.</span><span class="sxs-lookup"><span data-stu-id="265e5-134">Access published white-papers, samples, and presentations detailing the Peer Networking technology.</span></span><br/> |
| [<span data-ttu-id="265e5-135">Microsoft Peer Networking-Blog</span><span class="sxs-lookup"><span data-stu-id="265e5-135">Microsoft Peer Networking Blog</span></span>](/archive/blogs/p2p/)                          | <span data-ttu-id="265e5-136">Lesen Sie die neuesten Blogeinträge des Peernetzwerkteams von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="265e5-136">Read the latest blog entries from Microsoft's Peer Networking Team.</span></span><br/>                                 |
| [<span data-ttu-id="265e5-137">MSDN Peer Networking-Forum</span><span class="sxs-lookup"><span data-stu-id="265e5-137">MSDN Peer Networking Forum</span></span>](https://social.msdn.microsoft.com/forums/peertopeer/threads/)                              | <span data-ttu-id="265e5-138">Besprechen Sie Peertechnologien, und arbeiten Sie mit anderen Entwicklern zusammen.</span><span class="sxs-lookup"><span data-stu-id="265e5-138">Discuss Peer technologies and collaborate with other developers.</span></span><br/>                                    |
| [<span data-ttu-id="265e5-139">TechNet-Peernetzwerkressourcen für IT-Experten</span><span class="sxs-lookup"><span data-stu-id="265e5-139">TechNet Peer Networking Resources for IT Professionals</span></span>](https://technet.microsoft.com/library/bb742623.aspx) | <span data-ttu-id="265e5-140">Eine konzeptionelle Peernetzwerkübersicht sowie Anleitungen, die speziell für die Rolle "IT-Professional" spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="265e5-140">A conceptual Peer Networking overview, as well as guidance, specific to the IT Professional role.</span></span> <br/>  |



 

 

