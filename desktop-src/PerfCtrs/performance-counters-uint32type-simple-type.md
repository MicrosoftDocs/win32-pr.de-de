---
description: 'UInt32Type Simple Type (Leistungsindikatoren): Definiert einen ganzzahligen Typ ohne Vorzeichen.'
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Einfacher UInt32Type-Typ (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92eafff1be2c1dc924a7041ad45cadfca994d03d776f61a3c866d6c3c2f6f380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033380"
---
# <a name="uint32type-simple-type-performance-counters"></a>Einfacher UInt32Type-Typ (Leistungsindikatoren)

Definiert einen ganzzahligen Typ ohne Vorzeichen.

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Hinweise

Sie können den Wert als 4-Byte-Ganzzahl oder Hexadezimalwert im Bereich von 0 bis 4.294.967.295 angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




