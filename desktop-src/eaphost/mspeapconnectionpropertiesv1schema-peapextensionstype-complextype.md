---
title: Komplexer Typ von "Peer apextensionstype"
description: Enthält in Windows 7 vorgenommene Schema Erweiterungen. Zukünftige Schema Erweiterungen werden von PeapExtensionsTypeV2 behandelt.
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
keywords:
- Komplexer Typ von "etapextensionstype" EAPHost
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
ms.openlocfilehash: 7cb8c698122c5a466ae95f728838425a5f10c665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742841"
---
# <a name="peapextensionstype-complex-type"></a>Komplexer Typ von "Peer apextensionstype"

Der komplexe Typ " **etapextensionstype** " enthält in Windows 7 vorgenommene Schema Erweiterungen. Zukünftige Schema Erweiterungen werden von [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md)behandelt.

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



| Element                                                                                                                               | type | BESCHREIBUNG                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------|------|------------------------------------------------------------------------------------------------------------|
| [**extendedpeer: performservervalidation**](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | Windows 7 und höher: gibt an, ob die Server Validierung durchgeführt wird.<br/>                          |
| [**extendedetap: akzeptservername**](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | Windows 7 und höher: gibt an, ob der Name eines Servers gelesen wird.<br/>                            |
| [**extendedpeer: identityprivacy**](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | Windows 7 und höher: gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird.<br/> |
| [**extendedpeer: PeapExtensionsV2**](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | Windows 7 und höher: ermöglicht zukünftige Erweiterungen des Schemas.<br/>                                 |



## <a name="remarks"></a>Bemerkungen

Das Element " **Peer-extensionstype** " ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[komplexe mspeapconnectionpropertiesv1-Schema Typen](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





