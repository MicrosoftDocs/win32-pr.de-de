---
title: Komplexer PatternMapValueType-Typ
description: Wird nicht verwendet. Definiert die regulären Ausdrücke, die verwendet werden, um eine übereinstimmende Zeichenfolge in der Meldungszeichenfolge zu suchen und zu ändern.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- Komplexer PatternMapValueType-Typ EventLog
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc36564aefd4d2f3d19f3b216d785faad888612621386037ae0e5539ce511169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136163"
---
# <a name="patternmapvaluetype-complex-type"></a>Komplexer PatternMapValueType-Typ

Wird nicht verwendet. Definiert die regulären Ausdrücke, die verwendet werden, um eine übereinstimmende Zeichenfolge in der Meldungszeichenfolge zu suchen und zu ändern.

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



| Name  | type   | Beschreibung                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| name  | Zeichenfolge | Der reguläre Ausdruck, der verwendet wird, um eine übereinstimmende Zeichenfolge in der Meldungszeichenfolge zu finden.<br/>                   |
| value | Zeichenfolge | Der reguläre Ausdruck, der verwendet wird, um die übereinstimmende Zeichenfolge zu ändern, die in der Meldungszeichenfolge gefunden wurde.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





