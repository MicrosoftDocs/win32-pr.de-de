---
description: Eine der gängigsten Möglichkeiten zum Empfangen eines Ereignisses ist eine ausgeführte Anwendung, z. B. eine Verwaltungsanwendung, die Ereignisse sammelt und einem Benutzer anzeigt.
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: Empfangen von Ereignissen für die Dauer Ihrer Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6815c2ddd7725ccd12dd65b0047874ddce1038b2a2c07f90a40d6f87e6af3a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554218"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a>Empfangen von Ereignissen für die Dauer Ihrer Anwendung

Eine der gängigsten Möglichkeiten zum Empfangen eines Ereignisses ist eine ausgeführte Anwendung, z. B. eine Verwaltungsanwendung, die Ereignisse sammelt und einem Benutzer anzeigt. Solche Anwendungen werden als "temporär" bezeichnet, da ein temporärer Consumer beim Herunterfahren keine Ereignisbenachrichtigungen empfängt.

Ein temporärer Consumer ruft [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) im Skript oder [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ auf, um Ereignisse in einem Namespace zu abonnieren. Die diesem Abonnement zugeordnete Identität ist der Aufrufer.

Ein temporärer Ereignisverbraucher kann Benachrichtigungen entweder asynchron oder semisynchron in Skripts und C++ empfangen.

> [!Note]  
> Aus Sicherheitsgründen ist es wichtig zu beachten, dass asynchrone Ereignisbenachrichtigungen nicht empfohlen werden. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf.](setting-security-on-an-asynchronous-call.md) Ereignisverbraucher haben besondere Sicherheitsbedenken. Weitere Informationen finden Sie unter [Sichern von WMI-Ereignissen.](securing-wmi-events.md)

 

Weitere Informationen zum Empfangen von asynchronen und semisynchronen Ereignisbenachrichtigungen finden Sie unter [Empfangen von asynchronen Ereignisbenachrichtigungen](receiving-asynchronous-event-notifications.md) und [Empfangen von semisynchronen Ereignisbenachrichtigungen.](receiving-synchronous-and-semisynchronous-event-notifications.md)

 

 



