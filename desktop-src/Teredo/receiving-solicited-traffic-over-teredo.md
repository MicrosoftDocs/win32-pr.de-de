---
title: Empfangen von angeforderten Datenverkehr über Teredo
description: Viele Anwendungen, wie z. b. Microsoft Internet Explorer und Microsoft Outlook, initiieren nur Verbindungen mit dem Internet.
ms.assetid: bff5d65e-050d-4b09-9982-8024612ffa6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035d067afeb9c62795efb5acd0bb28adc3afcb16
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104517177"
---
# <a name="receiving-solicited-traffic-over-teredo"></a>Empfangen von angeforderten Datenverkehr über Teredo

Viele Anwendungen, wie z. b. Microsoft Internet Explorer und Microsoft Outlook, initiieren nur Verbindungen mit dem Internet. Für diese Anwendungen kann [Teredo](about-teredo.md) eine nahtlose Konnektivität über IPv6 bereitstellen, wenn keine anderen IPv6-Schnittstellen vorhanden sind. Darüber hinaus kann der angeforderte Datenverkehr über die Teredo-Schnittstelle auf den früheren Plattformen von Microsoft Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 empfangen werden.

In der folgenden Dokumentation wird erläutert, wie diese Anwendungen Konnektivität erreichen und in welchen Situationen Teredo verwendet wird.

## <a name="obtaining-a-destination-address"></a>Abrufen einer Zieladresse

