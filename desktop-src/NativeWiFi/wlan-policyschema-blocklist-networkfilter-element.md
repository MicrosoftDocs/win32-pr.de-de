---
description: Gibt die Liste der Drahtlos-LAN-Netzwerke an, mit denen ein Computer keine Verbindung herstellen darf.
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: blocklist-Element (NetworkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- blockList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e852286d00d93904bd185fef6c2f3444bb5987f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958679"
---
# <a name="blocklist-networkfilter-element"></a>blocklist-Element (NetworkFilter)

Das blocklist-Element (NetworkFilter) gibt die Liste der Drahtlos-LAN-Netzwerke an, mit denen ein Computer keine Verbindung herstellen darf.

``` syntax
<xs:element name="blockList">
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

Das **Block List** -Element wird durch das [**NetworkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                        | type                                                                     | BESCHREIBUNG                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [**Netzwerk**](wlan-policyschema-network-blocklist-element.md) | [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) | Das blockierte Netzwerk. <br/> |



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

 

 




