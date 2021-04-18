---
description: IPv6-Verbindungs-und Standort lokale Adressen werden als Bereichs bezogene Adressen bezeichnet.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: IPv6-Verbindungs lokale und Standort lokale Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80b8e201adf382b10dd31fe5607de903d6c588
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343295"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a><span data-ttu-id="a53e5-103">IPv6-Verbindungs lokale und Standort lokale Adressen</span><span class="sxs-lookup"><span data-stu-id="a53e5-103">IPv6 Link-local and Site-local Addresses</span></span>

<span data-ttu-id="a53e5-104">IPv6-Verbindungs-und Standort lokale Adressen werden als Bereichs bezogene Adressen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a53e5-104">IPv6 link-local and site-local addresses are called scoped addresses.</span></span> <span data-ttu-id="a53e5-105">Die Windows Sockets (Winsock)-API unterstützt das **sin6 \_ Scope \_ ID** -Element in der [**sockaddr \_ IN6**](sockaddr-2.md) -Struktur zur Verwendung mit Bereichs bezogenen Adressen.</span><span class="sxs-lookup"><span data-stu-id="a53e5-105">The Windows Sockets (Winsock) API supports the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure for use with scoped addresses.</span></span> <span data-ttu-id="a53e5-106">Bei IPv6-Verbindungs lokalen Adressen (FE80::/10-Präfix) ist das **sin6 \_ Scope- \_ ID** -Element in der **sockaddr \_ IN6** -Struktur die Schnittstellen Nummer.</span><span class="sxs-lookup"><span data-stu-id="a53e5-106">For IPv6 link-local addresses (fe80::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is the interface number.</span></span> <span data-ttu-id="a53e5-107">Für IPv6-Site-Local-Adressen (FEC0::/10-Präfix) ist das **sin6 \_ Scope- \_ ID** -Element in der **sockaddr \_ IN6** -Struktur ein Site Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a53e5-107">For IPv6 site-local addresses (fec0::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is a site identifier.</span></span>

<span data-ttu-id="a53e5-108">Ein Beispiel für eine Link-Local-IPv6-Adresse für Schnittstelle \# 5 ist Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a53e5-108">An example of a link-local IPv6 address on interface \#5 is the following:</span></span>

``` syntax
fe80::208:74ff:feda:625c%5
```

<span data-ttu-id="a53e5-109">Der folgende Befehl ist unter Windows XP mit Service Pack 1 (SP1) und höher zum Abfragen und Konfigurieren von IPv6 auf einem lokalen Computer verfügbar:</span><span class="sxs-lookup"><span data-stu-id="a53e5-109">The following command is available on Windows XP with Service Pack 1 (SP1) and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="a53e5-110">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="a53e5-110">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="a53e5-111">Konfigurationsänderungen, die mithilfe der Netsh.exe Befehle vorgenommen werden, sind permanent und gehen nicht verloren, wenn der Computer oder das IPv6-Protokoll neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a53e5-111">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="a53e5-112">Vor Windows XP mit Service Pack 1 (SP1) verwendeten die IPv6-Konfiguration und-Verwaltung mehrere ältere Befehlszeilen Tools (Net.exe, Ipv6.exe und Ipsec6.exe) zum Konfigurieren und Verwalten von IPv6.</span><span class="sxs-lookup"><span data-stu-id="a53e5-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools (Net.exe, Ipv6.exe, and Ipsec6.exe) to configure and manage IPv6.</span></span> <span data-ttu-id="a53e5-113">Wenn Sie diese älteren Tools verwenden, sind die IPv6-Änderungen nicht permanent und gehen verloren, wenn der Computer oder das IPv6-Protokoll neu gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="a53e5-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span> <span data-ttu-id="a53e5-114">Diese älteren Befehlszeilen Tools werden nur unter Windows XP unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a53e5-114">These older command-line tools are only supported on Windows XP.</span></span>

<span data-ttu-id="a53e5-115">Unter Windows XP mit SP1 wird mit dem folgenden Befehl die Liste der IPv6-Schnittstellen auf einem lokalen Computer angezeigt, einschließlich des Schnittstellen Indexes, des Schnittstellen namens und verschiedener anderer Schnittstelleneigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a53e5-115">On Windows XP with SP1, the following command will display the list of IPv6 interfaces on a local computer including the interface index, the interface name, and various other interface properties.</span></span>

<span data-ttu-id="a53e5-116">**Netsh Interface IPv6 Show Interface**</span><span class="sxs-lookup"><span data-stu-id="a53e5-116">**netsh interface ipv6 show interface**</span></span>

<span data-ttu-id="a53e5-117">Unter Windows XP mit SP1 ändert der folgende Befehl den einem Schnittstellen Index zugeordneten Site Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a53e5-117">On Windows XP with SP1, the following command will change the site identifier associated with an interface index.</span></span>

<span data-ttu-id="a53e5-118">**Netsh Interface IPv6 Set Interface <InterfaceIndex or Name> siteid = Value**</span><span class="sxs-lookup"><span data-stu-id="a53e5-118">**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid=value**</span></span>

<span data-ttu-id="a53e5-119">Unter Windows XP ändert der folgende ältere Befehl auch den Standort Bezeichner, der einer Standort lokalen Adresse zugeordnet ist, auf 3.</span><span class="sxs-lookup"><span data-stu-id="a53e5-119">On Windows XP, the following older command will also change the site identifier associated with a site-local address to 3.</span></span>

<span data-ttu-id="a53e5-120">**IPv6-RTU-FEC0::/10 3**</span><span class="sxs-lookup"><span data-stu-id="a53e5-120">**ipv6 rtu fec0::/10 3**</span></span>

<span data-ttu-id="a53e5-121">Wenn Sie eine Bereichs bezogene Adresse senden oder verbinden, kann das **sin6 Scope- \_ \_ ID** -Element in der [**sockaddr \_ IN6**](sockaddr-2.md) -Struktur nicht angegeben (null) bleiben, was eine mehrdeutige Bereichs bezogene Adresse darstellt.</span><span class="sxs-lookup"><span data-stu-id="a53e5-121">If you are sending or connecting to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure can be left unspecified (zero) which represents an ambiguous scoped address.</span></span> <span data-ttu-id="a53e5-122">Die folgende Link-Local-Adresse ist z. b. mehrdeutig:</span><span class="sxs-lookup"><span data-stu-id="a53e5-122">For example, the following link-local address is ambiguous:</span></span>

``` syntax
fe80::10
```

<span data-ttu-id="a53e5-123">Wenn Sie eine Bindung an eine Bereichs bezogene Adresse durchlaufen, muss das **sin6 \_ Scope \_ ID** -Element in der [**sockaddr \_ IN6**](sockaddr-2.md) -Struktur einen Wert ungleich 0 (null) enthalten, der eine gültige Schnittstellen Nummer für eine Link-Local-Adresse oder einen Site Bezeichner für eine Site-Local-Adresse angibt.</span><span class="sxs-lookup"><span data-stu-id="a53e5-123">If you are binding to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure must contain a nonzero value that specifies a valid interface number for a link-local address or a site identifier for a site-local address.</span></span>

## <a name="ambiguous-scoped-addresses"></a><span data-ttu-id="a53e5-124">Mehrdeutige Bereichs bezogene Adressen</span><span class="sxs-lookup"><span data-stu-id="a53e5-124">Ambiguous Scoped Addresses</span></span>

<span data-ttu-id="a53e5-125">Wenn Sie eine Bereichs bezogene Adresse senden oder verbinden und das **sin6 \_ Scope- \_ ID** -Element nicht in der [**sockaddr \_ IN6**](sockaddr-2.md) -Struktur angegeben haben, ist die Bereichs bezogene Adresse mehrdeutig.</span><span class="sxs-lookup"><span data-stu-id="a53e5-125">If you are sending or connecting to a scoped address and have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, then the scoped address is ambiguous.</span></span> <span data-ttu-id="a53e5-126">Um dieses Problem zu beheben, bestimmt das IPv6-Protokoll zuerst, ob Sie den Socket an eine Quelladresse gebunden haben.</span><span class="sxs-lookup"><span data-stu-id="a53e5-126">To resolve this, the IPv6 protocol first determines whether you have bound the socket to a source address.</span></span> <span data-ttu-id="a53e5-127">Wenn dies der Fall ist, löst die gebundene Quelladresse die Mehrdeutigkeit durch Bereitstellen einer Schnittstellen Nummer oder eines Website Bezeichners auf.</span><span class="sxs-lookup"><span data-stu-id="a53e5-127">If so, the bound source address resolves the ambiguity by supplying an interface number or site identifier.</span></span>

<span data-ttu-id="a53e5-128">Wenn Sie eine Bereichs bezogene Adresse senden oder verbinden und weder das **sin6 \_ Scope \_ ID** -Element noch eine Quelladresse angegeben haben, prüft das IPv6-Protokoll die Routing Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a53e5-128">If you are sending or connecting to a scoped address and have neither specified the **sin6\_scope\_id** member nor bound a source address, then the IPv6 protocol checks the routing table.</span></span> <span data-ttu-id="a53e5-129">Mit dem folgenden Befehl wird beispielsweise die IPv6-Routing Tabelle auf einem lokalen Computer angezeigt:</span><span class="sxs-lookup"><span data-stu-id="a53e5-129">For example, the following command will display the IPv6 routing table on a local computer:</span></span>

<span data-ttu-id="a53e5-130">**„netsh interface ipv6 show route“**</span><span class="sxs-lookup"><span data-stu-id="a53e5-130">**netsh interface ipv6 show route**</span></span>

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

<span data-ttu-id="a53e5-131">Dies gibt an, dass Link-Local-Adressen standardmäßig als Links zu Schnittstelle \# 13 und 14 behandelt werden \# .</span><span class="sxs-lookup"><span data-stu-id="a53e5-131">This indicates that link-local addresses are treated as on-link to interface \#13 and \#14 by default.</span></span>

<span data-ttu-id="a53e5-132">Die Mehrdeutigkeit ergibt sich, wenn ein lokaler Computer über mehrere Netzwerkadapter verfügt.</span><span class="sxs-lookup"><span data-stu-id="a53e5-132">Ambiguity arises when a local computer has multiple network adapters.</span></span> <span data-ttu-id="a53e5-133">Der obige Befehl **netsh** zeigt beispielsweise an, dass zwei Netzwerkschnittstellen vorhanden sind (LAN-Verbindung und drahtlose Netzwerkverbindung).</span><span class="sxs-lookup"><span data-stu-id="a53e5-133">For example, the **netsh** command above indicates there are two network interfaces (Local Area Connection and Wireless Network Connection).</span></span> <span data-ttu-id="a53e5-134">Wenn eine Anwendung eine Ziel-Link-Local-Adresse (z. b. FE80:: 10) ohne Bereichs-ID angibt, ist nicht klar, welcher Adapter zum Senden des Pakets verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a53e5-134">When an application specifies a destination link-local address (fe80::10, for example) without a scope ID, it is not clear which adapter to use to send the packet.</span></span> <span data-ttu-id="a53e5-135">Nur ein Link-Local-Unicast (FE80::/64) oder eine Verknüpfungs Bereichs-Multicast-IPv6-Zieladresse (FF00::/8) kann beim Senden eines Pakets keine Bereichs-ID aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a53e5-135">Only a link-local unicast (fe80::/64) or a link-scope multicast (ff00::/8) IPv6 destination address can suffer from not having a scope ID when sending a packet.</span></span>

## <a name="neighbor-discovery"></a><span data-ttu-id="a53e5-136">Nachbarsuche</span><span class="sxs-lookup"><span data-stu-id="a53e5-136">Neighbor Discovery</span></span>

<span data-ttu-id="a53e5-137">Wenn Sie das **sin6 \_ Scope \_ ID** -Element nicht in der [**sockaddr \_ IN6**](sockaddr-2.md) -Struktur angegeben, keine Quelladresse gebunden haben und keine Route für Link-Local-Adressen angegeben haben, versucht das IPv6-Protokoll die Nachbar Ermittlung, um die Ziel Link-Local-Adresse aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="a53e5-137">If you have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, have not bound a source address, and have not specified a route for link-local addresses, then the IPv6 protocol will try Neighbor Discovery to resolve the destination link-local address.</span></span> <span data-ttu-id="a53e5-138">Für ein bestimmtes Paket, das gesendet wird, wird eine Schnittstelle ausprobiert.</span><span class="sxs-lookup"><span data-stu-id="a53e5-138">For a given packet being sent, one interface is tried.</span></span> <span data-ttu-id="a53e5-139">Diese erste versuchte Schnittstelle wird als bevorzugte Schnittstelle betrachtet.</span><span class="sxs-lookup"><span data-stu-id="a53e5-139">This first interface that is tried is considered the most preferred interface.</span></span> <span data-ttu-id="a53e5-140">Wenn die Nachbar Ermittlung die Link-Local-Adresse auf einer Schnittstelle nicht auflösen kann, wird das zu sendende Paket gelöscht, und das System speichert, dass die Adresse des Zielverbindungs-lokalen über diese Schnittstelle nicht erreichbar ist.</span><span class="sxs-lookup"><span data-stu-id="a53e5-140">If Neighbor Discovery fails to resolve the link-local address on an interface, the packet to be sent is dropped and the system remembers that the destination link-local address is not reachable over that interface.</span></span> <span data-ttu-id="a53e5-141">Beim nächsten Paket, das unter allen gleichen Bedingungen gesendet werden soll, wird eine andere Oberfläche für die Nachbar Ermittlung ausprobiert.</span><span class="sxs-lookup"><span data-stu-id="a53e5-141">On the next packet to be sent under all of the same conditions, a different interface is tried for Neighbor Discovery.</span></span> <span data-ttu-id="a53e5-142">Dieser Prozess wird durch die einzelnen Schnittstellen auf einem lokalen Computer für jedes neue Paket fortgesetzt, bis die Nachbar Ermittlung auf die Ziel Link-Local-Adresse antwortet oder alle möglichen Schnittstellen fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="a53e5-142">This process continues through each of the interfaces on a local computer for each new packet until Neighbor Discovery responds for the destination link-local address or all of the possible interfaces have been tried and failed.</span></span> <span data-ttu-id="a53e5-143">Jedes Mal, wenn der Versuch, den Nachbar aufzulösen, fehlschlägt, wird für diesen Nachbarn eine Schnittstelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="a53e5-143">Each time an attempt to resolve the neighbor fails, one interface is eliminated for that neighbor.</span></span>

<span data-ttu-id="a53e5-144">Wenn die Ziel Link-Local-Adresse aufgelöst wird, wird diese Schnittstelle verwendet, um das aktuelle Paket zu senden.</span><span class="sxs-lookup"><span data-stu-id="a53e5-144">If the destination link-local address resolves, then that interface is used to send the current packet.</span></span> <span data-ttu-id="a53e5-145">Diese Schnittstelle wird auch für alle nachfolgenden, eindeutig beschränkten Pakete verwendet, die an dieselbe Verbindungs lokale Zieladresse gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a53e5-145">This interface is also used for any subsequent ambiguously-scoped packets that are sent to the same link-local destination address.</span></span>

<span data-ttu-id="a53e5-146">Wenn bei der Nachbar Ermittlung die Ziel Link-Local-Adresse für alle Schnittstellen nicht aufgelöst werden kann, versucht das System, das Paket an der am häufigsten bevorzugten Schnittstelle (die erste versuchte Schnittstelle) zu senden.</span><span class="sxs-lookup"><span data-stu-id="a53e5-146">If Neighbor Discovery fails to resolve the destination link-local address on all interfaces, the system then tries to send the packet on the most preferred interface (the first interface tried).</span></span> <span data-ttu-id="a53e5-147">Der Netzwerk Stapel versucht immer, die Ziel Link-Local-Adresse auf der bevorzugten Schnittstelle aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="a53e5-147">The network stack keeps trying to resolve the destination link-local address on the most preferred interface.</span></span> <span data-ttu-id="a53e5-148">Nach einem bestimmten Zeitraum, nachdem die Nachbar Ermittlung an allen Schnittstellen fehlgeschlagen ist, startet der Netzwerk Stapel den Prozess erneut und versucht, die Ziel-Link-Local-Adresse auf allen Schnittstellen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="a53e5-148">After a period of time after Neighbor Discovery has failed on all interfaces, the network stack will restart the process again and try to resolve the destination link-local address on all of the interfaces.</span></span> <span data-ttu-id="a53e5-149">Derzeit beträgt dieses Zeitintervall, in dem die Nachbar Ermittlung wieder auf allen Schnittstellen versucht wird, 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a53e5-149">Currently, this time interval when Neighbor Discovery is again tried on all interfaces is 60 seconds.</span></span> <span data-ttu-id="a53e5-150">Dieses Zeitintervall kann sich jedoch in Windows-Versionen ändern und sollte nicht von einer Anwendung angenommen werden.</span><span class="sxs-lookup"><span data-stu-id="a53e5-150">However, this time interval may change on versions of Windows and should not be assumed by an application.</span></span>

> [!Note]  
> <span data-ttu-id="a53e5-151">Wenn eine Anwendung dieselbe Link-Local-Adresse an eine andere Schnittstelle bindet, nachdem die Nachbar Ermittlung die Link-Local-Adresse aufgelöst hat, wird die Schnittstelle mit der von der Nachbar Ermittlung zurückgegebenen Verbindungs lokalen Zieladresse nicht überschrieben.</span><span class="sxs-lookup"><span data-stu-id="a53e5-151">If an application binds the same link-local address to a different interface after Neighbor Discovery has resolved the link-local address, that will not override the interface with the link-local destination address returned by Neighbor Discovery.</span></span>

 

<span data-ttu-id="a53e5-152">Weitere Informationen zur Nachbar Ermittlung für IP-Version 6 finden Sie unter [RFC4861](https://tools.ietf.org/html/rfc4861) veröffentlicht von IETF.</span><span class="sxs-lookup"><span data-stu-id="a53e5-152">For more information on Neighbor Discovery for IP version 6, see [RFC4861](https://tools.ietf.org/html/rfc4861) published by the IETF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a53e5-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a53e5-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a53e5-154">IPv6-Site Präfixe</span><span class="sxs-lookup"><span data-stu-id="a53e5-154">IPv6 Site Prefixes</span></span>](site-prefixes-2.md)
</dt> <dt>

[<span data-ttu-id="a53e5-155">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="a53e5-155">Ipv6.exe</span></span>](ipv6-exe-2.md)
</dt> <dt>

[<span data-ttu-id="a53e5-156">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="a53e5-156">Netsh.exe</span></span>](netsh-exe.md)
</dt> <dt>

[<span data-ttu-id="a53e5-157">Verwenden von IPv6</span><span class="sxs-lookup"><span data-stu-id="a53e5-157">Using IPv6</span></span>](using-ipv6-2.md)
</dt> </dl>

 

 



