---
title: Komplexer Typ valuemaptype
description: Definiert eine Liste von Name-Wert-Zuordnungen zwischen ganzzahligen Werten und Zeichen folgen Werten.
ms.assetid: 754578bf-d3c6-4467-af39-af56d5a11dce
keywords:
- "\"Valuemaptype Complex Type Event Log\""
topic_type:
- apiref
api_name:
- ValueMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28fde51466ba506802c8dbc5379f1628fd943fa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739713"
---
# <a name="valuemaptype-complex-type"></a>Komplexer Typ valuemaptype

Definiert eine Liste von Name-Wert-Zuordnungen zwischen ganzzahligen Werten und Zeichen folgen Werten.

``` syntax
<xs:complexType name="ValueMapType">
    <xs:sequence>
        <xs:element name="map"
            type="ValueMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                     | type                                                                           | BESCHREIBUNG                                                                 |
|-------------------------------------------------------------|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**bilden**](eventmanifestschema-map-valuemaptype-element.md) | [**Valuemapvaluetype**](eventmanifestschema-valuemapvaluetype-complextype.md) | Definiert die Zuordnung zwischen einem ganzzahligen Wert und einem Zeichen folgen Wert.<br/> |



## <a name="attributes"></a>Attributes



| Name   | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | Zeichenfolge                                                            | Der Name der Wertzuordnung. Verwenden Sie den Namen in einem Datenelement, um auf die Zuordnungen zu verweisen.<br/>                                                                                                                                                                                                                     |
| Symbol | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf die Zuordnungen in der Anwendung zu verweisen. Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die Zuordnung in der vom Compiler generierten Header Datei zu erstellen. Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





