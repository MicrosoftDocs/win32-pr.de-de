---
title: Eaphostconfig-Element
description: Enthält das EapMethod-Element und das config-oder configblob-Element. Die Elemente config und configblob können nicht gleichzeitig verwendet werden.
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- Eaphostconfig-Element EAPHost
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
ms.openlocfilehash: 125b5fa2cab8bf3f9da12bd842a1a102beee3fb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040030"
---
# <a name="eaphostconfig-element"></a>Eaphostconfig-Element

Das **eaphostconfig** -Element enthält das [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) -Element und das [**config**](eaphostconfigschema-config-eaphostconfig-element.md) -oder [**configblob**](eaphostconfigschema-configblob-eaphostconfig-element.md) -Element.

Die Elemente [**config**](eaphostconfigschema-config-eaphostconfig-element.md) und [**configblob**](eaphostconfigschema-configblob-eaphostconfig-element.md) können nicht gleichzeitig verwendet werden.

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



| Element                                                                    | type                                                                                     | BESCHREIBUNG                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Einstellungen**](eaphostconfigschema-config-eaphostconfig-element.md)         | [**Baseeapmethodconfig**](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | Wird verwendet, wenn die Methoden Konfiguration im XML-Textformular statt in einem binären BLOB erfolgt.<br/>       |
| [**Configblob**](eaphostconfigschema-configblob-eaphostconfig-element.md) | hexBinary                                                                                | Wird verwendet, wenn die Methoden Konfiguration im binären BLOB-Formular statt im Textformat der Zeichenfolge verwendet wird.<br/> |
| [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [**Eapmethodtype**](eapcommonschema-eapmethodtype-complextype.md)                       | Identifiziert die Methode, auf die verwiesen wird. <br/>                                                 |



## <a name="remarks"></a>Bemerkungen

Das Element **processContents** ermöglicht zukünftige Erweiterungen des Schemas. Das **processContents** -Element ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eaphostconfig-Schema](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





