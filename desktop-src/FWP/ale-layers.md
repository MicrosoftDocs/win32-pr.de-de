---
title: ALE Ebenen
description: Die Durchsetzung der Anwendungsschicht (ALE) besteht aus mehreren Filter Ebenen und vielen übereinstimmenden Verwerfungs Ebenen.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a96e3b2ae5092bf8cca014eb3603eea5efe8f71
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314721"
---
# <a name="ale-layers"></a>ALE Ebenen

Die Durchsetzung der Anwendungsschicht (ALE) besteht aus mehreren Filter Ebenen und vielen übereinstimmenden Verwerfungs Ebenen. Alle Windows Filtering Platform (WFP)-Filter-Engine-Ebenen (einschließlich ALE) werden unter [**Filtern von ebenenbezeichern**](management-filtering-layer-identifiers-.md)beschrieben. Dieses Thema enthält eine ausführlichere Beschreibung der Filter Ebenen, die Teil von ALE sind.

## <a name="resource_assignment"></a>Ressourcen \_ Zuweisung

Ein Filter auf der Ebene der Ebene der [**\_ Ebene der Ebene der \_ \_ Ressourcen \_ Zuweisung \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) wird für Netzwerk Bindungs Vorgänge, explizit oder implizit, abgeglichen.

Wenn ein Filter auf dieser Ebene mit der Autorisierung der rohsocket Erstellung übereinstimmt, wird das FWP-Bedingungs Kennzeichen festgelegt. [**\_ \_ \_ \_ \_**](filtering-condition-flags-.md)

