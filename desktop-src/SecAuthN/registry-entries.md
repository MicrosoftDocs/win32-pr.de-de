---
description: Erläutert die Registrierungseinträge für Winlogon-Ereignisse.
ms.assetid: dbebe23f-84ff-4a3e-8b8c-fa3bda10fa57
title: Registrierungseinträge (Authentifizierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 388cbe42d085543d5e7d4df1c9705504864b370cf94eb32f4025eaba12b89ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919446"
---
# <a name="registry-entries-authentication"></a>Registrierungseinträge (Authentifizierung)

Damit Ihr Paket Ereignisbenachrichtigungen von [*Winlogon*](../secgloss/w-gly.md)empfangen kann, müssen Sie den Namen des Pakets, die Namen der Ereignishandlerfunktionen im Paket, die DLL, die für die Implementierung des Pakets verantwortlich ist, sowie Informationen darüber angeben, ob die DLL asynchrone Ereignisse und Identitätswechsel unterstützt.

Sie sollten den Registrierungsschlüssel des Benachrichtigungspakets als Unterschlüssel von erstellen.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft Windows** \\ **NT** \\ **CurrentVersion** \\ **Winlogon** \\ **Notify**

Der Name des Schlüssels ist in der Regel mit dem Namen der DLL identisch. Dies ist jedoch nicht zwingend erforderlich. Der für Das Paket ausgewählte Name darf nicht mit den Namen anderer installierter Benachrichtigungspakete in Konflikt stehen.

Erstellen Sie **im Registrierungsschlüssel** Benachrichtigen die folgenden Registrierungswerte, wenn in Ihrem Paket eine relevante Ereignishandlerfunktion vorhanden ist.



| Datentyp des \[ Wertnamens\]                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Asynchron** \[ **REG \_ DWORD**\]<br/>    | Gibt an, ob das Paket Ereignisse asynchron behandeln kann. Wenn dieser Wert auf 1 festgelegt ist, ruft Winlogon die Paketfunktionen in einem separaten Thread auf. Andernfalls trifft dies nicht zu.<br/>                                                                                                                                                                                                                                 |
| **DllName** \[ **REG \_ EXPAND \_ SZ**\]<br/>    | Name der DLL, die das Benachrichtigungspaket implementiert, z. B. "Notify.dll".<br/>                                                                                                                                                                                                                                                                                                                          |
| **Identitätswechsel** \[ **REG \_ DWORD**\]<br/>     | Gibt an, ob winlogon [](../secgloss/c-gly.md) beim Aufrufen der Benachrichtigungspaketfunktionen die Identität des Sicherheitskontexts des angemeldeten Benutzers übernehmen soll. Wenn dieser Wert auf 1 festgelegt ist, verwendet winlogon einen Identitätswechsel. Andernfalls trifft dies nicht zu.<br/>                                                                                                                    |
| **Sperre** \[ **REG \_ SZ**\]<br/>               | Name der Funktion, die Desktopsperrereignisse behandelt, z.B. "WLEventLock".<br/>                                                                                                                                                                                                                                                                                                                           |
| **Abmelden** \[ **REG \_ SZ**\]<br/>             | Name der Funktion, die Abmeldeereignisse behandelt, z.B. "WLEventLogoff".<br/>                                                                                                                                                                                                                                                                                                                               |
| **Anmeldung** \[ **REG \_ SZ**\]<br/>              | Name der Funktion, die Anmeldeereignisse behandelt, z.B. "WLEventLogon".<br/>                                                                                                                                                                                                                                                                                                                                 |
| **Herunterfahren** \[ **REG \_ SZ**\]<br/>           | Name der Funktion, die Ereignisse zum Herunterfahren behandelt, z.B. "WLEventShutdown".<br/>                                                                                                                                                                                                                                                                                                                           |
| **SmartCardLogonNotify** \[ **DWORD**\]<br/> | Gibt an, ob winlogon eine Benachrichtigung für Anmeldeereignisse von Smartcards generieren soll. Wenn dieser Wert auf 1 festgelegt ist, lässt Winlogon Smartcardbenachrichtigungen zu. Andernfalls trifft dies nicht zu.<br/>                                                                                                                                                                                                                     |
| **StartScreenSaver** \[ **REG \_ SZ**\]<br/>   | Name der Funktion, die Startereignisse des Bildschirmschoners behandelt, z.B. "WLEventStartScreenSaver".<br/>                                                                                                                                                                                                                                                                                                          |
| **StartShell** \[ **REG \_ SZ**\]<br/>         | Name der Funktion, die Shellstartereignisse behandelt, z.B. "WLEventStartShell".<br/> Ein Shellstartereignis tritt auf, nachdem sich der Benutzer angemeldet hat, aber bevor der Desktop angezeigt wird. Sie unterscheidet sich vom Anmeldeereignis dadurch, [](../secgloss/c-gly.md) dass der Sicherheitskontext des Benutzers eingerichtet wurde und Ressourcen wie Netzwerkverbindungen verfügbar sind.<br/> |
| **Start** \[ **REG \_ SZ**\]<br/>            | Name der Funktion, die Systemstartereignisse behandelt, z.B. "WLEventStartup".<br/>                                                                                                                                                                                                                                                                                                                       |
| **StopScreenSaver** \[ **REG \_ SZ**\]<br/>    | Name der Funktion, die Stopereignisse des Bildschirmschoners behandelt, z.B. "WLEventStopScreenSaver".<br/>                                                                                                                                                                                                                                                                                                            |
| **Entsperren** \[ **REG \_ SZ**\]<br/>             | Name der Funktion, die Ereignisse zur Desktopentsperrung verarbeitet, z.B. "WLEventUnlock".<br/>                                                                                                                                                                                                                                                                                                                        |



 

 

 
