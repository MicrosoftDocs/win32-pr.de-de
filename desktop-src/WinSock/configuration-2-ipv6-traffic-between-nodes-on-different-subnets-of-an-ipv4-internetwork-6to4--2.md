---
description: IPv6-zu-IPv4 ist eine Methode zum Verbinden von IPv6-Hosts oder-Standorten über die vorhandene IPv4-Internet Infrastruktur.
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: 'Konfiguration 2: IPv6-Datenverkehr zwischen Knoten in unterschiedlichen Subnetzen eines IPv4-Netzwerks (6zu 4)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1abd5477005e6a1e71c13aaf19a734e9191097d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484950"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a><span data-ttu-id="cfa9c-103">Konfiguration 2: IPv6-Datenverkehr zwischen Knoten in unterschiedlichen Subnetzen eines IPv4-Netzwerks (6zu 4)</span><span class="sxs-lookup"><span data-stu-id="cfa9c-103">Configuration 2: IPv6 Traffic Between Nodes on Different Subnets of an IPv4 Internetwork (6to4)</span></span>

<span data-ttu-id="cfa9c-104">IPv6-zu-IPv4 ist eine Methode zum Verbinden von IPv6-Hosts oder-Standorten über die vorhandene IPv4-Internet Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-104">6to4 is a method for connecting IPv6 hosts or sites over the existing IPv4 Internet infrastructure.</span></span> <span data-ttu-id="cfa9c-105">Dabei wird ein eindeutiges Adress Präfix verwendet, um isolierten IPv6-Standorten ihren eigenen IPv6-Adressraum zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-105">It uses a unique address prefix to give isolated IPv6 sites their own IPv6 address space.</span></span> <span data-ttu-id="cfa9c-106">IPv6-zu-IPv4 ist vergleichbar mit einem "Pseudo ISP", der IPv6-Konnektivität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-106">6to4 is like a "pseudo-ISP" providing IPv6 connectivity.</span></span> <span data-ttu-id="cfa9c-107">Sie können IPv6-zu-IPv4 für die direkte Kommunikation mit anderen IPv6-zu-IPv4-Standorten verwenden.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-107">You can use 6to4 to communicate directly with other 6to4 sites.</span></span> <span data-ttu-id="cfa9c-108">IPv6-zu-IPv4 erfordert keine Verwendung von IPv6-Routern, und der IPv6-Datenverkehr ist mit einem IPv4-Header gekapselt.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-108">6to4 does not require the use of IPv6 routers and its IPv6 traffic is encapsulated with an IPv4 header.</span></span>

<span data-ttu-id="cfa9c-109">In der folgenden Abbildung wird die Konfiguration von zwei Knoten in separaten Subnetzen mit IPv6-zu-IPv4 für die Kommunikation über einen IPv4-Router veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-109">The following illustration shows the configuration of two nodes on separate subnets using 6to4 to communicate across an IPv4 router.</span></span>

![Knoten, die IPv6-zu-IPv4 zum kommunizieren über einen IPv4-Router verwenden.](images/v6mig-2.png)

<span data-ttu-id="cfa9c-111">Die wichtigste Voraussetzung für die Verwendung von 6to4 ist eine Global Routing fähige IPv4-Adresse für Ihre Website.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-111">The main requirement for using 6to4 is one globally routable IPv4 address for your site.</span></span> <span data-ttu-id="cfa9c-112">Angenommen, Ihr Standort besteht aus einer Sammlung von IPv6-Computern, die Sie verwalten (einige führen das Microsoft IPv6-Protokoll und einige andere IPv6-Implementierungen aus).</span><span class="sxs-lookup"><span data-stu-id="cfa9c-112">Suppose that your site consists of a collection of IPv6 computers that you manage (some running the Microsoft IPv6 protocol and some running other IPv6 implementations).</span></span> <span data-ttu-id="cfa9c-113">Nehmen Sie auch an, dass alle IPv6-Computer direkt über Ethernet oder 6-over-4 angeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-113">Assume also that all IPv6 computers are directly connected using Ethernet or 6-over-4.</span></span> <span data-ttu-id="cfa9c-114">Die Global Routing fähige IPv4-Adresse muss einem ihrer Computer zugewiesen werden, auf denen das Microsoft IPv6-Protokoll ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-114">The globally routable IPv4 address must be assigned to one of your computers running the Microsoft IPv6 protocol.</span></span> <span data-ttu-id="cfa9c-115">Dieser Computer ist Ihr IPv6-zu-IPv4-Gateway.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-115">This computer will be your 6to4 gateway.</span></span>

