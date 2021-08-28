---
description: Gibt den Namen und Typ eines Drahtlosnetzwerks an.
ms.assetid: 839afae0-b8e1-489f-8811-19a82c173627
title: komplexer networkItemType-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkItemType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c5a08eafebc81a1ff9f18c3d4c2cc9df9c096ac0fef9c10ff1caf1142a1ecf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800190"
---
# <a name="networkitemtype-complex-type"></a>komplexer networkItemType-Typ

Der komplexe NetworkItemType-Typ gibt den Namen und Typ eines Drahtlosnetzwerks an.

``` syntax
<xs:complexType name="networkItemType">
    <xs:sequence>
        <xs:element name="networkName"
            type="networkNameType"
         />
        <xs:element name="networkType"
            type="networkTypeType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                      | Typ                                                                    | Beschreibung                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| [**networkName**](wlan-policyschema-networkname-networkitemtype-element.md) | [**networkNameType**](wlan-policyschema-networknametype-simpletype.md) | Der Dienstsatzbezeichner (Service Set Identifier, SSID) des Netzwerks. <br/> |
| [**Networktype**](wlan-policyschema-networktype-networkitemtype-element.md) | [**networkTypeType**](wlan-policyschema-networktypetype-simpletype.md) | Der Netzwerktyp. <br/>                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




