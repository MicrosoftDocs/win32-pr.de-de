---
description: Die erste Konfiguration erfordert keine zusätzliche Konfiguration über die Installation des Microsoft IPv6-Technologievorschau Protokolls hinaus.
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: 'Konfiguration 1: einzelnes Subnetz mit Link-Local-Adressen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d09feb44c222b7213da18a6745fc632f3903209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041734"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a>Konfiguration 1: einzelnes Subnetz mit Link-Local-Adressen

Die erste Konfiguration erfordert keine zusätzliche Konfiguration über die Installation des Microsoft IPv6-Technologievorschau Protokolls hinaus. Diese Konfiguration besteht aus mindestens zwei Knoten im gleichen Subnetz. In der IPv6-Terminologie befinden sich die beiden Knoten in derselben Verbindung ohne zwischengeschaltete Router.

Die folgende Abbildung zeigt die Konfiguration von zwei Knoten in einem einzelnen Subnetz mithilfe von Link-Local-Adressen.

![zwei Knoten, die Link-Local-Adressen verwenden.](images/v6mig-1.png)

Standardmäßig konfiguriert IPv6 Verbindungs lokale IP-Adressen für jede Schnittstelle, die den installierten Ethernet-Netzwerkadaptern entspricht. Link-Local-Adressen haben das Präfix FE80::/64. Die letzten 64 Bits der IPv6-Adresse werden als Schnittstellen Bezeichner bezeichnet und von der 48-Bit-Mac-Adresse des Netzwerkadapters abgeleitet.

So erstellen Sie den IPv6-Schnittstellen Bezeichner aus der 48-Bit-Ethernet-MAC-Adresse (6 Byte):

-   Die hexadezimal Ziffern 0xFF-FE werden zwischen dem dritten und vierten Byte der Mac-Adresse eingefügt.
-   Das Universal/local-Bit, das zweite niedrig wertige Bit des ersten Bytes der Mac-Adresse, wird ergänzt. Wenn der Wert 1 ist, wird er in 0 (null) umgewandelt, und wenn er 0 ist, wird er in 1 umgewandelt.

Beispielsweise für die Mac-Adresse 00-60-08-52-F9-D8:

-   Die hexadezimal Ziffern 0xFF-FE werden zwischen 0x08 (das dritte Byte) und 0x52 (das vierte Byte) der Mac-Adresse eingefügt, wodurch die 64-Bit-Adresse 00-60-08-FF-FE-52-F9-D8 gebildet wird.
-   Das universelle/lokale Bit, das zweite niedrig wertige Bit von 0x00 (das erste Byte) der Mac-Adresse wird ergänzt. Das zweite niedrig wertige Bit von 0x00 ist 0 (null), das, wenn es ergänzt wird, 1 ist. Das Ergebnis ist, dass 0x00 für das erste Byte 0x02 wird.

Daher ist der IPv6-Schnittstellen Bezeichner, der der Ethernet-MAC-Adresse 00-60-08-52-F9-D8 entspricht, 02-60-08-FF-FE-52-F9-D8.

Die Link-Local-Adresse eines Knotens ist die Kombination aus dem Präfix FE80::/64 und dem 64-Bit-Schnittstellen Bezeichner, der in IPv6-Doppelpunkt-hexadezimal Notation ausgedrückt wird. Daher ist die Link-Local-Adresse dieses Beispiel Knotens mit dem Präfix FE80::/64 und dem Schnittstellen Bezeichner 02-60-08-FF-FE-52-F9-D8 FE80:: 260:8ff: FE52: F9D8.

Sie können Ihre lokale Linkadresse mit IPv6 anzeigen, wie im folgenden Beispiel gezeigt:

**IPv6 if**

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

Schnittstelle 4 ist eine Schnittstelle, die einem installierten Ethernet-Adapter mit der Link-Local-Adresse FE80:: 210:5AFF: Feaa: 20A2 entspricht.

Weitere Informationen zur IPv6-Adressierung und eine Übersicht über IPv6-Konzepte finden Sie im Whitepaper Introduction to IPv6 (Einführung in das IPv6).

## <a name="testing-connectivity-between-two-link-local-hosts"></a>Testen der Konnektivität zwischen zwei Verbindungs lokalen Hosts

Sie können einen einfachen Ping (einen Austausch von ICMPv6-Echo Anforderungs-und Echo Antwort Nachrichten) durchführen, indem Sie IPv6 zwischen zwei Verbindungs lokalen Hosts verwenden.

**So Pingen Sie mithilfe von IPv6 zwischen zwei Verbindungs lokalen Hosts**

1.  Installieren Sie die Microsoft IPv6-Technologievorschau für Windows auf zwei Windows-Hosts (Host A und Host B), die sich auf demselben Link (Subnetz) befinden.
2.  Verwenden Sie IPv6 if auf Host A zum Abrufen der Link-Local-Adresse für die Ethernet-Schnittstelle.

    Beispiel: die Link-Local-Adresse von Host A ist FE80:: 210:5AFF: Feaa: 20A2.

3.  Verwenden Sie IPv6 if auf Host B zum Abrufen der Link-Local-Adresse für die Ethernet-Schnittstelle.

    Beispiel: die Link-Local-Adresse von Host B lautet FE80:: 260:97FF: FE02:6EA5.

4.  Pingen Sie Host B von Host a mithilfe Ping6.exe.

    Beispiel: ping6 FE80:: 260:97FF: FE02:6EA5

Sie können auch die Option Ping6.exe-s verwenden, um die Quelladresse anzugeben, von der die Echo Anforderungs Nachrichten gesendet werden. Um z. B. Echo Anforderungen von der IPv6-Adresse FE80:: 210:5AFF: Feaa: 20A2 an Host B zu senden, verwenden Sie den folgenden Befehl:

**ping6-s FE80:: 210:5AFF: Feaa: 20A2% 4 FE80:: 260:97FF: FE02:6EA5**

Beim Pingen einer Link-lokal-oder Site-Local-Adresse empfiehlt es sich, die Bereichs-ID anzugeben, damit die Zieladresse eindeutig ist. Die Notation zum Angeben der Bereichs-ID lautet Address% Scope-ID. Bei Link-Local-Adressen ist die Bereichs-ID gleich der Schnittstellen Nummer, wie im IPv6-Befehl "if" angezeigt. Bei Site-Local-Adressen ist die Bereichs-ID gleich der Standort Nummer, wie im IPv6-Befehl "if" angezeigt. Verwenden Sie z. b. den folgenden Befehl, um Echo Anforderungs Nachrichten an Host B mithilfe von Scope-ID 4 zu senden:

**ping6 FE80:: 260:97FF: FE02:6EA5% 4**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Empfohlene Konfigurationen für IPv6](recommended-configurations-2.md)
</dt> </dl>

 

 