<span data-ttu-id="cfa9c-116">Wenn Sie über eine IPv4-Adresse verfügen, die Teil des privaten Adressraums (10.0.0.0/8, 172.16.0.0/12 oder 192.168.0.0/16) ist, oder den APIPA-Adressraum (Automatic Private IP Address) von 169.254.0.0/16, der von Windows 2000 verwendet wird, ist er nicht global Routing fähig.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-116">If you have an IPv4 address that is part of the private address space (10.0.0.0/8, 172.16.0.0/12, or 192.168.0.0/16) or the Automatic Private IP Addressing (APIPA) address space of 169.254.0.0/16 used by Windows 2000, it is not globally routable.</span></span> <span data-ttu-id="cfa9c-117">Andernfalls handelt es sich wahrscheinlich um eine öffentliche IP-Adresse, die Global Routing fähig ist.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-117">Otherwise, it is probably a public IP address and is globally routable.</span></span> <span data-ttu-id="cfa9c-118">Weitere Informationen zur Ermittlung, ob Ihre ISP-Verbindung IPv6-zu-IPv4 unterstützt, finden Sie im Thema zum [Debuggen](#debugging-6to4-configuration) von IPv6-zu-IPv4-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="cfa9c-118">See the [Debugging 6to4 Configuration](#debugging-6to4-configuration) topic in this document for more help in determining whether your ISP connection supports 6to4.</span></span>

## <a name="the-6to4cfgexe-tool"></a><span data-ttu-id="cfa9c-119">Das 6to4cfg.exe Tool</span><span class="sxs-lookup"><span data-stu-id="cfa9c-119">The 6to4cfg.exe Tool</span></span>

<span data-ttu-id="cfa9c-120">Das 6to4cfg.exe Tool automatisiert die IPv6-zu-IPv4-Konfiguration, ermittelt automatisch Ihre Global Routing fähige IPv4-Adresse und erstellt ein IPv6-zu-IPv4-Präfix.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-120">The 6to4cfg.exe tool automates 6to4 configuration, automatically discovering your globally routable IPv4 address and creating a 6to4 prefix.</span></span> <span data-ttu-id="cfa9c-121">Sie führt die Konfiguration entweder direkt aus, oder Sie kann ein Konfigurationsskript schreiben, das Sie später überprüfen und ausführen können.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-121">It either performs the configuration directly, or it can write a configuration script that you can inspect and run later.</span></span>

<span data-ttu-id="cfa9c-122">Die grundlegende 6to4cfg.exe Befehlssyntax lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-122">The basic 6to4cfg.exe command syntax is as follows.</span></span>

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span data-ttu-id="cfa9c-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*Einfügen*\]</span><span class="sxs-lookup"><span data-stu-id="cfa9c-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*filename*\]</span></span>
</dt> <dd>

<span data-ttu-id="cfa9c-124">Schreibt das Konfigurationsskript in eine Datei, wenn Sie einen Dateinamen angeben.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-124">Writes the configuration script to a file, if you specify a file name.</span></span> <span data-ttu-id="cfa9c-125">Das Konfigurationsskript verwendet Ipv6.exe.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-125">The configuration script uses Ipv6.exe.</span></span>

<span data-ttu-id="cfa9c-126">Sie können con als Dateinamen angeben, um das Konfigurationsskript in die Konsolenausgabe zu schreiben. Dies ist hilfreich, um zu sehen, welche 6to4cfg.exe in einem Testszenario ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-126">You can specify con for the file name to write the configuration script to console output, which is useful for seeing what 6to4cfg.exe will do in a test scenario.</span></span>

<span data-ttu-id="cfa9c-127">Wenn Sie keinen Dateinamen angeben, wird von 6to4cfg.exe die IPv6-Konfiguration auf Ihrem Computer direkt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-127">If you do not specify a file name, 6to4cfg.exe directly updates the IPv6 configuration on your computer.</span></span>

</dd> <dt>

<span data-ttu-id="cfa9c-128"><span id="-r"></span><span id="-R"></span>-r</span><span class="sxs-lookup"><span data-stu-id="cfa9c-128"><span id="-r"></span><span id="-R"></span>-r</span></span>
</dt> <dd>

<span data-ttu-id="cfa9c-129">Wird zu einem IPv6-zu-IPv4-Gatewayrouter für Ihr lokales Netzwerk, der das Routing an allen Schnittstellen und zugewiesenen Subnetzpräfixen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-129">Becomes a 6to4 gateway router for your local network, enabling routing on all of your interfaces and assigned subnet prefixes.</span></span>

</dd> <dt>

<span data-ttu-id="cfa9c-130"><span id="-s"></span><span id="-S"></span>-s</span><span class="sxs-lookup"><span data-stu-id="cfa9c-130"><span id="-s"></span><span id="-S"></span>-s</span></span>
</dt> <dd>

