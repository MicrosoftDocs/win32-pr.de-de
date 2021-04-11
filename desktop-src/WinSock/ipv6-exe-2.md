---
description: Alle IPv6-Konfigurationen werden mit dem Ipv6.exe-Tool ausgeführt.
ms.assetid: cb701070-cb7f-472a-97c7-1de9c0ddec0f
title: Ipv6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e6fb0266609d22116cc72151e0db26006c415a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214590"
---
# <a name="ipv6exe"></a><span data-ttu-id="b8b28-103">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="b8b28-103">Ipv6.exe</span></span>

<span data-ttu-id="b8b28-104">Alle IPv6-Konfigurationen werden mit dem Ipv6.exe-Tool ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8b28-104">All IPv6 configuration is done with the Ipv6.exe tool.</span></span> <span data-ttu-id="b8b28-105">Dieses Tool wird hauptsächlich zum Abfragen und Konfigurieren von IPv6-Schnittstellen, Adressen, Caches und Routen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8b28-105">This tool is primarily used for the querying and configuring of IPv6 interfaces, addresses, caches, and routes.</span></span> <span data-ttu-id="b8b28-106">Im folgenden finden Sie IPv6-Unterbefehle:</span><span class="sxs-lookup"><span data-stu-id="b8b28-106">The following are IPv6 subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="b8b28-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**IPv6 if** \[ sei\#\]</span><span class="sxs-lookup"><span data-stu-id="b8b28-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**ipv6 if** \[if\#\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b28-108">Zeigt Informationen über Schnittstellen an.</span><span class="sxs-lookup"><span data-stu-id="b8b28-108">Displays information about interfaces.</span></span> <span data-ttu-id="b8b28-109">Wenn eine Schnittstellen Nummer angegeben ist, werden nur Informationen zu dieser Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8b28-109">If an interface number is specified, only information about that interface is displayed.</span></span> <span data-ttu-id="b8b28-110">Andernfalls werden Informationen zu allen Schnittstellen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8b28-110">Otherwise, information about all interfaces is displayed.</span></span> <span data-ttu-id="b8b28-111">Die Ausgabe enthält die Verknüpfungs Schicht Adresse der Schnittstelle und die Liste der IPv6-Adressen, die der Schnittstelle zugewiesen sind, einschließlich der aktuellen MTU der Schnittstelle und der maximalen (echten) MTU, die von der Schnittstelle unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b8b28-111">The output includes the interface's link-layer address and the list of IPv6 addresses assigned to the interface, including the interface's current MTU and the maximum (true) MTU that the interface can support.</span></span>

<span data-ttu-id="b8b28-112">Schnittstelle \# 1 ist eine für Loopback verwendete Pseudo Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b8b28-112">Interface \#1 is a pseudo-interface used for loopback.</span></span> <span data-ttu-id="b8b28-113">Schnittstelle \# 2 ist eine Pseudo Schnittstelle für konfigurierte Tunnelung, automatische Tunnelung und IPv6-zu-IPv4-Tunnelung.</span><span class="sxs-lookup"><span data-stu-id="b8b28-113">Interface \#2 is a pseudo-interface used for configured tunneling, automatic tunneling, and 6to4 tunneling.</span></span> <span data-ttu-id="b8b28-114">Andere Schnittstellen werden sequenziell in der Reihenfolge nummeriert, in der Sie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b8b28-114">Other interfaces are numbered sequentially in the order in which they are created.</span></span> <span data-ttu-id="b8b28-115">Diese Bestellung variiert von einem Computer zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="b8b28-115">This order varies from one computer to another.</span></span>

<span data-ttu-id="b8b28-116">Adressen der Verknüpfungs Schicht im *AA* - *BB* - *CC* - *DD* - *EE* - *FF* -Format sind Ethernet-Adressen.</span><span class="sxs-lookup"><span data-stu-id="b8b28-116">Link-layer addresses in *aa*-*bb*-*cc*-*dd*-*ee*-*ff* format are Ethernet addresses.</span></span> <span data-ttu-id="b8b28-117">Die Adresse der Verknüpfungs Schicht in *einer*. *b*. *c*. Das *d* -Formular ist 6-over-4-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="b8b28-117">Link-layer address in *a*.*b*.*c*.*d* form are 6-over-4 interfaces.</span></span> <span data-ttu-id="b8b28-118">Weitere Informationen zu 6-over-4 finden Sie unter RFC 2529.</span><span class="sxs-lookup"><span data-stu-id="b8b28-118">For more information on 6-over-4, see RFC 2529.</span></span>

<span data-ttu-id="b8b28-119">Die beiden Pseudo Schnittstellen verwenden keine IPv6-Nachbar Ermittlung.</span><span class="sxs-lookup"><span data-stu-id="b8b28-119">The two pseudo-interfaces do not use IPv6 Neighbor Discovery.</span></span>

</dd> <dt>

<span data-ttu-id="b8b28-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**IPv6** -"IFC", wenn "Weiterleiten" angekündigt-weiterleitet: gibt den \# \[ \] \[ \] \[ \] \[ \] \[ \# \] \[ Standort Bezeichner der MTU-\]</span><span class="sxs-lookup"><span data-stu-id="b8b28-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**ipv6 ifc** if\# \[forwards\] \[advertises\] \[-forwards\] \[-advertises\] \[mtu \#bytes\] \[site site-identifier\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b28-121">Steuert Schnittstellen Attribute.</span><span class="sxs-lookup"><span data-stu-id="b8b28-121">Controls interface attributes.</span></span> <span data-ttu-id="b8b28-122">Schnittstellen können weitergeleitet werden. in diesem Fall leiten Sie Pakete mit Zieladressen weiter, die nicht der Schnittstelle zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b8b28-122">Interfaces can be forwarding, in which case they forward packets with destination addresses not assigned to the interface.</span></span> <span data-ttu-id="b8b28-123">Schnittstellen können Werbung sein. in diesem Fall senden Sie Routerankündigungen.</span><span class="sxs-lookup"><span data-stu-id="b8b28-123">Interfaces can be advertising, in which case they send router advertisements.</span></span> <span data-ttu-id="b8b28-124">Diese Attribute können unabhängig voneinander gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="b8b28-124">These attributes can be independently controlled.</span></span> <span data-ttu-id="b8b28-125">Eine Schnittstelle sendet entweder routerzuweisungen und empfängt Routerankündigungen, oder Sie empfängt routerzuweisungen und sendet Routerankündigungen.</span><span class="sxs-lookup"><span data-stu-id="b8b28-125">An interface either sends router solicitations and receives router advertisements, or receives router solicitations and sends router advertisements.</span></span>

<span data-ttu-id="b8b28-126">Da die beiden Pseudo Schnittstellen keine Nachbar Ermittlung verwenden, können Sie nicht für das Senden von Routerankündigungen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="b8b28-126">Because the two pseudo-interfaces do not use Neighbor Discovery, they cannot be configured to send router advertisements.</span></span>

<span data-ttu-id="b8b28-127">Weiterleitungen können als FORW abgekürzt und als ADV angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="b8b28-127">Forwards can be abbreviated as forw, and advertised as adv.</span></span>

<span data-ttu-id="b8b28-128">Die MTU für die Schnittstelle kann auch festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b8b28-128">The MTU for the interface can also be set.</span></span> <span data-ttu-id="b8b28-129">Die neue MTU muss kleiner oder gleich der maximalen (von IPv6 gemeldeten) MTU (wie von IPv6) und größer oder gleich der minimalen IPv6-MTU (1280 Bytes) sein.</span><span class="sxs-lookup"><span data-stu-id="b8b28-129">The new MTU must be less than or equal to the link's maximum (true) MTU (as reported by ipv6 if) and greater than or equal to the minimum IPv6 MTU (1280 bytes).</span></span>

<span data-ttu-id="b8b28-130">Der Standort Bezeichner für eine Schnittstelle kann ebenfalls geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b8b28-130">The site-identifier for an interface can also be changed.</span></span> <span data-ttu-id="b8b28-131">Website \_ Bezeichner werden im Feld sin6 Scope \_ ID mit Site-Local-Adressen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8b28-131">Site identifiers are used in the sin6\_scope\_id field with site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="b8b28-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**IPv6-IFD** , wenn\#</span><span class="sxs-lookup"><span data-stu-id="b8b28-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**ipv6 ifd** if\#</span></span>
</dt> <dd>

<span data-ttu-id="b8b28-133">Löscht eine Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b8b28-133">Deletes an interface.</span></span> <span data-ttu-id="b8b28-134">Die Loopback-und Tunnel Pseudo Schnittstellen können nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b8b28-134">The loopback and tunnel pseudo-interfaces cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="b8b28-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**IPv6-NC** \[ If- \# \[ Adresse\]\]</span><span class="sxs-lookup"><span data-stu-id="b8b28-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**ipv6 nc** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b28-136">Zeigt den Inhalt des Nachbar Caches an.</span><span class="sxs-lookup"><span data-stu-id="b8b28-136">Displays the contents of the neighbor cache.</span></span> <span data-ttu-id="b8b28-137">Wenn eine Schnittstellen Nummer angegeben ist, wird nur der Inhalt des Nachbar Caches dieser Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8b28-137">If an interface number is specified, only the contents of that interface's neighbor cache are displayed.</span></span> <span data-ttu-id="b8b28-138">Andernfalls werden die Inhalte der Nachbar Caches aller Schnittstellen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8b28-138">Otherwise, the contents of all the interface's neighbor caches are displayed.</span></span> <span data-ttu-id="b8b28-139">Wenn eine Schnittstelle angegeben ist, kann eine IPv6-Adresse angegeben werden, um nur diesen Nachbar Cache Eintrag anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b8b28-139">If an interface is specified, an IPv6 address can be specified to display only that neighbor cache entry.</span></span>

<span data-ttu-id="b8b28-140">Für jeden Nachbar Cache Eintrag werden die Schnittstelle, die IPv6-Adresse, die Adresse der Verbindungsschicht und der Status REACH angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8b28-140">For each neighbor cache entry, the interface, IPv6 address, link-layer address, and reach state are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="b8b28-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**IPv6-NCF** \[ If- \# \[ Adresse\]\]</span><span class="sxs-lookup"><span data-stu-id="b8b28-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**ipv6 ncf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b28-142">Leert die angegebenen Nachbar Cache Einträge.</span><span class="sxs-lookup"><span data-stu-id="b8b28-142">Flushes the specified neighbor cache entries.</span></span> <span data-ttu-id="b8b28-143">Nur benachbarte Cache Einträge ohne Verweise werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b8b28-143">Only neighbor cache entries without references are purged.</span></span> <span data-ttu-id="b8b28-144">Da Routen Cache Einträge Verweise auf Nachbar Cache Einträge enthalten, sollte der Routen Cache zuerst geleert werden.</span><span class="sxs-lookup"><span data-stu-id="b8b28-144">Because route cache entries hold references to neighbor cache entries, the route cache should be flushed first.</span></span> <span data-ttu-id="b8b28-145">Routing Tabelleneinträge können auch Verweise auf Nachbar Cache Einträge enthalten.</span><span class="sxs-lookup"><span data-stu-id="b8b28-145">Routing table entries can also hold references to neighbor cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="b8b28-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**IPv6 RC** \[ If- \# Adresse\]</span><span class="sxs-lookup"><span data-stu-id="b8b28-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**ipv6 rc** \[if\# address\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b28-147">Zeigt den Inhalt des Routen Caches an.</span><span class="sxs-lookup"><span data-stu-id="b8b28-147">Displays the contents of the route cache.</span></span> <span data-ttu-id="b8b28-148">Der Routen Cache ist der Name der Microsoft IPv6-Implementierung für den Zielcache.</span><span class="sxs-lookup"><span data-stu-id="b8b28-148">The route cache is the Microsoft IPv6 implementation name for the destination cache.</span></span> <span data-ttu-id="b8b28-149">Wenn eine Schnittstelle und eine Adresse angegeben werden, wird der Routen Cache Eintrag zum Erreichen der Adresse über die Schnittstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8b28-149">If an interface and address are specified, the route cache entry for reaching the address through the interface is displayed.</span></span> <span data-ttu-id="b8b28-150">Andernfalls werden alle Routen Cache Einträge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8b28-150">Otherwise, all route cache entries are displayed.</span></span>

<span data-ttu-id="b8b28-151">Für jeden Routen Cache Eintrag werden die IPv6-Adresse und die aktuelle Schnittstelle für den nächsten Hop und die Nachbaradresse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8b28-151">For each route cache entry, the IPv6 address and the current next-hop interface and neighbor address are displayed.</span></span> <span data-ttu-id="b8b28-152">Die bevorzugte Quelladresse für die Verwendung mit diesem Ziel, der aktuelle Pfad der MTU zum Erreichen dieses Ziels über die-Schnittstelle und die Bestimmung, ob dies ein Schnittstellen spezifischer –-Routen Cache Eintrag ist.</span><span class="sxs-lookup"><span data-stu-id="b8b28-152">The preferred source address for use with this destination, the current path MTU for reaching this destination through the interface, and the determination of whether this is an interface specific–route cache entry are also displayed.</span></span> <span data-ttu-id="b8b28-153">Eine beliebige Adresse (für Mobilität) für die Zieladresse wird ebenfalls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8b28-153">Any care-of address (for mobility) for the destination address is displayed as well.</span></span>

<span data-ttu-id="b8b28-154">Eine Zieladresse kann mehrere Routen Cache Einträge aufweisen – so viele wie eine für jede ausgehende Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b8b28-154">A destination address can have multiple route cache entries—as many as one for each outgoing interface.</span></span> <span data-ttu-id="b8b28-155">Eine Zieladresse kann jedoch maximal einen Routen Cache Eintrag aufweisen, der nicht Schnittstellen spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="b8b28-155">However, a destination address can have a maximum of one route cache entry that is not interface-specific.</span></span> <span data-ttu-id="b8b28-156">Ein Schnittstellen spezifischer –-Routen Cache Eintrag wird nur verwendet, wenn die Anwendung explizit diese ausgehende Schnittstelle angibt.</span><span class="sxs-lookup"><span data-stu-id="b8b28-156">An interface specific–route cache entry is only used if the application explicitly specifies that outgoing interface.</span></span>

</dd> <dt>

<span data-ttu-id="b8b28-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**IPv6-RCF** \[ If- \# \[ Adresse\]\]</span><span class="sxs-lookup"><span data-stu-id="b8b28-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**ipv6 rcf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b28-158">Leert die angegebenen Routen Cache Einträge.</span><span class="sxs-lookup"><span data-stu-id="b8b28-158">Flushes the specified route cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="b8b28-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**IPv6-BC**</span><span class="sxs-lookup"><span data-stu-id="b8b28-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**ipv6 bc**</span></span>
</dt> <dd>

<span data-ttu-id="b8b28-160">Zeigt den Inhalt des Bindungs Caches an, der Bindungen zwischen Privatadressen und Pflege Adressen für mobile IPv6 enthält.</span><span class="sxs-lookup"><span data-stu-id="b8b28-160">Displays the contents of the binding cache, which holds bindings between home addresses and care-of addresses for mobile IPv6.</span></span>

<span data-ttu-id="b8b28-161">Für jede Bindung werden die Privatadresse, die Adresse, die Bindungs Sequenznummer und die Lebensdauer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8b28-161">For each binding, the home address, care-of address, binding sequence number, and lifetime are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="b8b28-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**IPv6 Adu** if \# /Address \[ Lifetime VL \[ "/pl" \] \] \[ Anycast \] \[ Unicast\]</span><span class="sxs-lookup"><span data-stu-id="b8b28-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**ipv6 adu** if\#/address \[lifetime VL\[/PL\]\] \[anycast\] \[unicast\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b28-163">Fügt eine Unicast-oder Anycast-Adresszuweisung zu einer Schnittstelle hinzu oder entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="b8b28-163">Adds or removes a unicast or anycast address assignment on an interface.</span></span> <span data-ttu-id="b8b28-164">Die Unicastadresse wird befolgt, es sei denn, es wurde Anycast angegeben.</span><span class="sxs-lookup"><span data-stu-id="b8b28-164">The unicast address is acted upon unless anycast is specified.</span></span>

<span data-ttu-id="b8b28-165">Die Lebensdauer ist unendlich, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="b8b28-165">Lifetime is infinite if unspecified.</span></span> <span data-ttu-id="b8b28-166">Wenn nur eine gültige Gültigkeitsdauer angegeben wird, ist die bevorzugte Lebensdauer gleich der gültigen Gültigkeitsdauer.</span><span class="sxs-lookup"><span data-stu-id="b8b28-166">If only a valid lifetime is specified, the preferred lifetime is equal to the valid lifetime.</span></span> <span data-ttu-id="b8b28-167">Es kann eine unendliche Lebensdauer oder ein endlicher Wert in Sekunden angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b8b28-167">An infinite lifetime may be specified, or a finite value in seconds.</span></span> <span data-ttu-id="b8b28-168">Die bevorzugte Lebensdauer muss kleiner oder gleich der gültigen Gültigkeitsdauer sein.</span><span class="sxs-lookup"><span data-stu-id="b8b28-168">The preferred lifetime must be less than or equal to the valid lifetime.</span></span> <span data-ttu-id="b8b28-169">Die Angabe einer Lebensdauer von NULL bewirkt, dass die Adresse entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b8b28-169">Specifying a lifetime of zero causes the address to be removed.</span></span>

<span data-ttu-id="b8b28-170">Sie können die Lebensdauer als Lebensdauer abkürzen.</span><span class="sxs-lookup"><span data-stu-id="b8b28-170">You can abbreviate lifetime as life.</span></span>

<span data-ttu-id="b8b28-171">Bei Anycast-Adressen sind die einzigen gültigen Gültigkeitsdauer Werte 0 (null) und unendlich.</span><span class="sxs-lookup"><span data-stu-id="b8b28-171">For anycast addresses, the only valid lifetime values are zero and infinite.</span></span>

</dd> <dt>

<span data-ttu-id="b8b28-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**IPv6-SPT**</span><span class="sxs-lookup"><span data-stu-id="b8b28-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**ipv6 spt**</span></span>
</dt> <dd>

<span data-ttu-id="b8b28-173">Zeigt den aktuellen Inhalt der Site-Präfix Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="b8b28-173">Displays the current contents of the site prefix table.</span></span>

<span data-ttu-id="b8b28-174">Für jedes Site Präfix zeigt der Befehl das Präfix, die Schnittstelle, für die das Site Präfix gilt, und die Präfix Lebensdauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="b8b28-174">For each site prefix, the command displays the prefix, the interface to which the site prefix applies, and the prefix lifetime in seconds.</span></span>

<span data-ttu-id="b8b28-175">Standort Präfixe werden normalerweise automatisch von Routerankündigungen aus konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b8b28-175">Site prefixes are normally auto-configured from router advertisements.</span></span> <span data-ttu-id="b8b28-176">Sie werden in der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion verwendet, um ungeeignete Site lokale Adressen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="b8b28-176">They are used in the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function to filter inappropriate site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="b8b28-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>**IPv6-SPU** -Präfix bei \# \[ Lebensdauer L\]</span><span class="sxs-lookup"><span data-stu-id="b8b28-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>**ipv6 spu** prefix if\# \[lifetime L\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b28-178">Fügt ein Präfix in der Präfix Tabelle der Site hinzu, entfernt oder aktualisiert dieses.</span><span class="sxs-lookup"><span data-stu-id="b8b28-178">Adds, removes, or updates a prefix in the site prefix table.</span></span>

<span data-ttu-id="b8b28-179">Die Präfix-und Schnittstellen Nummer ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8b28-179">The prefix and interface number are required.</span></span> <span data-ttu-id="b8b28-180">Die Lebensdauer des Standortpräfixes, angegeben in Sekunden, ist standardmäßig unbegrenzt, wenn nichts angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b8b28-180">The site prefix lifetime, specified in seconds, defaults to infinite if not specified.</span></span> <span data-ttu-id="b8b28-181">Durch die Angabe einer Lebensdauer von NULL wird das Site Präfix gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b8b28-181">Specifying a lifetime of zero deletes the site prefix.</span></span>

<span data-ttu-id="b8b28-182">Dieser Befehl ist für die normale Konfiguration von Hosts oder Routern nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8b28-182">This command is unnecessary for the normal configuration of hosts or routers.</span></span>

</dd> <dt>

<span data-ttu-id="b8b28-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**IPv6-RT**</span><span class="sxs-lookup"><span data-stu-id="b8b28-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**ipv6 rt**</span></span>
</dt> <dd>

<span data-ttu-id="b8b28-184">Zeigt den aktuellen Inhalt der Routing Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="b8b28-184">Displays the current contents of the routing table.</span></span>

<span data-ttu-id="b8b28-185">Für jeden Routing Tabelleneintrag zeigt der Befehl das Routen Präfix, eine auf-Link-Schnittstelle oder einen Nachbar für den nächsten Hop auf einer Schnittstelle an, ein bevorzugter Wert (kleiner wird bevorzugt) und eine Lebensdauer in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="b8b28-185">For each routing table entry, the command displays the route prefix, an on-link interface or a next-hop neighbor on an interface, a preference value (smaller is preferred), and a lifetime in seconds.</span></span>

<span data-ttu-id="b8b28-186">Routing Tabelleneinträge können auch über **Veröffentlichungs** -und **Alterungs** Attribute verfügen.</span><span class="sxs-lookup"><span data-stu-id="b8b28-186">Routing table entries may also have **publish** and **aging** attributes.</span></span> <span data-ttu-id="b8b28-187">Standardmäßig werden Sie verwendet (die Lebensdauer wird nicht als verbleibende Konstante angezeigt), und Sie werden nicht veröffentlicht (beim Konstruieren von Routerankündigungen nicht verwendet).</span><span class="sxs-lookup"><span data-stu-id="b8b28-187">By default, they age (the lifetime counts down, rather than remaining constant) and are not published (not used in constructing router advertisements).</span></span>

<span data-ttu-id="b8b28-188">Auf Hosts werden Routing Tabelleneinträge normalerweise automatisch von Routerankündigungen aus konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="b8b28-188">On hosts, routing table entries are normally auto-configured from router advertisements.</span></span>

</dd> <dt>

<span data-ttu-id="b8b28-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>**IPv6-RTU** -Präfix, wenn \# \[ /nexthop \] \[ Lebensdauer L \] \[ \] \[ \] \[ -Einstellung P \] \[ SPL Site-Prefix-length\]</span><span class="sxs-lookup"><span data-stu-id="b8b28-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>**ipv6 rtu** prefix if\#\[/nexthop\] \[lifetime L\] \[preference P\] \[publish\] \[age\] \[spl site-prefix-length\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b28-190">Fügt eine Route in der Routing Tabelle hinzu oder entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="b8b28-190">Adds or removes a route in the routing table.</span></span> <span data-ttu-id="b8b28-191">Das Routen Präfix ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8b28-191">The route prefix is required.</span></span> <span data-ttu-id="b8b28-192">Das Präfix kann auf eine angegebene Schnittstelle oder auf den nächsten Hop mit einer Nachbaradresse auf einer Schnittstelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b8b28-192">The prefix can be on-link to a specified interface, or next-hop, specified with a neighbor address on an interface.</span></span> <span data-ttu-id="b8b28-193">Die Route kann eine Lebensdauer in Sekunden aufweisen, mit der Standardeinstellung unendlich und eine Voreinstellung mit dem Standardwert 0 (null) oder am bevorzugten.</span><span class="sxs-lookup"><span data-stu-id="b8b28-193">The route can have a lifetime in seconds, with the default infinite, and a preference, with the default of zero, or most preferred.</span></span> <span data-ttu-id="b8b28-194">Wenn Sie die Lebensdauer 0 angeben, wird die Route gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b8b28-194">Specifying a lifetime of zero deletes the route.</span></span>

<span data-ttu-id="b8b28-195">Wenn die Route als veröffentlicht angegeben wird, gibt Sie an, dass Sie beim Erstellen von Routerankündigungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8b28-195">If the route is specified as published, indicating it will be used in constructing router advertisements, it does not age.</span></span> <span data-ttu-id="b8b28-196">Die Lebensdauer der Route wird nicht nach unten gezählt und ist daher praktisch unendlich, aber der Wert wird in Routerankündigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8b28-196">The route's lifetime does not count down and therefore is effectively infinite, but the value is used in router advertisements.</span></span> <span data-ttu-id="b8b28-197">Optional kann eine Route auch als veröffentlichte Route angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b8b28-197">Optionally, a route can be specified as a published route that also ages.</span></span> <span data-ttu-id="b8b28-198">Eine nicht veröffentlichte Route ist standardmäßig immer Ages.</span><span class="sxs-lookup"><span data-stu-id="b8b28-198">A nonpublished route by default always ages.</span></span>

<span data-ttu-id="b8b28-199">Die optionale SPL-unter Option kann verwendet werden, um eine Site Präfix Länge anzugeben, die der Route zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b8b28-199">The optional spl suboption can be used to specify a site prefix length associated with the route.</span></span> <span data-ttu-id="b8b28-200">Die Site Präfix Länge wird nur beim Senden von Routerankündigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8b28-200">The site prefix length is used only when sending router advertisements.</span></span>

<span data-ttu-id="b8b28-201">Die Lebensdauer kann als "Life", als "Pref" und als "pub" veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="b8b28-201">Lifetime can be abbreviated as life, preference as pref, and publish as pub.</span></span>

</dd> </dl>

 

 



