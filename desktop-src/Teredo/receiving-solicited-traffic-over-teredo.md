---
title: Empfangen von angeforderten Datenverkehr über Teredo
description: Viele Anwendungen wie Microsoft Internet Explorer und Microsoft Outlook nur Verbindungen mit dem Internet initiieren.
ms.assetid: bff5d65e-050d-4b09-9982-8024612ffa6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f003755f49d04113108f83c8d3eff67084364ad6dfcf8e9f40cf1bf7e142e0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001678"
---
# <a name="receiving-solicited-traffic-over-teredo"></a>Empfangen von angeforderten Datenverkehr über Teredo

Viele Anwendungen wie Microsoft Internet Explorer und Microsoft Outlook nur Verbindungen mit dem Internet initiieren. Für diese Anwendungen kann [Teredo](about-teredo.md) nahtlose Konnektivität über IPv6 bereitstellen, wenn keine anderen IPv6-Schnittstellen verfügbar sind. Darüber hinaus kann angeforderter Datenverkehr über die Teredo-Schnittstelle auf den früheren Plattformen Microsoft Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 empfangen werden.

In der folgenden Dokumentation wird erläutert, wie diese Anwendungen Konnektivität erreichen und unter welchen Umständen Teredo verwendet wird.

## <a name="obtaining-a-destination-address"></a>Abrufen einer Zieladresse

Eine Anwendung versucht, die Zieladresse mithilfe verschiedener Methoden wie Domain Name System (DNS) oder Peer Name Resolution Protocol (PNRP) zu erhalten. Die Anwendung kann mit diesen Methoden mehrere IPv4- und IPv6-Adressen abrufen. Zu den typischen APIs zum Abrufen von IP-Adressen gehören Windows XP-API [**GetHostByName**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) und die neue Windows Vista-API [**GetAddrInfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo). Beispielsweise ermöglicht die Verwendung der GetAddrInfo-API mit dem parameter *ai \_ family,* der auf AF INET6 festgelegt ist, als addrinfo/protocol-Hinweis, dass der Benutzer DNS-Server speziell für \_ IPv6-Adressen abfragen kann. Die [**DnsQuery-API**](/windows/desktop/api/windns/nf-windns-dnsquery_a) mit dem Typ DNS TYPE AAAA kann auch zum Abfragen der \_ DNS-Server nach \_ AAAA-Einträgen verwendet werden.

## <a name="establishing-a-connection"></a>Herstellen einer Verbindung

Eine mit Teredo hergestellte Verbindung wird als "nahtlos" beschrieben, da sie wie jede andere IPv6-Verbindung verarbeitet wird. Die Programmierung einer Anwendung erfordert keine besonderen Überlegungen, um die Teredo-Schnittstelle nutzen zu können. Wenn eine Verbindung zwischen Teredo-Schnittstellen hergestellt wird, ist kein Relayrouter erforderlich, der typisch für 6to4 und andere native Schnittstellen ist. Teredo ist jedoch als letzte Übergangstechnologie für IPv6-Konnektivität konzipiert.

> [!Note]  
> Teredo wird nicht verwendet, wenn der angegebene Hostname nur in IPv4-Adressen aufzulösen ist.

 

Wenn eine Anwendung versucht, über IPv6-Adressen eine Verbindung mit einem Ziel herzustellen, geschieht Folgendes:

-   Die Anwendung ruft eine Liste von IPv6-Adressen ab, indem sie die [**GetAdaptersAddresses-API**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) aufruft. Der Windows Vista-Stapel gibt eine Liste aller Schnittstellen basierend auf der in [RFC 3484 angegebenen Sortierreihenfolge zurück.](https://www.irt.org/rfc/rfc3484.htm) Daher werden IPv6- und 6to4-IPv6-Schnittstellen vor der Teredo-Schnittstelle aufgelistet. Wenn jedoch keine native IPv6- oder 6to4-Konnektivität verfügbar ist, ist Teredo die einzige aufgeführte IPv6-fähige Schnittstelle.

    Beachten Sie, dass eine Anwendung jede vom Windows Vista-Stapel bereitgestellte Schnittstelle verwenden kann. Die Reihenfolge der zurückgegebenen Schnittstellenliste führt jedoch am häufigsten dazu, dass teredo zuletzt versucht wird.

-   Bevor Windows Vista versucht, eine Verbindung über die Teredo-Schnittstelle herzustellen, stellt das Betriebssystem sicher, dass sich die IPv6-Adresse stabilisiert hat. Dies erfolgt automatisch für ausgehende Verbindungen und ist kein wichtiger Aspekt für eine Anwendung. Wenn die Anwendung zur Gewährleistung der Adressstabilität erforderlich ist, kann die [**NotifyStableUnicastIpAddressTable-API**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) aufgerufen werden, um sicherzustellen, dass die Teredo-Adresse stabil ist.

-   Eine Teredo-Schnittstelle versucht, eine Verbindung mit einer anderen Teredo-Schnittstelle am Ziel herzustellen. Wenn keine Teredo-Schnittstelle vorhanden ist, wird eine Verbindung mit einer nativen oder 6to4-Zieladresse über ein hostspezifisches Relay hergestellt.

Es ist auch möglich, dass Anwendungen, die Verbindungen mit dem Internet initiieren, nicht angeforderten Datenverkehr empfangen. Weitere Informationen finden Sie unter [Empfangen von nicht angeforderten Datenverkehr über Teredo](receiving-unsolicited-traffic-over-teredo.md).

## <a name="using-the-wsaconnectbyname-api"></a>Verwenden der WSAConnectByName-API

Durch Aufrufen der WSAConnectByName-API kann eine Anwendung eine Verbindung mit einem Zielnamen herstellen, anstatt die genaue IP-Adresse anzugeben. Der Windows Vista-Stapel bevorzugt IPv6 gegenüber IPv4, und daher werden zuerst alle Verbindungsversuche mit IPv6-Adressen unternommen.

Durch aufrufen der WSAConnectByName-API werden alle IP-Zieladressen sortiert, die in der folgenden Reihenfolge erhalten werden:

-   Native IPv6-Adresse
-   6to4 IP-Adresse
-   IPv4-Adresse
-   Teredo-Adresse

Nachdem die Zieladressen intern sortiert wurden, wird versucht, eine Verbindung mit dem Ziel herzustellen, basierend auf der besten Route, die auf dem lokalen Host für die Zieladresse verfügbar ist. Wie in der Reihenfolge der sortierten Adressen angegeben, wird die IPv4-Adresse verwendet, um die Verbindung herzustellen, wenn der Zielname in eine IPv4- und Teredo-Adresse auflöset.

Die WSAConnectByName-API arbeitet intern, um die beste Übereinstimmung zwischen Adressen zu finden. Dieser Versuch basiert auf den Routen, die auf dem lokalen Host und den Zieladressen verfügbar sind.

Aufgrund des aktuellen Fehlens von Teredo-Relays im Internet ist es unwahrscheinlich, dass Verbindungen mit nativen IPv6-Adressen über die Teredo-Schnittstelle erfolgreich sind. Wenn WSAConnectByName aufgerufen wird, gibt Windows Vista keine AAAA-Abfragen aus, wenn Teredo die einzige verfügbare IPv6-fähige Schnittstelle ist. Dadurch wird sichergestellt, dass native IPv6-Adressen nicht als Ziel erhalten werden und verbindungen über IPv4 versucht werden, was die höchste Erfolgschancen hat. Um IPv6-Adressen zu erhalten, wenn Teredo die einzige IPv6-fähige Schnittstelle ist, muss eine Anwendung explizit die DnsQuery-API für AAAA-Einträge verwenden.

 

 