<span data-ttu-id="cfa9c-131">Ermöglicht die Standort lokale Adressierung an Ihrem IPv6-zu-IPv4-Standort.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-131">Enables site-local addressing in your 6to4 site.</span></span> <span data-ttu-id="cfa9c-132">Dieser Befehl ist nur nützlich, wenn er in Verbindung mit-r verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-132">This command is only useful when used in conjunction with -r.</span></span>

</dd> <dt>

<span data-ttu-id="cfa9c-133"><span id="-u"></span><span id="-U"></span>-u</span><span class="sxs-lookup"><span data-stu-id="cfa9c-133"><span id="-u"></span><span id="-U"></span>-u</span></span>
</dt> <dd>

<span data-ttu-id="cfa9c-134">Gibt an, dass die IPv6-zu-IPv4-Konfiguration umgekehrt wird.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-134">Specifies that the 6to4 configuration be reversed.</span></span> <span data-ttu-id="cfa9c-135">Aus diesem Grund kehrt IPv6-zu-4cfg-u die Auswirkung von 6um4cfg zurück, und 6um4cfg-r-u kehrt die Auswirkung von 6zu 4cfg-r um usw. um.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-135">Therefore 6to4cfg -u reverses the effect of 6to4cfg and 6to4cfg -r -u reverses the effect of 6to4cfg -r, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="cfa9c-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *Relay*</span><span class="sxs-lookup"><span data-stu-id="cfa9c-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *relay*</span></span>
</dt> <dd>

<span data-ttu-id="cfa9c-137">Gibt den Namen oder die IPv4-Adresse eines IPv6-zu-IPv4-Relay-Routers an.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-137">Specifies the name or IPv4 address of a 6to4 relay router.</span></span> <span data-ttu-id="cfa9c-138">Der Standardname ist 6to4.IPv6.Microsoft.com, der IPv6-zu-IPv4-Relayrouter im Internet.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-138">The default name is 6to4.ipv6.microsoft.com, the 6to4 relay router on the Internet.</span></span>

</dd> <dt>

<span data-ttu-id="cfa9c-139"><span id="-b"></span><span id="-B"></span>-b</span><span class="sxs-lookup"><span data-stu-id="cfa9c-139"><span id="-b"></span><span id="-B"></span>-b</span></span>
</dt> <dd>

<span data-ttu-id="cfa9c-140">Gibt an, dass 6to4cfg.exe anstelle des ersten die "beste" relayadresse auswählt.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-140">Specifies that 6to4cfg.exe picks the "best" relay address instead of the first.</span></span>

</dd> <dt>

<span data-ttu-id="cfa9c-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S- *Adresse*</span><span class="sxs-lookup"><span data-stu-id="cfa9c-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *address*</span></span>
</dt> <dd>

<span data-ttu-id="cfa9c-142">Gibt die lokale IPv4-Adresse für das IPv6-zu-IPv4-Präfix an.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-142">Specifies the local IPv4 address for the 6to4 prefix.</span></span>

</dd> </dl>

## <a name="manual-6to4-configuration"></a><span data-ttu-id="cfa9c-143">Manuelle IPv6-zu-IPv4-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa9c-143">Manual 6to4 Configuration</span></span>

<span data-ttu-id="cfa9c-144">In diesem Beispiel lautet die Adresse des IPv6-zu-IPv4-Gateways 172.31.42.239.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-144">In this example the address of the 6to4 gateway is 172.31.42.239.</span></span> <span data-ttu-id="cfa9c-145">Sie benötigen eine eigene Global Routing fähige IPv4-Adresse für die Verwendung von 6zu 4.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-145">You need your own globally routable IPv4 address to use 6to4.</span></span>

> [!Note]  
> <span data-ttu-id="cfa9c-146">Die IP-Adresse 172.31.42.239 wird nur zu Beispiel Zwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-146">The IP address 172.31.42.239 is used for example purposes only.</span></span> <span data-ttu-id="cfa9c-147">Dies ist eine private Adresse, die im Internet nicht global Routing fähig ist.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-147">This is a private address and is not globally routable on the Internet.</span></span>

 

