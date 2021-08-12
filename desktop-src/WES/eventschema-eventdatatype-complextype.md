---
title: Komplexer EventDataType-Typ
description: Definiert die Ereignisdatenelemente und -strukturen, die die Ereignisdaten enthalten.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- 'EventDataType: komplexer EventLog-Typ'
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 424f7f5f6472859a06605467c427fc7b9f210a960f0920fb8593778bd757fc06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589023"
---
# <a name="eventdatatype-complex-type"></a>Komplexer EventDataType-Typ

Definiert die Ereignisdatenelemente und -strukturen, die die Ereignisdaten enthalten.

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                              | Typ                                                               | BESCHREIBUNG                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Binäre**](eventschema-binary-eventdatatype-element.md)           | hexBinary                                                          | Ein binäres Datenblob für Ereignisse, die mithilfe der [Ereignisprotokollierung geschrieben werden.](/windows/desktop/EventLog/event-logging)<br/> |
| [**ComplexData**](eventschema-complexdata-eventdatatype-element.md) | [**ComplexDataType**](eventschema-complexdatatype-complextype.md) | Eine -Struktur, die in der Vorlage für das Ereignis definiert ist.<br/>                                |
| [**Daten**](eventschema-data-eventdatatype-element.md)               | [**Datatype**](eventschema-datafieldtype-complextype.md)          | Ein Datenelement der obersten Ebene, das in der Vorlage für das Ereignis definiert ist.<br/>                      |



## <a name="attributes"></a>Attributes



| Name | Typ   | BESCHREIBUNG                                                       |
|------|--------|-------------------------------------------------------------------|
| Name | Zeichenfolge | Der Name der Vorlage, die die Datenelemente enthält.<br/> |



## <a name="remarks"></a>Bemerkungen

Die [**EvtRender-Funktion**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) rendert Arrays und Strukturen als binäre Blobs.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

