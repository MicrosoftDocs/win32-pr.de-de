---
title: HexInt64Type Simple Type (Ereignis Schema)
description: Definiert einen 8-Byte-hexadezimal-Typ. | HexInt64Type Simple Type (Ereignis Schema)
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
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
ms.openlocfilehash: e290c2326415664fbbae3feed9628b86452b10c6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366417"
---
# <a name="hexint64type-simple-type-event-schema"></a>HexInt64Type Simple Type (Ereignis Schema)

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

Der einfache **HexInt64Type** -Typ ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:

-   `0[xX][0-9A-Fa-f]{1,16}`

    Der Wert kann zwischen einem und sechzehn hexadezimalen Zeichen (z. b. 0xA oder 0xac7bd361004fe190) enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





