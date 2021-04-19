---
title: HexInt32Type Simple Type (eventmanifest-Schema)
description: Definiert einen 4-Byte-hexadezimal-Typ. | HexInt32Type Simple Type (eventmanifest-Schema)
ms.assetid: b1006593-c6f2-4669-b242-758ce9977565
keywords:
- HexInt32Type einfaches Ereignisprotokoll
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4630bc4d7d513a0fedad2191c63ca71571ce655a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353309"
---
# <a name="hexint32type-simple-type-eventmanifest-schema"></a>HexInt32Type Simple Type (eventmanifest-Schema)

Definiert einen 4-Byte-hexadezimal-Typ.

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

Der einfache **HexInt32Type** -Typ ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:

-   `0[xX][0-9A-Fa-f]{1,8}`

    Der Wert kann zwischen 1 und acht hexadezimal Zeichen (z. b. 0xA oder 0xac7bd361) enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





