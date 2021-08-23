---
title: Komplexer ComplexDataType-Typ
description: Definiert eine -Struktur, die ein oder mehrere Datenelemente enthält.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- Komplexer ComplexDataType-Typ EventLog
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f86b15defc32469dd1a4abd0f6366e1a93d4b83441b1e1518ff7ac999f30bd59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055808"
---
# <a name="complexdatatype-complex-type"></a>Komplexer ComplexDataType-Typ

Definiert eine -Struktur, die ein oder mehrere Datenelemente enthält.

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                  | Typ                                                      | Beschreibung                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Daten**](eventschema-data-complexdatatype-element.md) | [**Datatype**](eventschema-datafieldtype-complextype.md) | Die Liste der Datenelemente in der Struktur. Die Liste der Elemente hat die gleiche Reihenfolge wie in der Vorlage definiert.<br/> |



## <a name="attributes"></a>Attributes



| Name | Typ   | Beschreibung                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name | Zeichenfolge | Der Name der -Struktur. Dies ist der Name, der angegeben wird, wenn Sie die Struktur in der Vorlage definiert haben (siehe den komplexen [**TemplateItemType-Typ).**](eventmanifestschema-templateitemtype-complextype.md)<br/> |



## <a name="remarks"></a>Hinweise

Die [**EvtRender-Funktion**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) rendert den Inhalt einer -Struktur als binäres Blob. Die -Funktion rendert nicht die einzelnen Datenelemente der -Struktur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





