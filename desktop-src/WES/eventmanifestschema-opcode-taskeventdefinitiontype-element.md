---
title: opcode (TaskEventDefinitionType) -Element
description: Enthält einen aufgabenspezifischen Opcode für ein Ereignis. Es wird davon ausgegangen, dass alle Opcodedefinitionen aufgabenspezifisch für den Task sind, der die Ereignisdefinitionen enthält.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- opcode-Element EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f3923e0a42375ac7d926d418943af81cc0264e111e6bdc4be56919780dfacf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652150"
---
# <a name="opcode-taskeventdefinitiontype-element"></a>opcode (TaskEventDefinitionType) -Element

\[Ab dem Nachrichtencompiler, der im Windows 7-Version des Windows SDK enthalten ist, ist dieses Element nicht mehr verfügbar.\]

Enthält einen aufgabenspezifischen Opcode für ein Ereignis. Es wird davon ausgegangen, dass alle Opcodedefinitionen aufgabenspezifisch für den Task sind, der die Ereignisdefinitionen enthält.

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

Das **opcode-Element** wird durch den komplexen [**TaskEventDefinitionType-Typ**](eventmanifestschema-taskeventdefinitiontype-complextype.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                   | Typ                                                                               | Beschreibung                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Ereignis**](eventmanifestschema-event-opcode-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Ein Ereignis, das mit einer Aufgabe veröffentlicht wird.<br/> |



## <a name="attributes"></a>Attributes



| Name | Typ      | Beschreibung                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Der Name des aufgabenspezifischen Opcodes.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**task (DefinitionType)**](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





