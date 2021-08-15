---
title: Connection (Connections)-Element
description: Definiert jede Konfigurationseinstellung und ordnet sie einem Namen zu. Das Connection-Element ist optional.
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- Connection-Element EAPHost
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
ms.openlocfilehash: 6948675f7910c46cb2b5db4285ce0df795fa057f275ce29b7f4c664b14c4ce1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498370"
---
# <a name="connection-connections-element"></a>Connection (Connections)-Element

Das **Connection (Connections)-Element** definiert jede Konfigurationseinstellung und ordnet sie einem Namen zu. Das **Connection-Element** ist optional.

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

Das **Connection-Element** wird durch das [**Connections-Element**](eapconnectionpropertiesv1schema-connections-element.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                 | type   | BESCHREIBUNG                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | Identifiziert das EAP-Konfigurationselement.<br/>                                                                    |
| [**Name**](eapconnectionpropertiesv1schema-name-connection-element.md) | Zeichenfolge | Erfasst den Namen der zu definierenden Verbindung und hilft dabei, mehrere Verbindungen zu identifizieren. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Verbindungen**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Verbindungen**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[EAPHost und Legacyschema](eaphost-schemas.md)
</dt> <dt>

[eapconnectionpropertiesv1-Schema](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





