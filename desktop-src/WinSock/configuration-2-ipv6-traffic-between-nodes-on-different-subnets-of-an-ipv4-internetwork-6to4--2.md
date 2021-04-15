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
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a>Konfiguration 2: IPv6-Datenverkehr zwischen Knoten in unterschiedlichen Subnetzen eines IPv4-Netzwerks (6zu 4)

IPv6-zu-IPv4 ist eine Methode zum Verbinden von IPv6-Hosts oder-Standorten über die vorhandene IPv4-Internet Infrastruktur. Dabei wird ein eindeutiges Adress Präfix verwendet, um isolierten IPv6-Standorten ihren eigenen IPv6-Adressraum zuzuweisen. IPv6-zu-IPv4 ist vergleichbar mit einem "Pseudo ISP", der IPv6-Konnektivität bereitstellt. Sie können IPv6-zu-IPv4 für die direkte Kommunikation mit anderen IPv6-zu-IPv4-Standorten verwenden. IPv6-zu-IPv4 erfordert keine Verwendung von IPv6-Routern, und der IPv6-Datenverkehr ist mit einem IPv4-Header gekapselt.

In der folgenden Abbildung wird die Konfiguration von zwei Knoten in separaten Subnetzen mit IPv6-zu-IPv4 für die Kommunikation über einen IPv4-Router veranschaulicht.

![Knoten, die IPv6-zu-IPv4 zum kommunizieren über einen IPv4-Router verwenden.](images/v6mig-2.png)

Die wichtigste Voraussetzung für die Verwendung von 6to4 ist eine Global Routing fähige IPv4-Adresse für Ihre Website. Angenommen, Ihr Standort besteht aus einer Sammlung von IPv6-Computern, die Sie verwalten (einige führen das Microsoft IPv6-Protokoll und einige andere IPv6-Implementierungen aus). Nehmen Sie auch an, dass alle IPv6-Computer direkt über Ethernet oder 6-over-4 angeschlossen sind. Die Global Routing fähige IPv4-Adresse muss einem ihrer Computer zugewiesen werden, auf denen das Microsoft IPv6-Protokoll ausgeführt wird. Dieser Computer ist Ihr IPv6-zu-IPv4-Gateway.

