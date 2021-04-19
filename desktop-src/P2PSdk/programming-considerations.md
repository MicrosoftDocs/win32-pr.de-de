---
description: In diesem Thema werden spezifische Programmierungs Überlegungen bei der Verwendung der Peer-Infrastruktur erläutert.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Überlegungen zur Programmierung (Peer-to-Peer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89956cbdbbc8d2ed89226a490bbae505862ab18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367943"
---
# <a name="programming-considerations-peer-to-peer"></a><span data-ttu-id="20ff8-103">Überlegungen zur Programmierung (Peer-to-Peer)</span><span class="sxs-lookup"><span data-stu-id="20ff8-103">Programming Considerations (Peer-to-Peer)</span></span>

<span data-ttu-id="20ff8-104">In diesem Thema werden spezifische Programmierungs Überlegungen bei der Verwendung der Peer-Infrastruktur erläutert.</span><span class="sxs-lookup"><span data-stu-id="20ff8-104">This topic discusses specific programming considerations when using the Peer Infrastructure.</span></span>

<span data-ttu-id="20ff8-105">Wenn Sie Peer-Anwendungen mithilfe der Peer Infrastruktur entwickeln, müssen Sie die folgenden Programmier Überlegungen berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="20ff8-105">When using the Peer Infrastructure to develop peer applications, you must take the following programming considerations into account:</span></span>

-   <span data-ttu-id="20ff8-106">IPv6</span><span class="sxs-lookup"><span data-stu-id="20ff8-106">IPv6</span></span>

    <span data-ttu-id="20ff8-107">Die Peer Infrastruktur erfordert, dass IPv6 installiert und gestartet wird, damit Peer Netzwerkanwendungen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="20ff8-107">The Peer Infrastructure requires that IPv6 be installed and started to enable peer networking applications to function.</span></span>

-   <span data-ttu-id="20ff8-108">Firewallports</span><span class="sxs-lookup"><span data-stu-id="20ff8-108">Firewall Ports</span></span>

    <span data-ttu-id="20ff8-109">Wenn eine Firewall in einem Netzwerk verwendet wird (z. b. die IPv6-Internetverbindungs Firewall), müssen bestimmte Ports geöffnet werden, damit die Peer Infrastruktur funktioniert.</span><span class="sxs-lookup"><span data-stu-id="20ff8-109">When a firewall is being used on a network (such as the IPv6 Internet Connection firewall), specific ports must be opened to allow the Peer Infrastructure to function.</span></span> <span data-ttu-id="20ff8-110">Die folgenden Ports müssen geöffnet sein:</span><span class="sxs-lookup"><span data-stu-id="20ff8-110">The following ports must be open:</span></span>

    <span data-ttu-id="20ff8-111">TCP-Port 3587 für die Peer Gruppierungs Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="20ff8-111">TCP port 3587 for the Peer Grouping Infrastructure.</span></span>

    <span data-ttu-id="20ff8-112">UDP-Port 3540 für die Peer graphinginfrastruktur.</span><span class="sxs-lookup"><span data-stu-id="20ff8-112">UDP port 3540 for the Peer Graphing Infrastructure.</span></span>

    > [!Note]  
    > <span data-ttu-id="20ff8-113">Anwendungen, die die Peer-graphinginfrastruktur über TCP verwenden, wählen beim Aufrufen von [**peergraphlover**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)ihren eigenen TCP-Port aus.</span><span class="sxs-lookup"><span data-stu-id="20ff8-113">Applications that use the Peer Graphing Infrastructure over TCP choose their own TCP port when calling [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span></span>

     

-   <span data-ttu-id="20ff8-114">Socketoption</span><span class="sxs-lookup"><span data-stu-id="20ff8-114">Socket Option</span></span>

    <span data-ttu-id="20ff8-115">Wenn Sie versuchen, direkt mit anderen IPv6-Peer Knoten zu verbinden (ohne die Peer Infrastruktur), stellen Sie sicher, dass die IPv6-Schutz Ebene für die Socket-Option \_ \_ auf **Schutz \_ Ebene \_ uneingeschränkt** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="20ff8-115">When attempting to connect to other IPv6 peer nodes directly (without using the Peer Infrastructure), ensure that the socket option IPV6\_PROTECTION\_LEVEL is set to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

-   <span data-ttu-id="20ff8-116">Bandbreite</span><span class="sxs-lookup"><span data-stu-id="20ff8-116">Bandwidth</span></span>

    <span data-ttu-id="20ff8-117">Bei der Verwendung von PNRP kann eine Anwendung einen oder mehrere [Peernamen](peer-names.md) veröffentlichen, die aufgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="20ff8-117">When using PNRP, an application can publish one or more [peer names](peer-names.md) that can be resolved.</span></span> <span data-ttu-id="20ff8-118">Für jeden in PNRP registrierten Peernamen gibt es eine Erhöhung der Netzwerkbandbreite, die PNRP zum Veröffentlichen des Peer namens verwendet, und bleibt verfügbar, damit Sie von anderen Knoten aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="20ff8-118">For each peer name registered with PNRP, there is an increase in the network bandwidth that PNRP uses to publish the peer name, and keep it available to be resolved by other nodes.</span></span>

    <span data-ttu-id="20ff8-119">Um zu vermeiden, dass zu viel Bandbreite verwendet wird, sollten Anwendungen eine große Anzahl von Peer Namen auf einem Computer nicht registrieren.</span><span class="sxs-lookup"><span data-stu-id="20ff8-119">To prevent using too much bandwidth, applications should avoid registering large numbers of peer names on a computer.</span></span> <span data-ttu-id="20ff8-120">Eine Anwendung, die beispielsweise Bilder veröffentlicht, sollte keinen Peernamen für jedes Bild erstellen, sondern einen Peernamen für den Dienst erstellen, der Bilder veröffentlicht, und ein anderes Protokoll verwenden, damit Clients den Dienst nach bestimmten Bildern Abfragen können.</span><span class="sxs-lookup"><span data-stu-id="20ff8-120">For example, an application that publishes pictures should not create a peer name for each picture, but should create one peer name for the service that publishes pictures, and use a different protocol for clients to query the service for specific pictures.</span></span>

-   <span data-ttu-id="20ff8-121">Peer Namen Registrierung</span><span class="sxs-lookup"><span data-stu-id="20ff8-121">Peer Name Registration</span></span>

    <span data-ttu-id="20ff8-122">Einige Anwendungen müssen möglicherweise denselben [Peernamen](peer-names.md) auf mehr als einem Computer registrieren.</span><span class="sxs-lookup"><span data-stu-id="20ff8-122">Some applications may be required to register the same [peer name](peer-names.md) on more than one computer.</span></span> <span data-ttu-id="20ff8-123">Dies geschieht in der Regel, wenn ein PeerName einer Person zugeordnet ist, die mehr als einen Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="20ff8-123">Typically, this happens if a peer name is associated with a person who uses more than one computer.</span></span> <span data-ttu-id="20ff8-124">Eine Methode, mit der Sie denselben Peernamen auf mehreren Computern registrieren können, besteht darin, eine Peer Gruppe für die Person zu erstellen und von allen Computern aus eine Verbindung mit dieser Gruppe herzustellen.</span><span class="sxs-lookup"><span data-stu-id="20ff8-124">One method that you can use to register the same peer name on multiple computers is to create a peer group for the person, and connect to that group from all computers.</span></span> <span data-ttu-id="20ff8-125">Eine andere Methode besteht darin, eine Peer Identität und einen Peernamen auf einem Computer zu erstellen, die Peer Identität von diesem Computer zu exportieren und auf anderen Computern zu importieren.</span><span class="sxs-lookup"><span data-stu-id="20ff8-125">Another method is to create a peer identity and peer name on one computer, export the peer identity from that computer, and import it on other computers.</span></span> <span data-ttu-id="20ff8-126">Dadurch kann derselbe sichere Peer Name auf allen Computern erstellt werden, die die Peer Identität importiert haben.</span><span class="sxs-lookup"><span data-stu-id="20ff8-126">This allows the same secure peer name to be created on all the computers that have imported the peer identity.</span></span>

 

 



