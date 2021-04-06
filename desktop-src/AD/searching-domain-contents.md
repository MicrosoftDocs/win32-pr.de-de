---
title: Suchen von Domänen Inhalten
description: Vor der Erörterung der Bindung, um eine Suche nach Objekten in einer Domäne zu beginnen, ist es hilfreich zu verstehen, wie Daten in Active Directory Domain Services gespeichert werden.
ms.assetid: fd0b4556-465b-4338-87cb-375450590c44
ms.tgt_platform: multiple
keywords:
- Domänen Inhalt Active Directory
- Durchsuchen von Domänen Inhalten Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c18cd879e950fd9c467f6674092947d430d8f87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036345"
---
# <a name="searching-domain-contents"></a>Suchen von Domänen Inhalten

Vor der Erörterung der Bindung, um eine Suche nach Objekten in einer Domäne zu beginnen, ist es hilfreich zu verstehen, wie Daten in Active Directory Domain Services gespeichert werden.

Wenn Sie über eine Gesamtstruktur mit mehr als einer Domäne verfügen, speichert Active Directory Domain Services nicht alle Objektdaten auf einem einzelnen Domänen Controller – aus Gründen der Leistung, Skalierbarkeit und Zuverlässigkeit. Ein Domänen Controller enthält alle Informationen über die Domäne, in der er Mitglied ist (er verfügt über ein vollständiges Replikat der Domäne). Ein Domänen Controller enthält jedoch keine kompletten Informationen zu einer anderen Domäne.

Wenn Sie die Bindung an das Domänen Objekt mit der Weiterleitungs-Nachverfolgung deaktiviert haben, können Sie nach jedem beliebigen Objekt in dieser Domäne und nur in dieser Domäne suchen. Weitere Informationen zur Verweis Verfolgung finden Sie unter " [Verweise](referrals.md)". Eine Suche kann jede beliebige Eigenschaft abrufen und kann einen Abfrage Filter mit einer beliebigen Eigenschaft verwenden.

In einer Gesamtstruktur sind Domänen hierarchisch als Domänen Strukturen angeordnet. Eine Domänen Struktur kann nur eine einzelne Domäne oder eine Domäne mit einer oder mehreren untergeordneten Domänen sein. Diese untergeordneten Domänen können wiederum untergeordnete Domänen darunter haben. Eine Domänen Struktur ist auch ein zusammenhängender Namespace. Ein zusammenhängender Namespace bedeutet, dass die untergeordneten Domänen eine Fortsetzung der Benennungs Hierarchie sind. Beispielsweise kann eine Domäne fabrikam.com (oder DC = fabrikam, DC = com) über eine untergeordnete Domäne mit dem Namen mydivision (mydivision.fabrikam.com oder DC = mydivision, DC = fabrikam, DC = com) verfügen, die wiederum eine untergeordnete Domäne mit dem Namen mydev (mydev.mydivision.fabrikam.com oder DC = mydev, DC = mydivision, DC = fabrikam, DC =

Wenn Sie eine Bindung an ein Domänen Objekt (bei aktivierter Verweis Verfolgung) für eine Domäne innerhalb einer Domänen Struktur herstellen, Durchsuchen Sie diese Domäne und die gesamte Hierarchie darin. Die Suche kann jede beliebige Eigenschaft abrufen und kann einen Abfrage Filter mit einer beliebigen Eigenschaft verwenden.

Wenn ein Domänen Controller ein vollständiges Replikat einer eigenen Domäne enthält, können Sie eine Unterstruktur Suche in einer Domänen Struktur durchführen. Eine Domäne enthält Verweise auf ihre untergeordneten Domänen. Wenn ein Domänen Controller eine Unterstruktur-Such Anforderung für seine eigene Domäne verarbeitet, durchsucht der Domänen Controller diese Domäne und gibt dann Verweise auf jede der untergeordneten Domänen an den Client zurück. Ein Verweis ist die Methode, mit der ein Verzeichnisserver kommuniziert, dass er nicht die zum Ausführen einer Anforderung erforderlichen Informationen (z. b. eine Abfrage) enthält, aber einen Verweis auf einen Server enthält, der möglicherweise die erforderlichen Informationen enthält. Bei einer Unterstruktur Suche einer Domänen Struktur wird ein Verweis für jede direkt untergeordnete Domäne zurückgegeben, sodass die Suche auf einem Domänen Controller in jeder untergeordneten Domäne fortgesetzt werden kann. Wenn die Weiterleitungs Verfolgung aktiviert ist, verwendet die LDAP-Client Bibliothek (Wldap32.dll) diese Verweise, um an einen Domänen Controller in den einzelnen untergeordneten Domänen zu binden und die Suche fortzusetzen. Wenn die Weiterleitungs Verfolgung deaktiviert ist, löst der LDAP-Client die Verweise nicht aus, und die Suche ist fertiggestellt.

Eine Unterstruktur Suche in einer Domänen Struktur, bei der die Weiterleitungs Verfolgung aktiviert ist, kann zeitaufwändig sein, wenn eine langsame Verbindung mit den Domänen Controllern für die untergeordneten Domänen vorliegt. Wenn Sie nur eine einzelne Domäne durchsuchen möchten, sollten Sie die Weiterleitungs Verfolgung deaktivieren, um zu vermeiden, dass die untergeordneten Domänen unnötig durchsucht werden müssen.

 

 




