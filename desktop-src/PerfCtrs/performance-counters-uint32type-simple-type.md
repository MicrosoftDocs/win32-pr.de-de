---
description: Definiert einen ganzzahligen Typ ohne Vorzeichen.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: UInt32Type Simple Type (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c32901167bcf181e5400ddb1d3b91ed7383965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348611"
---
# <a name="uint32type-simple-type-performance-counters"></a>UInt32Type Simple Type (Leistungsindikatoren)

Definiert einen ganzzahligen Typ ohne Vorzeichen.

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Bemerkungen

Sie können den Wert als 4-Byte-Ganzzahl oder Hexadezimalwert im Bereich von 0 bis 4.294.967.295 angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




