---
title: HexInt32Type Simple Type (Ereignisschema)
description: Definiert einen Hexadezimaltyp mit 4 Byte. | HexInt32Type Simple Type (Ereignisschema)
ms.assetid: f4b5226d-2a5e-4756-b4c5-30cfbf13568e
keywords:
- HexInt32Type, einfacher Typ EventLog
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25c977bca3ecf7b883b87a535b40b44024ded2a54025bdcb1ac107254ce932fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904750"
---
# <a name="hexint32type-simple-type-event-schema"></a>HexInt32Type Simple Type (Ereignisschema)

Definiert einen Hexadezimaltyp mit 4 Byte.

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

Der einfache **HexInt32Type-Typ** ist eine **Zeichenfolge,** die durch das folgende Muster eingeschränkt ist:

-   `0[xX][0-9A-Fa-f]{1,8}`

    Der Wert kann ein bis acht Hexadezimalzeichen enthalten (z. B. 0xa oder 0xac7bd361).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





