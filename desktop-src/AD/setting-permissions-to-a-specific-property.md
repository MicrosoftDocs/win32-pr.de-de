---
title: Festlegen von Berechtigungen für eine bestimmte Eigenschaft
description: Berechtigungen können so festgelegt werden, dass Sie auf eine bestimmte Eigenschaft eines Objekts angewendet werden.
ms.assetid: 7bafba5a-a437-4777-98a0-f478b738a8ca
ms.tgt_platform: multiple
keywords:
- Festlegen von Berechtigungen für eine bestimmte Eigenschaften Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99dbfc3dc682103166b41957a3f52206d84fe671
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038729"
---
# <a name="setting-permissions-to-a-specific-property"></a>Festlegen von Berechtigungen für eine bestimmte Eigenschaft

Berechtigungen können so festgelegt werden, dass Sie auf eine bestimmte Eigenschaft eines Objekts angewendet werden.

**So legen Sie Berechtigungen fest, die für eine bestimmte Eigenschaft eines Objekts gelten**

1.  Legen Sie die Eigenschaft [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS \_ right \_ DS \_ Read \_ Prop** und/oder **ADS \_ right \_ DS \_ Write \_ Prop** fest.
2.  Legen Sie die [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf **ADS \_ AceType \_ Access \_ Allowed \_ Object** oder **ADS \_ AceType \_ Access \_ denied \_ Object** fest.
3.  Legen Sie die [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf die **schemaIdGUID** der Eigenschaft fest. Dies ist die **schemaIdGUID** des **attributeSchema** -Objekts, das die Eigenschaft im Schema definiert. Die GUID muss als Zeichenfolge der Form angegeben werden, die von der [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) -Funktion in der com-Bibliothek erstellt wird.
4.  Legen Sie [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS-Flag- \_ \_ \_ Objekttyp \_ vorhanden** fest.

Weitere Informationen über die **schemaIdGUID** eines vordefinierten Attributs finden Sie unter [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).

Weitere Informationen und ein Codebeispiel, das zum Abrufen einer schemaIDGUID verwendet werden kann, finden Sie unter [Lesen von attributeSchema-und classSchema-Objekten](reading-attributeschema-and-classschema-objects.md).

Weitere Informationen zum Erstellen eines ACE finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).

Weitere Informationen und ein Codebeispiel, das verwendet werden kann, um einen Eigenschafts spezifischen ACE festzulegen, finden Sie unter [Beispielcode für das Festlegen eines ACE für ein Verzeichnis Objekt](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 