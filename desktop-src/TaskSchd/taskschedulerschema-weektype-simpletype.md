---
title: weektype simple-Typ
description: Definiert die Werte, die im Week-Element verwendet werden können.
ms.assetid: 83a525ae-020b-4528-9e14-1e7d9df7b8c0
keywords:
- weektype-Typ "Simple" Taskplaner
topic_type:
- apiref
api_name:
- weekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6513efe0fe0ef4fcbf6b849627d09ec9da6feb82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103278"
---
# <a name="weektype-simple-type"></a>weektype simple-Typ

Definiert die Werte, die im [**Week**](taskschedulerschema-week-weekstype-element.md) -Element verwendet werden können.

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

Der einfache **weektype** -Typ ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:

-   `[1-4]|Last`

    Gibt den ersten bis zur vierten Woche des Monats (1-4) oder immer die letzte Woche des Monats an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Einfache Typen von Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





