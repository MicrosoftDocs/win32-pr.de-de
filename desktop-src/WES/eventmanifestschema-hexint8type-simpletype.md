---
title: Einfacher UInt8Type-Typ
description: Definiert einen Bytetyp ohne Vorzeichen.
ms.assetid: bda12d06-683f-4183-a84b-2bc3159c4eff
keywords:
- Einfacher UInt8Type-Typ EventLog
topic_type:
- apiref
api_name:
- UInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a48c21e34edecbf4dfb4f9c2e87c85a77e3f500ec42b8607f1de004e7679ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511310"
---
# <a name="uint8type-simple-type"></a>Einfacher UInt8Type-Typ

Definiert einen Bytetyp ohne Vorzeichen. Der Wert kann als 1-Byte-Ganzzahl oder Hexadezimalwert im Bereich von 0 bis 255 angegeben werden.

``` syntax
<xs:simpleType name="UInt8Type">
    <xs:union
        memberValues="unsignedByte HexInt8Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





