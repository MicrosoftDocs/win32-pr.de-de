---
title: HexInt8Type Simple Type
description: Definiert einen Hexadezimaltyp mit 1 Byte.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- HexInt8Type– einfacher Typ EventLog
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d2d70b7258317f16ac4e134f011a85218fa1b63aa768136f68b1d21c901856e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121006"
---
# <a name="hexint8type-simple-type"></a>HexInt8Type Simple Type

Definiert einen Hexadezimaltyp mit 1 Byte.

``` syntax
<xs:simpleType name="HexInt8Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,2}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der einfache **HexInt8Type-Typ** ist eine [Zeichenfolge,](/dotnet/api/system.string) die durch das folgende Muster eingeschränkt ist:

-   `0[xX][0-9A-Fa-f]{1,2}`

    Der Wert kann ein bis zwei Hexadezimalzeichen enthalten (z. B. 0xa oder 0xac).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

