---
title: Komplexer maptype-Typ
description: Definiert eine Liste von Name-Wert-Paaren.
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- "\"Maptype Complex Type Event Log\""
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4daf6cfe677ab5585ac580e19c868f1bba17de45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740392"
---
# <a name="maptype-complex-type"></a>Komplexer maptype-Typ

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



| Element                                                          | type                                                                 | BESCHREIBUNG                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**bitMap**](eventmanifestschema-bitmap-maptype-element.md)     | [**Bitmaptype**](eventmanifestschema-bitmaptype-complextype.md)     | Definiert eine Liste von Name-Wert-Paaren, die Bitwerte und Zeichen folgen Werte zuordnen.<br/>     |
| [**valueMap**](eventmanifestschema-valuemap-maptype-element.md) | [**Valuemaptype**](eventmanifestschema-valuemaptype-complextype.md) | Definiert eine Liste von Name-Wert-Paaren, die ganzzahlige Werte und Zeichen folgen Werte zuordnen.<br/> |



## <a name="remarks"></a>Bemerkungen

In der Regel erstellen Sie Zuordnungen, um aufgelistete Zeichen folgen Werte für Ereignisdaten bereitzustellen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie eine Werte Zuordnung und eine Bitmap angegeben werden.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





