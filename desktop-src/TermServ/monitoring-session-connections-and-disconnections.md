---
title: Überwachen von Sitzungsverbindungen und -trennungen
description: Um eine Anwendung bei Remotedesktopdienste zu registrieren, speichern Sie den Namen der Virtuellen Kanalserveranwendung in der Registrierung, indem Sie einen Unterschlüssel hinzufügen.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2813399650d535d10864f384afb6b745fb9e50039f2b981df61ceb2e6452a608
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989100"
---
# <a name="monitoring-session-connections-and-disconnections"></a>Überwachen von Sitzungsverbindungen und -trennungen

Für eine Dienstanwendung, z. B. eine Serveranwendung für virtuelle Kanäle, zum Überwachen von Sitzungsverbindungen und Trennungen müssen Sie sie bei Remotedesktopdienste registrieren. Um die Anwendung bei Remotedesktopdienste zu registrieren, speichern Sie den Namen der Virtuellen Kanalserveranwendung in der Registrierung, indem Sie unter dem folgenden Speicherort einen Unterschlüssel hinzufügen:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **TerminalServer** \\ **Addins**

Der Unterschlüssel kann einen beliebigen Namen haben. Sie muss über den **REG \_ SZ-Wert** **Name** verfügen, der den symbolischen Namen der Anwendung enthält.

``` syntax
Name = AddinName
```

Die maximale Länge des Unterschlüssels und des Namens **beträgt** 99 Zeichen.

Der Unterschlüssel muss auch über einen **REG \_ DWORD-Wert** verfügen, der den Typ der Serveranwendung angibt.

``` syntax
Type = AddinType
```

*AddinType* muss der folgende Wert sein.



| Wert | Bedeutung                               |
|-------|---------------------------------------|
| 3     | Anwendung im Benutzermodus, Sitzungsbereich. |



 

Die Registrierung der Dienstanwendung wird nur in Sitzungen wirksam, die nach der Registrierung erstellt wurden.

Für jede registrierte Dienstanwendung signalisiert Remotedesktopdienste eine Reihe von Ereignisobjekten, wenn ein Client eine Verbindung mit der Sitzung herstellt oder die Verbindung mit der Sitzung trennt. Jedes Plug-In für virtuelle Kanäle muss sich selbst registrieren und die Benachrichtigungsereignisse erstellen, indem [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)aufgerufen wird. Die Namen dieser Ereignisobjekte entsprechen dem folgenden Format.

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

*AddinName* ist die Zeichenfolge, die im **Wert Name** des Registrierungsunterschlüssels angegeben ist, unter dem die Serveranwendung registriert ist. Das Erstellen dieser Ereignisse in einer Sitzung bewirkt, dass sie in einem speziellen Ereignisverzeichnis pro Sitzung erstellt werden. Das Ereignisverzeichnis bietet zusätzliche Sicherheit, indem verhindert wird, dass Anwendungen in anderen Sitzungen den Zustand dieser Ereignisse ändern.

Um zu steuern, ob RECONNECT- und DISCONNECT-Ereignisse auf dem Server empfangen werden, können Sie das **RemoteControlPersistent-Flag** in der Registrierung unter dem folgenden Schlüssel platzieren:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **TerminalServer** \\ **Addins** \\ *addinname*

Das Flag aktiviert oder deaktiviert das Signalisieren von RECONNECT- und DISCONNECT-Ereignissen, wenn eine Clientsitzung gestartet oder beendet wird. Die Syntax des **REG \_ DWORD-Werts** lautet wie folgt.

``` syntax
RemoteControlPersistent = flag
```

Der Wert des *Flags* kann 1 oder 0 (null) sein. 0 (null) ist der Standardwert. Wenn diese Einstellung auf 1 festgelegt ist, wird die Dienstanwendung nicht benachrichtigt, wenn die Clientsitzung gestartet oder beendet wird. Wenn null festgelegt ist, wird ein RECONNECT-Ereignis signalisiert, wenn die Clientsitzung gestartet wird, und ein DISCONNECT-Ereignis wird signalisiert, wenn die Clientsitzung beendet wird.

Das vorherige Format des Ereignisobjektnamens wird in Windows Server 2008 aus Gründen der Abwärtskompatibilität weiterhin unterstützt. Es wird empfohlen, das neuere Windows Server 2008-Format zu verwenden, da es sicherer ist.

Das vorherige Ereignisformat lautet wie folgt.

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

*AddinName* ist die Zeichenfolge, die im **Wert Name** des Registrierungsunterschlüssels angegeben ist, unter dem die Serveranwendung registriert ist. *SessionId* ist der Sitzungsbezeichner einer Clientsitzung.

 

 