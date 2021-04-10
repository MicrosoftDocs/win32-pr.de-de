---
title: einfacher prioritytype-Typ
description: Definiert die minimalen und maximalen Werte für das Priority-Element (settingstype).
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- einfacher prioritytype-Typ Taskplaner
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05b3c6d04adf557242438c813dab4f10d48cdb9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040851"
---
# <a name="prioritytype-simple-type"></a>einfacher prioritytype-Typ

Definiert die minimalen und maximalen Werte für das [**Priority-Element (settingstype)**](taskschedulerschema-priority-settingstype-element.md) .

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Enumerationswerte

Der einfache **prioritytype** -Typ definiert die folgenden Werte.



| Wert | BESCHREIBUNG                         |
|-------|-------------------------------------|
| 0     | Minimale Ganzzahl zulässig.<br/> |
| 10    | Maximale Ganzzahl zulässig.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Einfache Typen von Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





