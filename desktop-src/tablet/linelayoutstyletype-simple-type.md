---
description: Definiert die gültigen Werte für das Style-Attribut des linelayout-Elements.
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: Einfacher linelayoutstyletype-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 67b07d9de51e16148905768d7a6f268038bb1afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349698"
---
# <a name="linelayoutstyletype-simple-type"></a>Einfacher linelayoutstyletype-Typ

Definiert die gültigen Werte für das **Style** -Attribut des [linelayout-Elements](linelayout-element.md).

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der einfache Typ **linelayoutstyletype** ist eine Zeichenfolge, die durch das folgende Muster eingeschränkt ist:

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a>Bemerkungen

Gültige Werte für das **Style** -Attribut des [linelayout-Elements](linelayout-element.md) sind:

-   Keine
-   Basis
-   Strich
-   Punkt
-   DashDot
-   DashDotDot
-   Double

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



 

 




