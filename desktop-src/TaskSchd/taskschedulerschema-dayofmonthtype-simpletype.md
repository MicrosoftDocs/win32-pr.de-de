---
title: dayOfMonthType Simple Type
description: Definiert die möglichen Werte zum Angeben eines Tages des Monats.
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- dayOfMonthType simple type Taskplaner
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c3d3d549f2d84c292ad1dbdf3c03965bd6e4265559b57c41016811834167a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309353"
---
# <a name="dayofmonthtype-simple-type"></a>dayOfMonthType Simple Type

Definiert die möglichen Werte zum Angeben eines Tages des Monats.

``` syntax
<xs:simpleType name="dayOfMonthType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-9]|[1-2][0-9]|3[0-1]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der **einfache dayOfMonthType-Typ** ist eine **Zeichenfolge,** die durch das folgende Muster eingeschränkt ist:

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    Gibt den 1. bis 31. Tag des Monats oder immer den letzten Tag des Monats an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner schema simple types (Einfache Schematypen)](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





