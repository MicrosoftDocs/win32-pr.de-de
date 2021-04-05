---
description: Eine der gängigsten Methoden zum Empfangen eines Ereignisses ist eine ausgelaufende Anwendung, z. b. eine Verwaltungs Anwendung, die Ereignisse sammelt und an einen Benutzer anzeigt.
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: Empfangen von Ereignissen für die Dauer der Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd6b9731dd662a92296a86910a6cf8cb231cca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042006"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a>Empfangen von Ereignissen für die Dauer der Anwendung

Eine der gängigsten Methoden zum Empfangen eines Ereignisses ist eine ausgelaufende Anwendung, z. b. eine Verwaltungs Anwendung, die Ereignisse sammelt und an einen Benutzer anzeigt. Solche Anwendungen werden als "temporär" bezeichnet, da ein temporärer Consumer beim Herunterfahren keine Ereignis Benachrichtigungen empfängt.

Ein temporärer Consumer ruft [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) im Skript oder [**IWbemServices.Execnotificationquery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ auf, um Ereignisse in einem Namespace zu abonnieren. Die diesem Abonnement zugeordnete Identität ist der Aufrufer.

Ein temporärer Ereignisconsumer kann Benachrichtigungen entweder asynchron oder SemiSynchron in Skripts und C++ empfangen.

> [!Note]  
> Aus Sicherheitsgründen ist es wichtig zu beachten, dass asynchrone Ereignis Benachrichtigungen nicht empfohlen werden. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl. Ereignisconsumer haben besondere Sicherheitsbedenken. Weitere Informationen finden Sie unter [Sichern von WMI-Ereignissen](securing-wmi-events.md).

 

Weitere Informationen zum Empfangen von asynchronen und semisynchronen Ereignis Benachrichtigungen finden Sie unter [empfangen von asynchronen Ereignis](receiving-asynchronous-event-notifications.md) Benachrichtigungen und [empfangen von semisynchronen Ereignis Benachrichtigungen](receiving-synchronous-and-semisynchronous-event-notifications.md).

 

 



