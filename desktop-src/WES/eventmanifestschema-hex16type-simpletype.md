---
title: HexInt16Type einfacher Typ
description: Definiert einen 2-Byte-hexadezimal-Typ.
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- HexInt16Type einfaches Ereignisprotokoll
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6aaa5021fbc5a7de5c16083c0f7744bc4a154c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478663"
---
# <a name="hexint16type-simple-type"></a>HexInt16Type einfacher Typ

Definiert einen 2-Byte-hexadezimal-Typ.

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

Der einfache **HexInt16Type** -Typ ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:

-   `0[xX][0-9A-Fa-f]{1,4}`

    Der Wert kann zwischen einem und vier hexadezimal Zeichen (z. b. 0xA oder 0xac7b) enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





