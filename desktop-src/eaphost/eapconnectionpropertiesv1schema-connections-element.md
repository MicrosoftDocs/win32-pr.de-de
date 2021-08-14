---
title: Connections-Element
description: Erfahren Sie mehr über das Connections-Element. Dieses Element sammelt und enthält 0 (null) oder mehr Connection-Elemente.
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Connections-Element EAPHost
topic_type:
- apiref
api_name:
- Connections
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 62635d09030875a4f17deefa1aec05432df5662369eb483894f1a8cef4bbaf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498218"
---
# <a name="connections-element"></a>Connections-Element

Das **Connections-Element** sammelt und enthält 0 (null) oder [**mehr Connection-Elemente.**](eapconnectionpropertiesv1schema-connection-connections-element.md)

``` syntax
<xs:element name="Connections">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Connection"
                minOccurs="0"
                maxOccurs="unbounded"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Name"
                            type="string"
                         />
                        <xs:element
                            maxOccurs="unbounded"
                            ref="Eap"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                              | type   | BESCHREIBUNG                                                                                                                                                                                |
|--------------------------------------------------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | Identifiziert das EAP-Konfigurationselement.<br/>                                                                                                                                       |
| [**Verbindung**](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | Definiert jede Konfigurationseinstellung und ordnet sie einem Namen zu. Das [**Connection-Element**](eapconnectionpropertiesv1schema-connection-connections-element.md) ist optional.<br/> |
| [**Name**](eapconnectionpropertiesv1schema-name-connection-element.md)              | Zeichenfolge | Erfasst den Namen der verbindung, die definiert wird, und unterstützt sie bei der Identifizierung mehrerer Verbindungen.<br/>                                                                     |



## <a name="remarks"></a>Hinweise

Das **Connections-Element** wird nicht mit Legacymethoden über die EAPHost-APIs verwendet.

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Server<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eapconnectionpropertiesv1-Schema](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





