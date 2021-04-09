---
title: Überwachen von Sitzungs Verbindungen und verbindungsverbindungen
description: Um eine Anwendung bei Remotedesktopdienste zu registrieren, speichern Sie den Namen der virtuellen Kanal Serveranwendung in der Registrierung, indem Sie einen Unterschlüssel hinzufügen.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e819b13594ecec14a2b425560152cadedd4e9122
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039094"
---
# <a name="monitoring-session-connections-and-disconnections"></a>Überwachen von Sitzungs Verbindungen und verbindungsverbindungen

Für eine-Dienst Anwendung, z. b. eine Virtual Channel-Serveranwendung, um Sitzungs Verbindungen und-Verbindungen zu überwachen, müssen Sie Sie bei Remotedesktopdienste registrieren. Wenn Sie die Anwendung bei Remotedesktopdienste registrieren möchten, speichern Sie den Namen der Virtual Channel-Serveranwendung in der Registrierung, indem Sie einen Unterschlüssel unter folgendem Speicherort hinzufügen:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Terminalserver** \\ **AddIns**

Der Unterschlüssel kann einen beliebigen Namen haben. Er muss über einen **reg \_ SZ** -Wert **namens** verfügen, der den symbolischen Namen der Anwendung enthält.

``` syntax
Name = AddinName
```

Die maximale Länge des unter Schlüssels und des Werts von **Name** beträgt 99 Zeichen.

Der Unterschlüssel muss auch über einen **reg \_ DWORD** -Wert verfügen, der den Typ der Serveranwendung angibt.

``` syntax
Type = AddinType
```

*Addintype* muss den folgenden Wert aufweisen:



| Wert | Bedeutung                               |
|-------|---------------------------------------|
| 3     | Benutzermodusanwendung, Sitzungs Bereich. |



 

Die Registrierung der-Dienst Anwendung wird nur in Sitzungen wirksam, die nach der Registrierung erstellt wurden.

Für jede registrierte Dienst Anwendung signalisiert Remotedesktopdienste einen Satz von Ereignis Objekten, wenn ein Client eine Verbindung mit der Sitzung herstellt oder diese trennt. Jedes virtuelle Channel-Plug-in muss sich selbst registrieren und die Benachrichtigungs Ereignisse erstellen, indem [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)aufgerufen wird. Die Namen dieser Ereignis Objekte entsprechen dem folgenden Format.

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

*AddInName* ist die Zeichenfolge, die im **Name** -Wert des Registrierungs unter Schlüssels angegeben ist, unter dem die Serveranwendung registriert ist. Das Erstellen dieser Ereignisse in einer Sitzung bewirkt, dass Sie in einem speziellen Ereignis Verzeichnis pro Sitzung erstellt werden. Das Ereignis Verzeichnis stellt zusätzliche Sicherheit bereit, indem verhindert wird, dass Anwendungen in anderen Sitzungen den Zustand dieser Ereignisse ändern.

Um zu steuern, ob Verbindungs-und Trennungs Ereignisse auf dem Server empfangen werden, können Sie das Flag " **remotecontrolpersistent** " in der Registrierung unter folgendem Schlüssel platzieren:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Terminalserver** \\ **AddIns** \\ *AddInName*

Das Flag aktiviert oder deaktiviert das erneute Verbinden und trennen von Ereignissen, wenn eine Client Sitzung gestartet oder angehalten wird. Die Syntax des **reg \_ DWORD** -Werts lautet wie folgt:

``` syntax
RemoteControlPersistent = flag
```

Der Wert des *Flags* kann ein oder NULL sein. Der Standardwert ist 0 (null). Wenn diese Einstellung auf 1 festgelegt ist, wird die Dienst Anwendung nicht benachrichtigt, wenn die Client Sitzung gestartet oder beendet wird. Wenn der Wert auf 0 (null) festgelegt ist, wird beim Starten der Client Sitzung ein Ereignis zum erneuten Verbinden signalisiert, und beim Anhalten der Client Sitzung wird ein Disconnect-Ereignis signalisiert.

Das vorherige Ereignis Objekt Namensformat wird in Windows Server 2008 weiterhin aus Gründen der Abwärtskompatibilität unterstützt. Es wird empfohlen, dass Sie das neuere Windows Server 2008-Format verwenden, da es sicherer ist.

Das vorherige Ereignis Format lautet wie folgt.

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

*AddInName* ist die Zeichenfolge, die im **Name** -Wert des Registrierungs unter Schlüssels angegeben ist, unter dem die Serveranwendung registriert ist. *SessionID* ist der Sitzungs Bezeichner einer Client Sitzung.

 

 