---
title: Komplexer TaskEventDefinitionType-Typ
description: Definiert ein aufgabenspezifisches Ereignis, das Ihr Anbieter protokollieren kann. | Komplexer TaskEventDefinitionType-Typ
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- Komplexer TaskEventDefinitionType-Typ EventLog
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44a4fc7ca8784b3472fea3b0d4f4e657ce615fae05a8cc7372aa3cca0fedb431
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055838"
---
# <a name="taskeventdefinitiontype-complex-type"></a>Komplexer TaskEventDefinitionType-Typ

\[Ab dem Nachrichtencompiler, der mit der Windows 7-Version des Windows SDK ausgeliefert wird, ist der komplexe TaskEventDefinitionType-Typ nicht mehr verfügbar. Verwenden Sie stattdessen aufgabenspezifische Opcodes, um die gleiche Funktionalität bereitzustellen.\]

Definiert ein aufgabenspezifisches Ereignis, das Ihr Anbieter protokollieren kann.

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                      | Typ                                                                               | Beschreibung                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| **event**                                                                    | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Ein aufgabenspezifisches Ereignis, das mit einer Aufgabe veröffentlicht wurde.<br/> |
| [**Opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | Ein aufgabenspezifischer Opcode, der für ein Ereignis gilt. <br/>   |



## <a name="attributes"></a>Attributes



| Name | Typ      | Beschreibung                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Der Name des aufgabenspezifischen Opcodes.<br/> |
| name | anyURI    | Der Name der Aufgabe.<br/>                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





