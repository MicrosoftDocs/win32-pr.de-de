---
title: Komplexer CredentialsSourceParameters-Typ
description: Definiert das Element, das erforderlich ist, um die Quelle des Zertifikats anzugeben, das mit einer EAP-TLS-Authentifizierung verwendet werden soll.
ms.assetid: 1482694e-3025-4231-8154-4be0301fe5ce
keywords:
- 'CredentialsSourceParameters: komplexer Typ EAPHost'
topic_type:
- apiref
api_name:
- CredentialsSourceParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 881cd4225c0e7e2f557ad7206176224a0b3929cdac7398b29f30382506f816ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274007"
---
# <a name="credentialssourceparameters-complex-type"></a>Komplexer CredentialsSourceParameters-Typ

Der komplexe **CredentialsSourceParameters-Typ** definiert das Element, das erforderlich ist, um die Quelle des Zertifikats anzugeben, das mit einer EAP-TLS-Authentifizierung verwendet werden soll.

Es gibt eine Auswahl zwischen dem [**SmartCard-Element**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) oder [**dem CertificateStore-Element.**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)

``` syntax
<xs:complexType name="CredentialsSourceParameters">
    <xs:choice>
        <xs:element name="SmartCard"
            type="emptyString"
         />
        <xs:element name="CertificateStore"
            type="CertSelection"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                             | type                                                                                  | Beschreibung                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | Gibt an, dass EAP-TLS das Zertifikat aus dem My Store des Benutzers oder dem authentifizierten Computer lesen soll. <br/> |
| [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [**emptyString**](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | Gibt an, dass EAP-TLS das Zertifikat von der Smartcard lesen soll. <br/>                                          |



## <a name="remarks"></a>Hinweise

Die [**Elemente CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) und [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) können nicht gleichzeitig verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 : Komplexe Schematypen](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





