---
title: Zugreifen auf und Steuern von DWM-Frame Daten
description: In diesem Thema werden die Desktopfenster-Manager-APIs (DWM) erläutert, die für die Planung und die Medienpräsentation verwendet werden.
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- Desktopfenster-Manager (DWM), Planung und Media Presentation-APIs
- Dwm (Desktopfenster-Manager), Planung und Media Presentation-APIs
- Planen und Media Presentation-APIs
- Desktopfenster-Manager (DWM), zugreifen auf Frame Daten
- Dwm (Desktopfenster-Manager), zugreifen auf Frame Daten
- Zugreifen auf Frame Daten
- Desktopfenster-Manager (DWM), Steuern von Frame-Daten
- Dwm (Desktopfenster-Manager), Steuern von Frame-Daten
- Steuern von Frame-Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a577847dc20883c84af680d1c39e285a6085e70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310180"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a><span data-ttu-id="78e36-112">Zugreifen auf und Steuern von DWM-Frame Daten</span><span class="sxs-lookup"><span data-stu-id="78e36-112">Accessing and Controlling DWM Frame Data</span></span>

<span data-ttu-id="78e36-113">In diesem Thema werden die Desktopfenster-Manager-APIs (DWM) erläutert, die für die Planung und die Medienpräsentation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78e36-113">This topic discusses the Desktop Window Manager (DWM) APIs that are used for scheduling and media presentation.</span></span>

## <a name="dwm-frame-timing-api"></a><span data-ttu-id="78e36-114">DWM-Frame-API</span><span class="sxs-lookup"><span data-stu-id="78e36-114">DWM Frame Timing API</span></span>

<span data-ttu-id="78e36-115">Die APIs für die Planung und die Medienpräsentation ermöglichen eine genauere Steuerung, wann das Desktop Image zusammengesetzt und dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="78e36-115">The scheduling and media presentation APIs enable more detailed control of when the desktop image is composited and presented.</span></span> <span data-ttu-id="78e36-116">Dies wird in der Regel von Medien-und Videowiedergabe Anwendungen benötigt, für die der DWM-Dienst asynchron mit einem eigenen Präsentations Zeitplan ausgeführt wird. Dies kann zu Stichproben Artefakten führen, wenn diese nicht streng gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="78e36-116">This is typically needed by media and video playback applications for whom the DWM is running asynchronously with their own presentation schedule, which can lead to sampling artifacts if not tightly controlled.</span></span>

<span data-ttu-id="78e36-117">Die Funktionen für Planung und Medienpräsentation umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="78e36-117">The scheduling and media presentation functions include the following.</span></span> <span data-ttu-id="78e36-118">Details zu deren Verwendung finden Sie auf diesen Seiten.</span><span class="sxs-lookup"><span data-stu-id="78e36-118">Details of their use are found on those pages.</span></span>

-   <span data-ttu-id="78e36-119">[**Dwmenablemmcss**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss).</span><span class="sxs-lookup"><span data-stu-id="78e36-119">[**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss).</span></span> <span data-ttu-id="78e36-120">Benachrichtigt den DWM-Dienst, die MMCSS-Zeitplanung (Multimedia Class Schedule Service) zu aktivieren, während der Aufrufprozess aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="78e36-120">Notifies the DWM to enable Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span>
-   <span data-ttu-id="78e36-121">[**Dwmgetcompositiontiminginfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo).</span><span class="sxs-lookup"><span data-stu-id="78e36-121">[**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo).</span></span> <span data-ttu-id="78e36-122">Ruft die aktuellen Informationen zur Kompositions Zeit ab.</span><span class="sxs-lookup"><span data-stu-id="78e36-122">Retrieves the current composition timing information.</span></span>
-   <span data-ttu-id="78e36-123">[**Dwmmodifypreviousdxframeduration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration).</span><span class="sxs-lookup"><span data-stu-id="78e36-123">[**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration).</span></span> <span data-ttu-id="78e36-124">Ändert die Anzahl der Aktualisierungen, während der der vorherige Frame angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="78e36-124">Changes the number of refreshes during which the previous frame will be displayed.</span></span>
-   <span data-ttu-id="78e36-125">[**Dwmsetdxframeduration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration).</span><span class="sxs-lookup"><span data-stu-id="78e36-125">[**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration).</span></span> <span data-ttu-id="78e36-126">Legt die Anzahl der Aktualisierungen fest, in denen der dargestellte Frame angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="78e36-126">Sets the number of refreshes in which to display the presented frame.</span></span>
-   <span data-ttu-id="78e36-127">[**Dwmsetpresentparameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters).</span><span class="sxs-lookup"><span data-stu-id="78e36-127">[**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters).</span></span> <span data-ttu-id="78e36-128">Legt die aktuellen Parameter für die Frame Komposition fest.</span><span class="sxs-lookup"><span data-stu-id="78e36-128">Sets the present parameters for frame composition.</span></span>

 

 




