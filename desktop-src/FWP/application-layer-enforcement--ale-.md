---
title: Durchsetzung der Anwendungsschicht (ALE)
description: ALE ist ein Satz von Windows Filtering Platform (WFP)-kernelmodusschichten, die für die Zustands behaftete Filterung verwendet werden.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f4cab1b2583d221c59d83c513c451077c806129
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390269"
---
# <a name="application-layer-enforcement-ale"></a><span data-ttu-id="fd42e-103">Durchsetzung der Anwendungsschicht (ALE)</span><span class="sxs-lookup"><span data-stu-id="fd42e-103">Application Layer Enforcement (ALE)</span></span>

<span data-ttu-id="fd42e-104">ALE ist ein Satz von Windows Filtering Platform (WFP)-kernelmodusschichten, die für die Zustands behaftete Filterung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd42e-104">ALE is a set of Windows Filtering Platform (WFP) kernel-mode layers that are used for stateful filtering.</span></span>

<span data-ttu-id="fd42e-105">Durch die Zustands behaftete Filterung wird der Status von Netzwerkverbindungen nachverfolgt, und nur Pakete, die einem bekannten Verbindungsstatus entsprechen, werden zugelassen.</span><span class="sxs-lookup"><span data-stu-id="fd42e-105">Stateful filtering keeps track of the state of network connections and allows only packets that match a known connection state.</span></span> <span data-ttu-id="fd42e-106">Beispielsweise kann eine Zustands behaftete Filterung für eine TCP-Verbindung, die von hinter einer Firewall initiiert wurde, nur eingehende Pakete zulassen, die mit vorherigen ausgehenden Paketen, die von der Partei geschützt</span><span class="sxs-lookup"><span data-stu-id="fd42e-106">For example, stateful filtering for a TCP connection initiated from behind a firewall can allow only incoming packets that match previous outgoing packets sent by the party protected.</span></span>

<span data-ttu-id="fd42e-107">Filter in den ALE-Ebenen autorisieren die Erstellung von eingehenden und ausgehenden Verbindungen, Port Zuweisungen, Socketvorgänge wie " [**lauschen ()**](/windows/desktop/api/winsock2/nf-winsock2-listen)", die Erstellung von Rohdaten Socket und den Empfangsmodus.</span><span class="sxs-lookup"><span data-stu-id="fd42e-107">Filters in the ALE layers authorize inbound and outbound connection creation, port assignments, socket operations such as [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen), raw socket creation, and promiscuous mode receiving.</span></span>

<span data-ttu-id="fd42e-108">Der Datenverkehr auf der ALE Ebene wird entweder pro Verbindung oder pro Socket klassifiziert.</span><span class="sxs-lookup"><span data-stu-id="fd42e-108">Traffic at the ALE layers is classified either per-connection or per-socket operation.</span></span> <span data-ttu-id="fd42e-109">Bei nicht-ALE Ebenen kann der Datenverkehr nur auf Paketbasis von Filtern klassifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="fd42e-109">At non-ALE layers, filters can only classify traffic on a per-packet basis.</span></span>

<span data-ttu-id="fd42e-110">ALE Ebenen sind die einzigen WFP-Schichten, bei denen Netzwerk Datenverkehr basierend auf der Anwendungs Identität – mithilfe eines normalisierten Datei namens – und basierend auf der Benutzeridentität – mithilfe einer Sicherheits Beschreibung gefiltert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd42e-110">ALE layers are the only WFP layers where network traffic can be filtered based on the application identity—using a normalized file name—and based on the user identity—using a security descriptor.</span></span> <span data-ttu-id="fd42e-111">(Siehe "f \_ " Datei \_ Namen \_ Informationen in der Dokumentation zum Windows-Treiberkit (WDK), um weitere Informationen zu normalisierten Dateinamen zu erhalten.)</span><span class="sxs-lookup"><span data-stu-id="fd42e-111">(See FLT\_FILE\_NAME\_INFORMATION in the Windows Driver Kit (WDK) documentation, for more information on normalized file names.)</span></span>

