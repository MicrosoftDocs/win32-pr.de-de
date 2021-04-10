---
title: Komplexer Typ "kredentialssourceparameters"
description: Definiert das Element, das zum Angeben der Quelle des Zertifikats erforderlich ist, das mit einer EAP-TLS-Authentifizierung verwendet werden soll.
ms.assetid: 1482694e-3025-4231-8154-4be0301fe5ce
keywords:
- Der komplexe Typ "fidentialssourceparameters" EAPHost
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
ms.openlocfilehash: 912faa4a388d9a57225991959625a978ca0921f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104870"
---
# <a name="credentialssourceparameters-complex-type"></a>Komplexer Typ "kredentialssourceparameters"

Der komplexe Typ " **fordentialssourceparameters** " definiert das Element, das zum Angeben der Quelle des Zertifikats erforderlich ist, das mit einer EAP-TLS-Authentifizierung verwendet werden soll.

Zwischen dem [**Smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) -Element oder dem [**certifikatestore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) -Element kann eine Auswahl getroffen werden.

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



| Element                                                                                                             | type                                                                                  | BESCHREIBUNG                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [**Certselection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | Gibt an, dass EAP-TLS das Zertifikat aus dem eigenen Speicher des Benutzers oder dem Computer lesen soll, der authentifiziert wird. <br/> |
| [**Smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [**emptyString**](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | Gibt an, dass EAP-TLS das Zertifikat von der Smartcard lesen soll. <br/>                                          |



## <a name="remarks"></a>Bemerkungen

Die [**certifikatestore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) -und [**Smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) -Elemente können nicht gleichzeitig verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[komplexe eaptlsconnectionpropertiesv1-Schema Typen](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





