---
description: Ein Zugriffssteuerungseintrag (Access Control Entry, ACE) ist ein Element in einer Zugriffssteuerungsliste (Access Control List, ACL).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Access Control Einträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adcc382da130c57c55b869c47c8837c7780a7cff4e6dbdd881e55aa7b724dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785650"
---
# <a name="access-control-entries"></a>Access Control Einträge

Ein [*Zugriffssteuerungseintrag (Access Control Entry,*](/windows/desktop/SecGloss/a-gly) ACE) ist ein Element in einer [*Zugriffssteuerungsliste (Access Control List,*](/windows/desktop/SecGloss/a-gly) ACL). Eine ACL kann 0 (null) oder mehr ACEs aufweisen. Jeder ACE steuert oder überwacht den Zugriff auf ein Objekt durch einen angegebenen Vertrauensnehmer. Informationen zum Hinzufügen, Entfernen oder Ändern der ACEs in den ACLs eines Objekts finden Sie unter [Ändern der ACLs eines Objekts in C++](modifying-the-acls-of-an-object-in-c--.md).

Es gibt sechs Typen von ACEs, von denen drei von allen sicherungsfähigen Objekten unterstützt werden. Die anderen drei Typen sind [objektspezifische ACEs, die](object-specific-aces.md) von Verzeichnisdienstobjekten unterstützt werden.

Alle AcEs-Typen enthalten die folgenden Zugriffssteuerungsinformationen:

-   Eine [Sicherheits-ID](security-identifiers.md) (SID), die den [Vertrauensnehmer](trustees.md) identifiziert, für den der ACE gilt.
-   Eine [*Zugriffsmaske,*](/windows/desktop/SecGloss/a-gly) die die vom ACE gesteuerten [Zugriffsrechte](access-rights-and-access-masks.md) angibt.
-   Ein Flag, das den Ace-Typ angibt.
-   Ein Satz von Bitflags, die bestimmen, ob untergeordnete Container oder Objekte den ACE vom primären Objekt erben können, an das die ACL angefügt ist.

In der folgenden Tabelle sind die drei ACE-Typen aufgeführt, die von allen sicherungsfähigen Objekten unterstützt werden.



| type               | BESCHREIBUNG                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE "Zugriff verweigert"  | Wird in einer [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) verwendet, um einem Vertrauensnehmer Zugriffsrechte zu verweigern.                                       |
| Zugriffsberechtigung für ACE | Wird in einer DACL verwendet, um einem Vertrauensnehmer Zugriffsrechte zu gewähren.                                                                                                                                                                                              |
| ACE für Systemüberwachung   | Wird in einer [*Systemzugriffssteuerungsliste*](/windows/desktop/SecGloss/s-gly) (SACL) verwendet, um einen Überwachungsdatensatz zu generieren, wenn der Vertrauensnehmer versucht, die angegebenen Zugriffsrechte in Anspruch zu nehmen. |



 

Eine Tabelle mit objektspezifischen ACEs finden Sie unter [Objektspezifische ACEs.](object-specific-aces.md)

> [!Note]  
> System-Alarm-Objekt-ACEs werden derzeit nicht unterstützt.

 

 

 
