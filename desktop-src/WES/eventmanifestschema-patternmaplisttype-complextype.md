---
title: Komplexer PatternMapListType-Typ
description: Wird nicht verwendet. Definiert eine Liste regulärer Ausdruckspaare, die zum Ändern der Meldungszeichenfolge verwendet werden.
ms.assetid: f7b92821-a959-4b91-9e7e-47d0136ee61f
keywords:
- Komplexer PatternMapListType-Typ EventLog
topic_type:
- apiref
api_name:
- PatternMapListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbf96f7033f353662578e477fb8e35e0bfcda6db390f6492e29840e5e1faa5cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136203"
---
# <a name="patternmaplisttype-complex-type"></a>Komplexer PatternMapListType-Typ

Wird nicht verwendet. Definiert eine Liste regulärer Ausdruckspaare, die zum Ändern der Meldungszeichenfolge verwendet werden.

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



| Element                                                                         | type                                                                     | Beschreibung                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**patternMap**](eventmanifestschema-patternmap-patternmaplisttype-element.md) | [**PatternMapType**](eventmanifestschema-patternmaptype-complextype.md) | Definiert eine Zuordnung zwischen zwei regulären Ausdrücken. Ein Ausdruck wird verwendet, um eine übereinstimmende Zeichenfolge in der Meldungszeichenfolge zu finden, und der andere wird verwendet, um die Zeichenfolge zu ändern, bevor der Dienst sie wieder in die Meldungszeichenfolge eingibt. Die erste Musterzuordnung, die entspricht, wird verwendet, und andere Muster werden nicht versucht.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





