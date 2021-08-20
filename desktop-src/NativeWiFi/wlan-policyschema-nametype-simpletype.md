---
description: Definiert einen Zeichenfolgentyp für den Namen oder die Beschreibung eines WLAN-Richtlinienprofils.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: nameType Simple Type (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6bdef3bad487f404dc62932355b963377b44558d3dee92b6eb0d096c8b342d43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984575"
---
# <a name="nametype-simple-type-lan_policy"></a>nameType Simple Type (LAN_policy)

Der einfache NameType-Typ definiert einen Zeichenfolgentyp für den Namen oder die Beschreibung eines WLAN-Richtlinienprofils. Namen und Beschreibungen sind Zeichenfolgen, die mindestens ein Zeichen lang und höchstens 255 Zeichen lang sind.

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




