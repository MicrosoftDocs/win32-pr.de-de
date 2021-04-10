---
description: Windows Sockets ermöglicht die Multicast-listenerermittlung (MLD) in IPv6 und das Internet Group Management-Protokoll (IGMP) auf IPv4 für Multicast Anwendungen durch die Verwendung von Socketoptionen und IOCTLs.
ms.assetid: a5de4273-e86e-4f13-b068-256cb38706d4
title: MLD und IGMP mithilfe von Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6cb9f9c345463e283adea0136037d7ccd03cebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214593"
---
# <a name="mld-and-igmp-using-windows-sockets"></a>MLD und IGMP mithilfe von Windows Sockets

Windows Sockets ermöglicht die Multicast-listenerermittlung (MLD) in IPv6 und das Internet Group Management-Protokoll (IGMP) auf IPv4 für Multicast Anwendungen durch die Verwendung von Socketoptionen und IOCTLs. Auf dieser Seite werden die Socketoptionen beschrieben, die Multicast Programmierung ermöglichen, und es wird beschrieben, wie Sie verwendet werden. Informationen zu den Definitionen der einzelnen Socketoptionen finden Sie auf der Seite [Socketoptionen](socket-options.md) .

Weitere Informationen zur Verwendung von IOCTLs für Multicast Programmierung finden Sie unter [Final-State-based Multicast Programming](final-state-based-multicast-programming.md) weiter unten in diesem Abschnitt.

Unter Windows Vista und höher steht eine Reihe von Socketoptionen für Multicast Programmierung zur Verfügung, die IPv6-und IPv4-Adressen unterstützen. Diese Socketoptionen sind IP-agnostisch und können sowohl für IPv6 als auch für IPv4 verwendet werden. In IPv6 verwenden diese Socketoptionen MLDv2. Auf IPv4 verwenden diese Socketoptionen IGMPv3. Diese IP-agnostischen Optionen sind die bevorzugten Socketoptionen für Multicast Programmierung unter Windows Vista und höher. Windows Sockets verwendet die folgenden Socketoptionen: 

| Socketoption               | Argumenttyp                                            |
|-----------------------------|----------------------------------------------------------|
| mcast- \_ Block \_ Quelle        | [**Gruppe \_ \_Quellreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) -Struktur |
| mcast \_ - \_ joingruppe          | [**Gruppe \_ Req**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req) -Struktur                |
| mcast \_ Join- \_ Quell \_ Gruppe  | [**Gruppe \_ \_Quellreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) -Struktur |
| mcast \_ - \_ Gruppe verlassen         | [**Gruppe \_ Req**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req) -Struktur                |
| mcast \_ - \_ Quell \_ Gruppe verlassen | [**Gruppe \_ \_Quellreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) -Struktur |
| mcast- \_ Quelle "Unblock" \_      | [**Gruppe \_ \_Quellreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) -Struktur |



 

Eine Reihe von Socketoptionen sind für Multicast Programmierung verfügbar, die nur IPv6-Adressen unterstützen. Diese Socketoptionen verwenden MLDv1 oder MLDv2. Die verwendete Version von MLD hängt von der Windows-Version ab. MLDv2 wird unter Windows Vista und höher unterstützt. Windows Sockets verwendet die folgenden Socketoptionen: 

| Socketoption          | Argumenttyp                             |
|------------------------|-------------------------------------------|
| IPv6 \_ - \_ Mitgliedschaft hinzufügen  | [**IPv6- \_ MREQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) -Struktur |
| IPv6- \_ Drop- \_ Mitgliedschaft | [**IPv6- \_ MREQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) -Struktur |



 

Eine Reihe von Socketoptionen sind für Multicast Programmierung verfügbar, die nur IPv4-Adressen unterstützen. Diese Socketoptionen verwenden IGMPv3 oder igmpv2. Die verwendete Version von IGMP hängt von der Windows-Version ab. IGMPv3 wird unter Windows Vista und höher unterstützt. Windows Sockets verwendet die folgenden Socketoptionen:

| Socketoption                | Argumenttyp                                        |
|------------------------------|------------------------------------------------------|
| IP \_ - \_ Mitgliedschaft hinzufügen          | [**IP- \_ MREQ-**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) Struktur                |
| IP \_ - \_ Quell \_ Mitgliedschaft hinzufügen  | [**IP- \_ MREQ- \_ Quell**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) Struktur |
| IP- \_ Block \_ Quelle            | [**IP- \_ MREQ- \_ Quell**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) Struktur |
| IP- \_ Drop- \_ Mitgliedschaft         | [**IP- \_ MREQ-**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) Struktur                |
| IP- \_ Drop- \_ Quell \_ Mitgliedschaft | [**IP- \_ MREQ- \_ Quell**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) Struktur |
| IP- \_ Block \_ Quelle          | [**IP- \_ MREQ- \_ Quell**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) Struktur |



 

