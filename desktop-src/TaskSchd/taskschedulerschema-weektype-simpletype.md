---
title: weekType Simple Type
description: Definiert die Werte, die im Week-Element verwendet werden können.
ms.assetid: 83a525ae-020b-4528-9e14-1e7d9df7b8c0
keywords:
- weekType simple type Taskplaner
topic_type:
- apiref
api_name:
- weekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 923d5a5d672407f9d15fed62bd554853f23ce5b31debd6a7c331e4b1217f15fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757933"
---
# <a name="weektype-simple-type"></a>weekType Simple Type

Definiert die Werte, die im [**Week-Element**](taskschedulerschema-week-weekstype-element.md) verwendet werden können.

``` syntax
<xs:simpleType name="weekType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-4]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der einfache **WeekType-Typ** ist eine **Zeichenfolge,** die durch das folgende Muster eingeschränkt ist:

-   `[1-4]|Last`

    Gibt die erste bis vierte Woche des Monats (1-4) oder immer die letzte Woche des Monats an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner schema simple types (Einfache Schematypen)](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





