---
title: EapType-Element (mspeapconnectionpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des EapType-Elements aus dem BaseEapConnectionProperties-Schema. Für mspeapconnectionpropertiesv1schema.
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
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
ms.openlocfilehash: 47f3585f35b2e7ee7722cdd99c90605cdb7864b2211fcf28f7ec0ac662b5289b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117719771"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a>EapType-Element (mspeapconnectionpropertiesv1schema)

Das **EapType-Element** ist ein abgeleiteter Typ des [**EapType-Elements**](baseeapconnectionpropertiesv1schema-eaptype-element.md) aus dem [BaseEapConnectionProperties-Schema.](baseeapconnectionpropertiesv1schema-schema.md)

Dieses **abgeleitete EapType-Element** enthält die folgenden Elemente: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) und [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).

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
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                     | type                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | Beschreibt die innere Methode und die Methodenkonfiguration. Wenn das [**InnerEapOptional-Element**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) TRUE ist, muss [**das Eap-Element**](baseeapconnectionpropertiesv1schema-eap-element.md) vorhanden sein. Wenn das [**InnerEapOptional-Element**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) FALSE ist, muss [**das Eap-Element**](baseeapconnectionpropertiesv1schema-eap-element.md) fehlen.<br/>           |
| [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | boolean                                                                                                         | Gibt an, ob Nap-Überprüfungen (Network Access Protection, Netzwerkzugriffsschutz) durchgeführt werden. Wenn das [**EnableQuarantineChecks-Element**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) TRUE ist, führt PEAP NAP-Überprüfungen durch. , wenn FALSE PEAP keine NAP-Überprüfungen vorlädt. Das [**EnableQuarantineChecks-Element**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) ist optional.<br/>                                                                                |
| [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | boolean                                                                                                         | Gibt an, ob eine schnelle wiederhergestellte Verbindung hergestellt werden soll. Wenn das [**FastReconnect-Element**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) TRUE ist, versucht PEAP, eine schnelle Wiederherstellung der Verbindung durchzuführen. bei FALSE führt PEAP die vollständige Authentifizierung aus. Das [**FastReconnect-Element**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) ist optional.<br/>                                                                                                                       |
| [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [**IdentityPrivacyParameters**](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | Windows 7 oder höher: Gibt an, ob die echte Identität eines Benutzers oder eine anonyme Identität gesendet wird. Das [**IdentityPrivacy-Element**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) ist optional.<br/>                                                                                                                                                                                                                                                                                 |
| [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | boolean                                                                                                         | Gibt an, ob der GAST-Zugriff durchzuführen ist. Wenn das [**InnerEapOptional-Element**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) TRUE ist, muss das [**Eap-Element**](baseeapconnectionpropertiesv1schema-eap-element.md) vorhanden sein und die innere Methode und ihre Konfiguration beschreiben. bei FALSE führt PEAP GASTzugriff aus. Das [**InnerEapOptional-Element**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) ist optional.<br/>            |
| [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | Das [**PeapExtensions-Element**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) ermöglicht zukünftige Erweiterungen des Schemas. Das [**PeapExtensions-Element**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) ist optional.<br/>                                                                                                                                                                                                                                    |
| [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | boolean                                                                                                         | Gibt an, ob die Authentifizierung bei Servern erfolgen soll, die cryptobinding unterstützen. Wenn das [**RequireCryptoBinding-Element**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) TRUE ist, authentifiziert sich PEAP bei Servern, die cryptobinding nicht unterstützen. bei FALSE authentifiziert sich PEAP nur bei Servern, die cryptobinding unterstützen. Das [**RequireCryptoBinding-Element**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) ist optional.<br/> |
| [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | Enthält Informationen zum Ausführen der Serverüberprüfung. Das [**ServerValidation-Element**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) ist optional.<br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schemaelemente](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





