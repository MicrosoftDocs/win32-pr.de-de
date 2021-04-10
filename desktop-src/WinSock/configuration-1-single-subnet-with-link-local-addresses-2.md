---
description: Die erste Konfiguration erfordert keine zusätzliche Konfiguration über die Installation des Microsoft IPv6-Technologievorschau Protokolls hinaus.
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 'Konfiguration 1: einzelnes Subnetz mit Link-Local-Adressen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d09feb44c222b7213da18a6745fc632f3903209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041734"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a><span data-ttu-id="e6f99-103">Konfiguration 1: einzelnes Subnetz mit Link-Local-Adressen</span><span class="sxs-lookup"><span data-stu-id="e6f99-103">Configuration 1: Single Subnet with Link-local Addresses</span></span>

<span data-ttu-id="e6f99-104">Die erste Konfiguration erfordert keine zusätzliche Konfiguration über die Installation des Microsoft IPv6-Technologievorschau Protokolls hinaus.</span><span class="sxs-lookup"><span data-stu-id="e6f99-104">The first configuration requires no additional configuration beyond installing the Microsoft IPv6 Technology Preview protocol.</span></span> <span data-ttu-id="e6f99-105">Diese Konfiguration besteht aus mindestens zwei Knoten im gleichen Subnetz.</span><span class="sxs-lookup"><span data-stu-id="e6f99-105">This configuration consists of at least two nodes on the same subnet.</span></span> <span data-ttu-id="e6f99-106">In der IPv6-Terminologie befinden sich die beiden Knoten in derselben Verbindung ohne zwischengeschaltete Router.</span><span class="sxs-lookup"><span data-stu-id="e6f99-106">In IPv6 terminology, the two nodes are on the same link with no intermediate routers.</span></span>

<span data-ttu-id="e6f99-107">Die folgende Abbildung zeigt die Konfiguration von zwei Knoten in einem einzelnen Subnetz mithilfe von Link-Local-Adressen.</span><span class="sxs-lookup"><span data-stu-id="e6f99-107">The following illustration shows the configuration of two nodes on a single subnet using link-local addresses.</span></span>

![zwei Knoten, die Link-Local-Adressen verwenden.](images/v6mig-1.png)

<span data-ttu-id="e6f99-109">Standardmäßig konfiguriert IPv6 Verbindungs lokale IP-Adressen für jede Schnittstelle, die den installierten Ethernet-Netzwerkadaptern entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6f99-109">By default, IPv6 configures link-local IP addresses for each interface corresponding to installed Ethernet network adapters.</span></span> <span data-ttu-id="e6f99-110">Link-Local-Adressen haben das Präfix FE80::/64.</span><span class="sxs-lookup"><span data-stu-id="e6f99-110">Link-local addresses have the prefix fe80::/64.</span></span> <span data-ttu-id="e6f99-111">Die letzten 64 Bits der IPv6-Adresse werden als Schnittstellen Bezeichner bezeichnet und von der 48-Bit-Mac-Adresse des Netzwerkadapters abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e6f99-111">The last 64 bits of the IPv6 address is known as the interface identifier and is derived from the 48-bit MAC address of the network adapter.</span></span>

<span data-ttu-id="e6f99-112">So erstellen Sie den IPv6-Schnittstellen Bezeichner aus der 48-Bit-Ethernet-MAC-Adresse (6 Byte):</span><span class="sxs-lookup"><span data-stu-id="e6f99-112">To create the IPv6 interface identifier from the 48-bit (6-byte) Ethernet MAC address:</span></span>

-   <span data-ttu-id="e6f99-113">Die hexadezimal Ziffern 0xFF-FE werden zwischen dem dritten und vierten Byte der Mac-Adresse eingefügt.</span><span class="sxs-lookup"><span data-stu-id="e6f99-113">The hex digits 0xff-fe are inserted between the third and fourth byte of the MAC address.</span></span>
-   <span data-ttu-id="e6f99-114">Das Universal/local-Bit, das zweite niedrig wertige Bit des ersten Bytes der Mac-Adresse, wird ergänzt.</span><span class="sxs-lookup"><span data-stu-id="e6f99-114">The Universal/Local bit, the second low-order bit of the first byte of the MAC address, is complemented.</span></span> <span data-ttu-id="e6f99-115">Wenn der Wert 1 ist, wird er in 0 (null) umgewandelt, und wenn er 0 ist, wird er in 1 umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="e6f99-115">If it is a 1, it is turned to 0, and if it is a 0, it is turned to 1.</span></span>

