---
title: Bereitstellen von Status Aktualisierungen
description: Bereitstellen von Status Aktualisierungen
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- Mciwndabtactivetimer-Makro
- Mciwndabtinactivetimer-Makro
- Mciwndgetactivetimer-Makro
- Mciwndgetinactivetimer-Makro
- Mciwndsettimers-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd53c9580f3ae9be09817979178d10e60765ea3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388230"
---
# <a name="providing-status-updates"></a><span data-ttu-id="7bdfc-108">Bereitstellen von Status Aktualisierungen</span><span class="sxs-lookup"><span data-stu-id="7bdfc-108">Providing Status Updates</span></span>

<span data-ttu-id="7bdfc-109">Mciwnd verwendet Timer, um in regelmäßigen Abständen Informationen in der Fenstertitelleiste und der Scrollleiste zu aktualisieren und Benachrichtigungs Meldungen an das übergeordnete Fenster zu senden.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-109">MCIWnd uses timers to periodically update information in the window title bar and scroll bar, and to send notification messages to the parent window.</span></span> <span data-ttu-id="7bdfc-110">Ein Timer steuert den Aktualisierungs Zeitraum des aktiven mciwnd-Fensters, und ein zweiter Timer steuert den Update Zeitraum für inaktive mciwnd-Fenster.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-110">One timer controls the update period of the active MCIWnd window, and a second timer controls the update period for MCIWnd windows that are inactive.</span></span> <span data-ttu-id="7bdfc-111">Die Anwendung kann die mciwnd-Timer-Makros verwenden, um die aktuellen Zeit Geber Einstellungen abzurufen und die Aktualisierungs Zeiträume anzupassen.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-111">Your application can use the MCIWnd timer macros to retrieve the current timer settings and to adjust the update periods.</span></span>

<span data-ttu-id="7bdfc-112">Sie können den Update Zeitraum festlegen, der vom aktiven Zeit Geber verwendet wird, indem Sie das Makro [**mciwndsetactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) verwenden.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-112">You can set the update period used by the active window timer by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span> <span data-ttu-id="7bdfc-113">Dieses Makro legt den Zeitraum fest, der von mciwnd zum Aktualisieren der Trackleiste verwendet wird, um die in der Fenstertitelleiste gemeldete Wiedergabe Position zu aktualisieren und um das übergeordnete Fenster zu benachrichtigen, dass sich das Medium geändert hat.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-113">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window title bar, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="7bdfc-114">Sie können den aktuellen Aktualisierungs Zeitraum, der vom aktiven Fenster Timer verwendet wird, mit dem [**mciwndgetactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) -Makro abrufen.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-114">You can retrieve the current update period used by the active window timer by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span> <span data-ttu-id="7bdfc-115">Der Standard Update Zeitraum für den aktiven Zeit Geber beträgt 500 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-115">The default update period for the active window timer is 500 milliseconds.</span></span>

<span data-ttu-id="7bdfc-116">Sie können den Update Zeitraum festlegen, der vom inaktiven Fenster Timer verwendet wird, indem Sie das [**mciwndsetinactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-116">You can set the update period used by the inactive window timer by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span> <span data-ttu-id="7bdfc-117">Dieses Makro legt den Zeitraum fest, der von mciwnd zum Aktualisieren der Trackleiste verwendet wird, um die in der Fenster Beschriftung gemeldete Wiedergabe Position zu aktualisieren, und um das übergeordnete Fenster darüber zu benachrichtigen, dass sich das Medium geändert hat.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-117">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window caption, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="7bdfc-118">Sie können den aktuellen Aktualisierungs Zeitraum, der vom inaktiven Fenster Timer verwendet wird, mithilfe des [**mciwndgetinactivetimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) -Makros abrufen.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-118">You can retrieve the current update period used by the inactive window timer by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span> <span data-ttu-id="7bdfc-119">Der Standard Update Zeitraum für den Timer des inaktiven Fensters beträgt 2000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-119">The default update period for the inactive window timer is 2000 milliseconds.</span></span>

<span data-ttu-id="7bdfc-120">Die Anwendung kann den Update Zeitraum für beide Timer gleichzeitig mit dem [**mciwndsettimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) -Makro festlegen.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-120">Your application can simultaneously set the update period for both timers by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span> <span data-ttu-id="7bdfc-121">Der Speicher für den Wert des Aktualisierungs Zeitraums ist auf 16 Bits beschränkt.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-121">The storage for the value of the update period is limited to 16 bits.</span></span> <span data-ttu-id="7bdfc-122">Wenn eine größere Menge für einen der beiden Aktualisierungs Zeitraum erforderlich ist, legen Sie die Timer einzeln fest.</span><span class="sxs-lookup"><span data-stu-id="7bdfc-122">If a larger quantity for either update period is needed, set the timers individually.</span></span>

 

 