Wenn ein Filter auf dieser Ebene mit dem Autorisierungs Modus für den gemischten-Modus übereinstimmt, wird das Feld [**FWP Condition ALE in der "FWP \_ Condition \_ ALE \_ \_**](filtering-condition-identifiers-.md) " auf "sio \_ rcvall" festgelegt. Eine Beschreibung von "sio \_ rcvall" finden Sie unter [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).

> [!Note]  
> Dies ist die einzige Schicht, in der der gemischten-Modus gefiltert werden kann.

 

Wenn während **Bind ()** kein Port angegeben ist, d. h., Port wird auf 0 (null) festgelegt, dann wählt der TCP/IP-Stapel einen Port aus dem dynamischen Port Bereich aus (19152 – 65535). Der ausgewählte Port wird auf dieser Ebene klassifiziert, und das FWP-Bedingungs Kennzeichen ist ein Platzhalter- [**\_ \_ \_ \_ \_ Bindungsflag**](filtering-condition-flags-.md) .

Wenn die lokale Adresse nicht im [**Bind ()**](/windows/desktop/api/winsock/nf-winsock-bind) -Befehl angegeben ist, wird das Feld für die lokale Adresse auf [**FWP \_ empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)festgelegt.

## <a name="auth_listen"></a>auth \_ lauschen

Bei TCP-Abhör aufrufen [**()**](/windows/desktop/api/winsock2/nf-winsock2-listen) wird ein Filter auf der Ebene der Ebene " [**lwpm \_ Layer ALE auth" der Ebene " \_ \_ \_ \_ {4 \| 6}**](management-filtering-layer-identifiers-.md) " abgeglichen.

## <a name="auth_recv_accept"></a>Autorisierung über \_ \_ nehmen

Ein Filter auf der Ebene der swpm-Layer-ALE-Authentifizierungs-e/A-Version " [**\_ \_ \_ \_ \_ Accept \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) " wird für TCP- [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) -Aufrufe mit einem eindeutigen ICMP-Paket (Unicast) aus einem eindeutigen Remote Adress-/porttupel und für erste eingehende nicht Fehler-ICMP-Nachrichten (Unicast) mit einem eindeutigen IC

> [!Note]  
> Protokolle, die nicht TCP oder ICMP lauten, werden wie UDP behandelt.

 

Von unformatierten Sockets empfangene TCP-Pakete werden ähnlich wie UDP-Datenverkehr behandelt. Das heißt, dass nur das erste TCP [**Send ()**](/windows/desktop/api/winsock2/nf-winsock2-send) und das erste TCP- [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) über Unformatierte Sockets gefiltert werden.

## <a name="auth_connect"></a>Authentifizierung \_ herstellen

Bei TCP [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) -aufrufen wird ein Filter auf der [**fwpm \_ Layer ALE-Authentifizierung \_ \_ \_ Connect \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) für die ersten UDP-Pakete, die an eine eindeutige Remote Adresse und einen Port-Tupel gesendet werden, sowie für erste ausgehende, nicht Fehler-ICMP-Nachrichten mit einem eindeutigen ICMP-Typ, Code und der ID abgeglichen.

> [!Note]  
> Protokolle, die nicht TCP oder ICMP lauten, werden wie UDP behandelt.

 

Von rohsockets gesendete TCP-Pakete werden ähnlich wie UDP-Datenverkehr behandelt. Das heißt, dass nur das erste TCP [**Send ()**](/windows/desktop/api/winsock2/nf-winsock2-send) und das erste TCP- [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) über Unformatierte Sockets gefiltert werden.

## <a name="flow_established"></a>Flow \_ eingerichtet

Nach erfolgreichem Abschluss eines TCP-drei-Wege-Handshakes wird ein Filter auf der Ebene der auf dem [**WPM- \_ Schicht eingerichteten Ebene, der die \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) -Schicht erreicht hat Bei nicht-TCP-Datenverkehr wird der Filter unmittelbar nach dem Abgleich von Filtern von Authentifizierungs-oder Authentifizierungs **\_ Verbindungs** Ebenen abgeglichen. **\_ \_**

Ein Filter auf dieser Ebene sollte weder Block noch zulassen zurückgeben.

Diese Ebene wird von Legenden Treibern verwendet, um den Verbindungsstatus zu verfolgen, der in der Dokumentation zum [Windows-Treiberkit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) ausführlich beschrieben wird.

## <a name="resource_release"></a>Ressourcen \_ Freigabe

Nach dem Freigeben von Ressourcen, die über die **Ressourcen \_ Zuweisung** zugewiesen wurden, wird ein Filter auf der Ebene der Ebene der Ebene der [**Ebene der Ebene der Ebene der Ebene " \_ \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) " zugeordnet.

## <a name="endpoint_closure"></a>Endpunkt \_ Schließung

Beim Schließen eines verbundenen TCP-Flows oder eines UDP-Sockets-Endpunkts wird ein Filter auf der Ebene des SWF- [**Endpunkts der swpm-Ebene für den \_ \_ \_ Endpunkt \_ \_ \|**](management-filtering-layer-identifiers-.md) geschlossen.

## <a name="connect_redirect"></a>\_Umleitung verbinden

Ein Filter auf der Ebene der Ebene der [**swpm-Schicht für die \_ \_ \_ Verbindungs \_ Umleitung \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) ermöglicht die Änderung von Remote Adressen und Ports. Die ausgehende Verbindung wird für die Dauer der Verbindung umgeleitet.

## <a name="bind_redirect"></a>\_Umleitung binden

Ein Filter auf der Ebene der Ebene der [**swpm-Ebene der EM- \_ \_ \_ Bindungs \_ Umleitung \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) ermöglicht die Änderung der lokalen Adresse und Ports des zugrunde liegenden Sockets. Der lokale Socket wird für die Lebensdauer des Sockets umgeleitet.

## <a name="ale-discard-layers"></a>ALE Verwerfen von Ebenen

Für jede der oben beschriebenen ALE-Ebenen enthält die Filter-Engine eine passende Verwerfungs Ebene. Die ALE-Verwerfungs Ebenen werden von Legenden für Protokollierungs Zwecke verwendet. Pakete und Hinweise, die auf einer der ALE-Filter Ebenen verworfen wurden, werden der entsprechenden ALE-verworfungs Schicht angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Durchsetzung der Anwendungsschicht (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Status behaftete ALE Filterung](ale-stateful-filtering.md)
</dt> <dt>

[ALE Multicast-/Broadcast Datenverkehr](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Erneute ALE-Autorisierung](ale-re-authorization.md)
</dt> <dt>

[Anpassung des ALE-Flows](ale-flow-customization.md)
</dt> <dt>

[TCP-paketflows](tcp-packet-flows.md)
</dt> <dt>

[UDP-paketflows](udp-packet-flows.md)
</dt> <dt>

[Winsock-Funktionen](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[**Filtern von Bedingungs Flags**](filtering-condition-flags-.md)
</dt> <dt>

[**Filterbedingungen, die auf jeder Filter Ebene verfügbar sind**](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 