---
title: sessionStateChangeType Simple Type
description: Definiert Werte für die Art der Terminalserver-Sitzungszustandsänderung, die Sie verwenden können, um einen Task zum Starten auszulösen.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- sessionStateChangeType simple type Taskplaner
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a67334b2e8d51404a0e5e78a7d2b3e49908cd1c6ce74f499e66272d2db9be910
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099810"
---
# <a name="sessionstatechangetype-simple-type"></a>sessionStateChangeType Simple Type

Definiert Werte für die Art der Terminalserver-Sitzungszustandsänderung, die Sie verwenden können, um einen Task zum Starten auszulösen.

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

Der einfache **sessionStateChangeType-Typ** definiert die folgenden Werte.



| Wert             | BESCHREIBUNG                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConsoleConnect    | Verbindungsstatusänderung der Terminalserverkonsole. Wenn Sie beispielsweise eine Verbindung mit einer Benutzersitzung auf dem lokalen Computer herstellen, indem Sie benutzer auf dem Computer wechseln. <br/>                            |
| ConsoleDisconnect | Statusänderung beim Trennen der Verbindung mit der Terminalserverkonsole. Wenn Sie beispielsweise die Verbindung mit einer Benutzersitzung auf dem lokalen Computer trennen, indem Sie die Benutzer auf dem Computer wechseln. <br/>                      |
| RemoteConnect     | Statusänderung des Remoteverbindungsstatus des Terminalservers. Wenn ein Benutzer beispielsweise eine Verbindung mit einer Benutzersitzung mithilfe des Remotedesktopverbindung Programms von einem Remotecomputer herstellt. <br/>            |
| RemoteDisconnect  | Statusänderung der Remoteverbindung des Terminalservers. Beispiel: Wenn ein Benutzer bei Verwendung des Remotedesktopverbindung Programms von einem Remotecomputer die Verbindung mit einer Benutzersitzung trennt. <br/> |
| SessionLock       | Änderung des gesperrten Zustands der Terminalserversitzung. Diese Zustandsänderung bewirkt beispielsweise, dass die Aufgabe ausgeführt wird, wenn der Computer gesperrt ist. <br/>                                                       |
| SessionUnlock     | Zustandsänderung bei Entsperrung der Terminalserversitzung. Diese Zustandsänderung bewirkt beispielsweise, dass die Aufgabe ausgeführt wird, wenn der Computer entsperrt wird.<br/>                                                    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





