---
description: Die Multicastprogrammierung wird über Windows Sockets aktiviert.
ms.assetid: f729945b-b469-4baf-ac06-2431ee2d0e71
title: Multicastprogrammierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0582f9d03cd5614bbe284eb81cdcb40bea8233627564ec2d3603de11fb663e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858160"
---
# <a name="multicast-programming"></a>Multicastprogrammierung

Die Multicastprogrammierung wird über Windows Sockets aktiviert. Windows Sockets ermöglicht die Multicastlistenerermittlung (MLD) Versionen 1 (MLDv1) und 2 (MLDv2) unter IPv6 und die Internet Group Management Protocol-Versionen 2 (IGMPv2) und 3 (IGMPv3) mithilfe von Socketoptionen oder IOCTLs. Dieser Abschnitt beschreibt die Windows Implementierung, erläutert, wie Sie die Multicastprogrammierung mithilfe von Windows Sockets aktivieren, und enthält Programmierbeispiele, um deren Verwendung zu veranschaulichen.

Die zweite Version von IGMP, nachfolgend IGMPv2 genannt, ermöglicht Es Hosts, Multicastgruppen, die durch eine IPv4-Multicastadresse identifiziert werden, in einer bestimmten Netzwerkschnittstelle zu verbinden und zu be hinterlassen. Windows Sockets ermöglichen es einer Anwendung, solche Gruppen in bestimmten Sockets zu verbinden und zu be lassen. Ein Nachteil von IGMPv2 ist jedoch, dass jede IPv4-Quelladresse, die der IGMPv2-Gruppe beigetreten ist, an alle Mitglieder übertragen werden kann, wodurch die Gruppe möglicherweise überflutet und für Übertragungen, für die eine primäre Quelle erforderlich ist, wie z. B. eine Internetsendestation, unbrauchbar wird. Das Problem bei IGMPv2 ist die Unfähigkeit, selektiv eine einzelne IPv4-Quelladresse (oder sogar einige wenige Quellen) zu wählen, und die Unfähigkeit, Absender (z. B. nicht autorisierte Sende- oder Denial-of-Service-Sperre) für eine bestimmte Multicastgruppe zu blockieren. IGMPv3 behebt diese Mängel.

Mit Windows Sockets und IGMPv3 können Anwendungen ein bestimmtes Multicast-IPv4-Quelladressen- und Multicastgruppenpaar auswählen. Darüber hinaus ermöglicht Windows Sockets Entwicklern, zusätzliche Sendesender in einem bestimmten Quell-/Gruppenpaar selektiv zu erlauben, oder ermöglicht Es Anwendungen, bestimmte Sender zu blockieren. IGMPv3 wird unter Windows Vista und höher unterstützt.

Die erste Version von MLD unter IPv6, die als MLDv1 bezeichnet wird, ist IGMPv2 sehr ähnlich und hat dieselben Einschränkungen. MLDv1 ermöglicht Es Hosts, Multicastgruppen, die durch eine IPv6-Multicastadresse identifiziert werden, in einer bestimmten Netzwerkschnittstelle zu verbinden und zu be hinterlassen. Windows Sockets ermöglichen es einer Anwendung, solche Gruppen in bestimmten Sockets zu verbinden und zu be lassen. Jede IPv6-Quelladresse, die mit der MLDv1-Gruppe verbunden ist, kann jedoch an alle Mitglieder übertragen werden, wodurch die Gruppe möglicherweise überflutet und für Übertragungen, die eine primäre Quelle erfordern, unbrauchbar wird. Das Problem bei MLDv1 ist seine Unfähigkeit, selektiv eine einzelne IPv6-Quelladresse (oder sogar einige wenige Quellen) zu wählen, und seine Unfähigkeit, Absender (z. B. nicht autorisierte Sender oder Denial-of-Service-Sperre) für eine bestimmte Multicastgruppe zu blockieren. MLDv2 behebt diese Mängel.

Mit Windows Sockets und MLDv2 können Anwendungen ein bestimmtes Multicast-IPv6-Quelladressen- und Multicastgruppenpaar auswählen. Darüber hinaus ermöglicht Windows Sockets Entwicklern, zusätzliche Sendesender in einem bestimmten Quell-/Gruppenpaar selektiv zu erlauben, oder ermöglicht Es Anwendungen, bestimmte Sender zu blockieren. MLDv2 wird unter Windows Vista und höher unterstützt.

Es gibt zwei Ansätze, die ein Anwendungsprogrammierer bei der Entwicklung von Multicastanwendungen in Windows. Der erste Ansatz basiert auf Änderungen. Multicastquellen werden bei Bedarf mithilfe von Socketoptionen hinzugefügt oder entfernt, auch während der Übertragung. Der zweite Ansatz basiert auf dem endgültigen Zustand. Quelladressen und alle eingeschlossenen/ausgeschlossenen Adressen werden mit einer IOCTL angegeben. Jeder Ansatz ist eine gültige Multicasting-Methode, aber Entwickler finden die Verwendung von Socketoptionen und des änderungsbasierten Ansatzes möglicherweise intuitiver und flexibler.

Dieser Abschnitt enthält die folgenden Seiten: 

| Seitentitel                                                                             | BESCHREIBUNG                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MLD und IGMP mit Windows Sockets](igmp-and-windows-sockets.md)                     | Enumeriert die Multicastsocketoptionen, die für die Verwendung in der Windows Sockets-Programmierung mithilfe eines änderungsbasierten Programmieransatzes verfügbar sind. Definiert zwei Multicastanwendungskategorien. |
| [Verhalten der Multicastsocketoption](multicast-socket-option-behavior.md)               | Enthält eine umfassende Tabelle, in der die Auswirkungen und Anforderungen des Aufrufs von Multicastsocketoptionen in einer bestimmten Reihenfolge erläutert werden.                                                  |
| [Multicastprogrammierungsbeispiel](multicast-programming-sample.md)                       | Programmierausschnitt, der die Verwendung von Socketoptionen zum Aktivieren von Multicastanwendungen in Windows.                                                                        |
| [Final-State-based Multicast Programming](final-state-based-multicast-programming.md) | Erläutert den Final State-Ansatz und die Verwendung von IOCTLs für die Multicastprogrammierung mit Windows Sockets.                                                                               |
| [Portieren von Broadcastanwendungen zu IPv6](porting-broadcast-applications-to-ipv6.md)   | Enthält Richtlinien zum Portieren von IPv4-Broadcastanwendungen zu IPv6-Multicast.                                                                                                     |



 

 

 