<span data-ttu-id="e6f99-116">Beispielsweise für die Mac-Adresse 00-60-08-52-F9-D8:</span><span class="sxs-lookup"><span data-stu-id="e6f99-116">For example, for the MAC address 00-60-08-52-f9-d8:</span></span>

-   <span data-ttu-id="e6f99-117">Die hexadezimal Ziffern 0xFF-FE werden zwischen 0x08 (das dritte Byte) und 0x52 (das vierte Byte) der Mac-Adresse eingefügt, wodurch die 64-Bit-Adresse 00-60-08-FF-FE-52-F9-D8 gebildet wird.</span><span class="sxs-lookup"><span data-stu-id="e6f99-117">The hex digits 0xff-fe are inserted between 0x08 (the third byte) and 0x52 (the fourth byte) of the MAC address, forming the 64-bit address 00-60-08-ff-fe-52-f9-d8.</span></span>
-   <span data-ttu-id="e6f99-118">Das universelle/lokale Bit, das zweite niedrig wertige Bit von 0x00 (das erste Byte) der Mac-Adresse wird ergänzt.</span><span class="sxs-lookup"><span data-stu-id="e6f99-118">The Universal/Local bit, the second low-order bit of 0x00 (the first byte) of the MAC address is complemented.</span></span> <span data-ttu-id="e6f99-119">Das zweite niedrig wertige Bit von 0x00 ist 0 (null), das, wenn es ergänzt wird, 1 ist.</span><span class="sxs-lookup"><span data-stu-id="e6f99-119">The second low-order bit of 0x00 is 0 which, when complemented, becomes 1.</span></span> <span data-ttu-id="e6f99-120">Das Ergebnis ist, dass 0x00 für das erste Byte 0x02 wird.</span><span class="sxs-lookup"><span data-stu-id="e6f99-120">The result is that for the first byte, 0x00 becomes 0x02.</span></span>

<span data-ttu-id="e6f99-121">Daher ist der IPv6-Schnittstellen Bezeichner, der der Ethernet-MAC-Adresse 00-60-08-52-F9-D8 entspricht, 02-60-08-FF-FE-52-F9-D8.</span><span class="sxs-lookup"><span data-stu-id="e6f99-121">Therefore, the IPv6 interface identifier corresponding to the Ethernet MAC address of 00-60-08-52-f9-d8 is 02-60-08-ff-fe-52-f9-d8.</span></span>

<span data-ttu-id="e6f99-122">Die Link-Local-Adresse eines Knotens ist die Kombination aus dem Präfix FE80::/64 und dem 64-Bit-Schnittstellen Bezeichner, der in IPv6-Doppelpunkt-hexadezimal Notation ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="e6f99-122">The link-local address of a node is the combination of the prefix fe80::/64 and the 64-bit interface identifier expressed in IPv6 colon-hexadecimal notation.</span></span> <span data-ttu-id="e6f99-123">Daher ist die Link-Local-Adresse dieses Beispiel Knotens mit dem Präfix FE80::/64 und dem Schnittstellen Bezeichner 02-60-08-FF-FE-52-F9-D8 FE80:: 260:8ff: FE52: F9D8.</span><span class="sxs-lookup"><span data-stu-id="e6f99-123">Therefore, the link-local address of this example node with the prefix fe80::/64 and the interface identifier 02-60-08-ff-fe-52-f9-d8 is fe80::260:8ff:fe52:f9d8.</span></span>

<span data-ttu-id="e6f99-124">Sie können Ihre lokale Linkadresse mit IPv6 anzeigen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="e6f99-124">You can view your link local address by using ipv6 if, as demonstrated in the following example:</span></span>

