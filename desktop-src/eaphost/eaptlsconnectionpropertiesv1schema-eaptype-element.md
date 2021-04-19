---
title: Eaptype-Element (eaptlsconnectionpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des eaptype-Elements aus dem baseeapconnectionproperties-Schema. Für eaptlsconnectionpropertiesv1schema.
ms.assetid: cf92d500-f815-48e2-a7d5-1364cb13a1f0
keywords:
- Eaptype-Element EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b74341d9b1fdd9121f1d67e2a941d931be049e0f
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106358189"
---
# <a name="eaptype-element-eaptlsconnectionpropertiesv1schema"></a>Eaptype-Element (eaptlsconnectionpropertiesv1schema)

Das **eaptype** -Element ist ein abgeleiteter Typ des [**eaptype**](baseeapconnectionpropertiesv1schema-eaptype-element.md) -Elements aus dem [baseeapconnectionproperties](baseeapconnectionpropertiesv1schema-schema.md) -Schema.

Dieses abgeleitete **eaptype** -Element enthält die folgenden Elemente: " [**kredentialssource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)", " [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)", " [**differenentusername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)", " [**performservervalidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md)", " [**Accepted Server**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)Name" und "[**tlsextensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)".

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="CredentialsSource"
                        type="CredentialsSourceParameters"
                        minOccurs="0"
                     />
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="DifferentUsername"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: PerformServerValidation"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: AcceptServerName"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: TLSExtensions"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                                               | type                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**extendedtls: performservervalidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | Windows 7 und höher: gibt an, ob die Server Validierung durchgeführt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**extendedtls: akzeptservername**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | Windows 7 und höher: gibt an, ob der Name eines Servers gelesen wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**extendedtls: tlsextensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | Windows 7 und höher: ermöglicht zukünftige Erweiterungen des Schemas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**"Kredentialssource"**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [**"Kredentialssourceparameters"**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | Enthält Informationen zum Speicherort des EAP-TLS-Zertifikats (Transport Level Security). <br/> Das Element " [**kredentialssource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) " ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**Differenentusername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | boolean                                                                                                           | Bestimmt, welcher Benutzername von EAP-TLS verwendet werden soll. <br/> Wenn das [**differenentusername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) -Element **true** ist, sollte EAP-TLS einen anderen Benutzernamen als den Namen verwenden, der im Zertifikat angezeigt wird. Wenn das [**differenentusername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) -Element **false** ist, verwendet EAP-TLS den Benutzernamen, der im Zertifikat angezeigt wird.<br/> Das [**differenentusername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) -Element ist optional. <br/> |
| [**Server Validierung**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [**Servervalidationparameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | Enthält Informationen zum Durchführen der Server Validierung. Das [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) -Element ist optional. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



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

[eaptlsconnectionpropertiesv1-Schema Elemente](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





