---
title: Connection (Connections)-Element
description: Definiert jede Konfigurationseinstellung und verknüpft Sie mit einem Namen. Das Connection-Element ist optional.
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- Verbindungselement EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5aabc29a7fe5122a7f7571750b97ebccb38158d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340594"
---
# <a name="connection-connections-element"></a>Connection (Connections)-Element

Das **Connection (Connections)** -Element definiert jede Konfigurationseinstellung und ordnet ihr einen Namen zu. Das **Connection** -Element ist optional.

``` syntax
<xs:element name="Connection">
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
```

Das **Connection** -Element wird durch das [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                 | type   | BESCHREIBUNG                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | Identifiziert das EAP-Konfigurationselement.<br/>                                                                    |
| [**Name**](eapconnectionpropertiesv1schema-name-connection-element.md) | Zeichenfolge | Hiermit wird der Name der zu definierenden Verbindung erfasst und die Identifizierung mehrerer Verbindungen unterstützt. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Verbindungen**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Verbindungen**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eapconnectionpropertiesv1-Schema](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





