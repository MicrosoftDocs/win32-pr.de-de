---
description: Die erste Konfiguration erfordert über die Installation des Microsoft IPv6 Technology Preview-Protokolls hinaus keine zusätzliche Konfiguration.
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 'Konfiguration 1: Einzelnes Subnetz mit lokalen Linkadressen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a541edd96175dc61ec0aba3b1358c2bbd9464668e6aa1a11aeb6f2097e5b13bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051733"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a>Konfiguration 1: Einzelnes Subnetz mit lokalen Linkadressen

Die erste Konfiguration erfordert über die Installation des Microsoft IPv6 Technology Preview-Protokolls hinaus keine zusätzliche Konfiguration. Diese Konfiguration besteht aus mindestens zwei Knoten im gleichen Subnetz. In der IPv6-Terminologie befinden sich die beiden Knoten über die gleiche Verbindung ohne Zwischenrouter.

Die folgende Abbildung zeigt die Konfiguration von zwei Knoten in einem einzelnen Subnetz mithilfe von lokalen Linkadressen.

![zwei Knoten, die lokale Linkadressen verwenden.](images/v6mig-1.png)

Standardmäßig konfiguriert IPv6 link-local IP-Adressen für jede Schnittstelle, die installierten Ethernet-Netzwerkadaptern entspricht. Lokale Linkadressen haben das Präfix fe80::/64. Die letzten 64 Bits der IPv6-Adresse werden als Schnittstellenbezeichner bezeichnet und von der 48-Bit-MAC-Adresse des Netzwerkadapters abgeleitet.

So erstellen Sie den IPv6-Schnittstellenbezeichner aus der 48-Bit-Ethernet-MAC-Adresse (6 Byte):

-   Die Hexadezimalziffern 0xff-fe werden zwischen dem dritten und vierten Byte der MAC-Adresse eingefügt.
-   Das universelle/lokale Bit, das zweite low-order-Bit des ersten Byte der MAC-Adresse, wird ergänzt. Wenn es sich um eine 1 handelt, wird sie in 0 und bei 0 in 1 umgeschaltet.

Beispiel für die MAC-Adresse 00-60-08-52-f9-d8:

-   Die hexadezimalen Ziffern 0xff-fe werden zwischen 0x08 (drittes Byte) und 0x52 (viertes Byte) der MAC-Adresse eingefügt, was die 64-Bit-Adresse 00-60-08-ff-fe-52-f9-d8 bildet.
-   Das universelle/lokale Bit, das zweite bit von 0x00 (das erste Byte) der MAC-Adresse, wird ergänzt. Das zweite low-order-Bit von 0x00 ist 0, was, wenn es ergänzt wird, zu 1 wird. Das Ergebnis ist, dass für das erste Byte 0x00 wird 0x02.

Daher ist der IPv6-Schnittstellenbezeichner, der der Ethernet-MAC-Adresse 00-60-08-52-f9-d8 entspricht, 02-60-08-ff-fe-52-f9-d8.

Die link-local-Adresse eines Knotens ist die Kombination aus dem Präfix fe80::/64 und dem 64-Bit-Schnittstellenbezeichner, der in IPv6-Doppelpunkt-Hexadezimal-Notation ausgedrückt wird. Daher ist die link-local-Adresse dieses Beispielknotens mit dem Präfix fe80::/64 und dem Schnittstellenbezeichner 02-60-08-ff-fe-52-f9-d8 fe80::260:8ff:fe52:f9d8.

Sie können Ihre lokale Linkadresse anzeigen, indem Sie ipv6 verwenden, wenn dies im folgenden Beispiel gezeigt wird:

**ipv6, wenn**

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

Schnittstelle 4 ist eine Schnittstelle, die einem installierten Ethernet-Adapter mit der lokalen Linkadresse fe80::210:5aff:feaa:20a2 entspricht.

Weitere Informationen zur IPv6-Adressierung und eine Übersicht über IPv6-Konzepte finden Sie im Whitepaper Introduction to IPv6 (Einführung in IPv6).

## <a name="testing-connectivity-between-two-link-local-hosts"></a>Testen der Konnektivität zwischen zwei lokalen Linkhosts

Sie können einen einfachen Ping (einen Austausch von ICMPv6 Echo Request- und Echo Reply-Nachrichten) mithilfe von IPv6 zwischen zwei lokalen Linkhosts verwenden.

**So pingen Sie mit IPv6 zwischen zwei lokalen Linkhosts**

1.  Installieren Sie microsoft IPv6 Technology Preview für Windows auf zwei Windows-Hosts (Host A und Host B), die sich unter demselben Link (Subnetz) befinden.
2.  Verwenden Sie ipv6 auf Host A, um die lokale Linkadresse für die Ethernet-Schnittstelle zu erhalten.

    Beispiel: Die link-local-Adresse von Host A ist fe80::210:5aff:feaa:20a2.

3.  Verwenden Sie ipv6 auf Host B, um die link-local-Adresse für die Ethernet-Schnittstelle zu erhalten.

    Beispiel: Die lokale Linkadresse von Host B ist fe80::260:97ff:fe02:6ea5.

4.  Pingen Sie host B über Host A mit Ping6.exe.

    Beispiel: ping6 fe80::260:97ff:fe02:6ea5

Um die Quelladresse anzugeben, von der die Echo Request-Nachrichten gesendet werden, können Sie auch die Option Ping6.exe -s verwenden. Um beispielsweise Echoanforderungen von der IPv6-Adresse fe80::210:5aff:feaa:20a2 an Host B zu senden, verwenden Sie den folgenden Befehl:

**ping6 -s fe80::210:5aff:feaa:20a2%4 fe80::260:97ff:fe02:6ea5**

Beim Pingen einer lokalen link- oder standortbasierten Adresse wird empfohlen, die Bereichs-ID anzugeben, um die Zieladresse eindeutig zu machen. Die Notation zum Angeben der Bereichs-ID ist address%scope-ID. Bei lokalen Linkadressen entspricht die Bereichs-ID der Schnittstellennummer, die im Befehl ipv6 if angezeigt wird. Bei standortbasierten Adressen entspricht die Bereichs-ID der Standortnummer, die im Befehl ipv6 if angezeigt wird. Verwenden Sie beispielsweise den folgenden Befehl, um Echo Request-Nachrichten mit scope-ID 4 an Host B zu senden:

**ping6 fe80::260:97ff:fe02:6ea5%4**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Empfohlene Konfigurationen für IPv6](recommended-configurations-2.md)
</dt> </dl>

 

 



