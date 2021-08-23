---
description: Enthält die globalen Einstellungen für die automatische Konfiguration verkabelter Netzwerke.
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: globalFlags-Element (LANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfbfecbc1d60e34a913bb523f5af8c2ab25665fd689976c87725d392f6ea26c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801130"
---
# <a name="globalflags-lanpolicy-element"></a>globalFlags-Element (LANPolicy)

Das element globalFlags (LANPolicy) enthält die globalen Einstellungen für die automatische Konfiguration von kabelgebundenen Netzwerken.

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Das **globalFlags-Element** wird durch das [**LANPolicy-Element**](lan-policyschema-lanpolicy-element.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                           | Typ    | Beschreibung                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) | boolean | Gibt an, ob Computer den integrierten automatischen Konfigurationsdienst verwenden, um Verbindungen mit kabelgebundenen Netzwerken zu verwalten, die eine Layer-2-Authentifizierung erfordern (z. B. 802.1X).<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




