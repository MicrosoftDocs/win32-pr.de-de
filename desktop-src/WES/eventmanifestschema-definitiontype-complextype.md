---
title: Komplexer DefinitionType-Typ
description: Definiert eine Liste von Ereignissen, die von Ihrem Anbieter protokolliert werden können.
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- DefinitionType komplexer Typ (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82fbf7ec7db6f64f1bac9776376fa8fe89659d9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341002"
---
# <a name="definitiontype-complex-type"></a>Komplexer DefinitionType-Typ

Definiert eine Liste von Ereignissen, die von Ihrem Anbieter protokolliert werden können.

``` syntax
<xs:complexType name="DefinitionType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="event"
            type="EventDefinitionType"
         />
        <xs:element name="task"
            type="TaskEventDefinitionType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                           | type                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Veranstalter**](eventmanifestschema-event-definitiontype-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md)         | Definiert ein Ereignis, das von Ihrem Anbieter protokolliert werden kann.<br/>                                                                                                                                                                                                                                 |
| [**Task**](eventmanifestschema-task-definitiontype-element.md)   | [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) | Wird nicht unterstützt.<br/> **Windows Server 2008 und Windows Vista:** Definiert ein Aufgaben spezifisches Ereignis, das von Ihrem Anbieter protokolliert werden kann. (Beginnend mit dem Nachrichten Compiler, der mit der Windows 7-Version der Windows SDK ausgeliefert wird, werden aufgabenspezifische Ereignisse nicht mehr unterstützt.)<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





