---
title: Übersicht über Message Queuing Services-Architektur
description: Message Queuing Services (MSMQ) verwendet ein Site/Enterprise-Modell. In der Regel ist eine Site ein physischer Standort, z. b. ein Gebäude. Ein Unternehmen besteht aus einem oder mehreren Standorten und repräsentiert eine Organisation.
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2226c185d32cb628529b34ba33d5569bd51ac28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310724"
---
# <a name="overview-of-message-queuing-services-architecture"></a>Übersicht über Message Queuing Services-Architektur

Message Queuing Services (MSMQ) verwendet ein Site/Enterprise-Modell. In der Regel ist eine Site ein physischer Standort, z. b. ein Gebäude. Ein Unternehmen besteht aus einem oder mehreren Standorten und repräsentiert eine Organisation.

Das folgende Diagramm veranschaulicht die Architektur des MSMQ-Dienstanbieter.

![MSMQ-Architektur](images/msmq.png)

Das Herzstück von MSMQ ist die MQIS-Datenbank (Message Queue Information Service), die zusätzlich zu SQL Server ausgeführt wird. Ein Unternehmen verfügt über einen einzigen Master-MQIS, der als primärer Enterprise Controller bezeichnet wird. Jeder Standort verfügt über eigene MQIS, die als *primärer Standort Controller* und NULL oder mehr *Sicherungs Standort Controller* bezeichnet werden. Schließlich gibt es die einzelnen Client Computer, die jeweils über einen eigenen Warteschlangen-Manager verfügen und als Dienst implementiert werden. Der primäre Unternehmens Controller kann auch ein primärer Standort Controller sein, und jeder Controller kann auch ein Client sein.

Nachrichten Warteschlangen können entweder öffentlich oder privat sein. Öffentliche Warteschlangen werden in Active Directory registriert und sind über das Netzwerk zugänglich. Nachrichten in einer öffentlichen Warteschlange werden im gesamten Unternehmen unter Kontrolle von MSMQ weitergeleitet. Client Anwendungs Nachrichten werden vom Warteschlangen-Manager des Clients in die Ziel Warteschlange verschoben, indem zwischen den Warteschlangen-Managern der Standort Controller gewechselt wird.

Private Warteschlangen werden vom lokalen Warteschlangen-Manager verwaltet und sind nicht in Active Directory registriert. Der Bereich privater Warteschlangen Nachrichten ist auf den Computer beschränkt, auf dem Sie sich befinden.

 

 




