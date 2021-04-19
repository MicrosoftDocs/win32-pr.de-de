---
description: Ein Zugriffs Steuerungs Eintrag (ACE) ist ein Element in einer Zugriffs Steuerungs Liste (Access Control List, ACL).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Access Control Einträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fe98cf1c1c4d5fb23091a6539564ff964202cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356112"
---
# <a name="access-control-entries"></a>Access Control Einträge

Ein [*Zugriffs Steuerungs Eintrag*](/windows/desktop/SecGloss/a-gly) (ACE) ist ein Element in einer [*Zugriffs Steuerungs Liste (Access Control List*](/windows/desktop/SecGloss/a-gly) , ACL). Eine ACL kann NULL oder mehr ACEs enthalten. Jeder ACE steuert oder überwacht den Zugriff auf ein Objekt durch einen angegebenen Vertrauens nehmer. Weitere Informationen zum Hinzufügen, entfernen oder Ändern von ACEs in den ACLs eines Objekts finden Sie unter [Ändern der ACLs eines Objekts in C++](modifying-the-acls-of-an-object-in-c--.md).

Es gibt sechs Typen von ACEs, von denen drei von allen Sicherungs fähigen Objekten unterstützt werden. Die anderen drei Typen sind [objektspezifische ACEs](object-specific-aces.md) , die von Verzeichnisdienst Objekten unterstützt werden.

Alle Arten von ACEs enthalten die folgenden Zugriffs Steuerungsinformationen:

-   Eine [Sicherheits](security-identifiers.md) -ID (SID), die [den Vertrauens nehmer identifiziert, für](trustees.md) den der ACE gilt.
-   Eine [*Zugriffs Maske*](/windows/desktop/SecGloss/a-gly) , die die vom ACE kontrollierten [Zugriffsrechte](access-rights-and-access-masks.md) angibt.
-   Ein Flag, das den Typ des ACE angibt.
-   Ein Satz von Bitflags, die bestimmen, ob untergeordnete Container oder Objekte den ACE von dem primären Objekt erben können, an das die ACL angefügt ist.

In der folgenden Tabelle werden die drei ACE-Typen aufgelistet, die von allen Sicherungs fähigen Objekten unterstützt werden.



| type               | BESCHREIBUNG                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ace "Zugriff verweigert"  | Wird in einer freigegebenen [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) verwendet, um Zugriffsrechte für einen Vertrauens nehmer zu verweigern.                                       |
| Zugriffs zulässiger ACE | Wird in einer DACL verwendet, um Zugriffsrechte für einen Vertrauens nehmer zuzulassen.                                                                                                                                                                                              |
| System Überwachungs ACE   | Wird in einer [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) verwendet, um einen Überwachungsdaten Satz zu generieren, wenn der Treuhänder versucht, die angegebenen Zugriffsrechte auszuüben. |



 

Eine Tabelle mit Objekt spezifischen ACEs finden Sie unter [Object-Specific ACEs](object-specific-aces.md).

> [!Note]  
> System-Wecker-Objekt-ACEs werden zurzeit nicht unterstützt.

 

 

 
