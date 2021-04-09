---
title: UInt32Type simple-Typ (Windows-Ereignisprotokoll)
description: Definiert einen ganzzahligen Typ ohne Vorzeichen.
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- UInt32Type einfaches Ereignisprotokoll
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2a24326197c72b08032f5144fea1a69fbe68089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949828"
---
# <a name="uint32type-simple-type-windows-event-log"></a>UInt32Type simple-Typ (Windows-Ereignisprotokoll)

Definiert einen ganzzahligen Typ ohne Vorzeichen. Der Wert kann als 4-Byte-Ganzzahl oder Hexadezimalwert im Bereich zwischen 0 und 4.294.967.295 angegeben werden.

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





