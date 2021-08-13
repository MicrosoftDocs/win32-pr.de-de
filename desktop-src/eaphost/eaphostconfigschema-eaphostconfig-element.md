---
title: EapHostConfig-Element
description: Enthält das EapMethod-Element und das Config- oder ConfigBlob-Element. Die Elemente Config und ConfigBlob können nicht gleichzeitig verwendet werden.
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- EapHostConfig-Element EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c34ddd1607a59c0425f7ec789bedb4981a05983ead276a14308fbf6aaadf26de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274864"
---
# <a name="eaphostconfig-element"></a>EapHostConfig-Element

Das **EapHostConfig-Element** enthält das [**EapMethod-Element**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) und das [**Config-**](eaphostconfigschema-config-eaphostconfig-element.md) oder [**ConfigBlob-Element.**](eaphostconfigschema-configblob-eaphostconfig-element.md)

Die [**Elemente Config**](eaphostconfigschema-config-eaphostconfig-element.md) und [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) können nicht gleichzeitig verwendet werden.

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                    | type                                                                                     | Beschreibung                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Config**](eaphostconfigschema-config-eaphostconfig-element.md)         | [**BaseEapMethodConfig**](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | Wird verwendet, wenn die Methodenkonfiguration in XML-Textform und nicht in einem binären BLOB vorliegt.<br/>       |
| [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) | hexBinary                                                                                | Wird verwendet, wenn die Methodenkonfiguration in binärer BLOB-Form und nicht in Zeichenfolgentextform vorliegt.<br/> |
| [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)                       | Identifiziert die Methode, auf die verwiesen wird. <br/>                                                 |



## <a name="remarks"></a>Hinweise

Das **processContents-Element** ermöglicht zukünftige Erweiterungen des Schemas. Das **processContents-Element** ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaphostconfig-Schema](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