<span data-ttu-id="fd42e-112">Wenn IPSec zum Schutz der Verbindung verwendet wird, kann darüber hinaus auch die Filterung auf der Ebene der Remote Computer und die Identität des Remote Benutzers durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fd42e-112">In addition, when IPsec is used to secure the connection, filtering at ALE layers can also be performed on the remote machine identity and on the remote user identity.</span></span> <span data-ttu-id="fd42e-113">Der Remote Computer und die Benutzer Identitäten werden aus den Anmelde Informationen abgerufen, die beim Erstellen einer IPSec-Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd42e-113">The remote machine and user identities are obtained from the credentials used in the creation of an IPsec session.</span></span>

<span data-ttu-id="fd42e-114">Aus diesem Grund werden Richtlinien, die erzwingen, dass (z. b. "Administrator") und/oder welche Anwendung (z. b. "Internet Explorer") die oben erwähnten Netzwerk Vorgänge ausführen dürfen, auf der ALE Ebene erstellt.</span><span class="sxs-lookup"><span data-stu-id="fd42e-114">For this reason, policies that enforce who (for example, "administrator") and/or which application (for example, "Internet Explorer") are allowed to perform the network operations mentioned above are authored at the ALE layers.</span></span>

<span data-ttu-id="fd42e-115">ALE bietet die Erzwingung von Richtlinien wie z. b. "Windows Messenger allen Zugriff auf das Netzwerk gestatten, während alle anderen Anwendungen blockiert werden".</span><span class="sxs-lookup"><span data-stu-id="fd42e-115">ALE provides enforcement for policies such as "allow Windows Messenger all access to the network while blocking all other applications."</span></span> <span data-ttu-id="fd42e-116">Wenn z. b. die Anwendung "Messenger" über das Netzwerk eine Verbindung herstellt, fängt ALE das Ereignis ab, stellt fest, dass es von Messenger initiiert wurde, und fragt die WFP-Filter-Engine ab, um zu bestimmen, ob der Socket fortgesetzt werden darf.</span><span class="sxs-lookup"><span data-stu-id="fd42e-116">In such an example, when the application "Messenger" connects across the network, ALE traps the event, determines that it was initiated by Messenger and queries the WFP filter engine to determine whether the socket should be allowed to proceed.</span></span>

> [!Note]  
> <span data-ttu-id="fd42e-117">Aufgrund der Art von echten Dual-IP-Sockets treten möglicherweise keine Klassifizierungen auf der IPv4-ALE-Ebene auf.</span><span class="sxs-lookup"><span data-stu-id="fd42e-117">Due to the nature of true dual-IP sockets, classifications at the IPv4 ALE layer may not occur.</span></span> <span data-ttu-id="fd42e-118">Dies ist Entwurfs bedingt, da der Socket für alle Intents und Zwecke ein IPv6-Socket ist.</span><span class="sxs-lookup"><span data-stu-id="fd42e-118">This is by design, because for all intents and purposes, the socket is an IPv6 socket.</span></span> <span data-ttu-id="fd42e-119">Um den V4-Datenverkehr für einen solchen Socket anzuzeigen, erstellen Sie mithilfe der IPv6-zugeordneten Adresse Filter auf der v6-Schicht.</span><span class="sxs-lookup"><span data-stu-id="fd42e-119">To see the V4 traffic for such a socket, create filters at the V6 layer using the IPv6-mapped address.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fd42e-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd42e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd42e-121">ALE Ebenen</span><span class="sxs-lookup"><span data-stu-id="fd42e-121">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="fd42e-122">Status behaftete ALE Filterung</span><span class="sxs-lookup"><span data-stu-id="fd42e-122">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="fd42e-123">ALE Multicast-/Broadcast Datenverkehr</span><span class="sxs-lookup"><span data-stu-id="fd42e-123">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="fd42e-124">Erneute ALE-Autorisierung</span><span class="sxs-lookup"><span data-stu-id="fd42e-124">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="fd42e-125">Anpassung des ALE-Flows</span><span class="sxs-lookup"><span data-stu-id="fd42e-125">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 