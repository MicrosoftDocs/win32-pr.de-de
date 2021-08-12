---
title: EapHostUserCredentials-Element
description: Enthält das EapMethod-Element und das Credentials- oder CredentialsBlob-Element.
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- EapHostUserCredentials-Element EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a18922ef19bd828067ddb0153aa7c6369ecfeebd0446f5a6481f91fa64ca21b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274420"
---
# <a name="eaphostusercredentials-element"></a>EapHostUserCredentials-Element

Das **EapHostUserCredentials-Element** enthält das [**EapMethod-Element**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) und [**das Credentials-**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) oder [**CredentialsBlob-Element.**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md)

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
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



| Element                                                                                                | type                                                                                                                | Beschreibung                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Anmeldeinformationen**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [**BaseEapMethodUserCredentials**](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | Wird verwendet, wenn die Methodenkonfiguration in XML-Textform und nicht in einem binären BLOB vorliegt.<br/>   |
| [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | hexBinary                                                                                                           | Wird verwendet, wenn die Methodenkonfiguration ein binäres BLOB anstelle des XML-Textformats ist.<br/> |
| [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)                                                  | Identifiziert die Methode, auf die verwiesen wird. <br/>                                             |



## <a name="remarks"></a>Hinweise

Die [**Elemente Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) und [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) können nicht gleichzeitig verwendet werden.

Es gibt einen Erweiterungspunkt für andere Namespaces.

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

[eaphostusercredentials-Schema](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





