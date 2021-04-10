---
title: Komplexer debugdatatype-Typ
description: Definiert die Daten, die für Windows-Software-Ablaufverfolgungs-präprozessorereignisse (WPP) protokolliert werden können.
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- Ereignisprotokoll des komplexen debugdatatype-Typs
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c190d3b2b0e870ac249fed03485828685d5dc770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040033"
---
# <a name="debugdatatype-complex-type"></a>Komplexer debugdatatype-Typ

Definiert die Daten, die für Windows-Software-Ablaufverfolgungs-präprozessorereignisse (WPP) protokolliert werden können.

``` syntax
<xs:complexType name="DebugDataType">
    <xs:sequence>
        <xs:element name="SequenceNumber"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="FlagsName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="LevelName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Component"
            type="string"
         />
        <xs:element name="SubComponent"
            type="string"
            minOccurs="0"
         />
        <xs:element name="FileLine"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Function"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="Message"
            type="string"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                    | type        | BESCHREIBUNG                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [**Komponente**](eventschema-component-debugdatatype-element.md)           | Zeichenfolge      | Der Name der Komponente, die die Ablauf Verfolgungs Meldung protokolliert hat.<br/>                                                |
| [**FileLine**](eventschema-fileline-debugdatatype-element.md)             | Zeichenfolge      | Der Name der Quelldatei und die Zeile in der Quelldatei, die die Ablauf Verfolgungs Meldung protokolliert hat.<br/>          |
| [**Flagsname**](eventschema-flagname-debugdatatype-element.md)            | Zeichenfolge      | Der Flagwert, der beim Aktivieren an den Anbieter übermittelt wurde.<br/>                                              |
| [**Function**](eventschema-function-debugdatatype-element.md)             | unsignedInt | Der Name der Funktion, die die Ablauf Verfolgungs Meldung protokolliert hat.<br/>                                                 |
| [**LevelName**](eventschema-levelname-debugdatatype-element.md)           | Zeichenfolge      | Der bei der Aktivierung an den Anbieter über gegebene levelwert.<br/>                                             |
| [**`Message`**](eventschema-message-debugdatatype-element.md)               | Zeichenfolge      | Die Meldungszeichenfolge. Der XML-Code enthält dieses Element, wenn das Feld "formattedstring" vom WPP-Ereignis angegeben wurde.<br/> |
| [**SequenceNumber**](eventschema-sequencenumber-debugdatatype-element.md) | unsignedInt | Die lokale oder globale Sequenznummer der Ablauf Verfolgungs Meldung.<br/>                                               |
| [**Unterkomponente**](eventschema-subcomponent-debugdatatype-element.md)     | Zeichenfolge      | Der Name der Unterkomponente, die die Ablauf Verfolgungs Meldung protokolliert hat.<br/>                                             |



## <a name="remarks"></a>Bemerkungen

Die Elemente sind nur enthalten, wenn der Anbieter die \_ Umgebungsvariable% Trace Format Prefix% festgelegt hat \_ , um Sie einzubeziehen. Ausführliche Informationen zu diesen Elementen finden Sie unter Präfix der Ablauf Verfolgungs Meldung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





