---
description: 6to4 ist eine Methode zum Verbinden von IPv6-Hosts oder -Standorten über die vorhandene IPv4-Internetinfrastruktur.
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: 'Konfiguration 2: IPv6-Datenverkehr zwischen Knoten in verschiedenen Subnetzen eines IPv4-Internetwork (6to4)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d976aa3ea21d990ea22f861fbf05a816866e6b0d21502211e23a0e331a2f851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112500"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a>Konfiguration 2: IPv6-Datenverkehr zwischen Knoten in verschiedenen Subnetzen eines IPv4-Internetwork (6to4)

6to4 ist eine Methode zum Verbinden von IPv6-Hosts oder -Standorten über die vorhandene IPv4-Internetinfrastruktur. Es verwendet ein eindeutiges Adresspräfix, um isolierten IPv6-Standorten einen eigenen IPv6-Adressraum zu geben. 6to4 ist wie ein "Pseudo-ISP", der IPv6-Konnektivität bietet. Sie können 6to4 verwenden, um direkt mit anderen 6to4-Standorten zu kommunizieren. 6to4 erfordert nicht die Verwendung von IPv6-Routern, und der IPv6-Datenverkehr wird mit einem IPv4-Header gekapselt.

Die folgende Abbildung zeigt die Konfiguration von zwei Knoten in separaten Subnetzen mit 6to4 für die Kommunikation über einen IPv4-Router.

![Knoten, die 6to4 für die Kommunikation über einen ipv4-Router verwenden.](images/v6mig-2.png)

Die Hauptanforderung für die Verwendung von 6to4 ist eine global routingfähige IPv4-Adresse für Ihren Standort. Angenommen, Ihr Standort besteht aus einer Sammlung von IPv6-Computern, die Sie verwalten (einige mit dem Microsoft IPv6-Protokoll und andere mit anderen IPv6-Implementierungen). Angenommen, alle IPv6-Computer sind direkt über Ethernet oder 6-over-4 verbunden. Die global routingfähige IPv4-Adresse muss einem Ihrer Computer zugewiesen werden, auf denen das Microsoft IPv6-Protokoll ausgeführt wird. Dieser Computer ist Ihr 6to4-Gateway.

