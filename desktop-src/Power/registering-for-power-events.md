---
description: Anwendungen können Ihr Verhalten besser an den aktuellen Energiezustand des Computers anpassen, indem Sie sich für Strom Ereignisse registrieren.
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: Registrieren für Strom Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da084592414d1c58ab4ab43dd2b5c35f028552b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216023"
---
# <a name="registering-for-power-events"></a><span data-ttu-id="22968-103">Registrieren für Strom Ereignisse</span><span class="sxs-lookup"><span data-stu-id="22968-103">Registering for Power Events</span></span>

<span data-ttu-id="22968-104">Anwendungen können Ihr Verhalten besser an den aktuellen Energiezustand des Computers anpassen, indem Sie sich für Strom Ereignisse registrieren.</span><span class="sxs-lookup"><span data-stu-id="22968-104">Applications can better adapt their behavior to the current power state of the computer by registering for power events.</span></span> <span data-ttu-id="22968-105">Eine Anwendung sollte für jedes Strom Änderungs Ereignis registriert werden, das sich auf das Verhalten auswirken könnte.</span><span class="sxs-lookup"><span data-stu-id="22968-105">An application should register for each power change event that might impact its behavior.</span></span>

<span data-ttu-id="22968-106">Eine Anwendung oder ein Dienst verwendet die [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) -Funktion, um Benachrichtigungen für Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="22968-106">An application or service uses the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function to register for notifications.</span></span> <span data-ttu-id="22968-107">Wenn die entsprechende Energie Einstellung geändert wird, sendet das System wie folgt Benachrichtigungen:</span><span class="sxs-lookup"><span data-stu-id="22968-107">When the corresponding power setting changes, the system sends notifications as follows:</span></span>

-   <span data-ttu-id="22968-108">Eine Anwendung empfängt eine [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht mit einem *wParam* -Wert von [PBT \_ powersettingchange](pbt-powersettingchange.md) und einem *LPARAM* , der auf eine [**powerbroadcast- \_ Einstellungs**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) Struktur verweist.</span><span class="sxs-lookup"><span data-stu-id="22968-108">An application receives a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message with a *wParam* of [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) and an *lParam* that points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>
-   <span data-ttu-id="22968-109">Ein Dienst empfängt einen Aufruf der [*handlerex*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) -Rückruffunktion, die er durch Aufrufen der [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) -Funktion registriert hat.</span><span class="sxs-lookup"><span data-stu-id="22968-109">A service receives a call to the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) callback function it registered by calling the [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function.</span></span> <span data-ttu-id="22968-110">Der an die *handlerex* -Rückruffunktion gesendete *lpeer ventdata* -Parameter verweist auf eine [**powerbroadcast- \_ Einstellungs**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) Struktur.</span><span class="sxs-lookup"><span data-stu-id="22968-110">The *lpEventData* parameter sent to the *HandlerEx* callback function points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

<span data-ttu-id="22968-111">In der Struktur der [**powerbroadcast- \_ Einstellungen**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) enthält das **Powersetting** -Element die GUID, die die Benachrichtigung identifiziert, und das **Datenmember** enthält den neuen Wert der Energie Einstellung.</span><span class="sxs-lookup"><span data-stu-id="22968-111">In the [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure, the **PowerSetting** member contains the GUID that identifies the notification and the **Data** member contains the new value of the power setting.</span></span>

<span data-ttu-id="22968-112">Eine Liste der Powersetting-GUIDs für Benachrichtigungen, die für-Anwendungen am nützlichsten sind, finden Sie unter [**Power Setting-GUIDs**](power-setting-guids.md).</span><span class="sxs-lookup"><span data-stu-id="22968-112">For a list of power setting GUIDs for notifications that are most useful to applications, see [**Power Setting GUIDs**](power-setting-guids.md).</span></span>

 

 