Eine Anwendung versucht, die Zieladresse mithilfe verschiedener Methoden (z. b. Domain Name System (DNS) oder Peer Name Resolution Protocol (PNRP) abzurufen. Die Anwendung kann mithilfe dieser Methoden mehrere IPv4-und IPv6-IP-Adressen abrufen. Zu den typischen APIs, die zum Abrufen von IP-Adressen verwendet werden, gehören die Windows XP-API [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) und die neue Windows Vista-API [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo). Beispielsweise ermöglicht die Verwendung der getaddrinfo-API mit dem Parameter " *AI \_ Family* ", der auf "AF inet6" festgelegt ist, \_ als addrinfo-/Protokoll-Server die Abfrage von DNS-Servern für IPv6-Adressen. Die [**DNSQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) -API mit dem Typ "DNS \_ Type \_ AAAA" kann auch verwendet werden, um die DNS-Server für AAAA-Einträge abzufragen.

## <a name="establishing-a-connection"></a>Herstellen einer Verbindung

Eine mit Teredo festgelegte Verbindung wird als "nahtlos" beschrieben, da Sie wie jede andere IPv6-Verbindung behandelt wird. Die Programmierung einer Anwendung erfordert keine besondere Überlegung, um die Teredo-Schnittstelle verwenden zu können. Wenn eine Verbindung zwischen Teredo-Schnittstellen hergestellt wird, ist ein Relayrouter, der typisch für IPv6-zu-IPv4 und andere systemeigene Schnittstellen ist, nicht erforderlich. Teredo ist jedoch als letzte Übergangstechnologie für den Übergang der IPv6-Konnektivität konzipiert.

> [!Note]  
> Teredo wird nicht verwendet, wenn der angegebene Hostname nur zu IPv4-Adressen aufgelöst wird.

 

Wenn eine Anwendung versucht, eine Verbindung mit einem Ziel mithilfe von IPv6-Adressen herzustellen, tritt Folgendes auf:

-   Die Anwendung ruft eine Liste der IPv6-Adressen durch Aufrufen der [**getadaptersadressen**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) -API ab. Der Windows Vista-Stapel gibt eine Liste aller Schnittstellen basierend auf der in [RFC 3484](https://www.irt.org/rfc/rfc3484.htm)angegebenen Sortierreihenfolge zurück. Daher werden IPv6-und IPv6-zu-IPv4-IPv6-Schnittstellen vor der Teredo-Schnittstelle aufgelistet. Wenn jedoch keine systemeigene IPv6-oder IPv6-zu-IPv4-Konnektivität verfügbar ist, ist Teredo die einzige aufgelistete IPv6-fähige Schnittstelle.

    Beachten Sie, dass eine Anwendung jede beliebige Schnittstelle verwenden kann, die vom Windows Vista-Stapel bereitgestellt wird. die Reihenfolge der zurückgegebenen Schnittstellen Liste führt jedoch am häufigsten dazu, dass Teredo zuletzt versucht wird.

-   Bevor Windows Vista versucht, eine Verbindung über die Teredo-Schnittstelle herzustellen, stellt das Betriebssystem sicher, dass die IPv6-Adresse stabilisiert ist. Dies erfolgt automatisch für ausgehende Verbindungen und ist keine entscheidende Überlegung für eine Anwendung. Wenn die Anwendung die Adress Stabilität gewährleisten muss, kann die [**notifystableunicastipadresssstable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) -API aufgerufen werden, um sicherzustellen, dass die Teredo-Adresse stabil ist.

-   Eine Teredo-Schnittstelle versucht, eine Verbindung mit einer anderen Teredo-Schnittstelle am Ziel herzustellen. Wenn eine Teredo-Schnittstelle nicht vorhanden ist, wird eine Verbindung mit einer nativen oder IPv6-zu-IPv4-Zieladresse über ein Host spezifisches Relay hergestellt.

Es ist auch möglich, dass Anwendungen, die Verbindungen mit dem Internet initiieren, nicht angeforderten Datenverkehr empfangen. Weitere Informationen finden Sie unter [empfangen von angefordertem Datenverkehr über Teredo](receiving-unsolicited-traffic-over-teredo.md).

## <a name="using-the-wsaconnectbyname-api"></a>Verwenden der WSAConnectByName-API

Durch Aufrufen der WSAConnectByName-API ist es möglich, dass eine Anwendung eine Verbindung mit einem Zielnamen herstellt, anstatt die genaue IP-Adresse anzugeben. Der Windows Vista-Stapel bevorzugt IPv6 über IPv4, und daher werden alle Verbindungsversuche zuerst an IPv6-Adressen durchgeführt.

Durch Aufrufen der WSAConnectByName-API werden alle Ziel-IP-Adressen in der folgenden Reihenfolge sortiert:

-   Native IPv6-Adresse
-   IPv6-zu-IPv4 IP-Adresse
-   IPv4-Adresse
-   Teredo-Adresse

Nachdem die Zieladressen intern sortiert wurden, wird eine Verbindung mit dem Ziel basierend auf der am besten verfügbaren Route auf dem lokalen Host für die Zieladresse versucht. Wie in der Reihenfolge der sortierten Adressen angegeben, wird die IPv4-Adresse verwendet, um die Verbindung herzustellen, wenn der Zielname in eine IPv4-und Teredo-Adresse aufgelöst wird.

Die WSAConnectByName-API arbeitet intern, um die beste Entsprechung zwischen Adressen zu ermitteln. Dieser Versuch basiert auf den Routen, die auf dem lokalen Host und den Zieladressen verfügbar sind.

Aufgrund der aktuellen Abwesenheit von Teredo-Relays im Internet ist es unwahrscheinlich, dass Verbindungen mit nativen IPv6-Adressen über die Teredo-Schnittstelle hergestellt werden. Wenn WSAConnectByName aufgerufen wird, gibt Windows Vista keine AAAA-Abfragen aus, wenn Teredo die einzige verfügbare IPv6-fähige Schnittstelle ist. Dadurch wird sichergestellt, dass systemeigene IPv6-Adressen nicht als Ziel abgerufen werden und dass Verbindungen über IPv4 versucht werden, was die höchste Erfolgschance hat. Um IPv6-Adressen zu erhalten, wenn Teredo die einzige IPv6-fähige Schnittstelle ist, muss eine Anwendung explizit die DNSQuery-API für AAAA-Datensätze verwenden.

 

 