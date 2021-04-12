---
description: Definiert einen Zeichen Folgentyp für Service Set Identifier (SSIDs).
ms.assetid: c9e79a3d-7d5c-4320-ade2-40124de00920
title: einfacher networknametype-Typ
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
ms.openlocfilehash: 6b6463644e1bd174be256d51b34ae2ae4ad9ce07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960556"
---
# <a name="networknametype-simple-type"></a>einfacher networknametype-Typ

Der einfache Typ networknametype definiert einen Zeichen Folgentyp für Service Set Identifier (SSIDs). Eine SSID ist eine Zeichenfolge, die mindestens ein Zeichen lang und höchstens 32 Zeichen lang ist.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




