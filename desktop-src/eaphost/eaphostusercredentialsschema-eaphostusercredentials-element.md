---
title: Eaphustuser-Anmelde Informationen-Element
description: Enthält das EapMethod-Element und die-Anmelde Informationen oder das-Element für das-Element.
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- Eaphostuser-Anmelde Informationen-Element EAPHost
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
ms.openlocfilehash: 690770091219e51b3ebb550a1a72e50f76b20542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104871"
---
# <a name="eaphostusercredentials-element"></a>Eaphustuser-Anmelde Informationen-Element

Das **eapanstuseranmelde** -Element enthält das [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) -Element und die [**Anmelde**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) [**Informationen oder das**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) Element "-Element".

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



| Element                                                                                                | type                                                                                                                | BESCHREIBUNG                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Daten**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [**Baseeapmethoduseranmeldeinformationen**](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | Wird verwendet, wenn die Methoden Konfiguration im XML-Textformular statt in einem binären BLOB erfolgt.<br/>   |
| [**"Kredentialsblob"**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | hexBinary                                                                                                           | Wird verwendet, wenn die Methoden Konfiguration ein binäres Blob anstelle von im XML-Textformat ist.<br/> |
| [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [**Eapmethodtype**](eapcommonschema-eapmethodtype-complextype.md)                                                  | Identifiziert die Methode, auf die verwiesen wird. <br/>                                             |



## <a name="remarks"></a>Bemerkungen

Die Elemente " [**Anmelde**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) Informationen" und " [**kredentialsblob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) " können nicht gleichzeitig verwendet werden.

Es gibt einen Erweiterungs Punkt für andere Namespaces.

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

[eaphustuseranmelde-Schema](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





