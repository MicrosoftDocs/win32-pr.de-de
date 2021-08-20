---
title: Komplexer MapType-Typ
description: Definiert eine Liste von Name-Wert-Paaren.
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- Komplexer MapType-Typ EventLog
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 162676ab5d017c8fa6d6d280a07d1e4500e77cc79e0eacf25e23d5f20c0b3326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120918"
---
# <a name="maptype-complex-type"></a>Komplexer MapType-Typ

Definiert eine Liste von Name-Wert-Paaren.

``` syntax
<xs:complexType name="MapType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="valueMap"
            type="ValueMapType"
         />
        <xs:element name="bitMap"
            type="BitMapType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                          | Typ                                                                 | Beschreibung                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Bitmap**](eventmanifestschema-bitmap-maptype-element.md)     | [**BitMapType**](eventmanifestschema-bitmaptype-complextype.md)     | Definiert eine Liste von Name-Wert-Paaren, die Bitwerte und Zeichenfolgenwerte zuordnen.<br/>     |
| [**valueMap**](eventmanifestschema-valuemap-maptype-element.md) | [**ValueMapType**](eventmanifestschema-valuemaptype-complextype.md) | Definiert eine Liste von Name-Wert-Paaren, die ganzzahlige Werte und Zeichenfolgenwerte zuordnen.<br/> |



## <a name="remarks"></a>Hinweise

In der Regel erstellen Sie Zuordnungen, um aufzählte Zeichenfolgenwerte für Ereignisdaten zur Verfügung zu stellen.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie eine Wertzuordnung und eine Bitmap angeben.


```XML
<maps>
   <valueMap name="MyValueMap">
       <map value="5" message="$(string.value5)"/>
       <map value="45" message="$(string.value45)"/>
   </valueMap>
 
   <bitMap name="MyBitmap">
       <map value="0x8" message="$(string.bit3)/>
       <map value="0x80" message="$(string.bit7)/>
   </bitMap>
</maps>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





