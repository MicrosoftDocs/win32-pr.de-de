---
description: Gibt die Liste der Drahtlos-LAN-Netzwerke an, denen jeder Computer eine Verbindung herstellen darf.
ms.assetid: e24557d8-dedf-4381-bba0-cdb7ea26083b
title: AllowList-Element (NetworkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5488f962a1ba526b34ca2d10144a150d7c1417d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344855"
---
# <a name="allowlist-networkfilter-element"></a>AllowList-Element (NetworkFilter)

Das AllowList (NetworkFilter)-Element gibt die Liste der Drahtlos-LAN-Netzwerke an, denen jeder Computer eine Verbindung herstellen darf.

``` syntax
<xs:element name="allowList">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="network"
                type="networkItemType"
                maxOccurs="unbounded"
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

Das **AllowList** -Element wird durch das [**NetworkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                        | type                                                                     | BESCHREIBUNG                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**Netzwerk**](wlan-policyschema-network-allowlist-element.md) | [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) | Das Netzwerk, mit dem der Computer eine Verbindung herstellen kann.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Network Filter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Network Filter (wlanpolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




