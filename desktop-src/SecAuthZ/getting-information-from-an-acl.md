---
description: Es werden mehrere Funktionen bereitgestellt, die Zugriffs Steuerungsinformationen aus einer Zugriffs Steuerungs Liste (Access Control List, ACL) abrufen.
ms.assetid: a0839c49-09e9-4407-8702-051b88ef2231
title: Erhalten von Informationen aus einer ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f87aebc2bc9b05191b5026b990714c2519091be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217758"
---
# <a name="getting-information-from-an-acl"></a>Erhalten von Informationen aus einer ACL

Es werden mehrere Funktionen bereitgestellt, die Zugriffs Steuerungsinformationen aus einer [*Zugriffs Steuerungs Liste (Access Control List*](/windows/desktop/SecGloss/a-gly) , ACL) abrufen. Hierzu gehören Funktionen zum Bestimmen der Zugriffsrechte, die eine ACL für [einen bestimmten Vertrauens](trustees.md)nehmer gewährt oder überwacht. Mit anderen Funktionen können Sie Informationen zu den [*Zugriffs Steuerungs Einträgen*](/windows/desktop/SecGloss/a-gly) (ACEs) in einer ACL extrahieren.

Die [**getexplicitentriesfromacl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) -Funktion Ruft ein Array von [**expliziten \_ Zugriffs**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) Strukturen ab, die die ACEs in einer ACL beschreiben. Dies kann hilfreich sein, wenn ACE-Informationen aus einer ACL in eine andere kopiert werden. Beispielsweise kann ein Aufrufen von **getexplicitentriesfromacl** zum Abrufen von Informationen zu den ACEs in einer ACL befolgt werden, indem die zurückgegebenen **expliziten \_ Zugriffs** Strukturen in einem Aufrufen der [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) -Funktion übergeben werden, um äquivalente ACEs in einer neuen ACL zu erstellen.

Mit der [**GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) -Funktion können Sie die effektiven Zugriffsrechte ermitteln, die eine DACL einem bestimmten Vertrauens nehmer gewährt. Die effektiven Zugriffsrechte des Vertrauens nehmers sind die Zugriffsrechte, die eine DACL dem Vertrauens nehmer gewährt, oder allen Gruppen, deren Mitglied der Vertrauens nehmer ist. **GetEffectiveRightsFromAcl** überprüft alle Zugriffs zulässigen und zugriffsverweigerten ACEs in der angegebenen DACL.

**Verwenden Sie die folgenden Schritte, um die Zugriffsrechte eines Vertrauens nehmers für ein Objekt zu ermitteln.**

1.  Aufrufen der [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) -Funktion oder der [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) -Funktion, um einen Zeiger auf die DACL eines Objekts abzurufen.
2.  Rufen Sie die [**GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) -Funktion auf, um die Zugriffsrechte abzurufen, die die DACL einem angegebenen Vertrauens nehmer gewährt.

Mit der Funktion " [**getauditedpermissionsfromacl**](/windows/desktop/api/Aclapi/nf-aclapi-getauditedpermissionsfromacla) " können Sie eine SACL überprüfen, um die überwachten Zugriffsrechte für einen bestimmten Vertrauens nehmer oder für Gruppen, denen der Vertrauens nehmer angehört, zu bestimmen. Die überwachten Rechte geben die Typen von Zugriffsversuchen an, die bewirken, dass das System einen Überwachungsdaten Satz im Sicherheits Ereignisprotokoll generiert. Die Funktion gibt zwei [*Zugriffs Masken*](/windows/desktop/SecGloss/a-gly)zurück: eine mit den Zugriffsrechten, die für fehlgeschlagene Zugriffsversuche überwacht werden, und eine weitere, die die Zugriffsrechte enthält, die für den erfolgreichen Zugriff **Getauditedpermissionsfromacl** überprüft alle System Überwachungs-ACEs in einer SACL.

 

 
