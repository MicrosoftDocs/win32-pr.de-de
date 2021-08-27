---
title: IdleTriggerType Complex Type
description: Definiert den Basistyp für das IdleTrigger-Element.
ms.assetid: 05beabb7-2e6f-4df1-809a-9f64a578d80a
keywords:
- komplexer IdleTriggerType-Taskplaner
topic_type:
- apiref
api_name:
- idleTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5c1ae0c6a88576eb7996a8151e96bb92c4a47c0d732a3558deede3b835356f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100020"
---
# <a name="idletriggertype-complex-type"></a>IdleTriggerType Complex Type

Definiert den Basistyp für das [**IdleTrigger-Element.**](taskschedulerschema-idletrigger-triggergroup-element.md)

``` syntax
<xs:complexType name="idleTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
         />
    </xs:complexContent>
</xs:complexType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Komplexe Schematypen](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