<span data-ttu-id="cfa9c-148">Die 32-Bit-Global Routing fähige IPv4-Adresse wird mit dem 16-Bit-Präfix 2002::/16 kombiniert, um ein 48-Bit-IPv6-Adress Präfix für Ihre Website zu bilden.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-148">The 32-bit globally routable IPv4 address is combined with the 16-bit prefix 2002::/16 to form a 48-bit IPv6 address prefix for your site.</span></span> <span data-ttu-id="cfa9c-149">In diesem Beispiel ist das IPv6-zu-IPv4-Site Präfix 2002: ac1f: 2aef::/48.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-149">In this example, the 6to4 site prefix is 2002:ac1f:2aef::/48.</span></span> <span data-ttu-id="cfa9c-150">Beachten Sie, dass ac1f: 2aef die hexadezimale Codierung von 172.31.42.239 ist (natürlich verwenden Sie ein anderes Präfix basierend auf Ihrer eigenen Global Routing fähigen IPv4-Adresse).</span><span class="sxs-lookup"><span data-stu-id="cfa9c-150">Note that ac1f:2aef is the hexadecimal encoding of 172.31.42.239 (of course, you will use a different prefix based on your own globally routable IPv4 address).</span></span> <span data-ttu-id="cfa9c-151">Mit dem IPv6-zu-IPv4-Site Präfix können Sie Adressen und Subnetzpräfixe innerhalb Ihrer Website zuweisen.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-151">Using the 6to4 site prefix, you can assign addresses and subnet prefixes inside your site.</span></span>

<span data-ttu-id="cfa9c-152">In diesem Beispiel wird davon ausgegangen, dass Sie Subnetz 0 zum manuellen Konfigurieren einer IPv6-zu-IPv4-Adresse auf dem IPv6-zu-IPv4-Gatewaycomputer verwenden und dass Sie Subnetz 1 zum automatischen Konfigurieren von Adressen in Ihrem Ethernet-Netzwerksegment verwenden.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-152">This example assumes that you use subnet 0 for manually configuring a 6to4 address on your 6to4 gateway computer and that you use subnet 1 for automatically configuring addresses on your Ethernet network segment.</span></span> <span data-ttu-id="cfa9c-153">Es können jedoch auch andere Optionen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-153">However, other choices are possible.</span></span>

1.  <span data-ttu-id="cfa9c-154">Verwenden Sie Ipv6.exe zum Aktivieren von IPv6-zu-IPv4 auf dem IPv6-zu-IPv4-Gatewaycomputer</span><span class="sxs-lookup"><span data-stu-id="cfa9c-154">Use Ipv6.exe to enable 6to4 on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="cfa9c-155">**IPv6-RTU 2002::/16 2**</span><span class="sxs-lookup"><span data-stu-id="cfa9c-155">**ipv6 rtu 2002::/16 2**</span></span>

    <span data-ttu-id="cfa9c-156">Der **IPv6-RTU** -Befehl führt ein Update für eine Routing Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-156">The **ipv6 rtu** command performs a routing table update.</span></span> <span data-ttu-id="cfa9c-157">Sie kann verwendet werden, um eine Route hinzuzufügen, zu entfernen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-157">It can be used to add, remove, or update a route.</span></span> <span data-ttu-id="cfa9c-158">In diesem Fall wird IPv6-zu-IPv4 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-158">In this case it is enabling 6to4.</span></span>

    <span data-ttu-id="cfa9c-159">Das 2002::/16-Argument ist das Präfix der Route, das das eindeutige IPv6-zu-IPv4-Präfix angibt.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-159">The 2002::/16 argument is the prefix of the route, specifying the unique 6to4 prefix.</span></span>

    <span data-ttu-id="cfa9c-160">Das 2-Argument gibt die on-Link-Schnittstelle für dieses Präfix an.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-160">The 2 argument specifies the on-link interface for this prefix.</span></span> <span data-ttu-id="cfa9c-161">Schnittstelle \# 2 ist die "Pseudo Schnittstelle", die für konfigurierte Tunnel, automatische Tunnelung und 6to4 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-161">Interface \#2 is the "pseudo-interface" used for configured tunnels, automatic tunneling, and 6to4.</span></span> <span data-ttu-id="cfa9c-162">Wenn eine IPv6-Zieladresse mit dem Präfix 2002::/16 übereinstimmt, werden die 32 Bits, die dem Präfix in der Zieladresse folgen, extrahiert, um eine IPv4-Zieladresse zu bilden.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-162">When an IPv6 destination address matches the 2002::/16 prefix, the 32 bits that follow the prefix in the destination address are extracted to form an IPv4 destination address.</span></span> <span data-ttu-id="cfa9c-163">Das Paket ist mit einem IPv4-Header gekapselt und an die IPv4-Zieladresse gesendet.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-163">The packet is encapsulated with an IPv4 header and sent to the IPv4 destination address.</span></span>

