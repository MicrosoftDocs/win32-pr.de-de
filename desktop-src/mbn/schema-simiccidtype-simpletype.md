---
description: Definiert einen Typ für das simiccid-Element des mobilen Breitband Profils.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: einfacher simiccidtype-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355488"
---
# <a name="simiccidtype-simple-type"></a>einfacher simiccidtype-Typ

Der einfache Typ **simiccidtype** definiert einen Typ für das [**simiccid-**](schema-simiccid-mbnprofile-element.md) Element des mobilen Breitband Profils. Bei diesem Typ handelt es sich um eine Sammlung von Ziffern und/oder groß-und Kleinbuchstaben, mindestens ein Zeichen lang und höchstens 20 Zeichen lang.

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der einfache Typ **simiccidtype** ist ein Token, das durch das folgende Muster eingeschränkt wird:

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




