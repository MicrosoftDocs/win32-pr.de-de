---
title: Komplexer renderinginfotype-Typ
description: Definiert die gerenderten Nachrichten für das Ereignis.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- Renderinginfotype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d0e4224ec9b90e84cbacbf5ede852763edd8e4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478792"
---
# <a name="renderinginfotype-complex-type"></a>Komplexer renderinginfotype-Typ

Definiert die gerenderten Nachrichten für das Ereignis.

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                             | type   | BESCHREIBUNG                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [**Channel**](eventschema-task-renderingtype-element.md)           | Zeichenfolge | Die gerenderte Meldungs Zeichenfolge des Kanals, der im Ereignis angegeben ist.<br/> |
| [**Schlüsselwort**](eventschema-keyword-keywords-element.md)             | Zeichenfolge | Die gerenderte Meldungs Zeichenfolge eines im Ereignis angegebenen Schlüssel Worts.<br/>   |
| [**Keywords**](eventschema-keywords-renderingtype-element.md)      |        | Eine Liste von gerenderten Schlüsselwörtern.<br/>                                       |
| [**Geringen**](eventschema-level-renderingtype-element.md)            | Zeichenfolge | Die gerenderte Meldungs Zeichenfolge der im Ereignis angegebenen Ebene.<br/>   |
| [**`Message`**](eventschema-message-renderingtype-element.md)        | Zeichenfolge | Die gerenderte Meldungs Zeichenfolge des Ereignisses.<br/>                          |
| [**Opcode**](eventschema-opcode-renderingtype-element.md)          | Zeichenfolge | Die gerenderte Meldungs Zeichenfolge des im Ereignis angegebenen OpCodes.<br/>  |
| [**Anbieter**](eventschema-publisher-renderinginfotype-element.md) | Zeichenfolge | Die gerenderte Nachrichten Zeichenfolge für den Anbieter.<br/>                      |
| [**Aufgabe**](eventschema-task-renderingtype-element.md)              | Zeichenfolge | Die gerenderte Meldungs Zeichenfolge der im Ereignis angegebenen Aufgabe.<br/>    |



## <a name="attributes"></a>Attributes



| Name    | type     | BESCHREIBUNG                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| Kultur | language | Der Sprachen Name (z. b. en-US), der das Gebiets Schema identifiziert, das zum Rendering der Nachrichten Zeichenfolgen verwendet wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Dieser Abschnitt enthält nur Ereignisse, die mit dem [Windows-Ereignis](/windows/desktop/WEC/windows-event-collector) Sammlungs Dienst erfasst wurden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

