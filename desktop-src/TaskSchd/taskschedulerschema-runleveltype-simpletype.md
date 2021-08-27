---
title: runLevelType Simple Type
description: Definiert die möglichen Werte für das RunLevel -Element (principalType).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- runLevelType simple type Taskplaner
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ce534008ce0138293a773e4f5fa4a5270a2d4b27aad54dd062eafe286ab8ba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991070"
---
# <a name="runleveltype-simple-type"></a>runLevelType Simple Type

Definiert die möglichen Werte für das [**RunLevel -Element (principalType).**](taskschedulerschema-runlevel-principaltype-element.md)

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

Der einfache **runLevelType-Typ** definiert die folgenden Werte.



| Wert            | Beschreibung                                               |
|------------------|-----------------------------------------------------------|
| LeastPrivilege   | Aufgaben werden mit den geringsten Berechtigungen (LUA) ausgeführt.<br/> |
| HighestAvailable | Aufgaben werden mit den höchsten Berechtigungen ausgeführt.<br/>     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





