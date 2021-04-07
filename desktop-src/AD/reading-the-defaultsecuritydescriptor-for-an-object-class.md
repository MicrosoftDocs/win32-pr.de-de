---
title: Lesen von defaultSecurityDescriptor für eine Objektklasse
description: Mithilfe von ADSI können Sie das defaultSecurityDescriptor-Attribut für eine Objektklasse mit der IADs-Schnittstelle abrufen.
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, Lesen von defaultSecurityDescriptor für eine Objektklasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e217ae42214c2c07867c2a57427d74fb7636736
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038738"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a>Lesen von defaultSecurityDescriptor für eine Objektklasse

Mithilfe von ADSI können Sie das **defaultSecurityDescriptor** -Attribut für eine Objektklasse mit der [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -Schnittstelle abrufen. Um das **defaultSecurityDescriptor** -Attribut für eine Objektklasse zu erhalten, führen Sie die folgenden Schritte aus.

1.  Einen [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -Schnittstellen Zeiger auf das **classSchema** -Objekt für die Objektklasse erhalten.
2.  Verwenden Sie die [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) -Methode, um die Standard Sicherheits Beschreibung des-Objekts zu erhalten. Der Name der Eigenschaft, die die Sicherheits Beschreibung enthält, ist "defaultSecurityDescriptor". Die-Eigenschaft wird als [**Variante**](/windows/win32/api/oaidl/ns-oaidl-variant) zurückgegeben, die ein BSTR mit der Standard Sicherheits Beschreibung im SDDL-Zeichen folgen Format enthält.
3.  Verwenden Sie die [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) -Funktion, um die SDDL-Zeichen folgen Form in eine Sicherheits Beschreibung zu konvertieren.
4.  Verwenden Sie die Sicherheits-APIs [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**getsecuritydescriptorsacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)und [**getsecuritydescriptorcontrol**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) , um die Teile der Sicherheits Beschreibung zu lesen.

Ein Codebeispiel, in dem veranschaulicht wird, wie Sie dies tun, finden Sie unter [Beispielcode zum Lesen von defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).

 

 