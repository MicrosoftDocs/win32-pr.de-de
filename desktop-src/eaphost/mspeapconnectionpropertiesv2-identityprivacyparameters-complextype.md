---
title: Komplexer identityprivacyparameters-Typ
description: Enthält Informationen zur anonymen Identitäts Verwendung während der Peer-Authentifizierung.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8360065e2ce124531bec63637e2b6560cfc32f54
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104101138"
---
# <a name="identityprivacyparameters-complex-type"></a>Komplexer identityprivacyparameters-Typ

Der komplexe Typ **identityprivacyparameters** enthält Informationen zur anonymen Identitäts Verwendung während der Peer-Authentifizierung.


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





| Element                                                                                                               | type    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Enableidentityprivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | boolean | Gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird.                                                                                                                                                                                                                                                                           |
| [**AnonymousUserName**](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | Zeichenfolge  | enthält eine anonyme Identität, die anstelle der true-Identifizierung eines Benutzers verwendet wird. Sie wird während der ersten Phase der Peer-Authentifizierung gesendet, wenn die **Identität** als nur-Text gesendet wird. Die Verwendung der anonymen Identität wird vom [**enableidentityprivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) -Element bestimmt. |



 

## <a name="remarks"></a>Bemerkungen

Das identityprivacyparameters-Element ist optional.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv2-Schema](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[komplexe mspeapconnectionpropertiesv2-Typen](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




