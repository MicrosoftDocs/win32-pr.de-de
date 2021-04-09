---
title: Das Replikations Modell eines Programmierers in Active Directory Domain Services
description: Im folgenden finden Sie eine Beschreibung des Replikations Modells für Active Directory Domain Services.
ms.assetid: 45baf7ff-9474-4f86-81c8-03336901fec2
ms.tgt_platform: multiple
keywords:
- Ein Programmiermodell von Active Directory Replikations-AD
- Das Replikations Modell eines Programmierers in Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ada20bc07411528eaea4b7ff8c773c50ae8b6ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036269"
---
# <a name="a-programmers-model-of-replication-in-active-directory-domain-services"></a>Das Replikations Modell eines Programmierers in Active Directory Domain Services

Im folgenden finden Sie eine Beschreibung des Replikations Modells für Active Directory Domain Services.

Alle Updates des Active Directory-Domäne Controllers (DC) werden mithilfe von LDAP-Anforderungen ausgeführt, mit denen ein Objekt für jede Anforderung erstellt, geändert oder gelöscht wird. Mit einer einzelnen Anforderung können mehrere Attribute für ein Objekt festgelegt oder geändert werden.

Eine Aktualisierungs Anforderung wird bei einem DC als atomarische Transaktion verarbeitet. Entweder wird das gesamte Update durchgeführt, oder keines davon erfolgt. Wenn die anfordernde Person eine erfolgreiche Antwort auf eine Aktualisierungs Anforderung erhält, ist die gesamte Anforderung erfolgreich (committet). Dies wird als "Ursprungs Schreibvorgang" bezeichnet. Mehrere LDAP-Anforderungen können nicht in eine einzelne größere Transaktion gruppiert werden.

Bei einem Ursprungs Schreibvorgang berechnet ein DC einen "Stempel" für jeden neuen oder geänderten Attribut Wert und fügt diesen Stempel an den Wert an. wenn der Wert repliziert wird, wird der Stempel ebenfalls repliziert. Der neue Stempel ist eindeutig, und bei einem Update ist der neue Stempel größer als der Stempel des alten Werts auf diesem DC.

Gelegentlich wählt ein DC den Satz von Objekten aus, die sich seit der letzten Replikation des Domänen Controllers geändert haben. Anschließend sendet Sie für jedes Objekt eine einzelne Nachricht an alle anderen DCS, die alle aktuellen Werte von Attributen enthalten, die seit dem letzten Replizieren des Objekts geändert wurden. Replikations Nachrichten sind zuverlässig und werden in der richtigen Reihenfolge übermittelt, erfordern jedoch möglicherweise mehr Zeit für die Übermittlung.

Wenn ein Domänen Controller eine Replikations Nachricht von einem anderen Domänen Controller empfängt, wird er wie folgt verarbeitet: für jedes geänderte Attribut, wenn der Stempel des Werts in der Replikations Nachricht größer als der Stempel des aktuellen Werts ist, wendet der DC das Update an. Andernfalls verwirft der DC das Update. Jede Replikations Nachricht wird wie ein Ursprungs Schreibvorgang als atomarische Transaktion angewendet.

Dabei handelt es sich um das Active Directory Domain Services Replikations Modell. Wichtige Eigenschaften dieses Modells sind:

-   Ein Ausgangs Schreibvorgang in ein einzelnes Objekt ist atomarisch.
-   Beim Replizieren von Änderungen werden entweder alle Änderungen, die von einem Ursprungs Schreibvorgang vorgenommen werden, gesendet, oder keine von Ihnen.
-   Ein replizierter Schreibvorgang in ein einzelnes Objekt ist atomarisch, aber Konflikte werden mit Attribut-by-Attribute aufgelöst.

Das Modell garantiert nicht die Replikations Anordnung von Änderungen, die an unterschiedlichen Objekten vorgenommen werden. Schreiben Sie keine Anwendungen, bei denen davon ausgegangen wird, dass Änderungen in der ursprünglichen Schreib Reihenfolge repliziert werden Das Modell garantiert nicht, dass beide Werte repliziert werden, wenn ein Attribut eines Objekts zweimal geändert wird. Bei der Replikation wird nur der aktuelle Wert zum Zeitpunkt der Replikation gesendet.

Das Modell unterscheidet sich von der Realität auf verschiedene Weise, die nur die Leistung beeinträchtigen. Beispielsweise sendet der Active Directory Server Replikations Nachrichten mit den Änderungen an mehrere Objekte, verarbeitet jedoch den Inhalt einer solchen multiobjektnachricht, als ob es sich um eine Reihe von Einzelobjekt Nachrichten handelt. Der Active Directory Server führt keine Punkt-zu-Punkt-Replikation aus, wie im Modell beschrieben, sondern führt stattdessen eine komplexere und effizientere transitiv Replikation durch, die funktionell dem Modell entspricht.

 

 




