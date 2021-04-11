---
description: In diesem Thema wird die von WSDAPI implementierte Ermittlungs Funktionalität beschrieben, die in den DPWS-oder WS-Discovery Spezifikationen jedoch nicht anderweitig beschrieben wird.
ms.assetid: ae7eff53-c932-4cba-9e71-c60f308f0e2d
title: Zusätzliche WS-Discovery Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9856605273bec9c757e0b29c389991bf061309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217742"
---
# <a name="additional-ws-discovery-functionality"></a>Zusätzliche WS-Discovery Funktionen

In einigen Fällen definieren das [Geräte Profil für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) und verwandte Spezifikationen nicht explizit die Implementierungs Funktionalität. Die [WS-Discovery-](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) Spezifikation definiert z. b. kein Client-und Host Verhalten in Umgebungen mit mehreren Umgebungen. Wenn WSDAPI implementiert wurde, wurden einige Ermittlungs Funktionen über die in der Spezifikation definierten Funktionen hinaus erweitert.

WSDAPI implementiert auch ausgewählte Teile von WS-Discovery v 1.1 CD1 für die Kommunikation mit einem suchproxy über http.

In diesem Thema wird die von WSDAPI implementierte Ermittlungs Funktionalität beschrieben, die in den DPWS-oder WS-Discovery Spezifikationen jedoch nicht anderweitig beschrieben wird.

## <a name="ipv6-addresses-and-the-soapudp-uri-format"></a>IPv6-Adressen und das SOAP. UDP-URI-Format

SOAP-Over-UDP und WS-Discovery beschreiben nicht explizit, wie eine literale IPv6-Adresse im SOAP. UDP-URI-Format dargestellt wird. [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt)mit dem Titel "Uniform Resource Identifier (URI): generische Syntax" gibt an, dass literale IPv6-Adressen nicht vom SOAP. UDP-URI-Format unterstützt werden.

Der Einfachheit halber erkennt WSDAPI IPv6-Adressen, die in eckigen Klammern im SOAP. UDP-Schema enthalten sind. Beispielsweise wird die Adresse `soap.udp://[2001:abcd:0001:0002:0003:0004:0005:0032]:3702` von WSDAPI erkannt. Dies ähnelt der Art und Weise, wie IPv6-Adressen in http behandelt werden.

## <a name="hello-and-xaddrs"></a>Hello und xaddrs

Das DPWS-hostingobjekt von WSDAPI sendet nie eine WS-Discovery [Hello](hello-message.md) -Nachricht mit [xaddrs](xaddr-validation-rules.md) im Nachrichtentext. Ein Client sendet nach dem Empfang einer Hello-Nachricht immer eine [Resolve](resolve-message.md) -Nachricht, wenn der Client die xaddrs erhalten muss.

Dieser Ansatz bietet zwei Vorteile. Zuerst macht ein auf WSDAPI aufgebautes Gerät niemals xaddrs verfügbar, die die IP-Adressen privater Netzwerke offenlegen. Zweitens macht ein auf WSDAPI erstelltes Gerät nur xaddrs verfügbar, auf die der Client zugreifen kann. Dies bedeutet, dass IPv6-Adressen nie an einen IPv4-Client gesendet werden.

Wenn eine Test-oder Auflösungs Meldung empfangen wird, wird [nur eine einzige](probe-message.md) xaddr als Antwort gesendet. Die gesendete xaddr entspricht der lokalen Adresse, an der die Anforderung empfangen wurde. Wenn die Anforderung über IPv6 über Subnetze empfangen wurde, stellt WSDAPI in der Antwort eine globale IPv6-Adresse bereit.

## <a name="preferred-addresses"></a>Bevorzugte Adressen

