---
title: triggersType Complex Type
description: Definiert die Gruppe (triggerGroup) für alle Triggerelemente.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- triggersType complex type Taskplaner
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c2bd6fa4011841958ad08239640024f9878528aecb1307487c3354ac74e31db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610537"
---
# <a name="triggerstype-complex-type"></a>triggersType Complex Type

Definiert die Gruppe ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) für alle Triggerelemente. Die [**triggerGroup-Gruppe**](taskschedulerschema-triggergroup-group.md) enthält die Liste der Trigger, die in einer Aufgabe verwendet werden können.

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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





