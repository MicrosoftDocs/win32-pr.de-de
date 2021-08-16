---
title: Replikationsmodell eines Programmierers in Active Directory Domain Services
description: Im Folgenden finden Sie eine Beschreibung des Replikationsmodells für Active Directory Domain Services.
ms.assetid: 45baf7ff-9474-4f86-81c8-03336901fec2
ms.tgt_platform: multiple
keywords:
- A Programmer es Model of Active Directory Replication AD
- Replikationsmodell eines Programmierers in Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b758a31913d0c306105d0d3ce51e72607530e314d79601e8e5230495458d9793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841230"
---
# <a name="a-programmers-model-of-replication-in-active-directory-domain-services"></a>Replikationsmodell eines Programmierers in Active Directory Domain Services

Im Folgenden finden Sie eine Beschreibung des Replikationsmodells für Active Directory Domain Services.

Alle Updates am Active Directory-Domäne Controller (DC) werden mit LDAP-Anforderungen ausgeführt, die ein Objekt für jede Anforderung erstellen, ändern oder löschen. Eine einzelne Anforderung kann mehrere Attribute für ein Objekt festlegen oder ändern.

Eine Updateanforderung wird als atomarer Transaktion an einem DC verarbeitet. Entweder erfolgt das gesamte Update oder keines davon. Wenn der Anfordernde eine erfolgreiche Antwort auf eine Updateanforderung empfängt, ist die gesamte Anforderung erfolgreich (ein Committed) erfolgreich. Dies wird als "ursprünglicher Schreibzugriff" bezeichnet. Mehrere LDAP-Anforderungen können nicht in einer einzelnen größeren Transaktion gruppiert werden.

Bei einem ursprünglichen Schreibzugriff berechnet ein DC einen "Stempel" für jeden neuen oder geänderten Attributwert und hängt diesen Stempel an den Wert an, sodass bei der Replikation des Werts auch der Stempel repliziert wird. Der neue Stempel ist eindeutig, und bei einem Update ist der neue Stempel größer als der Stempel des alten Werts an diesem DC.

Gelegentlich wählt ein DC die Gruppe von Objekten aus, die sich seit der letzten Replikation des Domänencontrollers geändert haben. Anschließend sendet er für jedes Objekt eine einzelne Nachricht an alle anderen Dcs, die alle aktuellen Werte von Attributen enthalten, die seit der letzten Replikation des Objekts geändert wurden. Replikationsnachrichten sind zuverlässig und werden in der reihenfolgengeordneten Reihenfolge übermittelt, erfordern jedoch möglicherweise mehr Zeit, um zugestellt zu werden.

Wenn ein Domänencontroller eine Replikationsnachricht von einem anderen DC empfängt, verarbeitet er diese wie folgt: Wenn der Stempel für den Wert in der Replikationsnachricht für jedes geänderte Attribut größer als der Stempel des aktuellen Werts ist, wendet der Domänencontroller das Update an. Andernfalls verwirft der DC das Update. Jede Replikationsnachricht wird wie ein ursprünglicher Schreibvorgang als atomarer Transaktionsvorgang angewendet.

Dies ist das Active Directory Domain Services Replikationsmodell. Zu den wichtigsten Eigenschaften dieses Modells gehören:

-   Ein ursprünglicher Schreibzugriff auf ein einzelnes Objekt ist atomar.
-   Beim Replizieren von Änderungen werden entweder alle von einem ursprünglichen Schreibzugriff vorgenommenen Änderungen gesendet, oder keine davon.
-   Ein replizierter Schreibzugriff auf ein einzelnes Objekt ist atomar, Konflikte werden jedoch Attribut für Attribut gelöst.

Das Modell garantiert nicht die Replikations reihenfolge der Änderungen, die an verschiedenen Objekten vorgenommen wurden. Schreiben Sie keine Anwendungen, bei denen davon ausgegangen wird, dass Änderungen in der Reihenfolge der Ursprungs-/Schreibzugriffe repliziert werden. Das Modell garantiert nicht, dass beide Werte repliziert werden, wenn ein Attribut eines Objekts zweimal geändert wird. Die Replikation sendet nur den aktuellen Wert zum Zeitpunkt der Replikation.

Das Modell unterscheidet sich von der Realität auf verschiedene Weise, die sich nur auf die Leistung auswirken. Beispielsweise sendet der Active Directory-Server Replikationsmeldungen, die die Änderungen an mehrere Objekte enthalten, verarbeitet jedoch den Inhalt einer solchen Nachricht mit mehreren Objekten, als ob es sich um eine Reihe von Einzelobjektnachrichten würde. Der Active Directory-Server führt keine Punkt-zu-Punkt-Replikation durch, wie im Modell beschrieben, sondern führt stattdessen eine komplexere und effizientere transitive Replikation durch, die funktionell dem Modell entspricht.

 

 




