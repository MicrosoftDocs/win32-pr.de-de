---
description: Ein Winlogon-Benachrichtigungspaket ist eine DLL, die Funktionen exportiert, die Winlogon-Ereignisse behandeln. Wenn sich ein Benutzer beispielsweise beim System anmeldet, ruft Winlogon die Anmeldeereignishandlerfunktion jedes Benachrichtigungspakets auf, um Informationen zum Ereignis bereitzustellen.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Erstellen eines Winlogon-Benachrichtigungspakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84d0290f7afeba7a427f5c50caf1638fd88bfdb4b52ee513a9b1c0506aed9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008868"
---
# <a name="creating-a-winlogon-notification-package"></a>Erstellen eines Winlogon-Benachrichtigungspakets

Ein [*Winlogon-Benachrichtigungspaket*](/windows/desktop/SecGloss/w-gly) ist eine DLL, die Funktionen exportiert, die Winlogon-Ereignisse behandeln. Wenn sich ein Benutzer beispielsweise beim System anmeldet, ruft Winlogon die Anmeldeereignishandlerfunktion jedes Benachrichtigungspakets auf, um Informationen zum Ereignis bereitzustellen.

Die Namen der in einem Benachrichtigungspaket implementierten Ereignishandlerfunktionen bleiben dem Entwickler überlassen. Winlogon überprüft die Registrierung, um die Namen der Ereignishandlerfunktionen abzurufen. Beispielsweise könnte ein Benachrichtigungspaket die Anmeldeereignishandlerfunktion implementieren, während ein anderes verwenden `WLEventLogon` `HandleLogonEvent` könnte.

Sie müssen ereignishandler nicht für jedes Winlogon-Ereignis implementieren und registrieren, sondern nur für Ereignisse, die für Ihre Anwendung nützlich sind. Jede Ereignishandlerfunktion muss den Funktionsprototyp verwenden, der unter [Ereignishandlerfunktionsprototyp](event-handler-function-prototype.md)beschrieben ist. Dieser Prototyp verfügt über einen einzelnen Parameter: eine [**WLX \_ NOTIFICATION \_ INFO-Struktur,**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) die Details zum Ereignis enthält.

Winlogon ignoriert die Ausgabe von Ereignishandlerfunktionen. Wenn für die Behandlung eines Ereignisses die Interaktion mit Winlogon erforderlich ist, verwenden Sie die [Winlogon-Unterstützungsfunktionen](authentication-functions.md).

Um Ihr Winlogon-Benachrichtigungspaket zu verwenden, muss die DLL in den Ordner %SystemRoot% \\ system32 kopiert werden, und für das Benachrichtigungspaket muss ein Registrierungsupdate durchgeführt werden. Informationen zum Registrierungsupdate finden Sie unter [Registrieren eines Winlogon-Benachrichtigungspakets.](registering-a-winlogon-notification-package.md)

 

 
