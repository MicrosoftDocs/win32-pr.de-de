---
title: einfacher runleveltype-Typ
description: Definiert die möglichen Werte für das Runlevel-Element (principaltype).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- einfacher runleveltype-Typ Taskplaner
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d037dceeb3e6e4957cc96a17a2ac511a03a94b94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342863"
---
# <a name="runleveltype-simple-type"></a>einfacher runleveltype-Typ

Definiert die möglichen Werte für das [**Runlevel-Element (principaltype)**](taskschedulerschema-runlevel-principaltype-element.md) .

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Enumerationswerte

Der einfache **runleveltype** -Typ definiert die folgenden Werte.



| Wert            | BESCHREIBUNG                                               |
|------------------|-----------------------------------------------------------|
| Leastprivilege   | Tasks werden mit den geringsten Berechtigungen (LUA) ausgeführt.<br/> |
| HighestAvailable | Tasks werden mit den höchsten Berechtigungen ausgeführt.<br/>     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