<span data-ttu-id="e6f99-125">**IPv6 if**</span><span class="sxs-lookup"><span data-stu-id="e6f99-125">**ipv6 if**</span></span>

``` syntax
Interface 4 (site 1): Local Area Connection
  uses Neighbor Discovery
  link-level address: 00-10-5a-aa-20-a2
    preferred address fe80::210:5aff:feaa:20a2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ffaa:20a2, 1 refs, last reporter
  link MTU 1500 (true link MTU 1500)
  current hop limit 128
  reachable time 43500ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 3 (site 1): 6-over-4 Virtual Interface
  uses Neighbor Discovery
  link-level address: 10.0.0.2
    preferred address fe80::a00:2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ff00:2, 1 refs, last reporter
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 34000ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 2 (site 0): Tunnel Pseudo-Interface
  does not use Neighbor Discovery
  link-level address: 0.0.0.0
    preferred address ::10.0.0.2, infinite/infinite
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
Interface 1 (site 0): Loopback Pseudo-Interface
  does not use Neighbor Discovery
  link-level address:
    preferred address ::1, infinite/infinite
  link MTU 1500 (true link MTU 1500)
  current hop limit 1
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
```

<span data-ttu-id="e6f99-126">Schnittstelle 4 ist eine Schnittstelle, die einem installierten Ethernet-Adapter mit der Link-Local-Adresse FE80:: 210:5AFF: Feaa: 20A2 entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6f99-126">Interface 4 is an interface corresponding to an installed Ethernet adapter with a link-local address of fe80::210:5aff:feaa:20a2.</span></span>

<span data-ttu-id="e6f99-127">Weitere Informationen zur IPv6-Adressierung und eine Übersicht über IPv6-Konzepte finden Sie im Whitepaper Introduction to IPv6 (Einführung in das IPv6).</span><span class="sxs-lookup"><span data-stu-id="e6f99-127">For more information on IPv6 addressing and an overview of IPv6 concepts, see the Introduction to IPv6 white paper.</span></span>

## <a name="testing-connectivity-between-two-link-local-hosts"></a><span data-ttu-id="e6f99-128">Testen der Konnektivität zwischen zwei Verbindungs lokalen Hosts</span><span class="sxs-lookup"><span data-stu-id="e6f99-128">Testing Connectivity Between Two Link-local Hosts</span></span>

<span data-ttu-id="e6f99-129">Sie können einen einfachen Ping (einen Austausch von ICMPv6-Echo Anforderungs-und Echo Antwort Nachrichten) durchführen, indem Sie IPv6 zwischen zwei Verbindungs lokalen Hosts verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6f99-129">You can do a simple ping (an exchange of ICMPv6 Echo Request and Echo Reply messages) using IPv6 between two link-local hosts.</span></span>

<span data-ttu-id="e6f99-130">**So Pingen Sie mithilfe von IPv6 zwischen zwei Verbindungs lokalen Hosts**</span><span class="sxs-lookup"><span data-stu-id="e6f99-130">**To ping using IPv6 between two link-local hosts**</span></span>

1.  <span data-ttu-id="e6f99-131">Installieren Sie die Microsoft IPv6-Technologievorschau für Windows auf zwei Windows-Hosts (Host A und Host B), die sich auf demselben Link (Subnetz) befinden.</span><span class="sxs-lookup"><span data-stu-id="e6f99-131">Install the Microsoft IPv6 Technology Preview for Windows on two Windows hosts (Host A and Host B) that are on the same link (subnet).</span></span>
2.  <span data-ttu-id="e6f99-132">Verwenden Sie IPv6 if auf Host A zum Abrufen der Link-Local-Adresse für die Ethernet-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e6f99-132">Use ipv6 if on Host A to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="e6f99-133">Beispiel: die Link-Local-Adresse von Host A ist FE80:: 210:5AFF: Feaa: 20A2.</span><span class="sxs-lookup"><span data-stu-id="e6f99-133">Example: The link-local address of Host A is fe80::210:5aff:feaa:20a2.</span></span>

