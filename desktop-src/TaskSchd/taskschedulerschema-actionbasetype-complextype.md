---
title: komplexer Typ von "aktionbasetype"
description: Definiert das ID-Attribut für alle Elemente dieses Typs.
ms.assetid: adc7117f-881f-4a32-8578-0530f2a0c179
keywords:
- komplexer Typ von "aktionbasetype" Taskplaner
topic_type:
- apiref
api_name:
- actionBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a8091456b2f09e6be5a332930d68960b2473acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105890"
---
# <a name="actionbasetype-complex-type"></a>komplexer Typ von "aktionbasetype"

Definiert das ID-Attribut für alle Elemente dieses Typs.

``` syntax
<xs:complexType name="actionBaseType"
    abstract="true"
>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a>Attributes



| Name | type | BESCHREIBUNG                                        |
|------|------|----------------------------------------------------|
| id   | id   | Die ID der Aktion, die von der Aufgabe ausgeführt wurde.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Komplexe Typen von Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





