---
title: einfacher sessionstatechangetype-Typ
description: Definiert Werte für die Art der Sitzungs Zustandsänderung des Terminal Servers, die Sie verwenden können, um einen Task zu starten.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- sessionstatechangetype-Typ "Simple" Taskplaner
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a77fb563b59ccd8d63d38c6c85f16ff74ac404b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478378"
---
# <a name="sessionstatechangetype-simple-type"></a>einfacher sessionstatechangetype-Typ

Definiert Werte für die Art der Sitzungs Zustandsänderung des Terminal Servers, die Sie verwenden können, um einen Task zu starten.

``` syntax
<xs:simpleType name="sessionStateChangeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="ConsoleConnect"
         />
        <xs:enumeration
            value="ConsoleDisconnect"
         />
        <xs:enumeration
            value="RemoteConnect"
         />
        <xs:enumeration
            value="RemoteDisconnect"
         />
        <xs:enumeration
            value="SessionLock"
         />
        <xs:enumeration
            value="SessionUnlock"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Enumerationswerte

Der einfache Typ **sessionstatechangetype** definiert die folgenden Werte:



| Wert             | BESCHREIBUNG                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Consoleconnetct    | Statusänderung der Terminal Server-Konsolen Verbindung. Wenn Sie z. b. eine Verbindung mit einer Benutzersitzung auf dem lokalen Computer herstellen, indem Sie die Benutzer auf dem Computer wechseln. <br/>                            |
| Consoledisconnect | Statusänderung der Terminal Server Konsole wird getrennt. Wenn Sie z. b. eine Verbindung mit einer Benutzersitzung auf dem lokalen Computer trennen, indem Sie die Benutzer auf dem Computer wechseln. <br/>                      |
| Verbindung "     | Statusänderung für Terminal Server-Remote Verbindung. Dies ist beispielsweise der Fall, wenn ein Benutzer mithilfe des Remotedesktopverbindung Programms von einem Remote Computer aus eine Verbindung mit einer Benutzersitzung herstellt. <br/>            |
| Remotedisconnect  | Statusänderung des Terminal Server-Remote Verbindungs Wechsels. Dies ist beispielsweise der Fall, wenn ein Benutzer die Verbindung mit einer Benutzersitzung trennt, während das Remotedesktopverbindung Programm von einem Remote Computer aus verwendet wird. <br/> |
| Sessionlock       | Statusänderung für Terminal Server Sitzung gesperrt. Diese Statusänderung bewirkt beispielsweise, dass die Aufgabe ausgeführt wird, wenn der Computer gesperrt wird. <br/>                                                       |
| Sessionunlock     | Die Statusänderung der Terminal Server Sitzung wurde aufgehoben. Diese Statusänderung bewirkt beispielsweise, dass die Aufgabe ausgeführt wird, wenn der Computer entsperrt wird.<br/>                                                    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





