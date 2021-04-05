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
# <a name="receiving-events-for-the-duration-of-your-application"></a><span data-ttu-id="a0369-103">Empfangen von Ereignissen für die Dauer der Anwendung</span><span class="sxs-lookup"><span data-stu-id="a0369-103">Receiving Events for the Duration of Your Application</span></span>

<span data-ttu-id="a0369-104">Eine der gängigsten Methoden zum Empfangen eines Ereignisses ist eine ausgelaufende Anwendung, z. b. eine Verwaltungs Anwendung, die Ereignisse sammelt und an einen Benutzer anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a0369-104">One of the most common ways to receive an event is through a running application, such as a management application that collects and displays events to a user.</span></span> <span data-ttu-id="a0369-105">Solche Anwendungen werden als "temporär" bezeichnet, da ein temporärer Consumer beim Herunterfahren keine Ereignis Benachrichtigungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="a0369-105">Such applications are called "temporary" because a temporary consumer does not receive event notifications when shut down.</span></span>

<span data-ttu-id="a0369-106">Ein temporärer Consumer ruft [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) im Skript oder [**IWbemServices.Execnotificationquery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ auf, um Ereignisse in einem Namespace zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="a0369-106">A temporary consumer calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in script or [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ to subscribe to events in a namespace.</span></span> <span data-ttu-id="a0369-107">Die diesem Abonnement zugeordnete Identität ist der Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="a0369-107">The identity associated with this subscription is the caller.</span></span>

<span data-ttu-id="a0369-108">Ein temporärer Ereignisconsumer kann Benachrichtigungen entweder asynchron oder SemiSynchron in Skripts und C++ empfangen.</span><span class="sxs-lookup"><span data-stu-id="a0369-108">A temporary event consumer can receive notifications either asynchronously or semisynchronously in both scripts and C++.</span></span>

> [!Note]  
> <span data-ttu-id="a0369-109">Aus Sicherheitsgründen ist es wichtig zu beachten, dass asynchrone Ereignis Benachrichtigungen nicht empfohlen werden.</span><span class="sxs-lookup"><span data-stu-id="a0369-109">For security reasons, it is important to note that asynchronous event notifications are not recommended.</span></span> <span data-ttu-id="a0369-110">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="a0369-110">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span> <span data-ttu-id="a0369-111">Ereignisconsumer haben besondere Sicherheitsbedenken.</span><span class="sxs-lookup"><span data-stu-id="a0369-111">Event consumers have special security concerns.</span></span> <span data-ttu-id="a0369-112">Weitere Informationen finden Sie unter [Sichern von WMI-Ereignissen](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="a0369-112">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

 

<span data-ttu-id="a0369-113">Weitere Informationen zum Empfangen von asynchronen und semisynchronen Ereignis Benachrichtigungen finden Sie unter [empfangen von asynchronen Ereignis](receiving-asynchronous-event-notifications.md) Benachrichtigungen und [empfangen von semisynchronen Ereignis Benachrichtigungen](receiving-synchronous-and-semisynchronous-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="a0369-113">For more information about receiving asynchronous and semisynchronous event notifications, see [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md) and [Receiving Semisynchronous Event Notifications](receiving-synchronous-and-semisynchronous-event-notifications.md).</span></span>

 

 



