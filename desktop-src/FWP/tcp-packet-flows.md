---
title: TCP-Paketflüsse
description: Die Reihenfolge, in der die Ebenen der WFP-Filter-Engine (Windows Filtering Platform) während einer typischen TCP-Sitzung durchlaufen werden.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d4836da7a1912a6e39358b54e2a3086dd80efe844d6a301d079014d4a5b209
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746630"
---
# <a name="tcp-packet-flows"></a>TCP-Paketflüsse

In diesem Abschnitt wird die Reihenfolge beschrieben, in der die Ebenen der WFP-Filter-Engine (Windows Filtering Platform) während einer typischen TCP-Sitzung durchlaufen werden.

> [!Note]  
> TCP-Paketflüsse für IPv6 folgen dem gleichen Muster wie für IPv4.

 

> [!Note]  
> Nicht-TCP-Paketflüsse folgen dem gleichen Muster wie [UDP-Paketflüsse.](udp-packet-flows.md)

 

## <a name="tcp-connection-establishment"></a>TCP-Verbindungseinrichtung

<dl> Server (Empfänger) führt passives Öffnen aus

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (nur Windows 7/Windows Server 2008 R2)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4
-   listen: FWPM \_ LAYER \_ ALE \_ AUTH \_ LISTEN \_ V4

  
Client (Absender) führt Active Open aus

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (nur Windows 7/Windows Server 2008 R2)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4
-   connect: FWPM \_ LAYER \_ ALE \_ CONNECT REDIRECT \_ \_ V4 (nur Windows 7/Windows Server 2008 R2)
-   connect: FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V4
-   SYN: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   SYN: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

  
Server

-   SYN: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   SYN: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   SYN: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   SYN-ACK: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   SYN-ACK: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

  
Client

-   SYN-ACK: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   SYN-ACK: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   ACK: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   ACK: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

  
Server

-   ACK: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   ACK: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   Das Lauschen ist abgeschlossen. Der Server kann eine Annahme ausführen.

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a>TCP SYN Received with No One Listening on the Port or Protocol

Server (Empfänger)

-   SYN: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   SYN: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4 \_ DISCARD
-   RST: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   RST: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

> [!Note]  
> TCP SYN ohne Endpunkt wird bei TRANSPORT discard mit einer bestimmten Fehlerbedingung angegeben. Blockieren Sie dieses Paket bei TRANSPORT discard, um zu bewirken, dass der Stapel das entsprechende Ereignis (RST) nicht sendet. Ein Beispiel für die Filterung im geschütztem Modus finden Sie unter [Verhindern der Portüberprüfung.](preventing-port-scanning.md)

 

## <a name="data-transmitted-over-a-tcp-connection"></a>Über eine TCP-Verbindung übertragene Daten

<dl> Client (Absender)

-   Send
-   data: FWPM \_ LAYER \_ STREAM \_ V4
-   TCP-Segmente: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   IP-Datagramme: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

  
Server (Empfänger)

-   IP-Datagramme: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   TCP-Segmente: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   data: FWPM \_ LAYER \_ STREAM \_ V4
-   Die Daten sind zum Lesen verfügbar.

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a>Erfolgreiche erneute Authentifizierung eines TCP-Pakets

Server (Empfänger)

-   IP-Datagramme: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   TCP-Segment: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   TCP-Segment: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   data: FWPM \_ LAYER \_ STREAM \_ V4(INBOUND)

## <a name="failed-reauthorization-of-a-tcp-packet"></a>Fehler bei der erneuten Authentifizierung eines TCP-Pakets

Server (Empfänger)

-   IP-Datagramme: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   TCP-Segment: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   TCP-Segment: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   TCP-Segment: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4 \_ DISCARD

## <a name="tcp-connection-termination"></a>TCP-Verbindungsbeendigung

Tcp-Verbindungsbeendigung ist auf keiner WFP-Ebene angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erneute ALE-Autorisierung](ale-re-authorization.md)
</dt> <dt>

[**Filtern von Ebenenbezeichnern**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




