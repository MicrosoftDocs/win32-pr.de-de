---
description: 'Weitere Informationen finden Sie hier: WS-Discovery Specification-Konformität'
ms.assetid: b795a385-b48d-4a16-9d91-e48bca120572
title: Konformität der WS-Discovery Spezifikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcae062448b1913f0cc62dff3b6c86b98280a902
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393325"
---
# <a name="ws-discovery-specification-compliance"></a>Konformität der WS-Discovery Spezifikation

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) beschreibt, wie die folgenden Aufgaben ausgeführt werden:

-   Geben Sie die Verfügbarkeit von Diensten im lokalen Subnetz an.
-   Suchen nach Diensten im Subnetz
-   Einen zuvor referenzierten Dienst suchen

Zu diesem Zweck definiert WS-Discovery 2 1-Wege-nach [richten, "](probe-message.md) [Hello](hello-message.md) " und " [Bye](bye-message.md) [" und zwei](resolve-message.md)bidirektionale Such Nachrichten.

WS-Discovery bietet auch Adressen und einen reservierten Port für die lokale Ermittlung von IPv4-und IPv6-Verbindungen. Mit der Spezifikation können auch alternative Bindungen an anderer Stelle definiert werden, wie z. b. die Überprüfung der HTTP-Bindung, die im [Geräte Profil für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) definiert ist.

Die WS-Discovery Spezifikation beschreibt die wählbaren Funktionen mithilfe der Bedingungen, die in einer vorgegebenen Implementierungs Empfehlung oder-Einschränkung auftreten können. Die ausgelassene Funktionalität kann in der WS-Discovery Spezifikation, die nicht von WSDAPI implementiert wurde, als erforderlich beschrieben werden, oder es handelt sich um Funktionen, die von WSDAPI in einer anderen Methode in der WS-Discovery Spezifikation implementiert wurden.

In diesem Thema wird beschrieben, wie WS-Discovery Einschränkungen, Anforderungen und wählbaren Funktionen von der WSDAPI-Implementierung behandelt werden. Dieses Thema ist am besten in Zusammenhang mit der WS-Discovery Spezifikation zu lesen.

## <a name="ws-discovery-and-soap-over-udp-support"></a>Unterstützung von WS-Discovery und SOAP-Over-UDP

In SOAP-Over-UDP gibt Abschnitt 3,2 an, dass die UDP-Nachricht in ein 64-KB-Datagramm eingefügt werden muss. WSDAPI akzeptiert höchstens 64 KB-Nachrichten, aber die DPWS-Einschränkung der maximalen \_ Umschlag \_ Größe (32K) schränkt die Nachrichtengröße ein. Wie für die [WS-](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)Ermittlung erforderlich, unterstützt WSDAPI die Nachrichten Muster, die in Abschnitt 4 beschrieben werden.

WSDAPI kann so konfiguriert werden, dass das Sicherheitsmodell in den Abschnitten 7 und 8 unterstützt wird. Wenn dies konfiguriert ist, signiert WSDAPI ausgehende WS-Discovery Nachrichten und überprüft die Signaturen eingehender Nachrichten.

WSDAPI implementiert den Algorithmus für Neuübertragungen, der in Anhang i gemäß der Änderung durch DPWS Anhang i definiert wurde.

In WS-Discovery verwendet WSDAPI die Adressen, die in Abschnitt 2,4 angegeben sind. WSDAPI erweitert \_ die maximale APP- \_ Verzögerung aus Abschnitt 2,4, jedoch nicht entsprechend der Definition in DPWS Anhang I. Weitere Informationen zur \_ maximalen Verzögerung von apps \_ finden Sie unter [zusätzliche WS-Discovery Funktionen](additional-ws-discovery-functionality.md).

`uuid:`In WS-Discovery wird die URI-Format Empfehlung in Abschnitt 2,6 beschrieben, aber WSDAPI überschreibt diese Empfehlung. Stattdessen verwendet WSDAPI das `urn:uuid:` in DPWS beschriebene URI-Format.

In Abschnitt 3 von WS-Discovery wird beschrieben, wie ein Client mit einem suchproxy interagiert. WSDAPI erkennt diese Interaktion nicht und ignoriert Ankündigungen von Ermittlungs Proxys. In Windows 7 implementiert WSDAPI eine private Erweiterung des WS-Discovery Protokolls WS-Discovery Remote Erweiterungen, damit Ermittlungs Clients mithilfe von Anforderungen an zentralisierte Proxys Dienste suchen können, die in vielen verschiedenen Netzwerken verteilt sind. Weitere Informationen finden Sie unter [zusätzliche WS-Discovery Funktionen](additional-ws-discovery-functionality.md).

Abschnitt 4,1, Absatz 3 von WS-Discovery erfordert, dass ein Timer vergehen muss, bevor eine [Hello](hello-message.md) -Nachricht gesendet wird. Die Hosting-API wartet nicht, bevor eine Hello-Nachricht gesendet wird. Wenn ein Szenario vor dem Senden einer Hello-Nachricht eine Verzögerung erfordert, muss der Anwendungsentwickler einen Warte Vorgang implementieren.

WSDAPI implementiert alle in den WS-Discovery Abschnitten 4, 5 und 6 beschriebenen Nachrichten. WSDAPI erzwingt auch das Übereinstimmungs Timeout, das \_ in Abschnitt 7 gemäß der Änderung des DPWS-Anhangs I beschrieben wird. WSDAPI schützt nur vor den sicheren Überlegungen in Abschnitt 9 vor der Wiedergabe.

WSDAPI implementiert die Anwendungs Sequenzierung, wie in WS-Discovery Anhang I beschrieben.

 

 



