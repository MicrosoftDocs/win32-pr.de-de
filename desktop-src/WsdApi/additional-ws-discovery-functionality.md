---
description: Der Zweck dieses Themas besteht darin, die von WSDAPI implementierte Ermittlungsfunktionalität zu beschreiben, aber nicht anderweitig in den DPWS- oder WS-Discovery-Spezifikationen beschrieben.
ms.assetid: ae7eff53-c932-4cba-9e71-c60f308f0e2d
title: Zusätzliche WS-Discovery-Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7ee4094950c51ed84724abb9eaea493f7dad7cf7803832fb6e8762fdd99811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106778"
---
# <a name="additional-ws-discovery-functionality"></a>Zusätzliche WS-Discovery-Funktionalität

In einigen Fällen definieren das [Geräteprofil für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) und die zugehörigen Spezifikationen die Implementierungsfunktionalität nicht explizit. Beispielsweise definiert die [WS-Discovery-Spezifikation](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) das Client- und Hostverhalten in Umgebungen mit mehreren Startumgebungen nicht. Bei der Implementierung von WSDAPI wurden einige Ermittlungsfunktionen über die in der Spezifikation definierte Funktionalität hinaus hinzugefügt.

WSDAPI implementiert auch ausgewählte Teile von WS-Discovery v1.1 CD1 für die Kommunikation mit einem Ermittlungsproxy über HTTP.

Der Zweck dieses Themas besteht darin, die von WSDAPI implementierte Ermittlungsfunktionalität zu beschreiben, aber nicht anderweitig in den DPWS- oder WS-Discovery-Spezifikationen beschrieben.

## <a name="ipv6-addresses-and-the-soapudp-uri-format"></a>IPv6-Adressen und das soap.udp-URI-Format

SOAP-over-UDP und WS-Discovery beschreiben nicht explizit, wie eine literale IPv6-Adresse im soap.udp-URI-Format dargestellt wird. [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt)mit dem Titel "Uniform Resource Identifiers (URI): Generic Syntax" gibt an, dass literale IPv6-Adressen vom soap.udp-URI-Format nicht unterstützt werden.

Der Einfachheit halber erkennt WSDAPI IPv6-Adressen, die in eckige Klammern im soap.udp-Schema eingeschlossen sind. Beispielsweise wird die Adresse `soap.udp://[2001:abcd:0001:0002:0003:0004:0005:0032]:3702` von WSDAPI erkannt. Dies ähnelt der Behandlung von IPv6-Adressen in HTTP.

## <a name="hello-and-xaddrs"></a>Hello und XAddrs

Das DPWS-Hostingobjekt von WSDAPI sendet niemals eine WS-Discovery [Hello-Nachricht](hello-message.md) mit [XAddrs](xaddr-validation-rules.md) im Nachrichtentext. Ein Client sendet [](resolve-message.md) nach dem Empfang einer Hello-Nachricht immer eine Resolve-Nachricht, wenn der Client die XAddrs abrufen muss.

Dieser Ansatz bietet zwei Vorteile. Erstens macht ein gerät, das auf WSDAPI basiert, niemals XAddrs verfügbar, die die IP-Adressen privater Netzwerke offenlegen. Zweitens macht ein gerät, das auf WSDAPI basiert, nur XAddrs verfügbar, auf die der Client zugreifen kann. Das bedeutet, dass IPv6-Adressen nie an einen IPv4-Client gesendet werden.

Wenn eine [Test-](probe-message.md) oder Resolve-Nachricht empfangen wird, wird nur ein einzelner XAddr als Antwort gesendet. Der gesendete XAddr entspricht der lokalen Adresse, an der die Anforderung empfangen wurde. Wenn die Anforderung subnetzübergreifend über IPv6 empfangen wurde, stellt WSDAPI in der Antwort eine globale IPv6-Adresse bereit.

## <a name="preferred-addresses"></a>Bevorzugte Adressen