3.  <span data-ttu-id="e6f99-134">Verwenden Sie IPv6 if auf Host B zum Abrufen der Link-Local-Adresse für die Ethernet-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e6f99-134">Use ipv6 if on Host B to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="e6f99-135">Beispiel: die Link-Local-Adresse von Host B lautet FE80:: 260:97FF: FE02:6EA5.</span><span class="sxs-lookup"><span data-stu-id="e6f99-135">Example: The link-local address of Host B is fe80::260:97ff:fe02:6ea5.</span></span>

4.  <span data-ttu-id="e6f99-136">Pingen Sie Host B von Host a mithilfe Ping6.exe.</span><span class="sxs-lookup"><span data-stu-id="e6f99-136">From Host A, ping Host B using Ping6.exe.</span></span>

    <span data-ttu-id="e6f99-137">Beispiel: ping6 FE80:: 260:97FF: FE02:6EA5</span><span class="sxs-lookup"><span data-stu-id="e6f99-137">Example: ping6 fe80::260:97ff:fe02:6ea5</span></span>

<span data-ttu-id="e6f99-138">Sie können auch die Option Ping6.exe-s verwenden, um die Quelladresse anzugeben, von der die Echo Anforderungs Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6f99-138">To specify the source address from which the Echo Request messages are sent, you can also use the Ping6.exe -s option.</span></span> <span data-ttu-id="e6f99-139">Um z. B. Echo Anforderungen von der IPv6-Adresse FE80:: 210:5AFF: Feaa: 20A2 an Host B zu senden, verwenden Sie den folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="e6f99-139">For example, to send Echo Requests to Host B from the IPv6 address of fe80::210:5aff:feaa:20a2, use the following command:</span></span>

<span data-ttu-id="e6f99-140">**ping6-s FE80:: 210:5AFF: Feaa: 20A2% 4 FE80:: 260:97FF: FE02:6EA5**</span><span class="sxs-lookup"><span data-stu-id="e6f99-140">**ping6 -s fe80::210:5aff:feaa:20a2%4 fe80::260:97ff:fe02:6ea5**</span></span>

<span data-ttu-id="e6f99-141">Beim Pingen einer Link-lokal-oder Site-Local-Adresse empfiehlt es sich, die Bereichs-ID anzugeben, damit die Zieladresse eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="e6f99-141">When pinging a link-local or site-local address, it is recommended to specify the scope-ID to make the destination address unambiguous.</span></span> <span data-ttu-id="e6f99-142">Die Notation zum Angeben der Bereichs-ID lautet Address% Scope-ID.</span><span class="sxs-lookup"><span data-stu-id="e6f99-142">The notation to specify the scope-ID is address%scope-ID.</span></span> <span data-ttu-id="e6f99-143">Bei Link-Local-Adressen ist die Bereichs-ID gleich der Schnittstellen Nummer, wie im IPv6-Befehl "if" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6f99-143">For link-local addresses, the scope-ID is equal to the interface number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="e6f99-144">Bei Site-Local-Adressen ist die Bereichs-ID gleich der Standort Nummer, wie im IPv6-Befehl "if" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6f99-144">For site-local addresses, the scope-ID is equal to the site number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="e6f99-145">Verwenden Sie z. b. den folgenden Befehl, um Echo Anforderungs Nachrichten an Host B mithilfe von Scope-ID 4 zu senden:</span><span class="sxs-lookup"><span data-stu-id="e6f99-145">For example, to send Echo Request messages to Host B using scope-ID 4, use the following command:</span></span>

<span data-ttu-id="e6f99-146">**ping6 FE80:: 260:97FF: FE02:6EA5% 4**</span><span class="sxs-lookup"><span data-stu-id="e6f99-146">**ping6 fe80::260:97ff:fe02:6ea5%4**</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6f99-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6f99-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6f99-148">Empfohlene Konfigurationen für IPv6</span><span class="sxs-lookup"><span data-stu-id="e6f99-148">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> </dl>

 

 