Ein Gerät kann mehrere xaddrs in einer [Hello](hello-message.md)-, [Probe Match](probematches-message.md)-oder [resolvematch](resolvematches-message.md) -Nachricht bereitstellen. Ein Dienst kann auch an mehreren Endpunkten mit unterschiedlichen Transport Adressen verfügbar sein. In diesen Fällen versucht WSDAPI, mit dem Gerät auf der ersten verwendbaren Adresse zu kommunizieren, die es findet. Eine Adresse kann verwendet werden, wenn Sie aus einem verfügbaren Protokoll besteht, z. b. IPv4 auf einem Computer, auf dem IPv4 installiert ist, oder IPv6 auf einem Computer, auf dem IPv6 installiert ist. Wenn die Adresse von einem Gerät oder Dienst stammt, das sich nicht im lokalen Subnetz befindet, kann Sie außerdem nur verwendet werden, wenn es sich um IPv4, IPv6-Standort lokal oder IPv6-Link Local handelt.

## <a name="wsdl-in-metadata-exchange"></a>WSDL im Metadatenaustausch

Geräte und Dienste, die auf WSDAPI basieren, stellen Ihre WSDL nicht im Metadatenaustausch bereit, es sei denn, Sie werden von der Anwendung erweitert, um diese Informationen Standardmäßig ist die WSDL-Bereitstellung nicht Teil des Programmiermodells.

## <a name="app_max_delay"></a>maximale APP- \_ \_ Verzögerung

DPWS definiert APP- \_ Maximale \_ Verzögerung, das zufällige Intervall, das für den [](probe-message.md) Empfang eines Tests und das Senden eines [Probe Matches](probematches-message.md)als 5.000 Millisekunden verzögert werden soll. Die Windows-Firewall erfordert, dass das Multicast-Anforderungs-/Unicast-Antwortmodell für UDP nur innerhalb des vier Sekunden-firewallfensters funktioniert. Das Ergebnis ist, dass WSDAPI Antworten in 2.500 ms oder weniger übermittelt, anstelle des Fensters 5.000 ms, das durch maximale Verzögerung der APP beschrieben wird \_ \_ .

## <a name="iana-port-reservations"></a>IANA-Port Reservierungen

WSDAPI verwendet standardmäßig den TCP-Port 5357 für HTTP-Datenverkehr und den TCP-Port 5358 für HTTPS-Datenverkehr. Diese Ports sind für Prozesse mit niedrigerer Berechtigung über eine URL-Reservierung in HTTP.sys reserviert und auch für IANA reserviert.

## <a name="udp-port-sharing"></a>UDP-Port Freigabe

WSDAPI verwendet die Port Freigabe. An den Port 3702 gesendete Unicastnachrichten werden möglicherweise nicht von allen WSDAPI-basierten Anwendungen verarbeitet. Wenn eine Anwendung ausschließlich an Port 3702 gebunden wird, kann es sein, dass WSDAPI-basierte Anwendungen diesen Port nicht ordnungsgemäß verwenden.

## <a name="ws-discovery-v11-cd1-proxy"></a>WS-Discovery v 1.1 CD1 Proxy

WSDAPI sucht nach einem suchproxy, der das WS-Discovery v 1.1 CD1 Managed Mode-Protokoll implementiert, und kommuniziert damit. WS-Discovery v 1.1 CD1 ist die erste Revision von WS-Discovery, die eine explizite Beschreibung eines HTTP-Protokolls für die Kommunikation zwischen einem Proxy und einem Client oder Gerät einschließt.

Um die Anzahl der in Multicast Anforderungen verwendeten gleichzeitigen Versionen einzuschränken, sendet WSDAPI eine WS-Discovery Test Anforderung im Namespace 2005/04, sucht jedoch nach dem Typ WS-Discovery v 1.1 CD1 DiscoveryProxy. Wenn ein Proxy antwortet, sendet der WSDAPI einen HTTP-Test oder eine Auflösungs Anforderung an den angegebenen Proxy Endpunkt, wie in WS-Discovery v 1.1 CD1 definiert.

 

 



