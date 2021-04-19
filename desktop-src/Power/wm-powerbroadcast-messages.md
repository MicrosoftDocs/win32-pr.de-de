---
description: Das System überträgt immer dann eine Nachricht an alle Anwendungen und installierbaren Treiber, wenn ein Energie Verwaltungs Ereignis auftritt.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: WM_POWERBROADCAST Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f70c5848ec5d71666c26fcd4b5b161e31465543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348010"
---
# <a name="wm_powerbroadcast-messages"></a><span data-ttu-id="e8401-103">WM- \_ powerbroadcast-Meldungen</span><span class="sxs-lookup"><span data-stu-id="e8401-103">WM\_POWERBROADCAST Messages</span></span>

<span data-ttu-id="e8401-104">Das System überträgt immer dann eine Nachricht an alle Anwendungen und installierbaren Treiber, wenn ein Energie Verwaltungs Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="e8401-104">The system broadcasts a message to all applications and installable drivers whenever a power management event occurs.</span></span> <span data-ttu-id="e8401-105">Das System überträgt diese Ereignisse über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht, wobei der *wParam* -Parameter auf das entsprechende Energie Verwaltungs Ereignis festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e8401-105">The system broadcasts these events through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message, setting the *wParam* parameter to the appropriate power management event.</span></span> <span data-ttu-id="e8401-106">Beispielsweise zeigt das [PBT \_ apmpowerstatuschange](pbt-apmpowerstatuschange.md) -Ereignis eine Änderung des System Energiestatus an.</span><span class="sxs-lookup"><span data-stu-id="e8401-106">For example, the [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) event indicates a system power status change.</span></span> <span data-ttu-id="e8401-107">Sie müssen sicherstellen, dass Ihre Anwendung ordnungsgemäß auf die **WM- \_ powerbroadcast** -Nachricht antwortet.</span><span class="sxs-lookup"><span data-stu-id="e8401-107">You must ensure that your application responds properly to the **WM\_POWERBROADCAST** message.</span></span>

<span data-ttu-id="e8401-108">Das System überträgt ein [PBT \_ apmsuspend](pbt-apmsuspend.md) -Ereignis unmittelbar vor dem Anhalten des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e8401-108">The system broadcasts a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event immediately before suspending operation.</span></span> <span data-ttu-id="e8401-109">Dadurch haben Anwendungen und Treiber eine letzte Chance, das Ereignis vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="e8401-109">This gives applications and drivers one last chance to prepare for the event.</span></span> <span data-ttu-id="e8401-110">In vielen Fällen überträgt das System diese Nachrichten, ohne dafür die entsprechende Berechtigung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="e8401-110">In many cases, the system broadcasts these messages without requesting permission to do so.</span></span> <span data-ttu-id="e8401-111">Dies ist z. b. der Fall, wenn eine Anwendung die Unterbrechung mit der [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) -Funktion erzwingt.</span><span class="sxs-lookup"><span data-stu-id="e8401-111">This happens, for example, if an application forces suspension with the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

<span data-ttu-id="e8401-112">Das System überträgt das [PBT \_ apmresumesuspend](pbt-apmresumesuspend.md) -oder [PBT \_ apmresumecritical](pbt-apmresumecritical.md) -Ereignis, wenn der System Vorgang wieder hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e8401-112">The system broadcasts the [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) or [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event when system operation has been restored.</span></span> <span data-ttu-id="e8401-113">Wenn eine Anwendung ein [PBT \_ apmsuspend](pbt-apmsuspend.md) -Ereignis empfangen hat, bevor der Computer angehalten wurde, wird das PBT \_ apmresumesuspend-Ereignis empfangen.</span><span class="sxs-lookup"><span data-stu-id="e8401-113">If an application received a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended, it will receive the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="e8401-114">Andernfalls wird das PBT \_ apmresumecritical-Ereignis empfangen.</span><span class="sxs-lookup"><span data-stu-id="e8401-114">Otherwise, it will receive the PBT\_APMRESUMECRITICAL event.</span></span>

<span data-ttu-id="e8401-115">Das System sendet ein [PBT- \_ powersettingchange](pbt-powersettingchange.md) -Ereignis an Anwendungen, die mithilfe von [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification)für das jeweilige Ereignis registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="e8401-115">The system sends a [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) event to applications that have registered for the specific event using [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification).</span></span> <span data-ttu-id="e8401-116">Weitere Informationen finden Sie unter [registrieren für Power Events](registering-for-power-events.md).</span><span class="sxs-lookup"><span data-stu-id="e8401-116">For more information, see [Registering for Power Events](registering-for-power-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8401-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e8401-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8401-118">Informationen zur Energie Verwaltung</span><span class="sxs-lookup"><span data-stu-id="e8401-118">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



