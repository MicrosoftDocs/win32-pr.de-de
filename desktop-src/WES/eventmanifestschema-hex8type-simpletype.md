---
title: HexInt8Type einfacher Typ
description: Definiert einen hexadezimalen 1-Byte-Typ.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- HexInt8Type einfaches Ereignisprotokoll
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68e56340ee535531fb6711dcf01a72d92665cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479203"
---
# <a name="hexint8type-simple-type"></a>HexInt8Type einfacher Typ

Definiert einen hexadezimalen 1-Byte-Typ.

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

Der einfache **HexInt8Type** -Typ ist eine [Zeichenfolge](/dotnet/api/system.string) , die durch das folgende Muster eingeschränkt ist:

-   `0[xX][0-9A-Fa-f]{1,2}`

    Der Wert kann zwischen 1 und zwei hexadezimal Zeichen (z. b. 0xA oder 0xac) enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

