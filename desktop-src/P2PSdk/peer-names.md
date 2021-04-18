---
description: Peernamen werden vom Peer Name Resolution Protocol (PNRP), vom Peer Identity Manager und von der Peer Gruppierungs Infrastruktur verwendet.
ms.assetid: b0d78b17-6f48-4294-b8a2-8fcc1a7f8ef1
title: Peernamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18774939d5e0e9bad208999fbc6ca1e5f624300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351686"
---
# <a name="peer-names"></a><span data-ttu-id="b3594-103">Peernamen</span><span class="sxs-lookup"><span data-stu-id="b3594-103">Peer Names</span></span>

<span data-ttu-id="b3594-104">Peernamen werden vom Peer Name Resolution Protocol (PNRP), vom Peer Identity Manager und von der Peer Gruppierungs Infrastruktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3594-104">Peer names are used by Peer Name Resolution Protocol (PNRP), the Peer Identity Manager, and the Peer Grouping Infrastructure.</span></span> <span data-ttu-id="b3594-105">Peernamen sind stabile Namen für Ressourcen, z. b. Computer, Benutzer, Gruppen oder Dienste.</span><span class="sxs-lookup"><span data-stu-id="b3594-105">Peer names are stable names for resources such as computers, users, groups, or services.</span></span> <span data-ttu-id="b3594-106">PNRP verwendet Peernamen, um Knoten in einem Peer Netzwerk zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b3594-106">PNRP uses peer names to identify nodes in a peer network.</span></span>

> [!Note]  
> <span data-ttu-id="b3594-107">Ein Endpunkt, der von der Peer Infrastruktur verwendet wird, ist tatsächlich ein Tupel, das aus einer IPv4-oder IPv6-Adresse, einem Port und einem Protokoll (TCP oder UDP) besteht.</span><span class="sxs-lookup"><span data-stu-id="b3594-107">An endpoint that the Peer Infrastructure uses is actually a tuple that consists of an IPv4 or IPv6 address, port, and protocol (either TCP or UDP).</span></span> <span data-ttu-id="b3594-108">Ein PeerName kann mehr als ein Tupel enthalten.</span><span class="sxs-lookup"><span data-stu-id="b3594-108">One peer name can have more than one tuple.</span></span>

 

<span data-ttu-id="b3594-109">Ein PeerName ist eine Text Zeichenfolge, die das folgende Format aufweist:</span><span class="sxs-lookup"><span data-stu-id="b3594-109">A peer name is a text string that has the following format:</span></span>

-   <span data-ttu-id="b3594-110">"Authority. Classifier"</span><span class="sxs-lookup"><span data-stu-id="b3594-110">"Authority.Classifier"</span></span>

<span data-ttu-id="b3594-111">Der Wert einer Autorität hängt davon ab, ob der Name sicher oder unsicher ist.</span><span class="sxs-lookup"><span data-stu-id="b3594-111">The value of an Authority depends on whether the name is secure or unsecured.</span></span> <span data-ttu-id="b3594-112">Der Klassifizierer eines Peer namens ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b3594-112">The Classifier of a peer name is a string.</span></span> <span data-ttu-id="b3594-113">Ein Klassifizierer kann ein beliebiger Name sein, der 150 oder weniger Unicode-Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="b3594-113">A Classifier can be any name that contains 150 or less UNICODE characters.</span></span> <span data-ttu-id="b3594-114">Bei Peernamen wird die Groß-/Kleinschreibung beachtet, und Sie können als sicher oder unsicher registriert werden</span><span class="sxs-lookup"><span data-stu-id="b3594-114">Peer names are case-sensitive and can be registered as secured or unsecured.</span></span> <span data-ttu-id="b3594-115">In der folgenden Liste sind einige Beispiele für Peer Namen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="b3594-115">The following list identifies some examples of peer names:</span></span>

-   <span data-ttu-id="b3594-116">"0. myunsecuredpeer Name"</span><span class="sxs-lookup"><span data-stu-id="b3594-116">"0.MyUnsecuredPeerName"</span></span>
-   <span data-ttu-id="b3594-117">"0. JohnDoe. Games"</span><span class="sxs-lookup"><span data-stu-id="b3594-117">"0.JohnDoe.Games"</span></span>
-   <span data-ttu-id="b3594-118">"6520c005f 63fc1864b7d8f 3cabebd4916ae7f-ID. JohnDoe</span><span class="sxs-lookup"><span data-stu-id="b3594-118">"6520c005f63fc1864b7d8f3cabebd4916ae7f33d.JohnDoe"</span></span>