2.  <span data-ttu-id="cfa9c-164">Konfigurieren einer IPv6-zu-IPv4-Adresse auf dem IPv6-zu-IPv4-Gatewaycomputer</span><span class="sxs-lookup"><span data-stu-id="cfa9c-164">Configure a 6to4 address on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="cfa9c-165">**IPv6 Adu 2/2002: ac1f: 2aef:: ac1f: 2aef**</span><span class="sxs-lookup"><span data-stu-id="cfa9c-165">**ipv6 adu 2/2002:ac1f:2aef::ac1f:2aef**</span></span>

    <span data-ttu-id="cfa9c-166">Der **IPv6 Adu** -Befehl führt ein Adress Update durch.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-166">The **ipv6 adu** command performs an address update.</span></span> <span data-ttu-id="cfa9c-167">Sie kann verwendet werden, um eine Adresse für eine Schnittstelle hinzuzufügen, zu entfernen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-167">It can be used to add, remove, or update an address on an interface.</span></span> <span data-ttu-id="cfa9c-168">In dieser Instanz wird die IPv6-zu-IPv4-Adresse des Computers konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-168">In this instance, it is configuring the computer's 6to4 address.</span></span>

    <span data-ttu-id="cfa9c-169">Das Argument 2/2002: ac1f: 2aef:: ac1f: 2aef gibt sowohl die-Schnittstelle als auch die-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-169">The 2/2002:ac1f:2aef::ac1f:2aef argument specifies both the interface and the address.</span></span> <span data-ttu-id="cfa9c-170">Hierfür muss address 2002: ac1f: 2aef:: ac1f: 2aef für Schnittstelle \# 2 konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-170">It requires configuring address 2002:ac1f:2aef::ac1f:2aef on interface \#2.</span></span> <span data-ttu-id="cfa9c-171">Die Adresse wird mit dem Website Präfix 2002 erstellt: ac1f: 2aef::/48, Subnetz 0 zum Angeben eines Subnetzpräfixes 2002: ac1f: 2aef::/64 und eines 64-Bit-Schnittstellen Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-171">The address is created using the site prefix 2002:ac1f:2aef::/48, subnet 0 to give a subnet prefix 2002:ac1f:2aef::/64, and a 64-bit interface identifier.</span></span> <span data-ttu-id="cfa9c-172">In der dargestellten Konvention wird die IPv4-Adresse des Computers für den Schnittstellen Bezeichner für Adressen verwendet, die Schnittstelle 2 zugewiesen sind \# .</span><span class="sxs-lookup"><span data-stu-id="cfa9c-172">The convention demonstrated uses the computer's IPv4 address for the interface identifier for addresses assigned to interface \#2.</span></span> <span data-ttu-id="cfa9c-173">Ac1f: 2aef sollte für ihre Verwendung durch die hexadezimale Codierung Ihrer eigenen Global Routing fähigen IPv4-Adresse ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-173">For your use, ac1f:2aef should be replaced by the hexadecimal encoding of your own globally routable IPv4 address.</span></span>

<span data-ttu-id="cfa9c-174">Die zwei vorherigen Befehle sind ausreichend, um die Kommunikation mit anderen IPv6-zu-IPv4-Standorten zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-174">The two preceding commands are sufficient to allow communication with other 6to4 sites.</span></span> <span data-ttu-id="cfa9c-175">Sie können z. b. versuchen, die Microsoft IPv6-zu-IPv4-Website zu pingen:</span><span class="sxs-lookup"><span data-stu-id="cfa9c-175">For example, you can try pinging the Microsoft 6to4 site:</span></span>

<span data-ttu-id="cfa9c-176">**ping6 2002:836b: 9820:: 836b: 9820**</span><span class="sxs-lookup"><span data-stu-id="cfa9c-176">**ping6 2002:836b:9820::836b:9820**</span></span>

<span data-ttu-id="cfa9c-177">Um die Kommunikation mit dem 6bone zu ermöglichen, müssen Sie einen konfigurierten Standard Tunnel zu einem IPv6-zu-IPv4-Relay erstellen.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-177">To enable communication with the 6bone, you must create a default configured tunnel to a 6to4 relay.</span></span> <span data-ttu-id="cfa9c-178">Sie können den Microsoft IPv6-zu-IPv4-Relay-Router verwenden, 131.107.152.32:</span><span class="sxs-lookup"><span data-stu-id="cfa9c-178">You can use the Microsoft 6to4 relay router, 131.107.152.32:</span></span>

<span data-ttu-id="cfa9c-179">**IPv6-RTU::/0 2/:: 131.107.152.32 pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="cfa9c-179">**ipv6 rtu ::/0 2/::131.107.152.32 pub life 1800**</span></span>

