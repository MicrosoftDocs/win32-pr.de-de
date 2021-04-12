---
description: Enthält die globalen Einstellungen für die automatische Konfiguration von verkabelten Netzwerken.
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: globalflags-Element (lanpolicy)
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
ms.openlocfilehash: c9a244fbbc616e3092e2293fe187da1d7be0fa53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216927"
---
# <a name="globalflags-lanpolicy-element"></a>globalflags-Element (lanpolicy)

Das globalflags-Element (lanpolicy) enthält die globalen Einstellungen für die automatische Konfiguration von verkabelten Netzwerken.

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

Das **globalflags** -Element wird durch das [**lanpolicy**](lan-policyschema-lanpolicy-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                           | type    | BESCHREIBUNG                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**enableautoconfig**](lan-policyschema-enableautoconfig-globalflags-element.md) | boolean | Gibt an, ob Computer den integrierten automatischen Konfigurations Dienst zum Verwalten von Verbindungen mit verkabelten Netzwerken verwenden, die Layer 2-Authentifizierung erfordern (z. b. 802.1 x).<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Lanpolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Lanpolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




