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
# <a name="device-notifications"></a><span data-ttu-id="8cda1-103">Geräte Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="8cda1-103">Device Notifications</span></span>

<span data-ttu-id="8cda1-104">Das System überträgt eine Reihe von standardmäßigen Geräte Änderungs Ereignissen an alle Anwendungen und Dienste.</span><span class="sxs-lookup"><span data-stu-id="8cda1-104">The system broadcasts a set of default device change events to all applications and services.</span></span> <span data-ttu-id="8cda1-105">Sie müssen sich nicht registrieren, um diese Standard Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="8cda1-105">You do not need to register to receive these default events.</span></span> <span data-ttu-id="8cda1-106">Weitere Informationen finden Sie im Abschnitt "Hinweise" unter [**registerdevicenotifi.**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)</span><span class="sxs-lookup"><span data-stu-id="8cda1-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details.</span></span> <span data-ttu-id="8cda1-107">Verwenden Sie die **registerdevicenotifi-** Funktion, um andere Ereignisse anzugeben, die Ihre Anwendung oder Ihr Dienst empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="8cda1-107">To specify other events your application or service should receive, use the **RegisterDeviceNotification** function.</span></span>

<span data-ttu-id="8cda1-108">Wenn eine Anwendung oder ein Dienst [**registerdevicenotifiruft**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), wird auch das Fenster angegeben, in dem die Benachrichtigungs Ereignisse empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="8cda1-108">When an application or service calls [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), it also specifies the window that will receive the notification events.</span></span> <span data-ttu-id="8cda1-109">Dienste können ein Dienststatus handle anstelle eines Fenster Handles angeben.</span><span class="sxs-lookup"><span data-stu-id="8cda1-109">Services can specify a service status handle instead of a window handle.</span></span> <span data-ttu-id="8cda1-110">Wenn ein Dienst sein Dienststatus Handle angibt, empfängt der Dienst Steuerungs Handler die Benachrichtigungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="8cda1-110">If a service specifies its service status handle, its service control handler will receive the notification events.</span></span> <span data-ttu-id="8cda1-111">Weitere Informationen finden Sie unter [**handlerex**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span><span class="sxs-lookup"><span data-stu-id="8cda1-111">For more information, see [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="8cda1-112">Stellen Sie sicher, dass Plug & Play Geräte Ereignisse so schnell wie möglich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="8cda1-112">Be sure to handle Plug and Play device events as quickly as possible.</span></span> <span data-ttu-id="8cda1-113">Andernfalls reagiert das System möglicherweise nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="8cda1-113">Otherwise, the system may become unresponsive.</span></span> <span data-ttu-id="8cda1-114">Wenn der Ereignishandler einen Vorgang ausführen kann, der die Ausführung blockieren kann (z. b. e/a), empfiehlt es sich, einen weiteren Thread zu starten, um den Vorgang asynchron auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8cda1-114">If your event handler is to perform an operation that may block execution (such as I/O), it is best to start another thread to perform the operation asynchronously.</span></span>

<span data-ttu-id="8cda1-115">Die von [**registerdevicenotifizurück**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) gegebenen Geräte Benachrichtigungs Handles müssen geschlossen werden, indem die [**unregisterdevicenotifi-**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) Funktion aufgerufen wird, wenn Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="8cda1-115">Device notification handles returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) must be closed by calling the [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) function when they are no longer needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cda1-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8cda1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cda1-117">Registrierung für Gerätebenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="8cda1-117">Registering for device notification</span></span>](registering-for-device-notification.md)
</dt> </dl>

 

 