Ein Gerät kann mehrere XAddrs in einer [Hello-,](hello-message.md) [ProbeMatch-](probematches-message.md)oder [ResolveMatch-Nachricht](resolvematches-message.md) bereitstellen. Ein Dienst kann auch an mehreren Endpunkten mit unterschiedlichen Transportadressen verfügbar sein. In diesen Fällen versucht WSDAPI, mit dem Gerät über die erste verwendbare Adresse zu kommunizieren, die es findet. Eine Adresse kann verwendet werden, wenn sie aus einem verfügbaren Protokoll stammt, z. B. IPv4 auf einem Computer, auf dem IPv4 installiert ist, oder IPv6 auf einem Computer, auf dem IPv6 installiert ist. Wenn die Adresse von einem Gerät oder Dienst stammt, das sich nicht im lokalen Subnetz befindet, kann sie nur verwendet werden, wenn es sich um einen lokalen IPv4-, IPv6-Standort- oder IPv6-Link handelt.

## <a name="wsdl-in-metadata-exchange"></a>WSDL im Metadatenaustausch

Geräte und Dienste, die auf WSDAPI aufbauen, stellen ihre WSDL nicht im Metadatenaustausch bereit, es sei denn, sie wurden von der Anwendung erweitert, um diese Informationen bereitzustellen. Standardmäßig ist die WSDL-Bereitstellung nicht Teil des Programmiermodells.

## <a name="app_max_delay"></a>APP \_ MAX \_ DELAY

DPWS definiert APP \_ MAX \_ DELAY, das zufällige Intervall, das zwischen dem Empfang eines [Tests](probe-message.md) und dem Senden eines [ProbeMatch-Werts](probematches-message.md)verzögert werden soll, als 5.000 Millisekunden. Windows Die Firewall erfordert, dass das Multicastanforderungs-/Unicastantwortmodell für UDP nur innerhalb des 4-Sekunden-Firewallfensters funktioniert. Daher überträgt WSDAPI Antworten in maximal 2.500 ms anstelle des von APP MAX DELAY beschriebenen 5.000 \_ \_ ms-Fensters.

## <a name="iana-port-reservations"></a>IANA-Portreservierungen

WSDAPI verwendet standardmäßig TCP-Port 5357 für HTTP-Datenverkehr und TCP-Port 5358 für HTTPS-Datenverkehr. Diese Ports sind für Prozesse mit niedrigeren Berechtigungen über eine URL-Reservierung in HTTP.sys und auch für IANA reserviert.

## <a name="udp-port-sharing"></a>UDP-Portfreigabe

WSDAPI verwendet die Portfreigabe. Unicastnachrichten, die an Port 3702 gesendet werden, werden möglicherweise nicht von allen WSDAPI-basierten Anwendungen ordnungsgemäß verarbeitet. Wenn eine Anwendung ausschließlich an Port 3702 gebunden wird, kann dies verhindern, dass WSDAPI-basierte Anwendungen diesen Port ordnungsgemäß verwenden.

## <a name="ws-discovery-v11-cd1-proxy"></a>WS-Discovery v1.1 CD1-Proxy

WSDAPI sucht nach einem Ermittlungsproxy, der das Protokoll für den verwalteten Modus WS-Discovery v1.1 CD1 implementiert, und kommuniziert mit diesem. WS-Discovery v1.1 CD1 ist die erste Revision der WS-Discovery, die eine explizite Beschreibung eines HTTP-Protokolls für die Kommunikation zwischen einem Proxy und einem Client oder Gerät enthält.

Um die Anzahl gleichzeitiger Versionen zu begrenzen, die in Multicastanforderungen verwendet werden, sendet WSDAPI eine WS-Discovery Testanforderung im Namespace 2005/04, sucht jedoch nach dem DiscoveryProxy-Typ WS-Discovery v1.1 CD1. Wenn ein Proxy antwortet, sendet WSDAPI eine HTTP-Test- oder Resolve-Anforderung an den angegebenen Proxyendpunkt, wie in WS-Discovery v1.1 CD1 definiert.

 

 



