---
description: Windows Sockets ermöglicht die Multicastlistenerermittlung (MLD) unter IPv6 und das Internet Group Management Protocol (IGMP) unter IPv4 für Multicastanwendungen mithilfe von Socketoptionen und IOCTLs.
ms.assetid: a5de4273-e86e-4f13-b068-256cb38706d4
title: MLD und IGMP mit Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2c550cf2c1463f5b646efc286c05010274d3cb44e13b9559302452bccb81c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051648"
---
# <a name="mld-and-igmp-using-windows-sockets"></a>MLD und IGMP mit Windows Sockets

Windows Sockets ermöglicht die Multicastlistenerermittlung (MLD) unter IPv6 und das Internet Group Management Protocol (IGMP) unter IPv4 für Multicastanwendungen mithilfe von Socketoptionen und IOCTLs. Auf dieser Seite werden die Socketoptionen beschrieben, die die Multicastprogrammierung ermöglichen, und ihre Verwendung beschrieben. Definitionen der einzelnen Socketoptionen finden Sie auf der Seite [Socketoptionen.](socket-options.md)

Informationen zur Verwendung von IOCTLs für die Multicastprogrammierung finden Sie unter [Final-State-Based Multicast Programming](final-state-based-multicast-programming.md) weiter unten in diesem Abschnitt.

Unter Windows Vista und höher ist eine Reihe von Socketoptionen für die Multicastprogrammierung verfügbar, die IPv6- und IPv4-Adressen unterstützen. Diese Socketoptionen sind IP-unabhängig und können sowohl für IPv6 als auch für IPv4 verwendet werden. Unter IPv6 verwenden diese Socketoptionen MLDv2. Unter IPv4 verwenden diese Socketoptionen IGMPv3. Diese ipunabhängigen Optionen sind die bevorzugten Socketoptionen für die Multicastprogrammierung Windows Vista und höher. Windows Sockets verwendet die folgenden Socketoptionen: 

