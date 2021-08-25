---
title: ALE-Ebenen
description: Application Layer Enforcement (ALE) besteht aus mehreren Filterebenen und vielen übereinstimmenden Verwerfensebenen.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9d13c7b5493171caa7216e8f2991e0350b79dd46dca612f241c9446cafa39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901010"
---
# <a name="ale-layers"></a>ALE-Ebenen

Die Anwendungsschichterzwingung (Application Layer Enforcement, ALE) besteht aus mehreren Filterebenen und vielen übereinstimmenden Verwerfensebenen. Alle Filtermodulebenen Windows Filterplattform (WFP), einschließlich ALE, werden unter Filtern von [**Ebenenbezeichnern beschrieben.**](management-filtering-layer-identifiers-.md) Dieses Thema enthält eine ausführlichere Beschreibung der Filterebenen, die Teil von ALE sind.

## <a name="resource_assignment"></a>\_RESSOURCENZUWEISUNG

Ein Filter auf [**der Ebene FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) wird für explizite oder implizite Netzwerkbindungsvorgänge zugeordnet.

Wenn ein Filter auf dieser Ebene zum Autorisieren der Erstellung von Unformatierten Sockets verwendet wird, wird das [**Flag FWP \_ CONDITION FLAG IS RAW \_ \_ \_ \_ ENDPOINT**](filtering-condition-flags-.md) festgelegt.

Wenn ein Filter auf dieser Ebene zum Autorisieren des Empfangs im promiscuous-Modus verwendet wird, wird das [**Feld FWP \_ CONDITION \_ ALE PROMISCUOUS MODE (ALE \_ PROMISCUOUS \_ MODE)**](filtering-condition-identifiers-.md) auf SIO \_ RCGAS festgelegt. Eine Beschreibung von SIO \_ RCALI Finden Sie unter [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).

> [!Note]  
> Dies ist die einzige Ebene, auf der der promiscuous-Modus gefiltert werden kann.

 

Wenn während **bind()** kein Port angegeben wird, d. h. port auf 0 (null) festgelegt ist, wählt der TCP/IP-Stapel einen Port aus dem dynamischen Portbereich (19152 bis 65535) aus. Der ausgewählte Port wird auf dieser Ebene zusammen mit dem [**FWP \_ CONDITION FLAG \_ IS \_ \_ WILDCARD \_ BIND-Flag**](filtering-condition-flags-.md) klassifiziert.

Wenn die lokale Adresse nicht im [**bind()-Aufruf**](/windows/desktop/api/winsock/nf-winsock-bind) angegeben ist, wird das lokale Adressfeld auf [**FWP \_ EMPTY festgelegt.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)

## <a name="auth_listen"></a>\_AUTHENTIFIZIERUNGS-LAUSCHEN

Ein Filter auf [**der Ebene FWPM \_ LAYER \_ ALE \_ AUTH LISTEN \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) wird für [**TCP-Listen()-Aufrufe**](/windows/desktop/api/winsock2/nf-winsock2-listen) zugeordnet.

## <a name="auth_recv_accept"></a>AUTH \_ RECV \_ ACCEPT

Ein Filter auf der [**Ebene FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) wird für TCP [**accept()-Aufrufe,**](/windows/desktop/api/winsock2/nf-winsock2-accept) für erste UDP-Pakete (Unicast) von einer eindeutigen Remoteadresse/port-Tupel und für erste eingehende ICMP-Nachrichten ohne Fehler (Unicast) mit einem eindeutigen ICMP-Typ, Code und einer eindeutigen ID zugeordnet.

> [!Note]  
> Protokolle, die nicht TCP oder ICMP sind, werden wie UDP behandelt.

 

TCP-Pakete, die von unformatierten Sockets empfangen werden, werden ähnlich wie UDP-Datenverkehr verarbeitet. Das heißt, dass nur der erste [**TCP-Sendetyp ()**](/windows/desktop/api/winsock2/nf-winsock2-send) und der erste TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) über unformatierte Sockets gefiltert werden.

## <a name="auth_connect"></a>AUTH \_ CONNECT

