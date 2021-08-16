---
description: Ein Zugriffssteuerungseintrag (ACE) ist ein Element in einer Zugriffssteuerungsliste (Access Control List, ACL).
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

Ein [*Zugriffssteuerungseintrag*](/windows/desktop/SecGloss/a-gly) (ACE) ist ein Element in einer [*Zugriffssteuerungsliste*](/windows/desktop/SecGloss/a-gly) (Access Control List, ACL). Eine ACL kann null oder mehr ACEs haben. Jeder ACE steuert oder überwacht den Zugriff auf ein Objekt durch einen angegebenen Vertrauenshänder. Informationen zum Hinzufügen, Entfernen oder Ändern der ACEs in den ACLs eines Objekts finden Sie unter Ändern der ACLs eines [Objekts in C++.](modifying-the-acls-of-an-object-in-c--.md)

Es gibt sechs Arten von ACEs, von denen drei von allen sicherungsbaren Objekten unterstützt werden. Die anderen drei Typen sind [objektspezifische ACEs,](object-specific-aces.md) die von Verzeichnisdienstobjekten unterstützt werden.

Alle AcEs-Typen enthalten die folgenden Zugriffssteuerungsinformationen:

-   Eine [Sicherheits-ID](security-identifiers.md) (SID), die den Vertrauenshänder [identifiziert,](trustees.md) für den der ACE gilt.
-   Eine [*Zugriffsmaske,*](/windows/desktop/SecGloss/a-gly) die die [vom](access-rights-and-access-masks.md) ACE gesteuerten Zugriffsrechte angibt.
-   Ein Flag, das den Typ des ACE angibt.
-   Ein Satz von Bitflags, die bestimmen, ob untergeordnete Container oder Objekte den ACE vom primären Objekt erben können, an das die ACL angefügt ist.

In der folgenden Tabelle sind die drei ACE-Typen aufgeführt, die von allen sicherungsbaren Objekten unterstützt werden.



| type               | Beschreibung                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zugriffs verweigerter ACE  | Wird in einer [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) verwendet, um einem Vertrauenshänder Zugriffsrechte zu verweigern.                                       |
| Zugriffsberechtigung für ACE | Wird in einer DACL verwendet, um einem Vertrauenshänder Zugriffsrechte zu ermöglichen.                                                                                                                                                                                              |
| Ace zur Systemüberwachung   | Wird in einer [*Systemzugriffssteuerungsliste*](/windows/desktop/SecGloss/s-gly) (SACL) verwendet, um einen Überwachungsdatensatz zu generieren, wenn der Vertrauenshänder versucht, die angegebenen Zugriffsrechte zu verwenden. |



 

Eine Tabelle mit objektspezifischen ACEs finden Sie unter [Objektspezifische ACEs.](object-specific-aces.md)

> [!Note]  
> Systemalarmobjekt-ACEs werden derzeit nicht unterstützt.

 

 

 