Wenn IGMPv3 verfügbar ist, werden die Optionen IP-Quell \_ \_ \_ Mitgliedschaft, IP- \_ Block \_ Quelle, IP-Ablage \_ \_ Quell \_ Mitgliedschaft und IP- \_ Blockierungs \_ Quelle effizienter behandelt, da der Router das Filtern verarbeiten kann. Wenn nur igmpv2 verfügbar ist, muss der Host das Filtern verarbeiten.

Es gibt zwei Kategorien, in denen die meisten Anwendungen wahrscheinlich ausfallen: beliebige Quelle und kontrollierte Quelle.

-   Alle **-Quell** Anwendungen akzeptieren standardmäßig alle Quellen, sodass einzelne Quellen bei Bedarf deaktiviert werden können. Ein Beispiel für eine beliebige Quell Anwendung ist ein Videokonferenz-Telefon, mit dem alle Empfänger teilnehmen können.
-   **Kontrollierte Quell** Anwendungen beschränken die Quellen auf eine bestimmte Liste, z. b. eine Internet Radio Station oder die Übertragung eines Ereignisses. Der Prozess der Verwendung von Socketoptionen unterscheidet sich geringfügig voneinander.

Unter Windows Vista und höher gelten die folgenden Schritte für alle-Quell Anwendungen:

- Verwenden Sie die **\_ \_ Gruppe "mcast Join** ", um einer Gruppe beizutreten.  
- Verwenden Sie die **mcast- \_ Block \_ Quelle** , um bei Bedarf eine bestimmte Quelle zu deaktivieren.  
- Verwenden Sie die **mcast- \_ \_ Quelle zur Aufhebung der Blockierung** , um bei Bedarf eine blockierte Quelle erneut zuzulassen.  
- Verwenden Sie die **mcast- \_ \_ Gruppe verlassen** , um die Gruppe zu verlassen.  

Unter Windows Vista und höher gelten die folgenden Schritte für gesteuerte Quell Anwendungen:

- Verwenden Sie die **mcast \_ Join- \_ Quell \_ Gruppe** , um jedem Gruppen-/Quell-paar beizutreten.  
- Verwenden Sie die **mcast- \_ \_ Quell \_ Gruppe** , um die einzelnen Gruppen/Quellen zu verlassen, oder verwenden Sie die **mcast- \_ \_ Gruppe** , um alle Quellen zu verlassen, wenn die gleiche Gruppen Adresse von allen Quellen verwendet wird.  

Die folgenden Schritte gelten für alle-Quell Anwendungen:

- Verwenden **Sie IP- \_ \_ Mitgliedschaft hinzufügen** , um einer Gruppe beizutreten (IPv6-Mitgliedschaft für IPv6 **\_ Hinzufügen \_** ).  
- Verwenden Sie die **IP- \_ Block \_ Quelle** , um eine bestimmte Quelle zu deaktivieren, falls dies erforderlich ist.  
- Verwenden Sie die **IP- \_ \_ Quell Quellen Quelle** , um bei Bedarf eine blockierte Quelle erneut zuzulassen.  
- Verwenden Sie die **IP- \_ Drop- \_ Mitgliedschaft** , um die Gruppe zu verlassen (**IPv6- \_ Drop \_ Membership** für IPv6).  

Die folgenden Schritte gelten für gesteuerte Quell Anwendungen:

- Verwenden **Sie IP- \_ \_ Quell \_ Mitgliedschaft hinzufügen** , um jedem Gruppen-/quellpaar beizutreten.  
- Verwenden Sie die **IP-Ablage \_ \_ Quell \_ Mitgliedschaft** , um jede Gruppe/Quelle zu verlassen, oder verwenden Sie die **IP- \_ Drop- \_ Mitgliedschaft** , um alle Quellen zu verlassen, wenn die gleiche Gruppen Adresse von allen Quellen verwendet wird.  

Die Reihenfolge, in der diese Socketoptionen festgelegt sind, hat Regeln zugeordnet. Informationen und Informationen zur Problembehandlung bei Multicast Socketoptionen finden Sie unter [Multicast-socketoptionsverhalten](multicast-socket-option-behavior.md).