<span data-ttu-id="cfa9c-180">Der **IPv6-RTU** -Befehl führt eine Routing Tabellen Aktualisierung durch, wobei in dieser Instanz eine Standardroute zum IPv6-zu-IPv4-Relay festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-180">The **ipv6 rtu** command performs a routing table update, establishing, in this instance, a default route to the 6to4 relay.</span></span>

<span data-ttu-id="cfa9c-181">Das Argument::/0 ist das Routen Präfix.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-181">The ::/0 argument is the route prefix.</span></span> <span data-ttu-id="cfa9c-182">Das Präfix mit der Länge 0 gibt an, dass es sich um eine Standardroute handelt.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-182">The zero-length prefix indicates that it is a default route.</span></span>

<span data-ttu-id="cfa9c-183">Das Argument 2/:: 131.107.152.32 gibt den nächsten Hop-Nachbar für dieses Präfix an.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-183">The 2/::131.107.152.32 argument specifies the next-hop neighbor for this prefix.</span></span> <span data-ttu-id="cfa9c-184">Es erfordert, dass Pakete, die mit dem Präfix übereinstimmen, mit Schnittstelle 2 an address:: 131.107.152.32 \#</span><span class="sxs-lookup"><span data-stu-id="cfa9c-184">It requires that packets matching the prefix are forwarded to address ::131.107.152.32 using interface \#2.</span></span> <span data-ttu-id="cfa9c-185">Das Weiterleiten eines Pakets an:: 131.107.152.32 an Schnittstelle \# 2 bewirkt, dass es mit einem V4-Header gekapselt und an 131.107.152.32 gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-185">Forwarding a packet to ::131.107.152.32 on interface \#2 causes it to be encapsulated with a v4 header and sent to 131.107.152.32.</span></span>

<span data-ttu-id="cfa9c-186">Das Pub-Argument macht dies zu einer veröffentlichten Route.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-186">The pub argument makes this a published route.</span></span> <span data-ttu-id="cfa9c-187">Da dies nur für Router relevant ist, hat es keine Auswirkung, bis das Routing aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-187">Because this is only relevant for routers, it has no effect until routing is enabled.</span></span> <span data-ttu-id="cfa9c-188">Ebenso gilt die 30-minütige Lebensdauer nur, wenn das Routing aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-188">Similarly, the 30-minute lifetime pertains only if routing is enabled.</span></span>

<span data-ttu-id="cfa9c-189">Sie sollten in der Lage sein, auf 6bone-Websites und IPv6-zu-IPv4-Standorte zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-189">You should be able to access 6bone sites as well as 6to4 sites.</span></span> <span data-ttu-id="cfa9c-190">Sie können den folgenden Befehl verwenden, um dies zu testen:</span><span class="sxs-lookup"><span data-stu-id="cfa9c-190">You can use the following command to test this:</span></span>

<span data-ttu-id="cfa9c-191">**ping6 3FFE: 1cff: 0: F5:: 1**</span><span class="sxs-lookup"><span data-stu-id="cfa9c-191">**ping6 3ffe:1cff:0:f5::1**</span></span>

<span data-ttu-id="cfa9c-192">Der letzte Schritt besteht darin, das Routing auf dem IPv6-zu-IPv4-Gateway zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-192">The final step is to enable routing on your 6to4 gateway.</span></span> <span data-ttu-id="cfa9c-193">In diesem Beispiel wird davon ausgegangen, dass die Schnittstelle \# 3 auf Ihrem Gatewaycomputer eine Ethernet-Schnittstelle und Schnittstelle \# 4 6-over-4 ist.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-193">This example assumes that interface \#3 on your gateway computer is an Ethernet interface and interface \#4 is 6-over-4.</span></span> <span data-ttu-id="cfa9c-194">Der Computer kann seine Schnittstellen unterschiedlich unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-194">Your computer might number its interfaces differently.</span></span> <span data-ttu-id="cfa9c-195">Mit den folgenden beiden Befehlen werden den beiden Verknüpfungen Subnetzpräfixe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-195">The following two commands assign subnet prefixes to the two links.</span></span> <span data-ttu-id="cfa9c-196">Die Subnetzpräfixe werden aus dem IPv6-zu-IPv4-Präfix 2002 von der Site abgeleitet: ac1f: 2aef::/48:</span><span class="sxs-lookup"><span data-stu-id="cfa9c-196">The subnet prefixes are derived from the site's 6to4 prefix 2002:ac1f:2aef::/48:</span></span>

<span data-ttu-id="cfa9c-197">**IPv6-RTU 2002: ac1f: 2aef: 1::/64 3 pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="cfa9c-197">**ipv6 rtu 2002:ac1f:2aef:1::/64 3 pub life 1800**</span></span>

