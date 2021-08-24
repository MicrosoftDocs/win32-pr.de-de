---
title: UDP-Paketflüsse
description: Die Reihenfolge, in der die Ebenen der WFP-Filter-Engine (Windows Filtering Platform) während einer typischen UDP-Sitzung durchlaufen werden.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e850f67bce9a001d41ebb54b17d3d0d86b94b22f083529e4589d6b69841b7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746640"
---
# <a name="udp-packet-flows"></a>UDP-Paketflüsse

In diesem Abschnitt wird die Reihenfolge beschrieben, in der die Ebenen der WFP-Filter-Engine (Windows Filtering Platform) während einer typischen UDP-Sitzung durchlaufen werden.

> [!Note]  
> UDP-Paketflüsse für IPv6 folgen dem gleichen Muster wie für IPv4.

 

> [!Note]  
> Alle Nicht-TCP-Paketflüsse folgen dem gleichen Muster wie UDP-Paketflüsse.

 

## <a name="udp-connection-establishment"></a>Einrichtung der UDP-Verbindung

<dl> Server (Empfänger) führt passives Öffnen aus

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (nur Windows 7/Windows Server 2008 R2)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4

  
Client (Absender) führt Active Open aus

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (nur Windows 7/Windows Server 2008 R2)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4
-   sendto: FWPM \_ LAYER \_ ALE \_ CONNECT REDIRECT \_ \_ V4 (nur Windows 7/Windows Server 2008 R2)
-   sendto: FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   data: FWPM \_ LAYER \_ DATAGRAM \_ DATA \_ V4
-   UDP-Nachricht: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   IP-Datagramme: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

  
Server

-   IP-Datagramme: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   UDP-Nachricht: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   UDP-Nachricht: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   data: FWPM \_ LAYER \_ DATAGRAM \_ DATA \_ V4

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a>Empfangene UDP-Nachricht ohne Überwachung des Ports oder Protokolls

Server (Empfänger)

-   IP-Datagramme: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   IP-Datagramme: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4 \_ DISCARD
-   ICMP Dest Unreachable: FWPM \_ LAYER \_ OUTBOUND \_ ICMP \_ ERROR \_ V4
-   ICMP Dest Unreachable: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   ICMP Dest Unreachable: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

> [!Note]  
> UDP ohne Endpunkt wird bei DER IPPACKET-Verwerfung mit einer bestimmten Fehlerbedingung angegeben. Blockieren Sie dieses Paket bei DER IPPACKET-Verwerfung, damit der Stapel das entsprechende Ereignis nicht sendet (ICMP-Fehler).

 

## <a name="successful-reauthorization-of-a-udp-packet"></a>Erfolgreiche erneute Authentifizierung eines UDP-Pakets

Server (Empfänger)

-   IP-Datagramme: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   UDP-Nachricht: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   UDP-Nachricht: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   UDP-Nachricht: FWPM \_ LAYER \_ DATAGRAM \_ DATA \_ V4(INBOUND)

## <a name="failed-reauthorization-of-a-udp-packet"></a>Fehler bei der erneuten Authentifizierung eines UDP-Pakets

Server (Empfänger)

-   IP-Datagramme: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   UDP-Nachricht: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   UDP-Nachricht: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   UDP-Nachricht: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4 \_ DISCARD

## <a name="udp-connection-termination"></a>UDP-Verbindungsbeendigung

UDP-Verbindungsbeendigung ist auf keiner WFP-Ebene angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erneute ALE-Autorisierung](ale-re-authorization.md)
</dt> <dt>

[**Filtern von Ebenenbezeichnern**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




