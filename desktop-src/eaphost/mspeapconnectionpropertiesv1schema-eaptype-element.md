---
title: Eaptype-Element (mspeapconnectionpropertiesv1schema)
description: Dieses Element ist ein abgeleiteter Typ des eaptype-Elements aus dem baseeapconnectionproperties-Schema. Für mspeapconnectionpropertiesv1schema.
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
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
ms.openlocfilehash: 3336e943170afa0ec1f239d4cf7a0c603a0c8e71
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106368278"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a>Eaptype-Element (mspeapconnectionpropertiesv1schema)

Das **eaptype** -Element ist ein abgeleiteter Typ des [**eaptype**](baseeapconnectionpropertiesv1schema-eaptype-element.md) -Elements aus dem [baseeapconnectionproperties](baseeapconnectionpropertiesv1schema-schema.md) -Schema.

Dieses abgeleitete **eaptype** -Element enthält die folgenden Elemente: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**identityprivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**fastreconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**innereapoptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md), [**enablequarantäne-Prüfungen**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**requirecryptobinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) und [**peapextensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).

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
| [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | Beschreibt die innere-Methode und die-Methoden Konfiguration. Wenn das [**innereapoptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) -Element true ist, muss das [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) -Element vorhanden sein. Wenn das [**innereapoptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) -Element false ist, muss das [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) -Element nicht vorhanden sein.<br/>           |
| [**Enablequarantäne-Prüfungen**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | boolean                                                                                                         | Gibt an, ob Netzwerk Zugriffsschutz (NAP)-Überprüfungen durchgeführt werden sollen. Wenn das [**enablequarantäne**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) -Element auf "true" festgestellt wird, werden NAP-Überprüfungen durchgeführt. Wenn der Wert false ist, werden keine NAP-Überprüfungen durchgeführt. Das [**enablequarantäne inechecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) -Element ist optional.<br/>                                                                                |
| [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | boolean                                                                                                         | Gibt an, ob eine schnelle erneute Verbindungs Herstellung durchgeführt werden soll. Wenn das [**fastreconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) -Element "true" ist, versucht die Peer-APP, eine schnelle erneute Verbindungs Herstellung auszuführen. der Wert false gibt an, dass die vollständige Authentifizierung von Peer-App Das [**fastreconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) -Element ist optional.<br/>                                                                                                                       |
| [**Identityprivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [**Identityprivacyparameters**](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | Windows 7 oder höher: gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird. Das [**identityprivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) -Element ist optional.<br/>                                                                                                                                                                                                                                                                                 |
| [**Innereapoptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | boolean                                                                                                         | Gibt an, ob Gast Zugriff durchgeführt werden soll. Wenn das [**innereapoptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) -Element true ist, muss das [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) -Element vorhanden sein und die innere Methode und die zugehörige Konfiguration beschreiben. Wenn der Wert false ist, führt der Peer-Agent den Gast Zugriff aus. Das [**innereapoptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) -Element ist optional.<br/>            |
| [**"Peer Erweiterungen"**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [**Peer-extensionstype**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | Das Element " [**Peer-Erweiterungen**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) " ermöglicht zukünftige Erweiterungen des Schemas. Das Element " [**Peer-Extensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) " ist optional.<br/>                                                                                                                                                                                                                                    |
| [**Requirecryptobinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | boolean                                                                                                         | Gibt an, ob die Authentifizierung mit Servern durch die kryptobindung unterstützt wird. Wenn das Element " [**requirecryptobinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) " den Wert "true" hat, wird die Authentifizierung mit Servern durchführt, die cryptobinding nicht unterstützen. Wenn der Wert false ist, wird die Authentifizierung nur bei Servern durchführt, die cryptobinding unterstützen. Das Element " [**requirecryptobinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) " ist optional.<br/> |
| [**Server Validierung**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [**Servervalidationparameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | Enthält Informationen zum Durchführen der Server Validierung. Das [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) -Element ist optional.<br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema Elemente](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