<span data-ttu-id="cfa9c-198">**IPv6-RTU 2002: ac1f: 2aef: 2::/64 4 pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="cfa9c-198">**ipv6 rtu 2002:ac1f:2aef:2::/64 4 pub life 1800**</span></span>

<span data-ttu-id="cfa9c-199">Der **IPv6-RTU** -Befehl gibt an, dass das Präfix 2002: ac1f: 2aef: 1::/64 mit Schnittstelle 3 verknüpft ist \# .</span><span class="sxs-lookup"><span data-stu-id="cfa9c-199">The **ipv6 rtu** command specifies that the prefix 2002:ac1f:2aef:1::/64 is on-link to interface \#3.</span></span> <span data-ttu-id="cfa9c-200">Es konfiguriert das erste Subnetzpräfix in der Ethernet-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-200">It is configuring the first subnet prefix on the Ethernet interface.</span></span> <span data-ttu-id="cfa9c-201">Die Route wird mit einer Lebensdauer von 30 Minuten veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-201">The route is published with a lifetime of 30 minutes.</span></span>

<span data-ttu-id="cfa9c-202">Entsprechend wird das Präfix 2002: ac1f: 2aef: 2::/64 in der 6-over-4-Schnittstelle konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-202">Similarly, the 2002:ac1f:2aef:2::/64 prefix is configured on the 6-over-4 interface.</span></span>

<span data-ttu-id="cfa9c-203">Mit den nächsten drei Befehlen kann der IPv6-zu-IPv4-Gatewaycomputer als Router fungieren:</span><span class="sxs-lookup"><span data-stu-id="cfa9c-203">The next three commands enable the 6to4 gateway computer to function as a router:</span></span>

<span data-ttu-id="cfa9c-204">**IPv6-IFC 2-FORW**</span><span class="sxs-lookup"><span data-stu-id="cfa9c-204">**ipv6 ifc 2 forw**</span></span>

<span data-ttu-id="cfa9c-205">**IPv6-IP3-FORW-ADV**</span><span class="sxs-lookup"><span data-stu-id="cfa9c-205">**ipv6 ifc 3 forw adv**</span></span>

<span data-ttu-id="cfa9c-206">**IPv6-IP4-FORW-ADV**</span><span class="sxs-lookup"><span data-stu-id="cfa9c-206">**ipv6 ifc 4 forw adv**</span></span>

<span data-ttu-id="cfa9c-207">Mit dem IPv6-Befehl " **IFC** " werden Attribute einer Schnittstelle gesteuert.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-207">The **ipv6 ifc** command controls attributes of an interface.</span></span> <span data-ttu-id="cfa9c-208">Ein Router leitet Pakete weiter und sendet Routerankündigungen.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-208">A router forwards packets and sends router advertisements.</span></span> <span data-ttu-id="cfa9c-209">In der Microsoft IPv6-Implementierung werden diese schnittstellenspezifischen Attribute separat gesteuert.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-209">In the Microsoft IPv6 implementation, these per-interface attributes are controlled separately.</span></span>

<span data-ttu-id="cfa9c-210">Schnittstelle \# 2 ist für Werbung nicht erforderlich, da es sich um eine Pseudo Schnittstelle handelt.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-210">Interface \#2 is not needed for advertising because it is a pseudo-interface.</span></span>

<span data-ttu-id="cfa9c-211">Wenn Ihr Computer über zusätzliche Schnittstellen verfügt, sollten Sie auch für die Weiterleitung und Werbung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-211">If your computer has additional interfaces, they should also be configured to be forwarding and advertising.</span></span>

<span data-ttu-id="cfa9c-212">Nach dem Ausführen dieser Befehle konfiguriert das Microsoft IPv6-Protokolladressen an den Schnittstellen \# 3 und \# 4 automatisch mithilfe der entsprechenden Subnetzpräfixe, und die beiden Schnittstellen beginnen mit dem Senden von Routerankündigungen in ungefähr 3 bis 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-212">After running these commands, the Microsoft IPv6 protocol will automatically configure addresses on interfaces \#3 and \#4 using the respective subnet prefixes and the two interfaces will start sending router advertisements at approximately 3 to 10 minute intervals.</span></span>

<span data-ttu-id="cfa9c-213">Hosts, die diese Routerankündigungen empfangen, werden automatisch mit einer Standardroute und einer IPv6-zu-IPv4-Adresse konfiguriert, die aus dem Subnetzpräfix Ihres Links abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-213">Hosts receiving these router advertisements will automatically configure themselves with a default route and a 6to4 address derived from the subnet prefix of their link.</span></span> <span data-ttu-id="cfa9c-214">Die Kommunikation mit anderen IPv6-zu-IPv4-Standorten und dem IPv6-Kern erfolgt über den Gatewaycomputer.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-214">They will have communication to other 6to4 sites and the 6bone through the gateway computer.</span></span>

