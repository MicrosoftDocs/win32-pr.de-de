---
title: Festlegen von Berechtigungen auf eine bestimmte Eigenschaft
description: Berechtigungen können so festgelegt werden, dass sie auf eine bestimmte Eigenschaft eines Objekts angewendet werden.
ms.assetid: 7bafba5a-a437-4777-98a0-f478b738a8ca
ms.tgt_platform: multiple
keywords:
- Festlegen von Berechtigungen für ein bestimmtes Eigenschaften-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f55fba3ae2be54a29ade3dee1dc161fa0c6d2dbe478fb42f39319fbeaf4fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183314"
---
# <a name="setting-permissions-to-a-specific-property"></a>Festlegen von Berechtigungen auf eine bestimmte Eigenschaft

Berechtigungen können so festgelegt werden, dass sie auf eine bestimmte Eigenschaft eines Objekts angewendet werden.

**So legen Sie Berechtigungen fest, die für eine bestimmte Eigenschaft eines Objekts gelten**

1.  Legen Sie die [**Eigenschaft IADsAccessControlEntry.AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS RIGHT \_ \_ DS READ \_ \_ PROP** und/oder **ADS RIGHT \_ \_ DS WRITE PROP \_ \_ fest.**
2.  Legen Sie die [**IADsAccessControlEntry.AceType-Eigenschaft**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS \_ ACETYPE \_ ACCESS ALLOWED \_ \_ OBJECT** oder **ADS \_ ACETYPE ACCESS \_ \_ DENIED OBJECT \_ fest.**
3.  Legen Sie [**die IADsAccessControlEntry.ObjectType-Eigenschaft**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **schemaIDGUID der** Eigenschaft fest. Dies ist **die schemaIDGUID des** **attributeSchema-Objekts,** das die -Eigenschaft im Schema definiert. Die GUID muss als Zeichenfolge des Formulars angegeben werden, das von der [**StringFromGUID2-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) in der COM-Bibliothek erzeugt wird.
4.  Legen [**Sie IADsAccessControlEntry.Flags auf**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ADS FLAG OBJECT TYPE PRESENT **\_ \_ \_ \_ fest.**

Weitere Informationen zur **schemaIDGUID** eines vordefinierten Attributs finden Sie unter Active Directory Domain Services [Referenz.](active-directory-domain-services-reference.md)

Weitere Informationen und ein Codebeispiel, das zum Abrufen einer schemaIDGUID verwendet werden kann, finden Sie unter Lesen von attributeSchema und [classSchema Objects](reading-attributeschema-and-classschema-objects.md).

Weitere Informationen zum Erstellen eines ACE finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt.](setting-access-rights-on-an-object.md)

Weitere Informationen und ein Codebeispiel, das zum Festlegen eines eigenschaftenspezifischen ACE verwendet werden kann, finden Sie unter Beispielcode für das Festlegen eines [ACE für ein Verzeichnisobjekt.](example-code-for-setting-an-ace-on-a-directory-object.md)

 

 