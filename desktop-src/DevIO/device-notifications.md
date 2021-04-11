---
description: Das System überträgt eine Reihe von standardmäßigen Geräte Änderungs Ereignissen an alle Anwendungen und Dienste.
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: Geräte Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caeee8ba50a62a3bc393172347be09d1ac58085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127293"
---
# <a name="device-notifications"></a>Geräte Benachrichtigungen

Das System überträgt eine Reihe von standardmäßigen Geräte Änderungs Ereignissen an alle Anwendungen und Dienste. Sie müssen sich nicht registrieren, um diese Standard Ereignisse zu empfangen. Weitere Informationen finden Sie im Abschnitt "Hinweise" unter [**registerdevicenotifi.**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) Verwenden Sie die **registerdevicenotifi-** Funktion, um andere Ereignisse anzugeben, die Ihre Anwendung oder Ihr Dienst empfangen soll.

Wenn eine Anwendung oder ein Dienst [**registerdevicenotifiruft**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), wird auch das Fenster angegeben, in dem die Benachrichtigungs Ereignisse empfangen werden. Dienste können ein Dienststatus handle anstelle eines Fenster Handles angeben. Wenn ein Dienst sein Dienststatus Handle angibt, empfängt der Dienst Steuerungs Handler die Benachrichtigungs Ereignisse. Weitere Informationen finden Sie unter [**handlerex**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Stellen Sie sicher, dass Plug & Play Geräte Ereignisse so schnell wie möglich behandelt werden. Andernfalls reagiert das System möglicherweise nicht mehr. Wenn der Ereignishandler einen Vorgang ausführen kann, der die Ausführung blockieren kann (z. b. e/a), empfiehlt es sich, einen weiteren Thread zu starten, um den Vorgang asynchron auszuführen.

Die von [**registerdevicenotifizurück**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) gegebenen Geräte Benachrichtigungs Handles müssen geschlossen werden, indem die [**unregisterdevicenotifi-**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) Funktion aufgerufen wird, wenn Sie nicht mehr benötigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierung für Gerätebenachrichtigungen](registering-for-device-notification.md)
</dt> </dl>

 

 
