---
description: Ein Winlogon-Benachrichtigungs Paket ist eine DLL, die Funktionen exportiert, die Winlogon-Ereignisse verarbeiten. Wenn sich ein Benutzer beispielsweise beim System anmeldet, ruft Winlogon die Anmelde Ereignishandler-Funktion jedes Benachrichtigungs Pakets auf, um Informationen zum Ereignis bereitzustellen.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Erstellen eines Winlogon-Benachrichtigungs Pakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0127674967ee3155d42e143a1b142d8c83137c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359032"
---
# <a name="creating-a-winlogon-notification-package"></a>Erstellen eines Winlogon-Benachrichtigungs Pakets

Ein [*Winlogon*](/windows/desktop/SecGloss/w-gly) -Benachrichtigungs Paket ist eine DLL, die Funktionen exportiert, die Winlogon-Ereignisse verarbeiten. Wenn sich ein Benutzer beispielsweise beim System anmeldet, ruft Winlogon die Anmelde Ereignishandler-Funktion jedes Benachrichtigungs Pakets auf, um Informationen zum Ereignis bereitzustellen.

Die Namen der in einem Benachrichtigungs Paket implementierten Ereignishandlerfunktionen werden dem Entwickler überlassen. Winlogon überprüft die Registrierung, um die Namen der Ereignishandlerfunktionen zu erhalten. Beispielsweise kann ein Benachrichtigungs Paket die LOGON-Ereignishandlerfunktion so implementieren, als `WLEventLogon` wäre andere möglicherweise verwendende `HandleLogonEvent` .

Sie müssen für jedes Winlogon-Ereignis keine Ereignishandler implementieren und registrieren, sondern nur für Ereignisse, die für Ihre Anwendung nützlich sind. Jede Ereignishandlerfunktion muss den Funktionsprototyp verwenden, der im [Prototyp der Ereignishandler-Funktion](event-handler-function-prototype.md)beschrieben wird. Dieser Prototyp verfügt über einen einzelnen Parameter: eine [**wlx- \_ Benachrichtigungs \_ Informations**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) Struktur, die Details zum Ereignis enthält.

Winlogon ignoriert die Ausgabe von Ereignishandlerfunktionen. Wenn die Behandlung eines Ereignisses eine Interaktion mit Winlogon erfordert, verwenden Sie die [Winlogon-Unterstützungsfunktionen](authentication-functions.md).

Um das Winlogon-Benachrichtigungs Paket zu verwenden, muss die dll in den Ordner% SystemRoot% System32 kopiert werden \\ , und für das Benachrichtigungs Paket muss ein Registrierungs Update durchgeführt werden. Weitere Informationen zum Registrierungs Update finden Sie unter [Registrieren eines Winlogon-Benachrichtigungs Pakets](registering-a-winlogon-notification-package.md).

 

 