## <a name="secure-peer-names"></a><span data-ttu-id="b3594-119">Sichere Peernamen</span><span class="sxs-lookup"><span data-stu-id="b3594-119">Secure Peer Names</span></span>

<span data-ttu-id="b3594-120">Bei einem sicheren Namen ist die Autorität der SHA-Hash (Secure Hash Algorithmus) des öffentlichen Schlüssels des Peer namens und führt zu einer hexadezimalen Zeichenfolge von 40 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b3594-120">For a secure name, the Authority is the Secure Hash Algorithm (SHA) hash of the public key of the peer name, and results in a 40 character hexadecimal string.</span></span> <span data-ttu-id="b3594-121">Ein sicherer PeerName kann nur vom Besitzer oder Delegaten des Peer Namen Besitzers in PNRP registriert werden.</span><span class="sxs-lookup"><span data-stu-id="b3594-121">A secure peer name can only be registered with PNRP by the owner or delegate of the peer name owner.</span></span> <span data-ttu-id="b3594-122">Ein gesicherter Peername muss erstellt werden, indem [**peercreatepeername**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b3594-122">A secured peer name must be created by calling [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).</span></span>

## <a name="unsecured-peer-names"></a><span data-ttu-id="b3594-123">Unsichere Peernamen</span><span class="sxs-lookup"><span data-stu-id="b3594-123">Unsecured Peer Names</span></span>

<span data-ttu-id="b3594-124">Für einen ungesicherten Namen ist die Autorität NULL (0), und der Klassifizierer ist der einzige bedeutende Teil des Peer namens, der einen ungesicherten Peernamen ohne zugehörige [Identität](identity-manager-api.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3594-124">For an unsecured name, the Authority is zero (0), and the Classifier is the only significant part of the peer name, which creates an unsecured peer name without an associated [identity](identity-manager-api.md).</span></span> <span data-ttu-id="b3594-125">Nicht gesicherte Peernamen werden in der PNRP-namens Registrierung und-Auflösung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3594-125">Unsecured peer names are used in PNRP name registration and resolution.</span></span> <span data-ttu-id="b3594-126">Unsichere Peernamen bieten eine nützliche Möglichkeit zum Registrieren und Auflösen von Ressourcen, für die keine sichere Namensauflösung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b3594-126">Unsecured peer names provide a useful way to register and resolve resources that do not require secure name resolution.</span></span> <span data-ttu-id="b3594-127">Allerdings kann jeder beliebige Knoten den nicht gesicherten Namen veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="b3594-127">However, any node can publish any unsecured name.</span></span> <span data-ttu-id="b3594-128">Anwendungen, die die Sicherheit betreffen, müssen sicherstellen, dass Sie robust und sicher sind, wenn Sie ungesicherte Peernamen nutzen.</span><span class="sxs-lookup"><span data-stu-id="b3594-128">Applications concerned with security must ensure that they are robust and secure in their consumption of unsecured peer names.</span></span>

> [!Note]  
> <span data-ttu-id="b3594-129">Jeder kann einen ungesicherten Peernamen bei PNRP registrieren.</span><span class="sxs-lookup"><span data-stu-id="b3594-129">Anyone can register an unsecured peer name with PNRP.</span></span>

 

## <a name="pnrp-and-the-nearest-peer-name-instance"></a><span data-ttu-id="b3594-130">PNRP und die nächste Peer Namen Instanz</span><span class="sxs-lookup"><span data-stu-id="b3594-130">PNRP and the Nearest Peer Name Instance</span></span>

<span data-ttu-id="b3594-131">Es können mehrere Instanzen eines Peer namens vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b3594-131">There can be more than one instance of a peer name.</span></span> <span data-ttu-id="b3594-132">Wenn [PNRP](pnrp-namespace-provider-api.md) zum Auflösen eines Peer namens verwendet wird, gibt es ein Konzept einer **nächsten** Peer Namen Instanz. Dies bedeutet, dass der Name einen Dienst Speicherort aufweist, der dem in [**pnrpinfo \_ v1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) oder [**pnrpinfo \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))am nächsten liegenden **sahint** -Member entspricht.</span><span class="sxs-lookup"><span data-stu-id="b3594-132">When using [PNRP](pnrp-namespace-provider-api.md) to resolve a peer name, there is a concept of a **nearest** peer name instance, which means that the name has a service location closest to the **saHint** member specified in [**PNRPINFO\_V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) or [**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)).</span></span> <span data-ttu-id="b3594-133">, Wenn kein Hinweis angegeben wird, der am nächsten bei einer der lokalen IP-Adressen liegt.</span><span class="sxs-lookup"><span data-stu-id="b3594-133">If no hint is supplied, closest to one of the local IP addresses.</span></span>

 

 
