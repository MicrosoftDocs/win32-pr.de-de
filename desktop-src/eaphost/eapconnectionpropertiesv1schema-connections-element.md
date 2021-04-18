---
title: Connections-Element
description: Erfahren Sie mehr über das Connections-Element. Dieses Element sammelt und enthält keine oder mehrere Verbindungselemente.
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
ms.openlocfilehash: 6cdb23c9f1a6130e2fe77061286e8a0657c3e2f5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106340534"
---
# <a name="connections-element"></a>Connections-Element

Das **Connections** -Element sammelt und enthält keine oder mehrere [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) -Elemente.

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
| [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | Identifiziert das EAP-Konfigurationselement.<br/>                                                                                                                                       |
| [**Verbindung**](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | Definiert jede Konfigurationseinstellung und verknüpft Sie mit einem Namen. Das [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) -Element ist optional.<br/> |
| [**Name**](eapconnectionpropertiesv1schema-name-connection-element.md)              | Zeichenfolge | Hiermit wird der Name der zu definierenden Verbindung erfasst und die Identifizierung mehrerer Verbindungen unterstützt.<br/>                                                                     |



## <a name="remarks"></a>Bemerkungen

Das **Connections** -Element wird nicht mit Legacy Methoden über die EAPHost-APIs verwendet.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eapconnectionpropertiesv1-Schema](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





