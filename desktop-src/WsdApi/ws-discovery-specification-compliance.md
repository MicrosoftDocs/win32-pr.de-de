---
description: 'Erfahren Sie mehr über: WS-Discovery Spezifikationskonformität'
ms.assetid: b795a385-b48d-4a16-9d91-e48bca120572
title: WS-Discovery Spezifikationskonformität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07794140f05a065fb770ae2d5782f24180fb7e7ef66757278d5c5c93a3fd7e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991410"
---
# <a name="ws-discovery-specification-compliance"></a>WS-Discovery Spezifikationskonformität

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) beschreibt, wie die folgenden Aufgaben ausgeführt werden:

-   Ankündigen der Verfügbarkeit von Diensten im lokalen Subnetz
-   Suchen nach Diensten im Subnetz
-   Suchen eines zuvor referenzierten Diensts

Um dies zu erreichen, definiert WS-Discovery zwei unidirektionale Nachrichten, [Hello](hello-message.md) und [Bye,](bye-message.md)und zwei bidirektionale Suchnachrichten, [Test](probe-message.md) und [Resolve.](resolve-message.md)

WS-Discovery stellt auch Adressen und einen reservierten Port für die lokale IPv4- und IPv6-Linkermittlung bereit. Die Spezifikation ermöglicht auch die Definition alternativer Bindungen an anderer Stelle, z. B. die Im [Geräteprofil für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) definierte Test-over-HTTP-Bindung.

Die WS-Discovery Spezifikation beschreibt die Wahlfunktionalität mithilfe der Begriffe MAY oder SHOULD in einer bestimmten Implementierungsempfehlung oder -einschränkung. Ausgelassene Funktionen können funktionen sein, die in der WS-Discovery Spezifikation als ERFORDERLICH beschrieben werden, die nicht von WSDAPI implementiert wurde, oder es kann sich um Funktionen handelt, die WSDAPI in einer anderen Methode in der in der WS-Discovery Spezifikation angegebenen implementiert hat.

In diesem Thema wird beschrieben, wie WS-Discovery Einschränkungen, Anforderungen und Wahlfunktionen von der WSDAPI-Implementierung behandelt werden. Dieses Thema wird am besten zusammen mit der WS-Discovery-Spezifikation gelesen.

## <a name="ws-discovery-and-soap-over-udp-support"></a>WS-Discovery und SOAP-over-UDP-Unterstützung

In SOAP-over-UDP gibt Abschnitt 3.2 an, dass die UDP-Nachricht in ein 64K-Datagramm passen muss. WSDAPI akzeptiert 64.000 UDP-Nachrichten, aber die DPWS-Einschränkung von MAX \_ ENVELOPE \_ SIZE (32K) schränkt die Nachrichtengröße ein. Wie für [die WS-Ermittlung](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)erforderlich, unterstützt WSDAPI die in Abschnitt 4 beschriebenen Nachrichtenmuster.

WSDAPI kann zur Unterstützung des Sicherheitsmodells in den Abschnitten 7 und 8 konfiguriert werden. Wenn dies konfiguriert ist, signiert WSDAPI ausgehende WS-Discovery Nachrichten und überprüft Signaturen für eingehende Nachrichten.

WSDAPI implementiert den in Anhang I definierten Neuübertragungsalgorithmus, wie in Anhang I des DPWS-Anhangs I beschrieben.

Bei der WS-Ermittlung verwendet WSDAPI die in Abschnitt 2.4 angegebenen Adressen. WSDAPI erweitert APP \_ MAX DELAY aus Abschnitt \_ 2.4, jedoch nicht in dem umfang, wie in ANHANG I von DPWS definiert. Weitere Informationen zu APP \_ MAX DELAY finden Sie unter Zusätzliche \_ [WS-Discovery-Funktionalität.](additional-ws-discovery-functionality.md)

WS-Discovery beschreibt die `uuid:` URI-Formatempfehlung in Abschnitt 2.6, aber WSDAPI überschreibt diese Empfehlung. Stattdessen verwendet WSDAPI das `urn:uuid:` in DPWS beschriebene URI-Format.

In Abschnitt 3 WS-Discovery wird beschrieben, wie ein Client mit einem Ermittlungsproxy interagiert. WSDAPI erkennt diese Interaktion nicht und ignoriert Ankündigungen von Ermittlungsproxys. In Windows 7 implementiert WSDAPI eine private Erweiterung für das WS-Discovery-Protokoll, WS-Discovery Remoteerweiterungen, um Ermittlungsclients die Suche nach Diensten zu ermöglichen, die über viele verschiedene Netzwerke verteilt sind, indem Anforderungen an zentralisierte Proxys gesendet werden. Weitere Informationen finden Sie unter [Zusätzliche WS-Discovery-Funktionalität.](additional-ws-discovery-functionality.md)

Abschnitt 4.1 Absatz 3 WS-Discovery erfordert, dass ein Timer verstrichen sein muss, bevor eine [Hello-Nachricht](hello-message.md) gesendet wird. Die Hosting-API wartet nicht, bevor sie eine Hello-Nachricht sendet. Wenn für ein Szenario eine Verzögerung erforderlich ist, bevor eine Hello-Nachricht gesendet wird, muss der Anwendungsentwickler eine Wartezeit implementieren.

WSDAPI implementiert alle Nachrichten, die in WS-Discovery Abschnitten 4, 5 und 6 beschrieben sind. WSDAPI erzwingt auch das \_ in Abschnitt 7 beschriebene MATCH TIMEOUT gemäß der Ergänzung durch DPWS Anhang I. WSDAPI schützt nur vor "Wiedergabe" aus den Sicherheitsaspekten in Abschnitt 9.

WSDAPI implementiert die Anwendungssequenzierung, wie in WS-Discovery Anhang I beschrieben.

 

 



