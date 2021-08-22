---
description: Definiert einen hexadezimalen 4-Byte-Typ.
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: HexInt32Type Simple Type (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08b9ea7e483f6580e3f896a6a3f54a65e9117597538564889df8a5afb2fe795f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033480"
---
# <a name="hexint32type-simple-type-performance-counters"></a>HexInt32Type Simple Type (Leistungsindikatoren)

Definiert einen hexadezimalen 4-Byte-Typ.

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

Der **einfache HexInt32Type-Typ** ist ein **xs:string-Objekt,** das durch das folgende Muster eingeschränkt ist:

-   `0[xX][0-9A-Fa-f]{1,8}`

    Der Wert kann ein bis acht Hexadezimalzeichen enthalten (z. B. 0xa oder 0xac7bd361).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