## <a name="debugging-6to4-configuration"></a><span data-ttu-id="cfa9c-215">Konfiguration von IPv6-zu-IPv4</span><span class="sxs-lookup"><span data-stu-id="cfa9c-215">Debugging 6to4 Configuration</span></span>

<span data-ttu-id="cfa9c-216">**So debuggen Sie die 6zu 4-Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="cfa9c-216">**To debug your 6to4 configuration**</span></span>

1.  <span data-ttu-id="cfa9c-217">Überprüfen Sie die IPv4-Konnektivität mit dem IPv6-zu-IPv4-Relay-Router</span><span class="sxs-lookup"><span data-stu-id="cfa9c-217">Check your IPv4 connectivity to the 6to4 relay router:</span></span>

    <span data-ttu-id="cfa9c-218">**Ping-6to4.IPv6.Microsoft.com**</span><span class="sxs-lookup"><span data-stu-id="cfa9c-218">**ping 6to4.ipv6.microsoft.com**</span></span>

    <span data-ttu-id="cfa9c-219">Wenn dies nicht möglich ist, haben Sie keine globale Internet Verbindung.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-219">If this fails, then you do not have global Internet connectivity.</span></span>

2.  <span data-ttu-id="cfa9c-220">Überprüfen Sie die IPv6-Kapselung mithilfe der automatischen Tunnelung:</span><span class="sxs-lookup"><span data-stu-id="cfa9c-220">Check IPv6 encapsulation by using automatic tunneling:</span></span>

    <span data-ttu-id="cfa9c-221">**ping6 ::131.107.152.32**</span><span class="sxs-lookup"><span data-stu-id="cfa9c-221">**ping6 ::131.107.152.32**</span></span>

    <span data-ttu-id="cfa9c-222">Wenn dies nicht möglich ist, verfügen Sie möglicherweise über eine Firewall oder eine Netzwerk Adressübersetzung (Network Address Translator, NAT) zwischen Ihrem Computer und dem Internet.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-222">If this fails, then you might have a firewall or network address translator (NAT) between your computer and the Internet.</span></span> <span data-ttu-id="cfa9c-223">Wenn dies erfolgreich ist, kann die Internet Verbindung IPv6-zu-IPv4-Unterstützung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-223">If this is successful, then your Internet connection can support 6to4.</span></span>

3.  <span data-ttu-id="cfa9c-224">Überprüfen Sie, ob der Befehl IPv6 RT angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-224">Check the display of the ipv6 rt command.</span></span> <span data-ttu-id="cfa9c-225">Es sollte eine 2002::/16-> 2-Route angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-225">You should see a 2002::/16 -> 2 route.</span></span> <span data-ttu-id="cfa9c-226">Überprüfen Sie die Anzeige des IPv6-Befehls if 2.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-226">Check the display of the ipv6 if 2 command.</span></span> <span data-ttu-id="cfa9c-227">Eine bevorzugte Adresse mit einem Präfix von 2002::/16 sollte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-227">You should see a preferred address with a 2002::/16 prefix.</span></span>

> [!Note]  
> <span data-ttu-id="cfa9c-228">Die IPv4-Adresse des Microsoft IPv6-zu-IPv4-Relay-Routers von 131.107.152.32 unterliegt Änderungen.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-228">The IPv4 address of the Microsoft 6to4 relay router of 131.107.152.32 is subject to change.</span></span> <span data-ttu-id="cfa9c-229">Wenn Schritt 2 oben nicht funktioniert, überprüfen Sie die Ausgabe des Ping-Befehls in Schritt 1, um die IPv4-Adresse des Microsoft IPv6-zu-IPv4-Relay-Routers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cfa9c-229">If Step 2 above does not work, check the output of the ping command in step 1 to verify the IPv4 address of the Microsoft 6to4 relay router.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cfa9c-230">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cfa9c-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfa9c-231">Empfohlene Konfigurationen für IPv6</span><span class="sxs-lookup"><span data-stu-id="cfa9c-231">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> <dt>

[<span data-ttu-id="cfa9c-232">Einzelnes Subnetz mit Link-Local-Adressen</span><span class="sxs-lookup"><span data-stu-id="cfa9c-232">Single subnet with link-local addresses</span></span>](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="cfa9c-233">Verwenden von IPSec zwischen zwei lokalen Verknüpfungs Hosts</span><span class="sxs-lookup"><span data-stu-id="cfa9c-233">Using IPsec between two local link hosts</span></span>](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