Wenn Sie über eine IPv4-Adresse verfügen, die Teil des privaten Adressraums ist (10.0.0.0/8, 172.16.0.0/12 oder 192.168.0.0/16) oder der von Windows 2000 verwendete APIPA-Adressraum (Automatic Private IP Addressing, automatische private IP-Adressierung) von 169.254.0.0/16 ist nicht global routingfähig. Andernfalls handelt es sich wahrscheinlich um eine öffentliche IP-Adresse und ist global routingfähig. Weitere Informationen zum Bestimmen, ob Ihre ISP-Verbindung 6to4 unterstützt, finden Sie im Thema Debuggen der [6to4-Konfiguration](#debugging-6to4-configuration) in diesem Dokument.

## <a name="the-6to4cfgexe-tool"></a>Das 6to4cfg.exe Tool

Das 6to4cfg.exe-Tool automatisiert die 6to4-Konfiguration, erkennt automatisch Ihre global routingfähige IPv4-Adresse und erstellt ein 6to4-Präfix. Die Konfiguration wird entweder direkt ausgeführt, oder sie kann ein Konfigurationsskript schreiben, das Sie später überprüfen und ausführen können.

Die grundlegende 6to4cfg.exe befehlssyntax lautet wie folgt.

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span id="_filename_"></span><span id="_FILENAME_"></span>\[*Dateiname*\]
</dt> <dd>

Schreibt das Konfigurationsskript in eine Datei, wenn Sie einen Dateinamen angeben. Das Konfigurationsskript verwendet Ipv6.exe.

Sie können con für den Dateinamen angeben, um das Konfigurationsskript in die Konsolenausgabe zu schreiben. Dies ist hilfreich, um zu sehen, welche 6to4cfg.exe in einem Testszenario ausführen.

Wenn Sie keinen Dateinamen angeben, wird 6to4cfg.exe IPv6-Konfiguration direkt auf Ihrem Computer aktualisiert.

</dd> <dt>

<span id="-r"></span><span id="-R"></span>-r
</dt> <dd>

Wird zu einem 6:4-Gatewayrouter für Ihr lokales Netzwerk und ermöglicht das Routing für alle Ihre Schnittstellen und zugewiesenen Subnetzpräfixe.

</dd> <dt>

<span id="-s"></span><span id="-S"></span>-s
</dt> <dd>

Aktiviert die standortbasierte Adressierung an Ihrem 6to4-Standort. Dieser Befehl ist nur nützlich, wenn er in Verbindung mit -r verwendet wird.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>-u
</dt> <dd>

Gibt an, dass die 6to4-Konfiguration umgekehrt wird. Daher kehrt 6to4cfg -u den Effekt von 6to4cfg um, und 6to4cfg -r -u kehrt den Effekt von 6to4cfg -r um und so weiter.

</dd> <dt>

<span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *Relay*
</dt> <dd>

Gibt den Namen oder die IPv4-Adresse eines 6to4-Relayrouters an. Der Standardname ist 6to4.ipv6.microsoft.com, der 6to4-Relayrouter im Internet.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>-b
</dt> <dd>

Gibt an, 6to4cfg.exe die "beste" Relayadresse anstelle der ersten auswählt.

</dd> <dt>

<span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>*-S-Adresse*
</dt> <dd>

Gibt die lokale IPv4-Adresse für das Präfix 6to4 an.

</dd> </dl>

## <a name="manual-6to4-configuration"></a>Manuelle 6-zu-4-Konfiguration

In diesem Beispiel ist die Adresse des 6to4-Gateways 172.31.42.239. Sie benötigen Ihre eigene global routingfähige IPv4-Adresse, um 6to4 verwenden zu können.

> [!Note]  
> Die IP-Adresse 172.31.42.239 dient nur zu Beispielzwecken. Dies ist eine private Adresse und im Internet nicht global routingfähig.

 

Die global routingfähige 32-Bit-IPv4-Adresse wird mit dem 16-Bit-Präfix 2002::/16 kombiniert, um ein 48-Bit-IPv6-Adresspräfix für Ihren Standort zu bilden. In diesem Beispiel ist das 6to4-Standortpräfix 2002:ac1f:2aef::/48. Beachten Sie, dass ac1f:2aef die hexadezimale Codierung von 172.31.42.239 ist (natürlich verwenden Sie ein anderes Präfix basierend auf Ihrer eigenen global routingbaren IPv4-Adresse). Mit dem 6to4-Standortpräfix können Sie Adressen und Subnetzpräfixe innerhalb Ihres Standorts zuweisen.

In diesem Beispiel wird davon ausgegangen, dass Sie das Subnetz 0 zum manuellen Konfigurieren einer 6to4-Adresse auf Ihrem 6to4-Gatewaycomputer verwenden und dass Sie Subnetz 1 zum automatischen Konfigurieren von Adressen in Ihrem Ethernet-Netzwerksegment verwenden. Es sind jedoch andere Optionen möglich.

1.  Verwenden Ipv6.exe, um 6to4 auf Ihrem 6to4-Gatewaycomputer zu aktivieren:

    **ipv6 rtu 2002::/16 2**

    Mit **dem Befehl ipv6 rtu** wird eine Routingtabelle aktualisiert. Sie kann verwendet werden, um eine Route hinzuzufügen, zu entfernen oder zu aktualisieren. In diesem Fall wird "6to4" ermöglicht.

    Das Argument 2002::/16 ist das Präfix der Route und gibt das eindeutige Präfix 6to4 an.

    Das 2-Argument gibt die On-Link-Schnittstelle für dieses Präfix an. Schnittstelle 2 ist die "Pseudoschnittstelle", die für konfigurierte \# Tunnel, automatisches Tunneling und 6:4 verwendet wird. Wenn eine IPv6-Zieladresse dem Präfix 2002::/16 entspricht, werden die 32 Bits, die dem Präfix in der Zieladresse folgen, extrahiert, um eine IPv4-Zieladresse zu bilden. Das Paket wird mit einem IPv4-Header gekapselt und an die IPv4-Zieladresse gesendet.

2.  Konfigurieren Sie eine 6to4-Adresse auf Ihrem 6to4-Gatewaycomputer:

    **ipv6 adu 2/2002:ac1f:2aef::ac1f:2aef**

    Der **Befehl ipv6 adu** führt eine Adressaktualisierung durch. Sie kann verwendet werden, um eine Adresse auf einer Schnittstelle hinzuzufügen, zu entfernen oder zu aktualisieren. In diesem Fall wird die 6to4-Adresse des Computers konfiguriert.

    Das Argument 2/2002:ac1f:2aef::ac1f:2aef gibt sowohl die Schnittstelle als auch die Adresse an. Sie erfordert die Konfiguration der Adresse 2002:ac1f:2aef::ac1f:2aef auf Schnittstelle \# 2. Die Adresse wird mit dem Standortpräfix 2002:ac1f:2aef::/48, dem Subnetz 0 erstellt, um das Subnetzpräfix 2002:ac1f:2aef::/64 und einen 64-Bit-Schnittstellenbezeichner zu geben. Die gezeigte Konvention verwendet die IPv4-Adresse des Computers für den Schnittstellenbezeichner für Adressen, die Schnittstelle \# 2 zugewiesen sind. Für Ihre Verwendung sollte ac1f:2aef durch die hexadezimale Codierung Ihrer eigenen global routingbaren IPv4-Adresse ersetzt werden.

Die beiden vorangehenden Befehle sind ausreichend, um die Kommunikation mit anderen 6to4-Standorten zu ermöglichen. Sie können beispielsweise versuchen, die Microsoft 6to4-Website zu pingen:

**ping6 2002:836b:9820::836b:9820**

Um die Kommunikation mit 6bone zu ermöglichen, müssen Sie einen standardmäßig konfigurierten Tunnel zu einem 6to4-Relay erstellen. Sie können den Microsoft 6to4-Relayrouter 131.107.152.32 verwenden:

**ipv6 rtu ::/0 2/::131.107.152.32 pub life 1800**

Der **Befehl ipv6 rtu führt** eine Routingtabellenaktualisierung durch und erstellt in diesem Fall eine Standardroute zum 6to4-Relay.

Das Argument ::/0 ist das Routenpräfix. Das Präfix der Länge 0 (null) gibt an, dass es sich um eine Standardroute handelt.

Das Argument 2/::131.107.152.32 gibt den Nächsten-Hop-Nachbarn für dieses Präfix an. Es ist erforderlich, dass Pakete, die mit dem Präfix übereinstimmen, mithilfe von Schnittstelle 2 an die Adresse ::131.107.152.32 weitergeleitet \# werden. Die Weiterleitung eines Pakets an ::131.107.152.32 an Schnittstelle 2 bewirkt, dass es mit einem v4-Header gekapselt und an \# 131.107.152.32 gesendet wird.

Das Pub-Argument macht dies zu einer veröffentlichten Route. Da dies nur für Router relevant ist, hat dies keine Auswirkungen, bis das Routing aktiviert ist. Ebenso gilt die Gültigkeitsdauer von 30 Minuten nur, wenn das Routing aktiviert ist.

Sie sollten auf 6bone-Websites sowie auf 6to4-Websites zugreifen können. Sie können den folgenden Befehl verwenden, um dies zu testen:

**ping6 3ffe:1cff:0:f5::1**

Der letzte Schritt besteht im Aktivieren des Routings auf Ihrem 6to4-Gateway. In diesem Beispiel wird davon ausgegangen, dass Schnittstelle 3 auf Ihrem Gatewaycomputer eine Ethernet-Schnittstelle und Schnittstelle \# \# 4 6-über-4 ist. Die Schnittstellen des Computers werden möglicherweise anders nummert. Die folgenden beiden Befehle weisen den beiden Links Subnetzpräfixe zu. Die Subnetzpräfixe werden vom 6to4-Präfix 2002:ac1f:2aef::/48 des Standorts abgeleitet:

**ipv6 rtu 2002:ac1f:2aef:1::/64 3 pub life 1800**

**ipv6 rtu 2002:ac1f:2aef:2::/64 4 pub life 1800**

Der **Befehl ipv6 rtu** gibt an, dass das Präfix 2002:ac1f:2aef:1::/64 über einen Link zur Schnittstelle \# 3 steht. Es konfiguriert das erste Subnetzpräfix auf der Ethernet-Schnittstelle. Die Route wird mit einer Lebensdauer von 30 Minuten veröffentlicht.

Ebenso wird das Präfix 2002:ac1f:2aef:2::/64 für die 6-over-4-Schnittstelle konfiguriert.

Mit den nächsten drei Befehlen kann der 6to4-Gatewaycomputer als Router fungieren:

**ipv6 ifc 2 forw**

**ipv6 ifc 3 forw adv**

**ipv6 ifc 4 forw adv**

Der **ifc-Befehl ipv6** steuert Attribute einer Schnittstelle. Ein Router leitet Pakete weiter und sendet Routerankündigungen. In der Microsoft IPv6-Implementierung werden diese Schnittstellenattribute separat gesteuert.

Schnittstelle \# 2 ist für die Ankündigung nicht erforderlich, da es sich um eine Pseudoschnittstelle handelt.

Wenn Ihr Computer über zusätzliche Schnittstellen verfügt, sollten sie auch für weiterleitung und Werbung konfiguriert werden.

Nach dem Ausführen dieser Befehle konfiguriert das Microsoft IPv6-Protokoll automatisch Adressen für die Schnittstellen \# 3 und \# 4 mit den jeweiligen Subnetzpräfixen, und die beiden Schnittstellen beginnen in etwa 3 bis 10 Minuten mit dem Senden von Routerankündigungen.

Hosts, die diese Routerankündigungen erhalten, konfigurieren sich automatisch mit einer Standardroute und einer 6:4-Adresse, die vom Subnetzpräfix ihrer Verknüpfung abgeleitet wird. Sie verfügen über eine Kommunikation mit anderen 6to4-Standorten und dem 6-Bone über den Gatewaycomputer.

## <a name="debugging-6to4-configuration"></a>Debuggen der 6to4-Konfiguration

**So debuggen Sie Ihre 6to4-Konfiguration**

1.  Überprüfen Sie ihre IPv4-Konnektivität mit dem 6to4-Relayrouter:

    **ping 6to4.ipv6.microsoft.com**

    Wenn dies fehlschlägt, verfügen Sie nicht über eine globale Internetverbindung.

2.  Überprüfen Sie die IPv6-Kapselung mit automatischer Tunnelung:

    **ping6 ::131.107.152.32**

    Wenn dies fehlschlägt, verfügen Sie möglicherweise über eine Firewall oder NAT (Network Address Translator) zwischen Ihrem Computer und dem Internet. Wenn dies erfolgreich ist, kann Ihre Internetverbindung 6to4 unterstützen.

3.  Überprüfen Sie die Anzeige des Befehls ipv6 rt. Es sollte die Route 2002::/16 -> 2 angezeigt werden. Überprüfen Sie die Anzeige des Befehls ipv6 if 2. Es sollte eine bevorzugte Adresse mit dem Präfix 2002::/16 angezeigt werden.

> [!Note]  
> Die IPv4-Adresse des Microsoft 6to4-Relayrouters 131.107.152.32 kann geändert werden. Wenn Schritt 2 oben nicht funktioniert, überprüfen Sie die Ausgabe des Ping-Befehls in Schritt 1, um die IPv4-Adresse des Microsoft 6to4-Relayrouters zu überprüfen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Empfohlene Konfigurationen für IPv6](recommended-configurations-2.md)
</dt> <dt>

[Einzelnes Subnetz mit lokalen Linkadressen](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Verwenden von IPsec zwischen zwei lokalen Linkhosts](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



