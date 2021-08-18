---
description: Das System überträgt eine Reihe von Standardereignissen für Geräteänderung an alle Anwendungen und Dienste.
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: Gerätebenachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12186ab6349057258d723f7e690e889b7e79af4abe47f714055599cb6f648333
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636620"
---
# <a name="device-notifications"></a>Gerätebenachrichtigungen

Das System überträgt eine Reihe von Standardereignissen für Geräteänderung an alle Anwendungen und Dienste. Sie müssen sich nicht registrieren, um diese Standardereignisse zu empfangen. Weitere Informationen finden Sie im Abschnitt "Hinweise" in [**RegisterDeviceNotification.**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) Verwenden Sie die **RegisterDeviceNotification-Funktion,** um andere Ereignisse anzugeben, die Ihre Anwendung oder Ihr Dienst empfangen soll.

Wenn eine Anwendung oder ein Dienst [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)aufruft, wird auch das Fenster angegeben, in dem die Benachrichtigungsereignisse empfangen werden. Dienste können anstelle eines Fensterhandpunkts ein Dienststatushand handle angeben. Wenn ein Dienst sein Dienststatushand handle angibt, erhält sein Dienststeuerungshandler die Benachrichtigungsereignisse. Weitere Informationen finden Sie unter [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Achten Sie darauf, Plug & Play Geräteereignisse so schnell wie möglich zu behandeln. Andernfalls reagiert das System möglicherweise nicht mehr. Wenn Ihr Ereignishandler einen Vorgang ausführen soll, der die Ausführung blockieren kann (z. B. E/A), sollten Sie einen anderen Thread starten, um den Vorgang asynchron durchzuführen.

Gerätebenachrichtigungshandles, die [**von RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) zurückgegeben werden, müssen geschlossen werden, indem sie die [**UnregisterDeviceNotification-Funktion**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) aufrufen, wenn sie nicht mehr benötigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierung für Gerätebenachrichtigungen](registering-for-device-notification.md)
</dt> </dl>

 

 
