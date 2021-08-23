---
description: Ein Dienst, bei dem es sich um eine Konsolenanwendung handelt, kann einen Konsolensteuerungshandler registrieren, um Benachrichtigungen zu erhalten, wenn sich ein Benutzer abmeldet.
ms.assetid: 86ace8b8-c1cb-4646-bc92-86bd578a82c5
title: Empfangen von Ereignissen in einem Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe2312989208d5b6587067e64f10401c32229c2b19a7b4846163444576e63ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003708"
---
# <a name="receiving-events-in-a-service"></a>Empfangen von Ereignissen in einem Dienst

Ein Dienst, bei dem es sich um eine Konsolenanwendung handelt, kann einen [Konsolensteuerungshandler](/windows/console/console-control-handlers) registrieren, um Benachrichtigungen zu erhalten, wenn sich ein Benutzer abmeldet. Es wird jedoch kein Konsolenereignis gesendet, wenn sich ein interaktiver Benutzer anmeldet. Informationen zum Empfangen von Benachrichtigungen, wenn sich ein Benutzer anmeldet, finden Sie unter [Erstellen eines Winlogon-Benachrichtigungspakets.](/windows/desktop/SecAuthN/creating-a-winlogon-notification-package)

Das System überträgt Geräteänderungsereignisse an alle Dienste. Diese Ereignisse können von einem Dienst in einer Fensterprozedur oder in seinem Dienststeuerungshandler empfangen werden. Verwenden Sie die [**RegisterDeviceNotification-Funktion,**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) um anzugeben, welche Ereignisse Ihr Dienst empfangen soll.

Achten Sie darauf, Plug & Play Geräteereignisse so schnell wie möglich zu behandeln. Andernfalls reagiert das System möglicherweise nicht mehr. Wenn Ihr Ereignishandler einen Vorgang ausführen soll, der die Ausführung blockieren kann (z. B. E/A), empfiehlt es sich, einen anderen Thread zu starten, um den Vorgang asynchron auszuführen.

Wenn ein Dienst [**RegisterDeviceNotification aufruft,**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)gibt der Dienst auch ein Fensterhandle oder ein Dienststatushandle an. Wenn ein Dienst ein Fensterhandle angibt, empfängt die Fensterprozedur die Benachrichtigungsereignisse. Wenn ein Dienst sein Dienststatushandle angibt, empfängt der Dienststeuerungshandler die Benachrichtigungsereignisse. Weitere Informationen finden Sie unter [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex).

Von [**RegisterDeviceNotification zurückgegebene**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) Gerätebenachrichtigungshandles müssen geschlossen werden, indem die [**UnregisterDeviceNotification-Funktion**](/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification) aufgerufen wird, wenn sie nicht mehr benötigt werden.

 

 
