---
title: Opcode (TaskEventDefinitionType)-Element
description: Enthält einen aufgabenspezifischen Opcode für ein Ereignis. Für den Task, der die Ereignis Definitionen enthält, wird davon ausgegangen, dass alle Opcode-Definitionen aufgabenspezifisch sind.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- Opcode-Element EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9f3b58353163e1ee5b9abeb04007a4a9d449e5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341031"
---
# <a name="opcode-taskeventdefinitiontype-element"></a>Opcode (TaskEventDefinitionType)-Element

\[Beginnend mit dem Nachrichten Compiler, der mit der Windows 7-Version des Windows SDK ausgeliefert wird, ist dieses Element nicht mehr verfügbar.\]

Enthält einen aufgabenspezifischen Opcode für ein Ereignis. Für den Task, der die Ereignis Definitionen enthält, wird davon ausgegangen, dass alle Opcode-Definitionen aufgabenspezifisch sind.

``` syntax
<xs:element name="opcode">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="event"
                type="EventDefinitionType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
        <xs:attribute name="name"
            type="QName"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

Das **Opcode** -Element wird durch den komplexen [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) -Typ definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                   | type                                                                               | BESCHREIBUNG                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Veranstalter**](eventmanifestschema-event-opcode-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Ein Ereignis, das mit einer Aufgabe veröffentlicht wird.<br/> |



## <a name="attributes"></a>Attributes



| Name | type      | BESCHREIBUNG                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Der Name des aufgabenspezifischen OpCodes.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**Aufgabe (DefinitionType)**](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





