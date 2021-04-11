---
description: Definiert einen Zeichen Folgentyp für das iconfilepath-Element im mobilen Breitband Profil.
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: einfacher iconfiletype-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: 168c2709f8b3049270711e286a35fbbd11e1ffef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129013"
---
# <a name="iconfiletype-simple-type"></a>einfacher iconfiletype-Typ

Der einfache **iconfiletype** -Typ definiert einen Zeichen Folgentyp für das [**iconfilepath**](schema-iconfilepath-mbnprofile-element.md) -Element im mobilen Breitband Profil. Bei dieser Zeichenfolge handelt es sich um mindestens ein Zeichen, das höchstens 1024 Zeichen lang ist.

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




