---
description: Erstellen Sie eine Zugriffssteuerungsliste (Access Control List, ACL), indem Sie die Funktionen auf niedriger Ebene verwenden, einen Puffer für die ACL zuordnen und ihn dann initialisieren, indem Sie die InitializeAcl-Funktion aufrufen.
ms.assetid: 9dcbbd4c-b3b3-43fd-b3a6-0637a53a455a
title: Low-Level-ACL- und ACE-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab8c968c19e652f530abe25aaae11e47f36db1cd6ea7184120987c63a1bd9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670660"
---
# <a name="low-level-acl-and-ace-functions"></a>Low-Level-ACL- und ACE-Funktionen

Um eine [*Zugriffssteuerungsliste*](/windows/desktop/SecGloss/a-gly) (Access Control List, ACL) mithilfe der Funktionen auf niedriger Ebene zu erstellen, ordnen Sie einen Puffer für die ACL zu und initialisieren sie dann, indem Sie die [**InitializeAcl-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializeacl) aufrufen. Verwenden Sie die Funktionen [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) und [**AddAccessDeniedAce,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace) um Zugriffssteuerungseinträge (ACCESS Control [*Entries,*](/windows/desktop/SecGloss/a-gly) ACEs) am Ende einer DACL [*(Discretionary Access Control*](/windows/desktop/SecGloss/d-gly) List) hinzuzufügen. Die [**AddAuditAccessAce-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessace) fügt am Ende einer SACL [*(System Access Control List)*](/windows/desktop/SecGloss/s-gly) einen ACE hinzu. Sie können die [**AddAce-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) verwenden, um eine oder mehrere ACEs an einer angegebenen Position in einer ACL hinzuzufügen. Mit **der AddAce-Funktion** können Sie einer ACL auch einen vererbten ACE hinzufügen. Die [**DeleteAce-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-deleteace) entfernt einen ACE von einer angegebenen Position in einer ACL. Die [**GetAce-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) ruft einen ACE von einer angegebenen Position in einer ACL ab. Die [**FindFirstFreeAce-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-findfirstfreeace) ruft einen Zeiger auf das erste freie Byte in einer ACL ab.

Um eine vorhandene ACL im [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly)eines Objekts zu ändern, verwenden Sie die [**GetSecurityDescriptorDacl-**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl) oder [**GetSecurityDescriptorSacl-Funktion,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl) um die vorhandene ACL zu erhalten. Sie können die [**GetAce-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) verwenden, um ACEs aus der vorhandenen ACL zu kopieren. Verwenden Sie nach dem Zuordnen und Initialisieren einer neuen ACL Funktionen wie [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) und [**AddAce,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) um ACEs hinzuzufügen. Wenn Sie die neue ACL erstellt haben, verwenden Sie die [**Funktion SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) oder [**SetSecurityDescriptorSacl,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) um die neue ACL dem Sicherheitsdeskriptor des Objekts hinzuzufügen.

Sie können die [**Funktionen AddAccessAllowedObjectAce,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) [**AddAccessDeniedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedobjectace)oder [**AddAuditAccessObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessobjectace) verwenden, um [objektspezifische ACEs](object-specific-aces.md) am Ende einer ACL hinzuzufügen.

 

 
