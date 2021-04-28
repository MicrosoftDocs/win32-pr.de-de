---
description: 'UInt32Type Simple Type (Leistungsindikatoren): Definiert einen Ganzzahltyp ohne Vorzeichen.'
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Einfacher UInt32Type-Typ (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f8a4bbf00f569ba98dfc031f62717b1afc8734
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114578"
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

## <a name="remarks"></a>Bemerkungen

Sie können den Wert als 4-Byte-Ganzzahl oder Hexadezimalwert im Bereich von 0 bis 4.294.967.295 angeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



 

 




