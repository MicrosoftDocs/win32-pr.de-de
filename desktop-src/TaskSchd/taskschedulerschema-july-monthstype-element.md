---
title: Juli-Element (monthstype)
description: Gibt an, dass der Task im Juli ausgeführt wird.
ms.assetid: 6fcb06f1-0806-469c-a283-ba8f2ba2c256
keywords:
- Juli-Element Taskplaner
topic_type:
- apiref
api_name:
- July
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6901ca83792ffd98269e26dc9cf24dd575025c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742904"
---
# <a name="july-monthstype-element"></a>Juli-Element (monthstype)

Gibt an, dass der Task im Juli ausgeführt wird.

``` syntax
<xs:element name="July">
    <xs:complexType />
</xs:element>
```

Das **Juli** -Element wird durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                          | Abgeleitet von                                                     | BESCHREIBUNG                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Monate (monthlydayosweekscheduletype)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthstype**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.<br/> |
| [**Monate (monthlyscheduletype)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthstype**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.<br/>             |



## <a name="examples"></a>Beispiele

Im folgenden XML-Code wird ein Monatskalender definiert, in dem die Aufgabe im Juli ausgeführt wird.


```XML
<Months>
    <July/>
</Months>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





