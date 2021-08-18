---
title: Komplexer PeapExtensionsType-Typ
description: Enthält Schemaerweiterungen, die in Windows 7 vorgenommen wurden. Zukünftige Schemaerweiterungen werden von PeapExtensionsTypeV2 verarbeitet.
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
keywords:
- Komplexer PeapExtensionsType-Typ EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 212c8bf6b1421cfc461288e8f57258b40e11e9118c9ea2b2f620986e91d226f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984030"
---
# <a name="peapextensionstype-complex-type"></a>Komplexer PeapExtensionsType-Typ

Der **komplexe PeapExtensionsType-Typ** enthält Schemaerweiterungen, die in Windows 7 vorgenommen wurden. Zukünftige Schemaerweiterungen werden von [**PeapExtensionsTypeV2 verarbeitet.**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md)

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PerformServerValidation"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:AcceptServerName"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:IdentityPrivacy"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PeapExtensionsV2"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                                               | type | Beschreibung                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------|------|------------------------------------------------------------------------------------------------------------|
| [**extendedPeap:PerformServerValidation**](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | Windows 7 und höher: Gibt an, ob die Serverüberprüfung ausgeführt wird.<br/>                          |
| [**extendedPeap:AcceptServerName**](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | Windows 7 und höher: Gibt an, ob der Name eines Servers gelesen wird.<br/>                            |
| [**extendedPeap:IdentityPrivacy**](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | Windows 7 und höher: Gibt an, ob die echte Identität eines Benutzers oder eine anonyme Identität gesendet wird.<br/> |
| [**extendedPeap:PeapExtensionsV2**](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | Windows 7 und höher: ermöglicht zukünftige Erweiterungen des Schemas.<br/>                                 |



## <a name="remarks"></a>Hinweise

Das **PeapExtensionsType-Element** ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1 Schema Complex Types](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





