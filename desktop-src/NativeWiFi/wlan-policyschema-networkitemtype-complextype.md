---
description: Gibt den Namen und den Typ eines drahtlos Netzwerks an.
ms.assetid: 839afae0-b8e1-489f-8811-19a82c173627
title: komplexer networkitemtype-Typ
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
ms.openlocfilehash: 5db7c5fc4d9b5227d9cd29c5e2dfc69da6fad139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362653"
---
# <a name="networkitemtype-complex-type"></a>komplexer networkitemtype-Typ

Der komplexe Typ networkitemtype gibt den Namen und den Typ eines drahtlos Netzwerks an.

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



| Element                                                                      | type                                                                    | BESCHREIBUNG                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Network Name**](wlan-policyschema-networkname-networkitemtype-element.md) | [**networknametype**](wlan-policyschema-networknametype-simpletype.md) | Der Service Set Identifier (SSID) des Netzwerks. <br/> |
| [**Network Type**](wlan-policyschema-networktype-networkitemtype-element.md) | [**Network Typetype**](wlan-policyschema-networktypetype-simpletype.md) | Der Netzwerktyp. <br/>                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




