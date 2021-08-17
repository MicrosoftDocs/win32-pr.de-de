---
title: priorityType Simple Type
description: Definiert die Minimal- und Höchstwerte für das Priority (settingsType)-Element.
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- priorityType simple type Taskplaner
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 71bdf8b87a641247ce2064ccf44ee861d79aab0593229e4cd7b38035c5c7c124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424430"
---
# <a name="prioritytype-simple-type"></a>priorityType Simple Type

Definiert die Minimal- und Höchstwerte für das [**Priority (settingsType)-Element.**](taskschedulerschema-priority-settingstype-element.md)

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

Der einfache **PriorityType-Typ** definiert die folgenden Werte.



| Wert | Beschreibung                         |
|-------|-------------------------------------|
| 0     | Mindestens zulässige ganze Zahl.<br/> |
| 10    | Maximal zulässige ganze Zahl.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Taskplaner schema simple types (Einfache Schematypen)](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





