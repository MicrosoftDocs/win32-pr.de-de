---
title: HexInt64Type Simple Type (Ereignisschema)
description: Definiert einen Hexadezimaltyp mit 8 Byte. | HexInt64Type Simple Type (Ereignisschema)
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
keywords:
- HexInt64Type, einfacher Typ EventLog
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fcc4e3cea12be0fecaf7cef2dcd6f9687f4aa4340f9eaca4f8a6bad10c88eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120145"
---
# <a name="hexint64type-simple-type-event-schema"></a>HexInt64Type Simple Type (Ereignisschema)

Definiert einen Hexadezimaltyp mit 8 Byte.

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der einfache **HexInt64Type-Typ** ist eine **Zeichenfolge,** die durch das folgende Muster eingeschränkt ist:

-   `0[xX][0-9A-Fa-f]{1,16}`

    Der Wert kann zwischen 1 und 16 Hexadezimalzeichen (z. B. 0xa oder 0xac7bd361004fe190) enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





