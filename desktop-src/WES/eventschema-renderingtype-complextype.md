---
title: Komplexer RenderingInfoType-Typ
description: Definiert die gerenderten Nachrichten für das Ereignis.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- Komplexer RenderingInfoType-Typ EventLog
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d4a70c8bc97abc3dea7cd04e9ce491b64cb62dcc892fcde318d69dcdc996e2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588463"
---
# <a name="renderinginfotype-complex-type"></a>Komplexer RenderingInfoType-Typ

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



| Element                                                             | Typ   | BESCHREIBUNG                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [**Channel**](eventschema-task-renderingtype-element.md)           | Zeichenfolge | Die gerenderte Meldungszeichenfolge des im -Ereignis angegebenen Kanals.<br/> |
| [**Stichwort**](eventschema-keyword-keywords-element.md)             | Zeichenfolge | Die gerenderte Meldungszeichenfolge eines im -Ereignis angegebenen Schlüsselworts.<br/>   |
| [**Schlüsselwörter**](eventschema-keywords-renderingtype-element.md)      |        | Eine Liste der gerenderten Schlüsselwörter.<br/>                                       |
| [**Ebene**](eventschema-level-renderingtype-element.md)            | Zeichenfolge | Die gerenderte Meldungszeichenfolge der im -Ereignis angegebenen Ebene.<br/>   |
| [**Nachricht**](eventschema-message-renderingtype-element.md)        | Zeichenfolge | Die gerenderte Meldungszeichenfolge des Ereignisses.<br/>                          |
| [**Opcode**](eventschema-opcode-renderingtype-element.md)          | Zeichenfolge | Die gerenderte Meldungszeichenfolge des im -Ereignis angegebenen Opcodes.<br/>  |
| [**Anbieter**](eventschema-publisher-renderinginfotype-element.md) | Zeichenfolge | Die gerenderte Meldungszeichenfolge für den Anbieter.<br/>                      |
| [**Aufgabe**](eventschema-task-renderingtype-element.md)              | Zeichenfolge | Die gerenderte Meldungszeichenfolge der im -Ereignis angegebenen Aufgabe.<br/>    |



## <a name="attributes"></a>Attributes



| Name    | Typ     | BESCHREIBUNG                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| culture | language | Der Sprachname (z.B. en-US), der das Gebietsschema identifiziert, das zum Rendern der Meldungszeichenfolgen verwendet wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Nur Ereignisse, die mithilfe des [Windows Event Collector-Diensts](/windows/desktop/WEC/windows-event-collector) gesammelt wurden, enthalten diesen Abschnitt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

