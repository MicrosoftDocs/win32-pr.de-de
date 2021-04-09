---
description: Verwenden Sie die Funktionen GetSecurityInfo und GetNamedSecurityInfo, um einen Zeiger auf die Sicherheits Beschreibung eines Objekts abzurufen.
ms.assetid: 834f1b58-d403-4899-865e-5721a37587e9
title: Sicherheitsbeschreibungervorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5574a504468a4f4bb7dc14effe1f4717d695846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129905"
---
# <a name="security-descriptor-operations"></a>Sicherheitsbeschreibungervorgänge

Die Windows-API bietet Funktionen zum erhalten und Festlegen der Komponenten der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) , die einem Sicherungs fähigen Objekt zugeordnet ist. Verwenden Sie die Funktionen [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) und [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) , um einen Zeiger auf die Sicherheits Beschreibung eines Objekts abzurufen. Diese Funktionen können auch Zeiger auf die einzelnen Komponenten der Sicherheits Beschreibung abrufen: DACL, SACL, Besitzer-SID und primäre Gruppen-SID. Verwenden Sie die Funktionen [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) und [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , um die Komponenten der Sicherheits Beschreibung eines Objekts festzulegen.

Im Allgemeinen sollten Sie [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) und [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) mit Objekten verwenden, die durch ein Handle identifiziert werden, und [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) und [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) mit Objekten, die durch einen Namen identifiziert werden. Weitere Informationen zu den spezifischen Funktionen, die beim Arbeiten mit den verschiedenen Objekttypen verwendet werden, finden Sie unter Sicherungs [fähige Objekte](securable-objects.md).

Die Windows-API stellt zusätzliche Funktionen zum Bearbeiten der Komponenten einer Sicherheits Beschreibung bereit. Weitere Informationen zum Arbeiten mit Zugriffs Steuerungs Listen (DACLs oder SACLs) finden Sie unter Abrufen [von Informationen aus einer ACL](getting-information-from-an-acl.md) und [erstellen oder Ändern einer ACL](creating-or-modifying-an-acl.md). Weitere Informationen zu SIDs finden Sie unter [Sicherheits](security-identifiers.md) -IDs (SIDs).

Um die Steuerungsinformationen in einer Sicherheits Beschreibung abzurufen, müssen Sie die [**getsecuritydescriptorcontrol**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) -Funktion aufrufen. Um die Steuerungs Bits festzulegen, die sich auf die automatische ACE-Vererbung beziehen, müssen Sie die Funktion [**setsecuritydescriptorcontrol**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) aufrufen. Andere Steuerungs Bits werden von den verschiedenen Funktionen festgelegt, die eine Sicherheits beschreibungerkomponente festlegen. Wenn Sie z. b. [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) zum Ändern der DACL eines Objekts verwenden, legt die Funktion die Bits entsprechend fest oder löscht Sie, um anzugeben, ob die Sicherheits Beschreibung eine DACL hat, ob es sich um eine standarddacl handelt usw. Ein weiteres Beispiel sind die in der Sicherheits Beschreibung enthaltenen [*Ressourcen-Manager*](/windows/desktop/SecGloss/r-gly) -Steuerungs Bits (RM). Diese Bits werden gemäß der Implementierung des Ressourcen-Managers verwendet, und der Zugriff erfolgt über die Funktionen " [**getsecuritydescriptorrmcontrol**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorrmcontrol) " und " [**setsecuritydescriptorrmcontrol**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorrmcontrol) ".

 

 
