---
title: Komplexer DebugDataType-Typ
description: Definiert die Daten, die für Windows WPP-Ereignisse (Software Trace Preprocessor) protokolliert werden können.
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- Komplexer DebugDataType-Typ EventLog
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38d5ec0297fce91b28592dfb9a894a62d3558f516a01ff18c942d37cc9c93f2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124230"
---
# <a name="debugdatatype-complex-type"></a>Komplexer DebugDataType-Typ

Definiert die Daten, die für Windows WPP-Ereignisse (Software Trace Preprocessor) protokolliert werden können.

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



| Element                                                                    | type        | Beschreibung                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [**Komponente**](eventschema-component-debugdatatype-element.md)           | Zeichenfolge      | Der Name der Komponente, die die Ablaufverfolgungsmeldung protokolliert hat.<br/>                                                |
| [**FileLine**](eventschema-fileline-debugdatatype-element.md)             | Zeichenfolge      | Der Name der Quelldatei und die Zeile in der Quelldatei, die die Ablaufverfolgungsmeldung protokolliert hat.<br/>          |
| [**FlagsName**](eventschema-flagname-debugdatatype-element.md)            | Zeichenfolge      | Der Flagwert, der an den Anbieter übergeben wurde, als er aktiviert wurde.<br/>                                              |
| [**Function**](eventschema-function-debugdatatype-element.md)             | unsignedInt | Der Name der Funktion, die die Ablaufverfolgungsmeldung protokolliert hat.<br/>                                                 |
| [**LevelName**](eventschema-levelname-debugdatatype-element.md)           | Zeichenfolge      | Der Ebenenwert, der an den Anbieter übergeben wird, als er aktiviert wurde.<br/>                                             |
| [**`Message`**](eventschema-message-debugdatatype-element.md)               | Zeichenfolge      | Die Meldungszeichenfolge. Der XML-Code enthält dieses Element, wenn das WPP-Ereignis das Feld FormattedString angegeben hat.<br/> |
| [**Sequencenumber**](eventschema-sequencenumber-debugdatatype-element.md) | unsignedInt | Die lokale oder globale Sequenznummer der Ablaufverfolgungsmeldung.<br/>                                               |
| [**Unterkomponente**](eventschema-subcomponent-debugdatatype-element.md)     | Zeichenfolge      | Der Name der Unterkomponente, die die Ablaufverfolgungsmeldung protokolliert hat.<br/>                                             |



## <a name="remarks"></a>Hinweise

Die Elemente sind nur enthalten, wenn der Anbieter die Umgebungsvariable %TRACE FORMAT PREFIX% so festgelegt \_ \_ hat, dass sie eingeschlossen werden. Weitere Informationen zu diesen Elementen finden Sie unter Präfix für Ablaufverfolgungsmeldungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





