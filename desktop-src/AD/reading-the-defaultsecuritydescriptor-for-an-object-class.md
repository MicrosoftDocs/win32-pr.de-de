---
title: Lesen von defaultSecurityDescriptor für eine Objektklasse
description: Mit ADSI können Sie das defaultSecurityDescriptor-Attribut für eine Objektklasse mit der IADs-Schnittstelle abrufen.
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- 'Active Directory-Beispiele: Active Directory, Lesen von defaultSecurityDescriptor für eine Objektklasse'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26204ebe31155363a1be8bf30bd1c0495d16a939b58789f421a0772d6d90a9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184691"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a>Lesen von defaultSecurityDescriptor für eine Objektklasse

Mit ADSI können Sie das **defaultSecurityDescriptor-Attribut** für eine Objektklasse mit der [**IADs-Schnittstelle**](/windows/desktop/api/iads/nn-iads-iads) abrufen. Führen Sie die folgenden Schritte aus, um das **defaultSecurityDescriptor-Attribut** für eine Objektklasse zu erhalten.

1.  Hier erhalten Sie [**einen IADs-Schnittstellenzeiger**](/windows/desktop/api/iads/nn-iads-iads) auf das **classSchema-Objekt** für die Objektklasse.
2.  Verwenden Sie die [**IADs.Get-Methode,**](/windows/desktop/api/iads/nf-iads-iads-get) um die Standardsicherheitsbeschreibung des Objekts zu erhalten. Der Name der Eigenschaft, die den Sicherheitsdeskriptor enthält, ist "defaultSecurityDescriptor". Die Eigenschaft wird als [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) zurückgegeben, die einen BSTR mit dem Standardsicherheitsdeskriptor im SDDL-Zeichenfolgenformat enthält.
3.  Verwenden Sie [**die ConvertStringSecurityDescriptorToSecurityDescriptor-Funktion,**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) um das SDDL-Zeichenfolgenformular in einen Sicherheitsdeskriptor zu konvertieren.
4.  Verwenden Sie die Sicherheits-APIs [**GetSecurityDescriptorDacl,**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl) [**GetSecurityDescriptorSacl,**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl) [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)und [**GetSecurityDescriptorControl,**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) um die Teile des Sicherheitsdeskriptors zu lesen.

Ein Codebeispiel, das dies veranschaulicht, finden Sie unter Beispielcode zum Lesen von [defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).

 

 