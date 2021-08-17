---
description: Listet Winlogon-Benachrichtigungsereignisse auf.
ms.assetid: 48b0f389-5b3c-4b13-ad23-a8bc6bcd1850
title: Winlogon-Benachrichtigungsereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7359ef4d1d053e438d30564fcededbf3a0ccb10275cd6e4f669c2a20c54b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785716"
---
# <a name="winlogon-notification-events"></a>Winlogon-Benachrichtigungsereignisse

[*Winlogon*](../secgloss/w-gly.md) kann Ihr Benachrichtigungspaket über die folgenden Ereignisse informieren.



| Ereignis                               | Beschreibung                                                                                                                                                                                                                                                                                                         |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sperre**<br/>                 | Dieses Ereignis tritt auf, wenn der Benutzer die Arbeitsstation sperrt.<br/>                                                                                                                                                                                                                                                   |
| **Abmelden**<br/>               | Dieses Ereignis tritt auf, wenn sich ein Benutzer vom System abmeldet. Das **Logoff-Ereignis** wird synchron ausgeführt, auch wenn die Registrierungseinstellungen des Benachrichtigungspakets angeben, dass ereignisse asynchron behandelt werden können.<br/>                                                                                         |
| **Anmelden**<br/>                | Dieses Ereignis tritt auf, wenn sich ein Benutzer beim System anmeldet.<br/> Beachten Sie, dass das **Anmeldeereignis** auftritt, bevor die Netzwerkverbindungen des Benutzers wiederhergestellt werden. Wenn Ihr Ereignishandler Zugriff auf die Netzwerkverbindungen des Benutzers erfordert, sollte er das **StartShell-Ereignis** anstelle des **Anmeldeereignisses** behandeln.<br/> |
| **Herunterfahren**<br/>             | Dieses Ereignis tritt unmittelbar vor dem Herunterfahren des Systems auf.<br/>                                                                                                                                                                                                                                                     |
| **SmartCardLogonNotify**<br/> | Dieses Ereignis tritt auf, wenn sich ein Benutzer mit einer Smartcard beim System anmeldet.<br/>                                                                                                                                                                                                                                   |
| **StartScreenSaver**<br/>     | Dieses Ereignis tritt auf, wenn der Bildschirmschoner gestartet wurde. Dies geschieht in der Regel, nachdem ein Benutzer für einen bestimmten Zeitraum inaktiv war.<br/> Funktionen, die dieses Ereignis behandeln, sollten keine Benutzeroberfläche anzeigen. **Die StartScreenSaver-Ereignisbenachrichtigung** dient nur zu Informationszwecken.<br/> |
| **StartShell**<br/>           | Dieses Ereignis tritt auf, nachdem sich der Benutzer beim System angemeldet hat, Netzwerkverbindungen hergestellt wurden und das vom Benutzer angegebene Shellprogramm (in der Regel Windows Explorer) gestartet wurde.<br/>                                                                                                                |
| **Startup**<br/>              | Dieses Ereignis tritt auf, wenn das System gestartet oder neu gestartet wird.<br/>                                                                                                                                                                                                                                               |
| **StopScreenSaver**<br/>      | Dieses Ereignis tritt auf, wenn der Bildschirmschoner beendet wurde. Dies geschieht in der Regel, wenn Tastatur- oder Mausaktivitäten vorhanden sind.<br/> Funktionen, die dieses Ereignis behandeln, sollten keine Benutzeroberfläche anzeigen. **Die StopScreenSaver-Ereignisbenachrichtigung** dient nur zu Informationszwecken.<br/>                  |
| **Entsperren**<br/>               | Dieses Ereignis tritt auf, wenn der Benutzer die Arbeitsstation entsperrt oder wenn ein Systemadministrator die Sperre außer Kraft setzt und den Benutzer abmeldet.<br/>                                                                                                                                                                         |



 

 

 
