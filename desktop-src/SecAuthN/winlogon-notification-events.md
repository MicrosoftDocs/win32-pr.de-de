---
description: Listet Winlogon-Benachrichtigungs Ereignisse auf.
ms.assetid: 48b0f389-5b3c-4b13-ad23-a8bc6bcd1850
title: Winlogon-Benachrichtigungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58827dc2699c92dfc3a814d2366608e1bd3fb662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862391"
---
# <a name="winlogon-notification-events"></a>Winlogon-Benachrichtigungs Ereignisse

[*Winlogon*](../secgloss/w-gly.md) kann Ihr Benachrichtigungs Paket über die folgenden Ereignisse informieren.



| Ereignis                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                         |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sperre**<br/>                 | Dieses Ereignis tritt auf, wenn der Benutzer die Arbeitsstation sperrt.<br/>                                                                                                                                                                                                                                                   |
| **Abmeldung**<br/>               | Dieses Ereignis tritt auf, wenn sich ein Benutzer vom System abmeldet. Das Abmelde Ereignis wird synchron ausgeführt, auch **Wenn die Registrierungs** Einstellungen des Benachrichtigungs Pakets angeben, dass Ereignisse asynchron verarbeitet werden können.<br/>                                                                                         |
| **Anmelden**<br/>                | Dieses Ereignis tritt auf, wenn sich ein Benutzer beim System anmeldet.<br/> Beachten Sie, dass das **Anmelde** Ereignis auftritt, bevor die Netzwerkverbindungen des Benutzers wieder hergestellt werden. Wenn Ihr Ereignishandler Zugriff auf die Netzwerkverbindungen des Benutzers benötigt, sollte das **startshell** -Ereignis anstelle des **Anmelde** Ereignisses behandelt werden.<br/> |
| **Herunterfahren**<br/>             | Dieses Ereignis tritt unmittelbar vor dem heruntergefahren des Systems auf.<br/>                                                                                                                                                                                                                                                     |
| **Smartcardlogonnotify**<br/> | Dieses Ereignis tritt auf, wenn ein Benutzer sich mit einer Smartcard beim System anmeldet.<br/>                                                                                                                                                                                                                                   |
| **Startbildschirm**<br/>     | Dieses Ereignis tritt auf, wenn der Bildschirmschoner gestartet wurde. Dies geschieht in der Regel, wenn ein Benutzer für einen bestimmten Zeitraum inaktiv war.<br/> Funktionen, die dieses Ereignis verarbeiten, sollten keine Benutzeroberfläche anzeigen. Die Ereignis Benachrichtigung " **Startbildschirm** " dient nur zu Informationszwecken.<br/> |
| **Startshell**<br/>           | Dieses Ereignis tritt auf, nachdem sich der Benutzer beim System angemeldet hat, Netzwerkverbindungen hergestellt und das vom Benutzer angegebene Shellprogramm (normalerweise Windows-Explorer) gestartet wurde.<br/>                                                                                                                |
| **Startup**<br/>              | Dieses Ereignis tritt auf, wenn das System gestartet oder neu gestartet wird.<br/>                                                                                                                                                                                                                                               |
| **Stopbildschirm**<br/>      | Dieses Ereignis tritt auf, wenn der Bildschirmschoner angehalten wurde. Dies geschieht in der Regel, wenn eine Tastatur-oder Maus Aktivität vorliegt.<br/> Funktionen, die dieses Ereignis verarbeiten, sollten keine Benutzeroberfläche anzeigen. Die Ereignis Benachrichtigung " **StopScreenSaver** " dient nur zu Informationszwecken.<br/>                  |
| **Entsperren**<br/>               | Dieses Ereignis tritt auf, wenn der Benutzer die Arbeitsstation entsperrt oder wenn ein Systemadministrator die Sperre überschreibt und den Benutzer abmeldet.<br/>                                                                                                                                                                         |



 

 

 
