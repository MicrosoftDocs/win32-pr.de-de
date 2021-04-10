---
title: Registrieren für Änderungs Benachrichtigung
description: Ein Client kann sich registrieren, um Benachrichtigungen über Änderungen an Routing Informationen zu erhalten, die im Routing Tabellen-Manager gespeichert sind. Diese Anforderung kann nur vorgenommen werden, nachdem ein Client beim Routing Tabellen-Manager registriert wurde.
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3a98062fee73c481c1f47c32fa7eeb5465a112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309843"
---
# <a name="registering-for-change-notification"></a><span data-ttu-id="86141-104">Registrieren für Änderungs Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="86141-104">Registering for Change Notification</span></span>

<span data-ttu-id="86141-105">Ein Client kann sich registrieren, um Benachrichtigungen über Änderungen an Routing Informationen zu erhalten, die im Routing Tabellen-Manager gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="86141-105">A client can register to receive notification of changes to routing information that is stored in the routing table manager.</span></span> <span data-ttu-id="86141-106">Diese Anforderung kann nur vorgenommen werden, nachdem ein Client beim Routing Tabellen-Manager registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="86141-106">This request can only be made after a client has registered with the routing table manager.</span></span>

<span data-ttu-id="86141-107">Um sich für die Änderungs Benachrichtigung zu registrieren, muss ein Client [**rtmregisterforchangenotifizierung**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)aufrufen und die Typen der Änderungen angeben, für die der Client eine Benachrichtigung empfangen muss.</span><span class="sxs-lookup"><span data-stu-id="86141-107">To register for change notification, a client must call [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), specifying the types of changes for which the client must receive notification.</span></span> <span data-ttu-id="86141-108">Wenn der Client über Änderungen an bestimmten Zielen benachrichtigt werden muss, ruft der Client für jedes Ziel einmal [**rtmmarkdestforchangenotifizierung**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) auf.</span><span class="sxs-lookup"><span data-stu-id="86141-108">If the client must be notified of change to specific destinations, the client calls [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) once for each destination.</span></span>

<span data-ttu-id="86141-109">Der Client kann die Änderungs Benachrichtigungen durch Aufrufen von [**rtmderegisterfromchangenotifinicht**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)mehr empfangen.</span><span class="sxs-lookup"><span data-stu-id="86141-109">The client can stop receiving change notifications by calling [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).</span></span>

<span data-ttu-id="86141-110">Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [registrieren für Änderungs Benachrichtigungen](register-for-change-notification.md).</span><span class="sxs-lookup"><span data-stu-id="86141-110">For sample code that shows how to use these functions, see [Register For Change Notification](register-for-change-notification.md).</span></span>

 

 




