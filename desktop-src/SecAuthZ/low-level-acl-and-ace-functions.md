---
description: Erstellen Sie eine Zugriffs Steuerungs Liste (ACL) mithilfe der Funktionen auf niedriger Ebene, weisen Sie einen Puffer für die ACL zu, und initialisieren Sie ihn, indem Sie die InitializeAcl-Funktion aufrufen.
ms.assetid: 9dcbbd4c-b3b3-43fd-b3a6-0637a53a455a
title: ACL-und ACE-Funktionen auf niedriger Ebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac63c17d84996afe9bdc43d0ccdd021db69ab488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867804"
---
# <a name="low-level-acl-and-ace-functions"></a>ACL-und ACE-Funktionen auf niedriger Ebene

Um eine [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/a-gly) (ACL) mit den Funktionen auf niedriger Ebene zu erstellen, weisen Sie einen Puffer für die ACL zu, und initialisieren Sie ihn dann durch Aufrufen der [**InitializeAcl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializeacl) -Funktion. Verwenden Sie zum Hinzufügen von [*Zugriffs Steuerungs Einträgen*](/windows/desktop/SecGloss/a-gly) (ACEs) zum Ende einer freigegebenen [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) die Funktionen [**addaccesszuwedace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) und [**addaccessdeniedace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace) . Die [**addauditaccessace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessace) -Funktion fügt am Ende einer [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) einen ACE hinzu. Sie können die [**addace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) -Funktion verwenden, um einen oder mehrere ACEs an einer bestimmten Position in einer ACL hinzuzufügen. Mit der **addace** -Funktion können Sie auch einen vererbbaren ACE zu einer ACL hinzufügen. Die [**deleteace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-deleteace) -Funktion entfernt einen ACE von einer angegebenen Position in einer ACL. Die [**GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) -Funktion Ruft einen ACE von einer angegebenen Position in einer ACL ab. Die [**findfirstfreeace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-findfirstfreeace) -Funktion Ruft einen Zeiger auf das erste freie Byte in einer ACL ab.

Um eine vorhandene ACL in der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)eines Objekts zu ändern, verwenden Sie die Funktion [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl) oder [**getsecuritydescriptorsacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl) , um die vorhandene ACL zu erhalten. Sie können die [**GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) -Funktion verwenden, um ACEs aus der vorhandenen ACL zu kopieren. Verwenden Sie nach dem zuordnen und Initialisieren einer neuen ACL Funktionen wie " [**addaccesszuwedace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) " und " [**addace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) ", um ACEs hinzuzufügen. Wenn Sie die Erstellung der neuen ACL abgeschlossen haben, verwenden Sie die Funktion " [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) " oder " [**setsecuritydescriptorsacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) ", um die neue ACL der Sicherheits Beschreibung des Objekts hinzuzufügen.

Sie können die Funktionen [**addaccesszuwedobjectace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace), [**addaccessdeniedobjectace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedobjectace)oder [**addauditaccesbjectace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessobjectace) verwenden, um [objektspezifische ACEs](object-specific-aces.md) am Ende einer ACL hinzuzufügen.

 

 
