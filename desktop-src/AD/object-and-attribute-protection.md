---
title: Objekt- und Attributschutz
description: Eine Zugriffssteuerungsliste (Access Control List, ACL) schützt alle Objekte in Active Directory Domain Services.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Objekt- und Attributschutz
- Sicherheits-AD, Objekt- und Attributschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7798ca1498c3a8ffe58bf43117dfd8ae249d234115f551c636628ad5b811e04a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025614"
---
# <a name="object-and-attribute-protection"></a>Objekt- und Attributschutz

Eine Zugriffssteuerungsliste (Access Control List, ACL) schützt alle Objekte in Active Directory Domain Services. ACLs bestimmen, wer das Objekt anzeigen kann, welche Attribute er lesen kann und welche Aktionen jeder Benutzer für das Objekt ausführen kann. Das Vorhandensein eines Objekts oder Attributs wird keinem nicht autorisierten Benutzer offengelegt.

Eine Zugriffssteuerungsliste ist eine Liste von Zugriffssteuerungseinträgen (Access Control Entries, ACEs), die mit dem objekt gespeichert sind, das sie schützt. In Windows NT und Windows 2000 wird eine ACL als binärer Wert gespeichert, der als Sicherheitsdeskriptor bezeichnet wird. Jeder ACE enthält eine Sicherheits-ID (SID), die den Prinzipal (Benutzer oder Gruppe) identifiziert, für den der ACE gilt, und Daten darüber, welche Art von Zugriff der ACE gewährt oder verweigert.

ACLs für Verzeichnisobjekte enthalten ACEs, die für das Objekt als Ganzes gelten, und ACEs, die für die einzelnen Attribute des Objekts gelten. Dadurch kann ein Administrator nicht nur steuern, welche Benutzer ein Objekt sehen können, sondern auch, welche Eigenschaften diese Benutzer anzeigen können. Beispielsweise kann allen Benutzern Lesezugriff auf die E-Mail- und Telefonnummernattribute für alle anderen Benutzer gewährt werden, aber Sicherheitseigenschaften von Benutzern können allen Mitgliedern einer speziellen Sicherheitsadministratorgruppe bis auf diese verweigert werden. Einzelnen Benutzern kann schreibzugriff auf persönliche Attribute wie Telefon- und Postanschriftadressen für ihre eigenen Benutzerobjekte gewährt werden.

 

 




