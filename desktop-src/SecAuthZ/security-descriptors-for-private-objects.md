---
description: Um einen Sicherheitsdeskriptor zu erstellen, kann ein geschützter Server das gleiche Verfahren verwenden, das eine Anwendung zum Erstellen eines Sicherheitsdeskriptors für ein sicherungsfähiges Objekt verwendet.
ms.assetid: f40c4b62-a3f0-4e66-875e-2ef904d052e5
title: Sicherheitsbeschreibungen für private Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bae6615f309e572dc2e22f76310ccdf84bbbf5fff504aef0331d7d8e6b60ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413730"
---
# <a name="security-descriptors-for-private-objects"></a>Sicherheitsbeschreibungen für private Objekte

Um einen [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly)zu erstellen, kann ein geschützter Server das gleiche Verfahren verwenden, das eine Anwendung zum Erstellen eines Sicherheitsdeskriptors für ein sicherungsfähiges Objekt verwenden würde. Beispielcode finden Sie unter [Creating a Security Descriptor for a New Object in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md)(Erstellen eines Sicherheitsdeskriptors für ein neues Objekt in C++). Alternativ dazu kann eine geschützte Serveranwendung die [**Funktion BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) aufrufen. Wenn ein Zeiger auf [](/windows/desktop/SecGloss/s-gly) einen vorhandenen selbst relativen Sicherheitsdeskriptor für **BuildSecurityDescriptor** bereitgestellt wird, wird der neue Sicherheitsdeskriptor mit Informationen aus diesem Sicherheitsdeskriptor mit neuen Zugriffssteuerungsinformationen zusammengeführt, die als Parameter im Funktionsaufruf übergeben werden. Der Besitzer und die Gruppe werden optional durch [**DIE VERTRAUENS-Strukturen angegeben,**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) die an die Funktion übergeben werden. Der von **BuildSecurityDescriptor erstellte Sicherheitsdeskriptor** hat das *selbst relative* Format.

Darüber hinaus stellt die Windows-API eine Reihe von Funktionen zum Zusammenführen von Clientsicherheitsinformationen mit Informationen bereit, die vom Sicherheitsdeskriptor für ein übergeordnetes Objekt oder von einem Standardsicherheitsdeskriptor geerbt wurden. Die [**Funktionen CreatePrivateObjectSecurity,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) [**GetPrivateObjectSecurity,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity) [**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)und [**DestroyPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity) bieten die Möglichkeit, Standardinformationen aus einem Zugriffstoken [*abzurufen,*](/windows/desktop/SecGloss/a-gly)Vererbung zu unterstützen und bestimmte Teile des Sicherheitsdeskriptors zu bearbeiten. Dies kann nützlich sein, wenn ein Client ein privates Objekt in einer Hierarchie geschützter Objekte erstellt. Beispielsweise können Sie die **CreatePrivateObjectSecurity-Funktion** verwenden, um einen Sicherheitsdeskriptor zu erstellen, der vom Client angegebene ACEs, ACEs, die von einem übergeordneten Objekt geerbt wurden, und den Standardbesitzer aus dem Zugriffstoken des erstellenden Clients enthält. Während [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) Sicherheitsdeskriptoren entweder aus Zugriffssteuerungsinformationen erstellt, die an den Funktionsaufruf übergeben werden, oder aus einem vorhandenen Sicherheitsdeskriptor, erstellt **CreatePrivateObjectSecurity** einen Sicherheitsdeskriptor ausschließlich aus den Informationen in vorhandenen Sicherheitsdeskriptoren.

[**Die LookupSecurityDescriptorParts-Funktion**](/windows/desktop/api/Aclapi/nf-aclapi-lookupsecuritydescriptorpartsa) erhält Sicherheitsdeskriptorinformationen aus einem vorhandenen [*selbst relativen Sicherheitsdeskriptor.*](/windows/desktop/SecGloss/s-gly) Diese Informationen umfassen die Besitzer- und Gruppenspezifikation, die Anzahl von ACEs in der SACL oder DACL und die Liste der ACEs in der SACL oder DACL.

 

 
