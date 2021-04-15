---
description: Ein Dienst, bei dem es sich um eine Konsolenanwendung handelt, kann einen Konsolen Steuerungs Handler registrieren, um eine Benachrichtigung zu erhalten, wenn sich ein Benutzer
ms.assetid: 86ace8b8-c1cb-4646-bc92-86bd578a82c5
title: Empfangen von Ereignissen in einem Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95f7329383ffc8aea08102a2fe8cf8b49e0ef9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530080"
---
# <a name="receiving-events-in-a-service"></a>Empfangen von Ereignissen in einem Dienst

Ein Dienst, bei dem es sich um eine Konsolenanwendung handelt, kann einen [Konsolen Steuerungs Handler](/windows/console/console-control-handlers) registrieren, um eine Benachrichtigung zu erhalten, wenn sich ein Benutzer Es wird jedoch kein Konsolen Ereignis gesendet, wenn sich ein interaktiver Benutzer anmeldet. Informationen zum Empfangen von Benachrichtigungen, wenn sich ein Benutzer anmeldet, finden Sie unter [Erstellen eines Winlogon-Benachrichtigungs Pakets](/windows/desktop/SecAuthN/creating-a-winlogon-notification-package).

Das System überträgt Geräte Änderungs Ereignisse an alle Dienste. Diese Ereignisse können von einem Dienst in einer Fenster Prozedur oder in seinem Dienst Steuerungs Handler empfangen werden. Verwenden Sie die [**registerdevicenotifi-**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) Funktion, um anzugeben, welche Ereignisse der Dienst empfangen soll.

Stellen Sie sicher, dass Plug & Play Geräte Ereignisse so schnell wie möglich behandelt werden. Andernfalls reagiert das System möglicherweise nicht mehr. Wenn der Ereignishandler einen Vorgang ausführen kann, der die Ausführung blockieren kann (z. b. e/a), empfiehlt es sich, einen weiteren Thread zu starten, um den Vorgang asynchron auszuführen.

Wenn ein Dienst [**registerdevicenotifizierung**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)aufruft, gibt der Dienst auch ein Fenster Handle oder ein Dienststatus Handle an. Wenn ein Dienst ein Fenster Handle angibt, empfängt die Fenster Prozedur die Benachrichtigungs Ereignisse. Wenn ein Dienst sein Dienststatus Handle angibt, empfängt der Dienst Steuerungs Handler die Benachrichtigungs Ereignisse. Weitere Informationen finden Sie unter [**handlerex**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex).

Die von [**registerdevicenotifizurück**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) gegebenen Geräte Benachrichtigungs Handles müssen geschlossen werden, indem die [**unregisterdevicenotifi-**](/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification) Funktion aufgerufen wird, wenn Sie nicht mehr benötigt werden.

 

 
