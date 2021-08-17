---
description: Verwenden Sie die Funktionen GetSecurityInfo und GetNamedSecurityInfo, um einen Zeiger auf einen Objektsicherheitsdeskriptor abzurufen.
ms.assetid: 834f1b58-d403-4899-865e-5721a37587e9
title: Sicherheitsbeschreibungsvorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9c7a7d1dab22f27bad785c6e1394403588a1719b2cc29932aba909aec89ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780132"
---
# <a name="security-descriptor-operations"></a>Sicherheitsbeschreibungsvorgänge

Die Windows-API bietet Funktionen zum Abrufen und Festlegen der Komponenten der [*Sicherheitsbeschreibung,*](/windows/desktop/SecGloss/s-gly) die einem sicherungsfähigen Objekt zugeordnet ist. Verwenden Sie die Funktionen [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) und [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) um einen Zeiger auf die Sicherheitsbeschreibung eines Objekts abzurufen. Diese Funktionen können auch Zeiger auf die einzelnen Komponenten der Sicherheitsbeschreibung abrufen: DACL, SACL, Besitzer-SID und primäre Gruppen-SID. Verwenden Sie die Funktionen [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) und [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) um die Komponenten der Sicherheitsbeschreibung eines Objekts festzulegen.

Im Allgemeinen sollten Sie [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) und [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) mit Objekten verwenden, die durch ein Handle identifiziert werden, und [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) und [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) mit Objekten, die durch einen Namen identifiziert werden. Weitere Informationen zu den spezifischen Funktionen, die beim Arbeiten mit den verschiedenen Objekttypen verwendet werden sollen, finden Sie unter [Sicherungsfähige Objekte.](securable-objects.md)

Die Windows-API bietet zusätzliche Funktionen zum Bearbeiten der Komponenten eines Sicherheitsdeskriptors. Informationen zum Arbeiten mit Zugriffssteuerungslisten (DACLs oder SACLs) finden Sie unter [Abrufen von Informationen aus einer Zugriffssteuerungsliste](getting-information-from-an-acl.md) und Erstellen oder Ändern einer [Zugriffssteuerungsliste.](creating-or-modifying-an-acl.md) Informationen zu SIDs finden Sie unter [Sicherheitsbezeichner](security-identifiers.md) (SIDs).

Rufen Sie die [**GetSecurityDescriptorControl-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) auf, um die Steuerelementinformationen in einem Sicherheitsdeskriptor abzurufen. Um die Steuerungsbits festzulegen, die sich auf die automatische ACE-Vererbung beziehen, rufen Sie die [**SetSecurityDescriptorControl-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) auf. Andere Steuerungsbits werden von den verschiedenen Funktionen festgelegt, die eine Sicherheitsbeschreibungskomponente festlegen. Wenn Sie z. B. [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) verwenden, um die DACL eines Objekts zu ändern, legt die Funktion die Bits entsprechend fest oder löscht sie, um anzugeben, ob der Sicherheitsdeskriptor über eine DACL verfügt, ob es sich um eine Standard-DACL handelt usw. Ein weiteres Beispiel sind die Resource Manager-Steuerungsbits (RM), die in der Sicherheitsbeschreibung enthalten sind. [](/windows/desktop/SecGloss/r-gly) Diese Bits werden gemäß der Implementierung des Ressourcen-Managers verwendet und über die Funktionen [**GetSecurityDescriptorRMControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorrmcontrol) und [**SetSecurityDescriptorRMControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorrmcontrol) aufgerufen.

 

 