| Socketoption               | Argumenttyp                                            |
|-----------------------------|----------------------------------------------------------|
| \_MCAST-BLOCKQUELLE \_        | [**GROUP \_ SOURCE \_ REQ-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| MCAST \_ JOIN \_ GROUP          | [**GROUP \_ REQ-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req)                |
| MCAST \_ JOIN \_ SOURCE \_ GROUP  | [**GROUP \_ SOURCE \_ REQ-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| MCAST \_ LEAVE \_ GROUP         | [**GROUP \_ REQ-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req)                |
| \_MCAST– \_ QUELLGRUPPE \_ VERLASSEN | [**GROUP \_ SOURCE \_ REQ-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| MCAST \_ UNBLOCK \_ SOURCE      | [**GROUP \_ SOURCE \_ REQ-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |



 

Für die Multicastprogrammierung, die nur IPv6-Adressen unterstützt, stehen verschiedene Socketoptionen zur Verfügung. Diese Socketoptionen verwenden MLDv1 oder MLDv2. Die verwendete MLD-Version hängt von der Version des Windows. MLDv2 wird unter Windows Vista und höher unterstützt. Windows Sockets verwendet die folgenden Socketoptionen: 

| Socketoption          | Argumenttyp                             |
|------------------------|-------------------------------------------|
| IPV6– \_ MITGLIEDSCHAFT \_ HINZUFÜGEN  | [**ipv6 \_ mreq-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |
| IPV6 \_ DROP \_ MEMBERSHIP | [**ipv6 \_ mreq-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |



 

Eine Reihe von Socketoptionen sind für die Multicastprogrammierung verfügbar, die nur IPv4-Adressen unterstützen. Diese Socketoptionen verwenden IGMPv3 oder IGMPv2. Die verwendete IGMP-Version hängt von der Version des Windows. IGMPv3 wird unter Windows Vista und höher unterstützt. Windows Sockets verwendet die folgenden Socketoptionen:

| Socketoption                | Argumenttyp                                        |
|------------------------------|------------------------------------------------------|
| \_IP-MITGLIEDSCHAFT \_ HINZUFÜGEN          | [**ip \_ mreq-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| \_IP-ADRESSE: \_ \_ QUELLMITGLIEDSCHAFT HINZUFÜGEN  | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) structure |
| \_ \_ IP-BLOCKQUELLE            | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) structure |
| IP \_ DROP \_ MEMBERSHIP         | [**ip \_ mreq-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| IP \_ DROP \_ SOURCE \_ MEMBERSHIP | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) structure |
| \_ \_ IP-ENTSPERRUNGSQUELLE          | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) structure |



 

Wenn IGMPv3 verfügbar ist, werden die Optionen IP \_ ADD \_ SOURCE \_ MEMBERSHIP, IP BLOCK SOURCE, IP DROP SOURCE MEMBERSHIP und IP UNBLOCK SOURCE effizienter verarbeitet, da der Router die Filterung verarbeiten \_ \_ \_ \_ \_ \_ \_ kann. Wenn nur IGMPv2 verfügbar ist, muss der Host die Filterung verarbeiten.

Es gibt zwei Kategorien, in die die meisten Anwendungen wahrscheinlich fallen: "any-source" und "controlled-source".

-   **Alle Quellanwendungen** akzeptieren standardmäßig alle Quellen, sodass einzelne Quellen nach Bedarf deaktiviert werden können. Ein Beispiel für eine Any-Source-Anwendung ist ein Videokonferenzaufruf, der allen Empfängern die Teilnahme ermöglicht.
-   **Anwendungen mit kontrollierter** Quelle beschränken Quellen auf eine bestimmte Liste, z. B. einen Internetsender oder die Übertragung eines wichtigen Ereignisses. Der Prozess der Verwendung von Socketoptionen ist für jede etwas anders.

Unter Windows Vista und höher gelten die folgenden Schritte für Alle-Quellanwendungen:

- Verwenden **Sie MCAST \_ JOIN \_ GROUP,** um einer Gruppe bei beitritten.  
- Verwenden **Sie MCAST \_ BLOCK \_ SOURCE,** um eine bestimmte Quelle bei Bedarf zu deaktivieren.  
- Verwenden **Sie MCAST \_ UNBLOCK \_ SOURCE,** um eine blockierte Quelle bei Bedarf erneut zu erlauben.  
- Verwenden **Sie MCAST \_ LEAVE \_ GROUP,** um die Gruppe zu verlassen.  

Unter Windows Vista und höher gelten die folgenden Schritte für Anwendungen mit kontrollierter Quelle:

- Verwenden **Sie MCAST \_ JOIN SOURCE \_ \_ GROUP,** um jedes Gruppen-/Quellpaar zu verbinden.  
- Verwenden **Sie MCAST \_ LEAVE SOURCE \_ \_ GROUP,** um jede Gruppe/Quelle zu verlassen, oder verwenden Sie **MCAST LEAVE \_ \_ GROUP,** um alle Quellen zu verlassen, wenn dieselbe Gruppenadresse von allen Quellen verwendet wird.  

Die folgenden Schritte gelten für Alle-Quellanwendungen:

- Verwenden Sie **IP \_ ADD \_ MEMBERSHIP** zum Beitreten zu einer Gruppe (**IPV6 \_ ADD \_ MEMBERSHIP** for IPv6).  
- Verwenden **Sie IP BLOCK \_ \_ SOURCE,** um eine bestimmte Quelle bei Bedarf zu deaktivieren.  
- Verwenden **Sie IP \_ UNBLOCK \_ SOURCE,** um eine blockierte Quelle bei Bedarf erneut zu erlauben.  
- Verwenden **Sie IP DROP \_ \_ MEMBERSHIP,** um die Gruppe **(IPV6 \_ DROP \_ MEMBERSHIP** für IPv6) zu verlassen.  

Die folgenden Schritte gelten für Anwendungen mit kontrollierter Quelle:

- Verwenden Sie **IP \_ ADD SOURCE \_ \_ MEMBERSHIP,** um die einzelnen Gruppen-/Quellpaare zu verbinden.  
- Verwenden **Sie IP DROP SOURCE \_ \_ \_ MEMBERSHIP,** um jede Gruppe/Quelle zu verlassen, oder verwenden Sie **IP DROP \_ \_ MEMBERSHIP,** um alle Quellen zu verlassen, wenn dieselbe Gruppenadresse von allen Quellen verwendet wird.  

Der Reihenfolge, in der diese Socketoptionen festgelegt werden, sind Regeln zugeordnet. Informationen und Informationen zur Problembehandlung bei Multicastsocketoptionen finden Sie unter [Verhalten der Multicastsocketoption](multicast-socket-option-behavior.md).
