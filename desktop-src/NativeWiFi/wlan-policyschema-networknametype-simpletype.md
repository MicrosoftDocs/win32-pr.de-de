---
description: Definiert einen Zeichenfolgentyp für Dienstsatzbezeichner (Service Set Identifiers, SSIDs).
ms.assetid: c9e79a3d-7d5c-4320-ade2-40124de00920
title: networkNameType Simple Type
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkNameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8f653c84f36730ed9f6f078b3713dde414fbf63469bd4ea43f632842d33d7e14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064750"
---
# <a name="networknametype-simple-type"></a>networkNameType Simple Type

Der einfache networkNameType-Typ definiert einen Zeichenfolgentyp für Dienstsatzbezeichner (Service Set Identifiers, SSIDs). Eine SSID ist eine Zeichenfolge, die mindestens ein Zeichen und höchstens 32 Zeichen lang ist.

``` syntax
<xs:simpleType name="networkNameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="32"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




