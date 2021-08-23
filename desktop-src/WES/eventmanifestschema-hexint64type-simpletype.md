---
title: Einfacher UInt64Type-Typ (EventManifest-Schema)
description: Definiert einen long-Typ ohne Vorzeichen.
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- UInt64Type simple type EventLog
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 088cdead48fb62adf816b6065e211afcc994ec618db8b7e9a0597e6f72c1780e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511340"
---
# <a name="uint64type-simple-type"></a>Einfacher UInt64Type-Typ

Definiert einen long-Typ ohne Vorzeichen. Der Wert kann als 8-Byte-Ganzzahl oder Hexadezimalwert im Bereich von 0 bis 18.446.744.073.709.551.615 angegeben werden.

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





