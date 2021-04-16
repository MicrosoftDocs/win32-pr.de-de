---
title: Dateityp "dayof monthtype"
description: Definiert die möglichen Werte zum Angeben eines Monats Tags.
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- der Typ "dayof monthtype" ist Taskplaner
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a8428688ff429809c7509bae42adb156efe00ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517504"
---
# <a name="dayofmonthtype-simple-type"></a>Dateityp "dayof monthtype"

Definiert die möglichen Werte zum Angeben eines Monats Tags.

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

Der einfache Typ " **dayosmonthtype** " ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    Gibt den 1. bis zum 31. Tag des Monats oder immer den letzten Tag des Monats an.

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

 

 





