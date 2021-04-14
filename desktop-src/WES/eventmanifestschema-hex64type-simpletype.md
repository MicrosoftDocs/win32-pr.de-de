---
title: HexInt64Type einfacher Typ
description: Definiert einen 8-Byte-hexadezimal-Typ. | HexInt64Type einfacher Typ
ms.assetid: 2e81ec2b-cf67-42df-92a0-bf45b6dca051
keywords:
- HexInt64Type einfaches Ereignisprotokoll
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8947e594bb067140510b0b5d2046a898018a291e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393941"
---
# <a name="hexint64type-simple-type"></a>HexInt64Type einfacher Typ

Definiert einen 8-Byte-hexadezimal-Typ.

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

Der einfache **HexInt64Type** -Typ ist eine [Zeichenfolge](/dotnet/api/system.string) , die durch das folgende Muster eingeschränkt ist:

-   `0[xX][0-9A-Fa-f]{1,16}`

    Der Wert kann zwischen einem und sechzehn hexadezimalen Zeichen (z. b. 0xA oder 0xac7bd361004fe190) enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

