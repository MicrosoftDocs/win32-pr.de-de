---
title: Komplexer eventdatatype-Typ
description: Definiert die Ereignisdaten Elemente und-Strukturen, die die Ereignisdaten enthalten.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- Ereignisprotokoll des komplexen eventdatatype-Typs
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a93695db477ebb0c7b5652419198f8f5c6370dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740376"
---
# <a name="eventdatatype-complex-type"></a>Komplexer eventdatatype-Typ

Definiert die Ereignisdaten Elemente und-Strukturen, die die Ereignisdaten enthalten.

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



| Element                                                              | type                                                               | BESCHREIBUNG                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Binary**](eventschema-binary-eventdatatype-element.md)           | hexBinary                                                          | Ein binäres Daten-BLOB für Ereignisse, die mithilfe der [Ereignisprotokollierung](/windows/desktop/EventLog/event-logging)geschrieben werden.<br/> |
| [**Complexdata**](eventschema-complexdata-eventdatatype-element.md) | [**Complexdatatype**](eventschema-complexdatatype-complextype.md) | Eine-Struktur, die in der Vorlage für das-Ereignis definiert ist.<br/>                                |
| [**Daten**](eventschema-data-eventdatatype-element.md)               | [**DataType**](eventschema-datafieldtype-complextype.md)          | Ein Datenelement der obersten Ebene, das in der Vorlage für das-Ereignis definiert ist.<br/>                      |



## <a name="attributes"></a>Attributes



| Name | type   | BESCHREIBUNG                                                       |
|------|--------|-------------------------------------------------------------------|
| Name | Zeichenfolge | Der Name der Vorlage, die die Datenelemente enthält.<br/> |



## <a name="remarks"></a>Bemerkungen

Die [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) -Funktion rendert Arrays und Strukturen als binäre Blob.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

