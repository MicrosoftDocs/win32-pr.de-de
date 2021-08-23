---
title: HexInt16Type Simple Type
description: Definiert einen Hexadezimaltyp mit 2 Byte.
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- HexInt16Type – einfacher Typ EventLog
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5f441071daa84f162a1dacbd16513fe2550b99d34d24ed90205ff4d8d184493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055959"
---
# <a name="hexint16type-simple-type"></a>HexInt16Type Simple Type

Definiert einen Hexadezimaltyp mit 2 Byte.

``` syntax
<xs:simpleType name="HexInt16Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,4}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der einfache **HexInt16Type-Typ** ist eine **Zeichenfolge,** die durch das folgende Muster eingeschränkt ist:

-   `0[xX][0-9A-Fa-f]{1,4}`

    Der Wert kann ein bis vier Hexadezimalzeichen enthalten (z. B. 0xa oder 0xac7b).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





