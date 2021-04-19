---
title: komplexer triggerstype-Typ
description: Definiert die Gruppe (triggergroup) für alle Triggerelemente.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- komplexer triggerstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344721"
---
# <a name="triggerstype-complex-type"></a>komplexer triggerstype-Typ

Definiert die Gruppe ([**triggergroup) für alle Triggerelemente**](taskschedulerschema-triggergroup-group.md). Die Gruppe [**triggergroup**](taskschedulerschema-triggergroup-group.md) enthält die Liste der Trigger, die in einer Aufgabe verwendet werden können.

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