Ein Filter auf der [**Ebene FWPM \_ LAYER \_ ALE \_ AUTH CONNECT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) wird für TCP [**connect()-Aufrufe,**](/windows/desktop/api/winsock2/nf-winsock2-connect) für erste UDP-Pakete, die an eine eindeutige Remoteadresse und ein Eindeutiges Port-Tupel gesendet werden, und für erste ausgehende ICMP-Nachrichten ohne Fehler mit eindeutigem ICMP-Typ, -Code und -ID abgewendet.

> [!Note]  
> Protokolle, die nicht TCP oder ICMP sind, werden wie UDP behandelt.

 

Tcp-Pakete, die von unformatierten Sockets gesendet werden, werden ähnlich wie UDP-Datenverkehr verarbeitet. Das heißt, dass nur der erste [**TCP-Sendetyp ()**](/windows/desktop/api/winsock2/nf-winsock2-send) und der erste TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) über unformatierte Sockets gefiltert werden.

## <a name="flow_established"></a>FLOW \_ ESTABLISHED

Nach erfolgreichem Abschluss eines DREI-Wege-TCP-Handshakes wird ein Filter auf der [**Ebene FWPM \_ LAYER \_ ALE FLOW ESTABLISHED \_ \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) zugeordnet. Bei Nicht-TCP-Datenverkehr wird der Filter unmittelbar nach dem Abgleich von Filtern aus **den Ebenen AUTH \_ RECV \_ ACCEPT** oder **AUTH \_ CONNECT** übereinstimmen.

Ein Filter auf dieser Ebene sollte block oder permit nicht zurückgeben.

Diese Ebene wird von Callouttreibern zum Nachverfolgen des Verbindungszustands verwendet, der in der Dokumentation Windows [Driver Kit ausführlich beschrieben](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) wird.

## <a name="resource_release"></a>\_RESSOURCENFREIGABE

Ein Filter auf [**der Ebene FWPM \_ LAYER \_ ALE RESOURCE RELEASE \_ \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) wird nach der Freigabe von Ressourcen, die über **RESOURCE \_ ASSIGNMENT** zugeordnet wurden, zugeordnet.

## <a name="endpoint_closure"></a>\_ENDPUNKTABSCHLUSS

Ein Filter auf [**der Ebene FWPM \_ LAYER \_ ALE ENDPOINT CLOSURE \_ \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) wird abgewungen, wenn ein verbundener TCP-Fluss oder UDP-Socketendpunkt geschlossen wird.

## <a name="connect_redirect"></a>CONNECT \_ REDIRECT

Ein Filter auf [**der Ebene FWPM \_ LAYER \_ ALE CONNECT REDIRECT \_ \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) ermöglicht die Änderung von Remoteadressen und Ports. Die ausgehende Verbindung wird für die Dauer dieser Verbindung umgeleitet.

## <a name="bind_redirect"></a>\_BINDUNGSUMLEITUNG

Ein Filter auf [**der Ebene FWPM \_ LAYER \_ ALE BIND REDIRECT \_ \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) ermöglicht die Änderung der lokalen Adresse und ports des zugrunde liegenden Sockets. Der lokale Socket wird für die Lebensdauer des Sockets umgeleitet.

## <a name="ale-discard-layers"></a>ALE DISCARD-Ebenen

Für jede der oben beschriebenen ALE-Ebenen enthält die Filter-Engine eine übereinstimmende Verwerfensebene. Die ALE-Verwerfensebenen werden von Rückrufen zu Protokollierungszwecken verwendet. Pakete und Hinweise, die auf einer der ALE-Filterebenen verworfen wurden, werden für die entsprechende ALE-Verwerfensebene angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erzwingung der Anwendungsschicht (Application Layer Enforcement, ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Zustands behaftete ALE-Filterung](ale-stateful-filtering.md)
</dt> <dt>

[ALE-Multicast-/Broadcastdatenverkehr](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Erneute ALE-Autorisierung](ale-re-authorization.md)
</dt> <dt>

[ALE Flow Anpassung](ale-flow-customization.md)
</dt> <dt>

[TCP-Paketflüsse](tcp-packet-flows.md)
</dt> <dt>

[UDP-Paketflüsse](udp-packet-flows.md)
</dt> <dt>

[Winsock-Funktionen](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[**Filterbedingungsflags**](filtering-condition-flags-.md)
</dt> <dt>

[**Filterbedingungen, die auf jeder Filterebene verfügbar sind**](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 