---
title: Einfacher LengthType-Typ
description: Definiert einen Längentyp, der verwendet wird, um die Anzahl von Bytes oder Zeichen in einem Datenelement variabler Länge anzugeben, z. B. binäre Daten oder eine ANSI- oder Unicode-Zeichenfolge.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- 'LengthType : EventLog vom typ "simple"'
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9ded861e3e46cd5e4fc6c069d95bba9f0ab3457559bf319aef41cdf906e193b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997860"
---
# <a name="lengthtype-simple-type"></a>Einfacher LengthType-Typ

Definiert einen Längentyp, der verwendet wird, um die Anzahl von Bytes oder Zeichen in einem Datenelement variabler Länge anzugeben, z. B. binäre Daten oder eine ANSI- oder Unicode-Zeichenfolge. Der Wert kann als xs:unsignedShort-Wert oder als Zeichenfolge angegeben werden, die auf den Namen des Datenelementknotens verweist, der den unsigned short-Wert enthält.

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





