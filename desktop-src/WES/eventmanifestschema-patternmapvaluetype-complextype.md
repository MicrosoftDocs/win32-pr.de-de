---
title: Komplexer patternmapvaluetype-Typ
description: Nicht verwendet. Definiert die regulären Ausdrücke, mit denen eine übereinstimmende Zeichenfolge in der Meldungs Zeichenfolge gesucht und geändert wird.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- "\"Patternmapvaluetype\"-Ereignisprotokoll"
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739729"
---
# <a name="patternmapvaluetype-complex-type"></a>Komplexer patternmapvaluetype-Typ

Nicht verwendet. Definiert die regulären Ausdrücke, mit denen eine übereinstimmende Zeichenfolge in der Meldungs Zeichenfolge gesucht und geändert wird.

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributes



| Name  | type   | BESCHREIBUNG                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| name  | Zeichenfolge | Der reguläre Ausdruck, der zum Suchen einer übereinstimmenden Zeichenfolge in der Meldungs Zeichenfolge<br/>                   |
| value | Zeichenfolge | Der reguläre Ausdruck zum Ändern der übereinstimmenden Zeichenfolge, die in der Meldungs Zeichenfolge gefunden wurde.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





