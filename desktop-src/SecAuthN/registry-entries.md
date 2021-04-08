---
description: Erläutert die Registrierungseinträge für Winlogon-Ereignisse.
ms.assetid: dbebe23f-84ff-4a3e-8b8c-fa3bda10fa57
title: Registrierungseinträge (Authentifizierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d50b413d99d2bc31a7af4e8e101ab27e51a8892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864788"
---
# <a name="registry-entries-authentication"></a>Registrierungseinträge (Authentifizierung)

Damit Ihr Paket Ereignis Benachrichtigungen von [*Winlogon*](../secgloss/w-gly.md)empfangen kann, müssen Sie den Namen des Pakets, die Namen der Ereignishandlerfunktionen im Paket, die für die Implementierung des Pakets verantwortliche dll und Informationen darüber angeben, ob die dll asynchrone Ereignisse und Identitätswechsel unterstützt.

Sie sollten den Registrierungsschlüssel des Benachrichtigungs Pakets als Unterschlüssel von erstellen.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **Benachrichtigen**

Der Name des Schlüssels ist in der Regel mit dem Namen der dll identisch. Dies ist jedoch nicht zwingend erforderlich. Der für das Paket ausgewählte Name darf nicht mit den Namen anderer installierter Benachrichtigungs Pakete in Konflikt stehen.

Erstellen Sie im Registrierungsschlüssel **Benachrichtigen** die folgenden Registrierungs Werte, wenn in Ihrem Paket eine relevante Ereignishandlerfunktion vorhanden ist.



| Datentyp "Wertname" \[\]                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Asynchron** \[ **Reg \_ DWORD**\]<br/>    | Gibt an, ob das Paket Ereignisse asynchron verarbeiten kann. Wenn dieser Wert auf 1 festgelegt ist, ruft Winlogon die Paketfunktionen in einem separaten Thread auf. Andernfalls trifft dies nicht zu.<br/>                                                                                                                                                                                                                                 |
| **DllName** \[ **Reg \_ Erweitern von \_ SZ**\]<br/>    | Der Name der dll, die das Benachrichtigungs Paket implementiert, z. b.: "Notify.dll".<br/>                                                                                                                                                                                                                                                                                                                          |
| Identität annehmen  \[ **Reg \_ DWORD**\]<br/>     | Gibt an, ob Winlogon die Identität des Sicherheits [*Kontexts*](../secgloss/c-gly.md) des angemeldeten Benutzers annehmen soll, wenn er die Funktionen des Benachrichtigungs Pakets aufruft. Wenn dieser Wert auf 1 festgelegt ist, verwendet Winlogon den Identitätswechsel. Andernfalls trifft dies nicht zu.<br/>                                                                                                                    |
| **Sperre** \[ **Reg \_ SZ**\]<br/>               | Der Name der Funktion, die Desktop Sperr Ereignisse behandelt, z. b.: "WLEventLock".<br/>                                                                                                                                                                                                                                                                                                                           |
|  Abmelden \[ **Reg \_ SZ**\]<br/>             | Der Name der Funktion, die Abmelde Ereignisse behandelt, z. b.: "WLEventLogoff".<br/>                                                                                                                                                                                                                                                                                                                               |
| **Anmelden** \[ **Reg \_ SZ**\]<br/>              | Der Name der Funktion, die Anmelde Ereignisse behandelt, z. b.: "WLEventLogon".<br/>                                                                                                                                                                                                                                                                                                                                 |
| **Herunter** \[ fahren **Reg \_ SZ**\]<br/>           | Der Name der Funktion, die Shutdown-Ereignisse behandelt, z. b.: "WLEventShutdown".<br/>                                                                                                                                                                                                                                                                                                                           |
| **Smartcardlogonnotify** \[ **DWORD**\]<br/> | Gibt an, ob Winlogon eine Benachrichtigung für Anmelde Ereignisse von Smartcards generieren soll. Wenn dieser Wert auf 1 festgelegt ist, lässt Winlogon smartcardbenachrichtigungen zu. Andernfalls trifft dies nicht zu.<br/>                                                                                                                                                                                                                     |
| **Startbildschirm** \[ **Reg \_ SZ**\]<br/>   | Der Name der Funktion, die Bildschirmschoner-Start Ereignisse behandelt, z. b.: "wleventstartbildschirm".<br/>                                                                                                                                                                                                                                                                                                          |
| **Startshell** \[ **Reg \_ SZ**\]<br/>         | Der Name der Funktion, die shellstartereignisse behandelt, z. b.: "wleventstartshell".<br/> Ein shellstartereignis tritt auf, nachdem sich der Benutzer angemeldet hat, aber bevor der Desktop angezeigt wird. Dies unterscheidet sich vom Anmelde Ereignis, wenn der Sicherheits [*Kontext*](../secgloss/c-gly.md) des Benutzers eingerichtet wurde und Ressourcen wie Netzwerkverbindungen verfügbar sind.<br/> |
| **Starten** \[ **Reg \_ SZ**\]<br/>            | Der Name der Funktion, die Systemstart Ereignisse behandelt, z. b.: "WLEventStartup".<br/>                                                                                                                                                                                                                                                                                                                       |
| **Stopbildschirm** \[ **Reg \_ SZ**\]<br/>    | Der Name der Funktion, die Bildschirmschoner-Stopp Ereignisse behandelt, z. b.: "wleventstopbildschirm".<br/>                                                                                                                                                                                                                                                                                                            |
| **Entsperren** \[ **Reg \_ SZ**\]<br/>             | Der Name der Funktion, die Desktop entsperrungs Ereignisse behandelt, z. b.: "WLEventUnlock".<br/>                                                                                                                                                                                                                                                                                                                        |



 

 

 
