---
title: Objekt-und Attribut Schutz
description: Eine Zugriffs Steuerungs Liste (Access Control List, ACL) schützt alle Objekte in Active Directory Domain Services.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Objekt-und Attribut Schutz
- Sicherheit AD, Objekt-und Attribut Schutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c046df35740f21f8706120ee6e11cfad1d4f626
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707595"
---
# <a name="object-and-attribute-protection"></a>Objekt-und Attribut Schutz

Eine Zugriffs Steuerungs Liste (Access Control List, ACL) schützt alle Objekte in Active Directory Domain Services. ACLs legen fest, wer das Objekt anzeigen kann, welche Attribute Sie lesen können und welche Aktionen die einzelnen Benutzer für das Objekt ausführen können. Das vorhanden sein eines Objekts oder Attributs wird niemals einem nicht autorisierten Benutzer offengelegt.

Eine ACL ist eine Liste von Zugriffs Steuerungs Einträgen (ACEs), die mit dem Objekt gespeichert werden, das Sie schützt. In Windows NT und Windows 2000 wird eine ACL als ein binärer Wert, der als Sicherheits Beschreibung bezeichnet wird, gespeichert. Jeder ACE enthält eine Sicherheits-ID (SID), die den Prinzipal (Benutzer oder Gruppe) identifiziert, auf den der ACE angewendet wird, sowie Daten darüber, welche Art von Zugriff der ACE gewährt oder verweigert.

ACLs für Verzeichnisobjekte enthalten ACEs, die auf das Objekt als Ganzes und ACEs angewendet werden, die für die einzelnen Attribute des Objekts gelten. Dies ermöglicht es einem Administrator, nicht nur zu steuern, welche Benutzer ein Objekt sehen können, sondern auch die Eigenschaften, die diese Benutzer anzeigen können. Beispielsweise können allen Benutzern Lesezugriff auf die e-Mail-und Telefonnummern Attribute für alle anderen Benutzer gewährt werden, aber Sicherheitseigenschaften von Benutzern werden möglicherweise allen Mitgliedern einer speziellen Sicherheitsadministrator Gruppe verweigert. Einzelnen Benutzern können Schreibzugriff auf persönliche Attribute erteilt werden, z. b. Telefon-und Mailing Adressen für Ihre eigenen Benutzer Objekte.

 

 




