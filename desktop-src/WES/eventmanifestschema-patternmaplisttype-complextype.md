---
title: Komplexer Typ von patternmaplisttype
description: Nicht verwendet. Definiert eine Liste von Paaren für reguläre Ausdrücke, die zum Ändern der Meldungs Zeichenfolge verwendet werden.
ms.assetid: f7b92821-a959-4b91-9e7e-47d0136ee61f
keywords:
- Datentyp "patternmaplisttype", Ereignisprotokoll
topic_type:
- apiref
api_name:
- PatternMapListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d1bb655dcf13c70fb989756cb9f5716301934c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340307"
---
# <a name="patternmaplisttype-complex-type"></a>Komplexer Typ von patternmaplisttype

Nicht verwendet. Definiert eine Liste von Paaren für reguläre Ausdrücke, die zum Ändern der Meldungs Zeichenfolge verwendet werden.

``` syntax
<xs:complexType name="PatternMapListType">
    <xs:sequence>
        <xs:element name="patternMap"
            type="PatternMapType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                         | type                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**patternmap**](eventmanifestschema-patternmap-patternmaplisttype-element.md) | [**Patternmaptype**](eventmanifestschema-patternmaptype-complextype.md) | Definiert eine Zuordnung zwischen zwei regulären Ausdrücken. Ein Ausdruck wird verwendet, um nach einer übereinstimmenden Zeichenfolge in der Meldungs Zeichenfolge zu suchen, und die andere wird verwendet, um die Zeichenfolge zu ändern Die erste übereinstimmende Musterzuordnung wird verwendet, und andere Muster werden nicht ausprobiert.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





