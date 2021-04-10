---
title: TCP-paketflows
description: Die Reihenfolge, in der die Ebenen der Filter-Engine der Windows-Filter Plattform (WFP) während einer typischen TCP-Sitzung durchlaufen werden.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2203ccb4b2793983bd5b1052d53c2700d3033a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947887"
---
# <a name="tcp-packet-flows"></a>TCP-paketflows

In diesem Abschnitt wird die Reihenfolge beschrieben, in der die Ebenen der Filter-Engine der Windows-Filter Plattform (WFP) während einer typischen TCP-Sitzung durchlaufen werden.

> [!Note]  
> Bei TCP-Paket Flüssen für IPv6 folgt dasselbe Muster wie für IPv4.

 

> [!Note]  
> Nicht-TCP-Paket Flüsse folgen dem gleichen Muster wie [UDP-paketflows](udp-packet-flows.md).

 

## <a name="tcp-connection-establishment"></a>TCP-Verbindungs Einrichtung

<dl> Der Server (Empfänger) führt ein passives öffnen aus.

-   BIND: auf der swpm \_ -Schicht ist die \_ \_ \_ Umleitung \_ V4 (nur Windows 7/Windows Server 2008 R2)
-   BIND: f- \_ \_ \_ Ressourcen \_ Zuweisung \_ der Ebene "f"
-   lauschen: lwpm \_ Layer \_ ALE \_ auth \_ hört \_ v4

  
Der Client (Absender) führt aktive offene Vorgänge aus.

-   BIND: auf der swpm \_ -Schicht ist die \_ \_ \_ Umleitung \_ V4 (nur Windows 7/Windows Server 2008 R2)
-   BIND: f- \_ \_ \_ Ressourcen \_ Zuweisung \_ der Ebene "f"
-   Verbindung: swpm \_ -Schicht- \_ \_ Verbindungs \_ Umleitung \_ V4 (nur Windows 7/Windows Server 2008 R2)
-   verbinden: f-v-Schicht-Authentifizierung \_ \_ \_ \_ Connect \_ v4
-   SYN: \_ \_ ausgehender \_ Transport \_ der WPM-Schicht
-   SYN: WPM- \_ Schicht ausgehend von \_ \_ ippacket \_ v4

  
Server

-   SYN: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4
-   SYN: WPM- \_ Schicht \_ eingehender \_ Transport \_ v4
-   SYN: Abbild-e/a- \_ Ebene der \_ \_ \_ v \_ \_ -Version
-   SYN-ACK: \_ \_ ausgehender \_ Transport-Transport \_ der WPM-Schicht
-   SYN-ACK: WPM- \_ Schicht ausgehend von \_ \_ ippacket \_ v4

  
Client

-   SYN-ACK: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4
-   SYN-ACK: WPM- \_ Schicht \_ eingehender \_ Transport \_ v4
-   Lwpm- \_ Schicht- \_ ALE Daten \_ Fluss \_ festgelegt \_
-   ACK: \_ \_ ausgehender \_ Transport \_ der WPM-Schicht
-   ACK: WPM- \_ Schicht ausgehend von \_ \_ ippacket \_ v4

  
Server

-   ACK: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4
-   Bestätigung: \_ \_ eingehender \_ Transport \_ von der WPM-Schicht
-   Lwpm- \_ Schicht- \_ ALE Daten \_ Fluss \_ festgelegt \_
-   Lauschen ist abgeschlossen. Der Server kann eine Annahme durchführen.

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a>TCP-SYN empfangen, ohne dass der Port oder das Protokoll überwacht wird.

Server (Empfänger)

-   SYN: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4
-   SYN: WPM- \_ Schicht \_ eingehender \_ Transport \_ V4 \_ verwerfen
-   RST: \_ \_ ausgehender \_ Transport \_ der WPM-Schicht
-   RST: WPM- \_ Ebene ausgehend von \_ \_ ippacket \_ v4

> [!Note]  
> TCP-SYN ohne Endpunkt wird bei Transport verwerfen mit einem bestimmten Fehlerzustand angegeben. Blockieren Sie dieses Paket bei Transport verwerfen, damit der Stapel nicht das entsprechende Ereignis (RST) sendet. Ein Beispiel für die Filterung im Geheimnis Modus finden Sie unter [verhindern von Port Scans](preventing-port-scanning.md).

 

## <a name="data-transmitted-over-a-tcp-connection"></a>Über eine TCP-Verbindung übertragene Daten

<dl> Client (Absender)

-   Send
-   Daten: WPM \_ Layer \_ Stream \_ v4
-   TCP-Segmente: \_ \_ ausgehender \_ Transport \_ der WPM-Schicht
-   IP-Datagramme: WPM-Ebene ausgehend von \_ \_ \_ ippacket \_ v4

  
Server (Empfänger)

-   IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4
-   TCP-Segmente: \_ \_ eingehender \_ Transport \_ der WPM-Schicht
-   Daten: WPM \_ Layer \_ Stream \_ v4
-   Daten sind zum Lesen verfügbar.

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a>Erfolgreiche erneute Autorisierung eines TCP-Pakets

Server (Empfänger)

-   IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4
-   TCP-Segment: \_ \_ eingehender \_ Transport \_ von der WPM-Schicht
-   TCP-Segment: Abbild-e/a-Version der Abbild Version \_ \_ \_ \_ \_ \_ v4
-   Daten: WPM- \_ \_ ebenenstream \_ V4 (eingehend)

## <a name="failed-reauthorization-of-a-tcp-packet"></a>Fehler bei der erneuten Autorisierung eines TCP-Pakets.

Server (Empfänger)

-   IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4
-   TCP-Segment: \_ \_ eingehender \_ Transport \_ von der WPM-Schicht
-   TCP-Segment: Abbild-e/a-Version der Abbild Version \_ \_ \_ \_ \_ \_ v4
-   TCP-Segment: f-v-Ebene der Abbild \_ \_ \_ \_ \_ Annahme \_ \_

## <a name="tcp-connection-termination"></a>Beenden der TCP-Verbindung

Die Beendigung der TCP-Verbindung wird in keiner WFP-Schicht angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erneute ALE-Autorisierung](ale-re-authorization.md)
</dt> <dt>

[**Filtern von ebenenbezeichgern**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




