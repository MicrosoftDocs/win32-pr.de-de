---
title: Komplexer servervalidationparameters-Typ (Peer)
description: Erfahren Sie mehr über den komplexen servervalidationparameters-Typ. Dieser Typ enthält Informationen zum Durchführen der Server Validierung. | Komplexer servervalidationparameters-Typ (Peer)
ms.assetid: 65b3199c-9462-447b-b560-0713348f9130
keywords:
- Servervalidationparameters komplexer Typ EAPHost
topic_type:
- apiref
api_name:
- ServerValidationParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42416723c4aaa86665f09ee8aa01d5dc1463c522
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961292"
---
# <a name="servervalidationparameters-complex-type-peap"></a>Komplexer servervalidationparameters-Typ (Peer)

Der komplexe Typ **servervalidationparameters** enthält Informationen zum Durchführen der Server Validierung.

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="complextype"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="PerformServerValidation"
        type="boolean"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                                                                    | type        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Disableuserpromptforservervalidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | boolean     | Gibt an, ob der Benutzer zur Server Validierung aufgefordert werden soll. <br/> Wenn [**disableuserpromptforservervalidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) den Wert true hat, führt die Überprüfung des Servers ohne Benutzereingaben durch. Wenn die Überprüfung fehlschlägt, schlägt die Authentifizierung fehl.<br/> Wenn [**disableuserpromptforservervalidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) den Wert false hat, wird der Benutzer zur Eingabe eines validierten Serverzertifikats oder-Namens bzw. einer Stamm Zertifizierungsstelle aufgefordert.<br/> Das [**disableuserpromptforservervalidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) -Element ist optional.<br/> |
| [**ServerNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | complexType | Stellt eine Liste von Servern dar, denen der Client vertraut. Jeder Servername wird durch Semikolons getrennt und kann durch reguläre Ausdrücke dargestellt werden. <br/> Das [**servernames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) -Element ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Treuhändrootca**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | hexBinary   | Zeichnet den Fingerabdruck der Stamm Zertifizierungsstellen (CAS) auf, die vom Client als vertrauenswürdig eingestuft werden. <br/> Der Thumb-Abdruck ist eine hexadezimale Zeichenfolge, die den SHA-1-Hash des Zertifikats enthält.<br/> Das Element " [**treuhändrootca**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) " ist optional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="attributes"></a>Attributes



| Name                    | type    | BESCHREIBUNG                                                                                                                                                                                                                  |
|-------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Performservervalidation | boolean | Windows 7 oder höher: gibt an, ob die Server Validierung durchgeführt wird. Das [**performservervalidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) -Element ist optional.<br/> |



## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1-Schema](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[komplexe mspeapconnectionpropertiesv1-Schema Typen](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> <dt>

[**Akzeptservername**](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





