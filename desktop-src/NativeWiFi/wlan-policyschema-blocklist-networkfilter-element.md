---
description: Gibt die Liste der WLAN-Netzwerke an, mit denen ein Computer keine Verbindung herstellen darf.
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: blockList-Element (networkFilter)
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
ms.openlocfilehash: 9c5bd795ee9f5fc21dc205c24306820b4dec7f074638aa0e4f11ba3acde68cd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684420"
---
# <a name="blocklist-networkfilter-element"></a>blockList-Element (networkFilter)

Das blockList-Element (networkFilter) gibt die Liste der WLAN-Netzwerke an, mit denen ein Computer keine Verbindung herstellen darf.

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

Das **blockList-Element** wird durch das [**networkFilter-Element**](wlan-policyschema-networkfilter-wlanpolicy-element.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                        | Typ                                                                     | Beschreibung                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [**Netzwerk**](wlan-policyschema-network-blocklist-element.md) | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Das blockierte Netzwerk. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




