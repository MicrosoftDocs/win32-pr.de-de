---
title: logontype simple-Typ
description: Definiert die möglichen Werte des logontype-Elements.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- logontype Simple Type Taskplaner
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58d8c859502e81b5c5101adac3c8c26539870dd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105213"
---
# <a name="logontype-simple-type"></a>logontype simple-Typ

Definiert die möglichen Werte des [**logontype**](taskschedulerschema-logontype-principaltype-element.md) -Elements.

``` syntax
<xs:simpleType name="logonType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="S4U"
         />
        <xs:enumeration
            value="Password"
         />
        <xs:enumeration
            value="InteractiveToken"
         />
        <xs:enumeration
            value="InteractiveTokenOrPassword"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Enumerationswerte

Der einfache **logontype** -Typ definiert die folgenden Werte.



| Wert                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S4U                        | Der Benutzer muss sich mithilfe eines Diensts für die Benutzeranmeldung (S4U) anmelden. Wenn eine S4U-Anmeldung verwendet wird, wird kein Kennwort vom System gespeichert, und es gibt keinen Zugriff auf das Netzwerk oder verschlüsselte Dateien.<br/>                                                                                                                                                          |
| Kennwort                   | Der Benutzer muss sich mit einem Kennwort anmelden.<br/>                                                                                                                                                                                                                                                                                                              |
| Interactivetoken           | Der Benutzer muss bereits angemeldet sein. Der Task wird nur in einer vorhandenen interaktiven Sitzung ausgeführt.<br/>                                                                                                                                                                                                                                                   |
| Interactiveper kenorpassword | Wird nicht mehr verwendet. aktuell identisch mit dem Kennwort.<br/> **Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista und Windows Server 2008:** Der Task wird in einer vorhandenen interaktiven Sitzung ausgeführt, oder der Benutzer muss sich mit einem Kennwort anmelden.<br/> <br/> |



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

 

 