Wenn Sie über eine IPv4-Adresse verfügen, die Teil des privaten Adressraums (10.0.0.0/8, 172.16.0.0/12 oder 192.168.0.0/16) ist, oder den APIPA-Adressraum (Automatic Private IP Address) von 169.254.0.0/16, der von Windows 2000 verwendet wird, ist er nicht global Routing fähig. Andernfalls handelt es sich wahrscheinlich um eine öffentliche IP-Adresse, die Global Routing fähig ist. Weitere Informationen zur Ermittlung, ob Ihre ISP-Verbindung IPv6-zu-IPv4 unterstützt, finden Sie im Thema zum [Debuggen](#debugging-6to4-configuration) von IPv6-zu-IPv4-Konfigurationen

## <a name="the-6to4cfgexe-tool"></a>Das 6to4cfg.exe Tool

Das 6to4cfg.exe Tool automatisiert die IPv6-zu-IPv4-Konfiguration, ermittelt automatisch Ihre Global Routing fähige IPv4-Adresse und erstellt ein IPv6-zu-IPv4-Präfix. Sie führt die Konfiguration entweder direkt aus, oder Sie kann ein Konfigurationsskript schreiben, das Sie später überprüfen und ausführen können.

Die grundlegende 6to4cfg.exe Befehlssyntax lautet wie folgt.

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span id="_filename_"></span><span id="_FILENAME_"></span>\[*Einfügen*\]
</dt> <dd>

Schreibt das Konfigurationsskript in eine Datei, wenn Sie einen Dateinamen angeben. Das Konfigurationsskript verwendet Ipv6.exe.

Sie können con als Dateinamen angeben, um das Konfigurationsskript in die Konsolenausgabe zu schreiben. Dies ist hilfreich, um zu sehen, welche 6to4cfg.exe in einem Testszenario ausgeführt werden.

Wenn Sie keinen Dateinamen angeben, wird von 6to4cfg.exe die IPv6-Konfiguration auf Ihrem Computer direkt aktualisiert.

</dd> <dt>

<span id="-r"></span><span id="-R"></span>-r
</dt> <dd>

Wird zu einem IPv6-zu-IPv4-Gatewayrouter für Ihr lokales Netzwerk, der das Routing an allen Schnittstellen und zugewiesenen Subnetzpräfixen ermöglicht.

</dd> <dt>

<span id="-s"></span><span id="-S"></span>-s
</dt> <dd>

Ermöglicht die Standort lokale Adressierung an Ihrem IPv6-zu-IPv4-Standort. Dieser Befehl ist nur nützlich, wenn er in Verbindung mit-r verwendet wird.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>-u
</dt> <dd>

Gibt an, dass die IPv6-zu-IPv4-Konfiguration umgekehrt wird. Aus diesem Grund kehrt IPv6-zu-4cfg-u die Auswirkung von 6um4cfg zurück, und 6um4cfg-r-u kehrt die Auswirkung von 6zu 4cfg-r um usw. um.

</dd> <dt>

<span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *Relay*
</dt> <dd>

Gibt den Namen oder die IPv4-Adresse eines IPv6-zu-IPv4-Relay-Routers an. Der Standardname ist 6to4.IPv6.Microsoft.com, der IPv6-zu-IPv4-Relayrouter im Internet.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>-b
</dt> <dd>

Gibt an, dass 6to4cfg.exe anstelle des ersten die "beste" relayadresse auswählt.

</dd> <dt>

<span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S- *Adresse*
</dt> <dd>

Gibt die lokale IPv4-Adresse für das IPv6-zu-IPv4-Präfix an.

</dd> </dl>

## <a name="manual-6to4-configuration"></a>Manuelle IPv6-zu-IPv4-Konfiguration

In diesem Beispiel lautet die Adresse des IPv6-zu-IPv4-Gateways 172.31.42.239. Sie benötigen eine eigene Global Routing fähige IPv4-Adresse für die Verwendung von 6zu 4.

> [!Note]  
> Die IP-Adresse 172.31.42.239 wird nur zu Beispiel Zwecken verwendet. Dies ist eine private Adresse, die im Internet nicht global Routing fähig ist.

 

Die 32-Bit-Global Routing fähige IPv4-Adresse wird mit dem 16-Bit-Präfix 2002::/16 kombiniert, um ein 48-Bit-IPv6-Adress Präfix für Ihre Website zu bilden. In diesem Beispiel ist das IPv6-zu-IPv4-Site Präfix 2002: ac1f: 2aef::/48. Beachten Sie, dass ac1f: 2aef die hexadezimale Codierung von 172.31.42.239 ist (natürlich verwenden Sie ein anderes Präfix basierend auf Ihrer eigenen Global Routing fähigen IPv4-Adresse). Mit dem IPv6-zu-IPv4-Site Präfix können Sie Adressen und Subnetzpräfixe innerhalb Ihrer Website zuweisen.

In diesem Beispiel wird davon ausgegangen, dass Sie Subnetz 0 zum manuellen Konfigurieren einer IPv6-zu-IPv4-Adresse auf dem IPv6-zu-IPv4-Gatewaycomputer verwenden und dass Sie Subnetz 1 zum automatischen Konfigurieren von Adressen in Ihrem Ethernet-Netzwerksegment verwenden. Es können jedoch auch andere Optionen ausgewählt werden.

1.  Verwenden Sie Ipv6.exe zum Aktivieren von IPv6-zu-IPv4 auf dem IPv6-zu-IPv4-Gatewaycomputer

    **IPv6-RTU 2002::/16 2**

    Der **IPv6-RTU** -Befehl führt ein Update für eine Routing Tabelle aus. Sie kann verwendet werden, um eine Route hinzuzufügen, zu entfernen oder zu aktualisieren. In diesem Fall wird IPv6-zu-IPv4 aktiviert.

    Das 2002::/16-Argument ist das Präfix der Route, das das eindeutige IPv6-zu-IPv4-Präfix angibt.

    Das 2-Argument gibt die on-Link-Schnittstelle für dieses Präfix an. Schnittstelle \# 2 ist die "Pseudo Schnittstelle", die für konfigurierte Tunnel, automatische Tunnelung und 6to4 verwendet wird. Wenn eine IPv6-Zieladresse mit dem Präfix 2002::/16 übereinstimmt, werden die 32 Bits, die dem Präfix in der Zieladresse folgen, extrahiert, um eine IPv4-Zieladresse zu bilden. Das Paket ist mit einem IPv4-Header gekapselt und an die IPv4-Zieladresse gesendet.

2.  Konfigurieren einer IPv6-zu-IPv4-Adresse auf dem IPv6-zu-IPv4-Gatewaycomputer

    **IPv6 Adu 2/2002: ac1f: 2aef:: ac1f: 2aef**

    Der **IPv6 Adu** -Befehl führt ein Adress Update durch. Sie kann verwendet werden, um eine Adresse für eine Schnittstelle hinzuzufügen, zu entfernen oder zu aktualisieren. In dieser Instanz wird die IPv6-zu-IPv4-Adresse des Computers konfiguriert.

    Das Argument 2/2002: ac1f: 2aef:: ac1f: 2aef gibt sowohl die-Schnittstelle als auch die-Adresse an. Hierfür muss address 2002: ac1f: 2aef:: ac1f: 2aef für Schnittstelle \# 2 konfiguriert werden. Die Adresse wird mit dem Website Präfix 2002 erstellt: ac1f: 2aef::/48, Subnetz 0 zum Angeben eines Subnetzpräfixes 2002: ac1f: 2aef::/64 und eines 64-Bit-Schnittstellen Bezeichners. In der dargestellten Konvention wird die IPv4-Adresse des Computers für den Schnittstellen Bezeichner für Adressen verwendet, die Schnittstelle 2 zugewiesen sind \# . Ac1f: 2aef sollte für ihre Verwendung durch die hexadezimale Codierung Ihrer eigenen Global Routing fähigen IPv4-Adresse ersetzt werden.

Die zwei vorherigen Befehle sind ausreichend, um die Kommunikation mit anderen IPv6-zu-IPv4-Standorten zuzulassen. Sie können z. b. versuchen, die Microsoft IPv6-zu-IPv4-Website zu pingen:

**ping6 2002:836b: 9820:: 836b: 9820**

Um die Kommunikation mit dem 6bone zu ermöglichen, müssen Sie einen konfigurierten Standard Tunnel zu einem IPv6-zu-IPv4-Relay erstellen. Sie können den Microsoft IPv6-zu-IPv4-Relay-Router verwenden, 131.107.152.32:

**IPv6-RTU::/0 2/:: 131.107.152.32 pub Life 1800**

Der **IPv6-RTU** -Befehl führt eine Routing Tabellen Aktualisierung durch, wobei in dieser Instanz eine Standardroute zum IPv6-zu-IPv4-Relay festgelegt wird.

Das Argument::/0 ist das Routen Präfix. Das Präfix mit der Länge 0 gibt an, dass es sich um eine Standardroute handelt.

Das Argument 2/:: 131.107.152.32 gibt den nächsten Hop-Nachbar für dieses Präfix an. Es erfordert, dass Pakete, die mit dem Präfix übereinstimmen, mit Schnittstelle 2 an address:: 131.107.152.32 \# Das Weiterleiten eines Pakets an:: 131.107.152.32 an Schnittstelle \# 2 bewirkt, dass es mit einem V4-Header gekapselt und an 131.107.152.32 gesendet wird.

Das Pub-Argument macht dies zu einer veröffentlichten Route. Da dies nur für Router relevant ist, hat es keine Auswirkung, bis das Routing aktiviert ist. Ebenso gilt die 30-minütige Lebensdauer nur, wenn das Routing aktiviert ist.

Sie sollten in der Lage sein, auf 6bone-Websites und IPv6-zu-IPv4-Standorte zuzugreifen. Sie können den folgenden Befehl verwenden, um dies zu testen:

**ping6 3FFE: 1cff: 0: F5:: 1**

Der letzte Schritt besteht darin, das Routing auf dem IPv6-zu-IPv4-Gateway zu aktivieren. In diesem Beispiel wird davon ausgegangen, dass die Schnittstelle \# 3 auf Ihrem Gatewaycomputer eine Ethernet-Schnittstelle und Schnittstelle \# 4 6-over-4 ist. Der Computer kann seine Schnittstellen unterschiedlich unterscheiden. Mit den folgenden beiden Befehlen werden den beiden Verknüpfungen Subnetzpräfixe zugewiesen. Die Subnetzpräfixe werden aus dem IPv6-zu-IPv4-Präfix 2002 von der Site abgeleitet: ac1f: 2aef::/48:

**IPv6-RTU 2002: ac1f: 2aef: 1::/64 3 pub Life 1800**

**IPv6-RTU 2002: ac1f: 2aef: 2::/64 4 pub Life 1800**

Der **IPv6-RTU** -Befehl gibt an, dass das Präfix 2002: ac1f: 2aef: 1::/64 mit Schnittstelle 3 verknüpft ist \# . Es konfiguriert das erste Subnetzpräfix in der Ethernet-Schnittstelle. Die Route wird mit einer Lebensdauer von 30 Minuten veröffentlicht.

Entsprechend wird das Präfix 2002: ac1f: 2aef: 2::/64 in der 6-over-4-Schnittstelle konfiguriert.

Mit den nächsten drei Befehlen kann der IPv6-zu-IPv4-Gatewaycomputer als Router fungieren:

**IPv6-IFC 2-FORW**

**IPv6-IP3-FORW-ADV**

**IPv6-IP4-FORW-ADV**

Mit dem IPv6-Befehl " **IFC** " werden Attribute einer Schnittstelle gesteuert. Ein Router leitet Pakete weiter und sendet Routerankündigungen. In der Microsoft IPv6-Implementierung werden diese schnittstellenspezifischen Attribute separat gesteuert.

Schnittstelle \# 2 ist für Werbung nicht erforderlich, da es sich um eine Pseudo Schnittstelle handelt.

Wenn Ihr Computer über zusätzliche Schnittstellen verfügt, sollten Sie auch für die Weiterleitung und Werbung konfiguriert werden.

Nach dem Ausführen dieser Befehle konfiguriert das Microsoft IPv6-Protokolladressen an den Schnittstellen \# 3 und \# 4 automatisch mithilfe der entsprechenden Subnetzpräfixe, und die beiden Schnittstellen beginnen mit dem Senden von Routerankündigungen in ungefähr 3 bis 10 Minuten.

Hosts, die diese Routerankündigungen empfangen, werden automatisch mit einer Standardroute und einer IPv6-zu-IPv4-Adresse konfiguriert, die aus dem Subnetzpräfix Ihres Links abgeleitet ist. Die Kommunikation mit anderen IPv6-zu-IPv4-Standorten und dem IPv6-Kern erfolgt über den Gatewaycomputer.

## <a name="debugging-6to4-configuration"></a>Konfiguration von IPv6-zu-IPv4

**So debuggen Sie die 6zu 4-Konfiguration**

1.  Überprüfen Sie die IPv4-Konnektivität mit dem IPv6-zu-IPv4-Relay-Router

    **Ping-6to4.IPv6.Microsoft.com**

    Wenn dies nicht möglich ist, haben Sie keine globale Internet Verbindung.

2.  Überprüfen Sie die IPv6-Kapselung mithilfe der automatischen Tunnelung:

    **ping6 ::131.107.152.32**

    Wenn dies nicht möglich ist, verfügen Sie möglicherweise über eine Firewall oder eine Netzwerk Adressübersetzung (Network Address Translator, NAT) zwischen Ihrem Computer und dem Internet. Wenn dies erfolgreich ist, kann die Internet Verbindung IPv6-zu-IPv4-Unterstützung unterstützen.

3.  Überprüfen Sie, ob der Befehl IPv6 RT angezeigt wird. Es sollte eine 2002::/16-> 2-Route angezeigt werden. Überprüfen Sie die Anzeige des IPv6-Befehls if 2. Eine bevorzugte Adresse mit einem Präfix von 2002::/16 sollte angezeigt werden.

> [!Note]  
> Die IPv4-Adresse des Microsoft IPv6-zu-IPv4-Relay-Routers von 131.107.152.32 unterliegt Änderungen. Wenn Schritt 2 oben nicht funktioniert, überprüfen Sie die Ausgabe des Ping-Befehls in Schritt 1, um die IPv4-Adresse des Microsoft IPv6-zu-IPv4-Relay-Routers zu überprüfen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Empfohlene Konfigurationen für IPv6](recommended-configurations-2.md)
</dt> <dt>

[Einzelnes Subnetz mit Link-Local-Adressen](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Verwenden von IPSec zwischen zwei lokalen Verknüpfungs Hosts](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



