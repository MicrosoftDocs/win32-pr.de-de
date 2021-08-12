---
title: Komplexer DefinitionType-Typ
description: Definiert eine Liste von Ereignissen, die Ihr Anbieter protokollieren kann.
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- Komplexer DefinitionType-Typ EventLog
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f62ab040f57fdeb4e4208554c642e9b0bc2fb1135512d1c512f0b0ef90b69e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589635"
---
# <a name="definitiontype-complex-type"></a>Komplexer DefinitionType-Typ

Definiert eine Liste von Ereignissen, die Ihr Anbieter protokollieren kann.

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



| Element                                                           | Typ                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ereignis**](eventmanifestschema-event-definitiontype-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md)         | Definiert ein Ereignis, das ihr Anbieter protokollieren kann.<br/>                                                                                                                                                                                                                                 |
| [**Aufgabe**](eventmanifestschema-task-definitiontype-element.md)   | [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) | Wird nicht unterstützt.<br/> **Windows Server 2008 und Windows Vista:** Definiert ein aufgabenspezifisches Ereignis, das ihr Anbieter protokollieren kann. (Ab dem Nachrichtencompiler, der mit der Windows 7-Version des Windows SDK ausgeliefert wird, werden taskspezifische Ereignisse nicht mehr unterstützt.)<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





