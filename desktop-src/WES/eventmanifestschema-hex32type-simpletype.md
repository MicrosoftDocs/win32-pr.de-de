---
title: HexInt32Type Simple Type (EventManifest Schema)
description: Definiert einen hexadezimalen 4-Byte-Typ. | HexInt32Type Simple Type (EventManifest-Schema)
ms.assetid: b1006593-c6f2-4669-b242-758ce9977565
keywords:
- HexInt32Type simple type EventLog
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c78a101ec9854b8820b7c9170ea43f06258528de9fdc9d4b02bb41945ba3a7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248100"
---
# <a name="hexint32type-simple-type-eventmanifest-schema"></a>HexInt32Type Simple Type (EventManifest Schema)

Definiert einen hexadezimalen 4-Byte-Typ.

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der **einfache HexInt32Type-Typ** ist eine **Zeichenfolge,** die durch das folgende Muster eingeschränkt wird:

-   `0[xX][0-9A-Fa-f]{1,8}`

    Der Wert kann ein bis acht Hexadezimalzeichen enthalten (z. B. 0xa oder 0xac7bd361).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





