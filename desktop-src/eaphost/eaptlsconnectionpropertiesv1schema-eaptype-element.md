---
title: EapType-Element (eaptlsconnectionpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des EapType-Elements aus dem BaseEapConnectionProperties-Schema. Für eaptlsconnectionpropertiesv1schema.
ms.assetid: cf92d500-f815-48e2-a7d5-1364cb13a1f0
keywords:
- EapType-Element EAPHost
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
ms.openlocfilehash: b7d448524c65e53ad9142d52786a651e085eddcfc7f3eb28bff558a38fc619fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785205"
---
# <a name="eaptype-element-eaptlsconnectionpropertiesv1schema"></a>EapType-Element (eaptlsconnectionpropertiesv1schema)

Das **EapType-Element** ist ein abgeleiteter Typ des [**EapType-Elements**](baseeapconnectionpropertiesv1schema-eaptype-element.md) aus dem [BaseEapConnectionProperties-Schema.](baseeapconnectionpropertiesv1schema-schema.md)

Dieses abgeleitete **EapType-Element** enthält die folgenden Elemente: [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)und [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).

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
| [**extendedTLS: PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | Windows 7 und höher: Gibt an, ob die Serverüberprüfung ausgeführt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**extendedTLS: AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | Windows 7 und höher: Gibt an, ob der Name eines Servers gelesen wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**extendedTLS: TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | Windows 7 und höher: ermöglicht zukünftige Verbesserungen am Schema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | Enthält Informationen zum Speicherort des EAP-TLS-Zertifikats (Transport Level Security). <br/> Das [**CredentialsSource-Element**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | boolean                                                                                                           | Bestimmt, welcher Benutzername EAP-TLS verwendet werden soll. <br/> Wenn das [**DifferentUsername-Element**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) **TRUE** ist, sollte EAP-TLS einen anderen Benutzernamen als den Namen verwenden, der im Zertifikat angezeigt wird. Wenn das [**DifferentUsername-Element**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) **FALSE** ist, verwendet EAP-TLS den Benutzernamen, der im Zertifikat angezeigt wird.<br/> Das [**DifferentUsername-Element**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) ist optional. <br/> |
| [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | Enthält Informationen zum Ausführen der Servervalidierung. Das [**ServerValidation-Element**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) ist optional. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schemaelemente](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





