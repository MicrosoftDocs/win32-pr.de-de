---
title: Komplexer IdentityPrivacyParameters-Typ
description: Enthält Informationen zur Verwendung anonymer Identitäten während der PEAP-Authentifizierung.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 18bef3eb69ab2799f7139fe2886d89e996fb8fb47d178997694c568450fb8340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983900"
---
# <a name="identityprivacyparameters-complex-type"></a>Komplexer IdentityPrivacyParameters-Typ

Der **komplexe IdentityPrivacyParameters-Typ** enthält Informationen zur Verwendung anonymer Identitäten während der PEAP-Authentifizierung.


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| Element                                                                                                               | type    | Beschreibung                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | boolean | Gibt an, ob die echte Identität eines Benutzers oder eine anonyme Identität gesendet wird.                                                                                                                                                                                                                                                                           |
| [**AnonymousUserName**](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | Zeichenfolge  | enthält eine anonyme Identität, die statt der tatsächlichen Identifizierung eines Benutzers verwendet wird. Er wird während der ersten Phase der PEAP-Authentifizierung gesendet, wenn **identität** als Nur-Text gesendet wird. Die Verwendung anonymer Identitäten wird durch das [**EnableIdentityPrivacy-Element**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) bestimmt. |



 

## <a name="remarks"></a>Hinweise

Das IdentityPrivacyParameters-Element ist optional.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv2-Schema](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Komplexe mspeapconnectionpropertiesv2-Typen](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




