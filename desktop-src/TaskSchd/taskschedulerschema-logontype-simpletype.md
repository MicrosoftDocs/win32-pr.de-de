---
title: logonType Simple Type
description: Definiert die möglichen Werte des LogonType-Elements.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- LogonType simple type Taskplaner
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f40301957ec323b8abf7c09829bf3b551e2e1665a811409622d342784d86e54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758892"
---
# <a name="logontype-simple-type"></a>logonType Simple Type

Definiert die möglichen Werte des [**LogonType-Elements.**](taskschedulerschema-logontype-principaltype-element.md)

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

Der **einfache LogonType-Typ** definiert die folgenden Werte.



| Wert                      | Beschreibung                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S4u                        | Der Benutzer muss sich mit einem Dienst für die Benutzeranmeldung (S4U) anmelden. Wenn eine S4U-Anmeldung verwendet wird, wird kein Kennwort vom System gespeichert, und es besteht kein Zugriff auf das Netzwerk oder auf verschlüsselte Dateien.<br/>                                                                                                                                                          |
| Kennwort                   | Der Benutzer muss sich mit einem Kennwort anmelden.<br/>                                                                                                                                                                                                                                                                                                              |
| InteractiveToken           | Der Benutzer muss bereits angemeldet sein. Die Aufgabe wird nur in einer vorhandenen interaktiven Sitzung ausgeführt.<br/>                                                                                                                                                                                                                                                   |
| InteractiveTokenOrPassword | Wird nicht mehr verwendet. derzeit identisch mit Kennwort.<br/> **Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista und Windows Server 2008:** Die Aufgabe wird in einer vorhandenen interaktiven Sitzung ausgeführt, oder der Benutzer muss sich mit einem Kennwort anmelden.<br/> <br/> |



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

 

 





