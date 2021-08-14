---
description: Es werden mehrere Funktionen bereitgestellt, die Zugriffssteuerungsinformationen aus einer Zugriffssteuerungsliste (Access Control List, ACL) abrufen.
ms.assetid: a0839c49-09e9-4407-8702-051b88ef2231
title: Abrufen von Informationen aus einer ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5ef90d40058efd19790829f92c37a976359cbc61601d72fa2fee4cc4a93ec7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913672"
---
# <a name="getting-information-from-an-acl"></a>Abrufen von Informationen aus einer ACL

Es werden mehrere Funktionen bereitgestellt, die Zugriffssteuerungsinformationen aus einer [*Zugriffssteuerungsliste (Access Control List,*](/windows/desktop/SecGloss/a-gly) ACL) abrufen. Dazu gehören Funktionen zum Bestimmen der Zugriffsrechte, die eine Zugriffssteuerungsliste für einen angegebenen [Vertrauensnehmer](trustees.md)gewährt oder überwacht. Mit anderen Funktionen können Sie Informationen zu den [*Zugriffssteuerungseinträgen (ACEs)*](/windows/desktop/SecGloss/a-gly) in einer Zugriffssteuerungsliste extrahieren.

Die [**GetExplicitEntriesFromAcl-Funktion**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) ruft ein Array von [**EXPLICIT \_ ACCESS-Strukturen**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) ab, die die ACEs in einer ACL beschreiben. Dies kann beim Kopieren von ACE-Informationen von einer ACL in eine andere nützlich sein. Beispielsweise kann auf einen Aufruf von **GetExplicitEntriesFromAcl** zum Abrufen von Informationen zu den ACEs in einer ACL gefolgt werden, indem die zurückgegebenen **EXPLICIT \_ ACCESS-Strukturen** in einem Aufruf der [**SetEntriesInAcl-Funktion**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) übergeben werden, um entsprechende ACEs in einer neuen ACL zu erstellen.

Mit der [**GetEffectiveRightsFromAcl-Funktion**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) können Sie die effektiven Zugriffsrechte bestimmen, die eine DACL einem angegebenen Vertrauensnehmer gewährt. Die effektiven Zugriffsrechte des Vertrauensnehmers sind die Zugriffsrechte, die eine DACL dem Vertrauensnehmer oder allen Gruppen gewährt, deren Mitglied der Vertrauensnehmer ist. **GetEffectiveRightsFromAcl** überprüft alle zugriffs- und zugriffsverweigerungsbasierten ACEs in der angegebenen DACL.

**Verwenden Sie die folgenden Schritte, um die Zugriffsrechte eines Vertrauensnehmers auf ein Objekt zu bestimmen.**

1.  Rufen Sie die [**Funktion GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) oder [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) auf, um einen Zeiger auf die DACL eines Objekts abzurufen.
2.  Rufen Sie die [**GetEffectiveRightsFromAcl-Funktion**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) auf, um die Zugriffsrechte abzurufen, die die DACL einem angegebenen Vertrauensnehmer gewährt.

Mit der [**GetAuditedPermissionsFromAcl-Funktion**](/windows/desktop/api/Aclapi/nf-aclapi-getauditedpermissionsfromacla) können Sie eine SACL überprüfen, um die überwachten Zugriffsrechte für einen angegebenen Vertrauensnehmer oder für alle Gruppen zu bestimmen, deren Mitglied der Vertrauensnehmer ist. Die überwachten Rechte geben die Arten von Zugriffsversuchen an, die bewirken, dass das System einen Überwachungsdatensatz im Sicherheitsereignisprotokoll generiert. Die Funktion gibt zwei [*Zugriffsmasken*](/windows/desktop/SecGloss/a-gly)zurück: eine mit den Zugriffsrechten, die auf fehlgeschlagene Zugriffsversuche überwacht werden, und eine mit den Zugriffsrechten, die für den erfolgreichen Zugriff überwacht werden. **GetAuditedPermissionsFromAcl** überprüft alle Systemüberwachungs-ACEs in einer SACL.

 

 
