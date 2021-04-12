---
title: UDP-paketflows
description: Die Reihenfolge, in der die Ebenen der Filter-Engine der Windows-Filter Plattform (WFP) während einer typischen UDP-Sitzung durchlaufen werden.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790de49e971d5506c1732b9c4d30b88643c7af0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310695"
---
# <a name="udp-packet-flows"></a>UDP-paketflows

In diesem Abschnitt wird die Reihenfolge beschrieben, in der die Ebenen der Filter-Engine der Windows-Filter Plattform (WFP) während einer typischen UDP-Sitzung durchlaufen werden.

> [!Note]  
> UDP-paketflows für IPv6 folgen dem gleichen Muster wie für IPv4.

 

> [!Note]  
> Alle nicht-TCP-Paket Flüsse folgen dem gleichen Muster wie UDP-paketflows.

 

## <a name="udp-connection-establishment"></a>UDP-Verbindungs Einrichtung

<dl> Der Server (Empfänger) führt ein passives öffnen aus.

-   BIND: auf der swpm \_ -Schicht ist die \_ \_ \_ Umleitung \_ V4 (nur Windows 7/Windows Server 2008 R2)
-   BIND: f- \_ \_ \_ Ressourcen \_ Zuweisung \_ der Ebene "f"

  
Der Client (Absender) führt aktive offene Vorgänge aus.

-   BIND: auf der swpm \_ -Schicht ist die \_ \_ \_ Umleitung \_ V4 (nur Windows 7/Windows Server 2008 R2)
-   BIND: f- \_ \_ \_ Ressourcen \_ Zuweisung \_ der Ebene "f"
-   SendTo: fwpm \_ Layer \_ ALE \_ Verbindungs \_ Umleitung \_ V4 (nur Windows 7/Windows Server 2008 R2)
-   SendTo: fwpm \_ Layer \_ ALE \_ auth \_ Connect \_ v4
-   Lwpm- \_ Schicht- \_ ALE Daten \_ Fluss \_ festgelegt \_
-   Daten: \_ \_ Datagramm-Daten von Datagramm-Daten, \_ \_ v4
-   UDP-Meldung: ausgehender Transport-WPM- \_ \_ \_ Transport \_ v4
-   IP-Datagramme: WPM-Ebene ausgehend von \_ \_ \_ ippacket \_ v4

  
Server

-   IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4
-   UDP-Nachricht: \_ \_ eingehender \_ Transport \_ von der WPM-Schicht
-   UDP-Nachricht: Abbild-e/a-Version der \_ \_ \_ \_ v \_ \_ -Version
-   Lwpm- \_ Schicht- \_ ALE Daten \_ Fluss \_ festgelegt \_
-   Daten: \_ \_ Datagramm-Daten von Datagramm-Daten, \_ \_ v4

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a>Es wurde eine UDP-Nachricht empfangen, die nicht auf dem Port oder Protokoll lauscht.

Server (Empfänger)

-   IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4
-   IP-Datagramme: auf der WPM- \_ Schicht \_ eingehende \_ ippacket \_ V4 \_ verwerfen
-   ICMP dest nicht erreichbar: \_ \_ \_ ICMP- \_ Fehler \_ V4 in fwpm-Schicht
-   ICMP dest nicht erreichbar: ausgehender Transport-fwpm- \_ \_ \_ Transport \_ v4
-   ICMP dest nicht erreichbar: fwpm-Schicht ausgehend von \_ \_ \_ ippacket \_ v4

> [!Note]  
> UDP ohne Endpunkt wird mit einem bestimmten Fehlerzustand in "ippacket Discard" angegeben. Blockieren Sie dieses Paket bei der "ippacket"-Verwerfungs Methode, damit der Stapel das entsprechende Ereignis nicht sendet (ICMP-Fehler).

 

## <a name="successful-reauthorization-of-a-udp-packet"></a>Erfolgreiche erneute Autorisierung eines UDP-Pakets

Server (Empfänger)

-   IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4
-   UDP-Nachricht: \_ \_ eingehender \_ Transport \_ von der WPM-Schicht
-   UDP-Nachricht: Abbild-e/a-Version der \_ \_ \_ \_ v \_ \_ -Version
-   UDP-Nachricht: \_ \_ Datagramm-Datagramm-Datagrammdaten \_ \_ V4 (eingehend)

## <a name="failed-reauthorization-of-a-udp-packet"></a>Fehler bei der erneuten Autorisierung eines UDP-Pakets.

Server (Empfänger)

-   IP-Datagramme: WPM- \_ Schicht \_ eingehender \_ ippacket \_ v4
-   UDP-Nachricht: \_ \_ eingehender \_ Transport \_ von der WPM-Schicht
-   UDP-Nachricht: Abbild-e/a-Version der \_ \_ \_ \_ v \_ \_ -Version
-   UDP-Nachricht: die Standard Authentifizierung der \_ v-Layer- \_ \_ \_ v \_ \_ \_ -Version

## <a name="udp-connection-termination"></a>Beenden der UDP-Verbindung

Die UDP-Verbindungs Beendigung wird in keiner WFP-Schicht angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erneute ALE-Autorisierung](ale-re-authorization.md)
</dt> <dt>

[**Filtern von ebenenbezeichgern**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




