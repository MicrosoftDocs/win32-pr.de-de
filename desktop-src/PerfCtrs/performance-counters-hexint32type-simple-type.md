---
description: Definiert einen 4-Byte-hexadezimal-Typ.
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: HexInt32Type Simple Type (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d2392f2240ca9ca61525b27993e16bcab979a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359040"
---
# <a name="hexint32type-simple-type-performance-counters"></a>HexInt32Type Simple Type (Leistungsindikatoren)

Definiert einen 4-Byte-hexadezimal-Typ.

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der einfache Typ " **HexInt32Type** " ist eine **xs: String** , die durch das folgende Muster eingeschränkt ist:

-   `0[xX][0-9A-Fa-f]{1,8}`

    Der Wert kann zwischen 1 und acht hexadezimal Zeichen (z. b. 0xA oder 0xac7bd361) enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




