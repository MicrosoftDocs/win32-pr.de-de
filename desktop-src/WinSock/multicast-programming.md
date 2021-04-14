---
description: Multicast Programmierung wird durch Windows Sockets ermöglicht.
ms.assetid: f729945b-b469-4baf-ac06-2431ee2d0e71
title: Multicast Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67af0eeb087e8c6a5938f26a0644dc346d55cf51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526153"
---
# <a name="multicast-programming"></a>Multicast Programmierung

Multicast Programmierung wird durch Windows Sockets ermöglicht. Windows Sockets ermöglicht die MLD (Multicast Listener Discovery)-Versionen 1 (MLDv1) und 2 (MLDv2) in IPv6 und die Internet Group Management-Protokoll Versionen 2 (igmpv2) und 3 (IGMPv3) durch die Verwendung von Socketoptionen oder IOCTLs. In diesem Abschnitt wird die Windows-Implementierung beschrieben. es wird erläutert, wie Sie die Multicast Programmierung mit Windows Sockets aktivieren und Programmierbeispiele zur Veranschaulichung der Verwendung bereitstellen.

Die zweite Version von IGMP, die im folgenden als igmpv2 bezeichnet wird, ermöglicht Hosts, Multicast Gruppen, die durch eine IPv4-Multicast Adresse identifiziert werden, an einer bestimmten Netzwerkschnittstelle beizutreten und zu verlassen. Windows Sockets ermöglicht einer Anwendung das beitreten zu einer solchen Gruppe zu bestimmten Sockets. Ein Nachteil von igmpv2 ist jedoch, dass alle IPv4-Quelladressen, die mit der igmpv2-Gruppe verknüpft sind, an alle Mitglieder übertragen werden können. Dies kann die Gruppe überfluten und für Übertragungen, die eine primäre Quelle benötigen, z. b. eine Internet Radio Station, unbrauchbar machen. Das Problem bei igmpv2 besteht darin, dass eine einzelne IPv4-Quelladresse (oder sogar nur wenige Quellen) nicht selektiv ausgewählt werden kann und Absender (z. b. nicht autorisierte Absender oder Denial-of-Service-Täter) für eine bestimmte Multicast Gruppe nicht blockiert werden können. IGMPv3 behandelt diese Mängel.

Mit Windows Sockets und IGMPv3 können Anwendungen eine bestimmte IPv4-Quelladresse und ein Multicast Gruppen paar auswählen. Außerdem ermöglicht Windows Sockets Entwicklern das selektive zulassen von zusätzlichen Sendern in einem bestimmten Quell-/gruppenpaar oder das Blockieren bestimmter Sender für Anwendungen. IGMPv3 wird unter Windows Vista und höher unterstützt.

Die erste Version von MLD in IPv6, die als MLDv1 bezeichnet wird, ähnelt igmpv2 und unterscheidet sich von denselben Einschränkungen. MLDv1 ermöglicht Hosts, Multicast Gruppen, die durch eine IPv6-Multicast Adresse identifiziert werden, an einer bestimmten Netzwerkschnittstelle beizutreten und zu verlassen. Windows Sockets ermöglicht einer Anwendung das beitreten zu einer solchen Gruppe zu bestimmten Sockets. Allerdings kann jede IPv6-Quelladresse, die mit der Gruppe MLDv1 verknüpft ist, an alle Mitglieder übertragen werden, die die Gruppe potenziell überfluten und für Übertragungen, die eine primäre Quelle erfordern, unbrauchbar machen. Das Problem mit MLDv1 besteht darin, dass eine einzelne IPv6-Quelladresse (oder sogar nur wenige Quellen) nicht selektiv ausgewählt werden kann und Absender (z. b. nicht autorisierte Absender oder Denial-of-Service-Täter) für eine bestimmte Multicast Gruppe nicht blockiert werden können. MLDv2 behandelt diese Mängel.

Mit Windows Sockets und MLDv2 können Anwendungen eine bestimmte Multicast-IPv6-Quelladresse und ein Multicast Gruppen paar auswählen. Außerdem ermöglicht Windows Sockets Entwicklern das selektive zulassen von zusätzlichen Sendern in einem bestimmten Quell-/gruppenpaar oder das Blockieren bestimmter Sender für Anwendungen. MLDv2 wird unter Windows Vista und höher unterstützt.

Es gibt zwei Ansätze, die ein Anwendungsprogrammierer bei der Entwicklung von Multicast Anwendungen in Windows Unternehmen kann. Der erste Ansatz ist Änderungs basiert. Multicast Quellen werden bei Bedarf mithilfe von Socketoptionen hinzugefügt oder entfernt, auch während der Übertragung. Der zweite Ansatz ist das endgültige Zustands basierte. Quelladressen und alle enthaltenen/ausgeschlossenen Adressen werden mit einer ioctl angegeben. Bei jedem Ansatz handelt es sich um eine gültige multicastingübung, aber Entwickler können die Verwendung von Socketoptionen und des Änderungs basierten Ansatzes intuitiver und flexibler gestalten.

Dieser Abschnitt enthält die folgenden Seiten: 

| Seitentitel                                                                             | BESCHREIBUNG                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MLD und IGMP mithilfe von Windows Sockets](igmp-and-windows-sockets.md)                     | Listet die Multicast-Socketoptionen auf, die für die Verwendung in der Windows Sockets-Programmierung verfügbar sind, mithilfe eines Änderungs basierten Programmier Ansatzes. Definiert zwei Multicast-Anwendungskategorien. |
| [Multicast-socketoptionsverhalten](multicast-socket-option-behavior.md)               | Bietet eine ausführliche Tabelle, in der die Auswirkungen und Anforderungen des Aufrufs von Multicast-Socketoptionen in bestimmter Reihenfolge erläutert werden.                                                  |
| [Beispiel für Multicast Programmierung](multicast-programming-sample.md)                       | Programmier Ausschnitt, der die Verwendung von Socketoptionen zum Aktivieren von Multicast Anwendungen in Windows veranschaulicht.                                                                        |
| [Abschließende Zustands basierte Multicast Programmierung](final-state-based-multicast-programming.md) | Erläutert den Endzustands Ansatz und erläutert, wie IOCTLs für Multicast Programmierung mit Windows Sockets verwendet wird.                                                                               |
| [Portieren von Broadcast Anwendungen auf IPv6](porting-broadcast-applications-to-ipv6.md)   | Enthält Richtlinien zum Portieren von IPv4-Broadcast Anwendungen auf IPv6-Multicast.                                                                                                     |



 

 

 



