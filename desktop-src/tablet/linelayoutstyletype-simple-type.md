---
description: Definiert die gültigen Werte für das Style-Attribut des LineLayout-Elements.
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: Einfacher LineLayoutStyleType-Typ
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
ms.openlocfilehash: d2aa0a42ca2f295cdcccad05931ba651d4018ba377d8d10f09f85b82dcaaea8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031838"
---
# <a name="linelayoutstyletype-simple-type"></a>Einfacher LineLayoutStyleType-Typ

Definiert die gültigen Werte für das **Style-Attribut** des [LineLayout-Elements.](linelayout-element.md)

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

Der einfache **LineLayoutStyleType-Typ** ist eine Zeichenfolge, die durch das folgende Muster eingeschränkt ist:

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a>Hinweise

Gültige Werte für das **Style-Attribut** des [LineLayout-Elements](linelayout-element.md) sind:

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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



 

 




