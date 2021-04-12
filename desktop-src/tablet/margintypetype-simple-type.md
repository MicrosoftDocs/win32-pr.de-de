---
description: Definiert den Typ, der gültige Werte für das Type-Attribut für das Margin-Element enthält.
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: Margintypetype simple-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MarginTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4e8a09e98611fabc54a029c9cac9cb37dfc1373f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218044"
---
# <a name="margintypetype-simple-type"></a>Margintypetype simple-Typ

Definiert den Typ, der gültige Werte für das **Type** -Attribut für das [Margin-Element](margin-element.md)enthält.

``` syntax
<xs:simpleType name="MarginTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Left|Right"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der einfache Typ von **margintypetype** ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:

-   `Left|Right`

## <a name="remarks"></a>Bemerkungen

Gültige Werte für das **Type** -Attribut für das [Margin-Element](margin-element.md) sind "Left" und "Right".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



 

 




