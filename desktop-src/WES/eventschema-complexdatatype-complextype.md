---
title: Komplexer complexdatatype-Typ
description: Definiert eine-Struktur, die ein oder mehrere Datenelemente enthält.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- "\"Complexdatatype Complex Type Event Log\""
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 598f2cc02f1e3675ff0c8fd6eae7f9a5e02b9407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339356"
---
# <a name="complexdatatype-complex-type"></a>Komplexer complexdatatype-Typ

Definiert eine-Struktur, die ein oder mehrere Datenelemente enthält.

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



| Element                                                  | type                                                      | BESCHREIBUNG                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Daten**](eventschema-data-complexdatatype-element.md) | [**DataType**](eventschema-datafieldtype-complextype.md) | Die Liste der Datenelemente in der-Struktur. Die Liste der Elemente wird in derselben Reihenfolge wie in der Vorlage definiert.<br/> |



## <a name="attributes"></a>Attributes



| Name | type   | BESCHREIBUNG                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name | Zeichenfolge | Der Name der Struktur. Dies ist der Name, der angegeben wird, wenn Sie die Struktur in der Vorlage definiert haben (siehe den komplexen Typ " [**templateitemtype**](eventmanifestschema-templateitemtype-complextype.md) ").<br/> |



## <a name="remarks"></a>Bemerkungen

Die [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) -Funktion rendert den Inhalt einer Struktur als binäres Blob. die-Funktion stellt die einzelnen Datenelemente der-Struktur nicht dar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





