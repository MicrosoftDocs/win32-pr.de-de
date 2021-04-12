---
title: Anpassen von Geschwindigkeit, Volume und Zoom
description: Anpassen von Geschwindigkeit, Volume und Zoom
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- Mciwndsetspeed-Makro
- Mciwndgetspeed-Makro
- Mciwndsetvolume-Makro
- Mciwndgetvolume-Makro
- Mciwndsetzoom-Makro
- Mciwndgetzoom-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02b1e14a5153e279e3cfdf6989beade31cf6f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388350"
---
# <a name="adjusting-speed-volume-and-zoom"></a><span data-ttu-id="12532-109">Anpassen von Geschwindigkeit, Volume und Zoom</span><span class="sxs-lookup"><span data-stu-id="12532-109">Adjusting Speed, Volume, and Zoom</span></span>

<span data-ttu-id="12532-110">Die Makros "Geschwindigkeit", "Volume" und "Zoom" stellen die Funktionalität der Befehle " **View**", " **Volume**" und " **Speed** " im mciwnd-Menü bereit.</span><span class="sxs-lookup"><span data-stu-id="12532-110">The speed, volume, and zoom macros provide the functionality of the **View**, **Volume**, and **Speed** commands on the MCIWnd menu.</span></span> <span data-ttu-id="12532-111">Die in diesem Abschnitt beschriebenen Makros werden im Allgemeinen mit Videos und anderen Geräten verwendet, die während der Wiedergabe Bilder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="12532-111">The macros described in this section are generally used with video and other devices that display images during playback.</span></span>

<span data-ttu-id="12532-112">Einige Geräte unterstützen mehrere Wiedergabe Geschwindigkeitsänderungen.</span><span class="sxs-lookup"><span data-stu-id="12532-112">Some devices support multiple playback speed changes.</span></span> <span data-ttu-id="12532-113">Sie können die Wiedergabegeschwindigkeit für diese Geräte mit dem [**mciwndsetspeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) -Makro festlegen.</span><span class="sxs-lookup"><span data-stu-id="12532-113">You can set the playback speed for these devices by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span> <span data-ttu-id="12532-114">Dieses Makro definiert die Wiedergabegeschwindigkeit als 1000.</span><span class="sxs-lookup"><span data-stu-id="12532-114">This macro defines the playback speed as 1000.</span></span> <span data-ttu-id="12532-115">Höhere Werte weisen auf schnellere Geschwindigkeiten hin.</span><span class="sxs-lookup"><span data-stu-id="12532-115">Higher values indicate faster speeds.</span></span> <span data-ttu-id="12532-116">Niedrigere Werte weisen auf eine langsamere Geschwindigkeit hin.</span><span class="sxs-lookup"><span data-stu-id="12532-116">Lower values indicate slower speeds.</span></span>

<span data-ttu-id="12532-117">Sie können die aktuelle Wiedergabegeschwindigkeit abrufen, indem Sie das [**mciwndgetspeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="12532-117">You can retrieve the current playback speed by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span> <span data-ttu-id="12532-118">Dieses Makro verwendet dieselben Werte und denselben Bereich wie die von **mciwndsetspeed** verwendeten Werte.</span><span class="sxs-lookup"><span data-stu-id="12532-118">This macro uses the same values and range as those used by **MCIWndSetSpeed**.</span></span>

<span data-ttu-id="12532-119">Einige Geräte unterstützen volumeänderungen.</span><span class="sxs-lookup"><span data-stu-id="12532-119">Some devices support volume changes.</span></span> <span data-ttu-id="12532-120">Sie können das Volume anpassen oder festlegen, indem Sie das [**mciwndsetvolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="12532-120">You can adjust or set the volume by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span> <span data-ttu-id="12532-121">Dieses Makro definiert die normale Volumeebene als 1000.</span><span class="sxs-lookup"><span data-stu-id="12532-121">This macro defines the normal volume level as 1000.</span></span> <span data-ttu-id="12532-122">Höhere Werte weisen auf lauter Volumes hin.</span><span class="sxs-lookup"><span data-stu-id="12532-122">Higher values indicate louder volumes.</span></span> <span data-ttu-id="12532-123">Niedrigere Werte weisen auf ruhigere Volumes hin.</span><span class="sxs-lookup"><span data-stu-id="12532-123">Lower values indicate quieter volumes.</span></span>

<span data-ttu-id="12532-124">Sie können die aktuelle Volumeebene abrufen, indem Sie das [**mciwndgetvolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="12532-124">You can retrieve the current volume level by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span> <span data-ttu-id="12532-125">Dieses Makro verwendet dieselben numerischen Werte und denselben Bereich wie die von **mciwndsetvolume** verwendeten Werte.</span><span class="sxs-lookup"><span data-stu-id="12532-125">This macro uses the same numerical values and range as those used by **MCIWndSetVolume**.</span></span>

<span data-ttu-id="12532-126">Bei Geräten, die ein Wiedergabe Fenster verwenden, unterstützt mciwnd eine Zoomfunktion, mit der die Größe des Wiedergabe Bilds festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="12532-126">For devices that use a playback window, MCIWnd supports a zoom feature that sets the size of the playback image.</span></span> <span data-ttu-id="12532-127">Sie können die Wiedergabe Bildgröße mit dem [**mciwndsetzoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) -Makro festlegen.</span><span class="sxs-lookup"><span data-stu-id="12532-127">You can set the playback image size by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span> <span data-ttu-id="12532-128">Das Makro definiert die Wiedergabe Bildgröße neu, während gleichzeitig ein konstantes Seitenverhältnis für das Bild beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="12532-128">The macro redefines the playback image size while maintaining a constant aspect ratio for the image.</span></span> <span data-ttu-id="12532-129">Der Zoomwert wird als Prozentsatz der ursprünglichen Bildgröße definiert.</span><span class="sxs-lookup"><span data-stu-id="12532-129">The zoom value is defined as a percentage of the original image size.</span></span> <span data-ttu-id="12532-130">Daher stellt 100 die ursprüngliche Bildgröße dar, 50 gibt an, dass das angezeigte Bild eine halbe Originalgröße hat, und 200, dass das angezeigte Bild doppelt so groß wie die ursprüngliche Größe ist.</span><span class="sxs-lookup"><span data-stu-id="12532-130">Thus, 100 represents the original image size, 50 indicates the image shown is half its original size, and 200 indicates that the image shown is twice its original size.</span></span>

<span data-ttu-id="12532-131">Sie können den aktuellen Zoomwert abrufen, indem Sie das [**mciwndgetzoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="12532-131">You can retrieve the current zoom value by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span> <span data-ttu-id="12532-132">Dieses Makro verwendet dieselben Werte und denselben Bereich wie die von **mciwndsetzoom** verwendeten Werte.</span><span class="sxs-lookup"><span data-stu-id="12532-132">This macro uses the same values and range as those used by **MCIWndSetZoom**.</span></span>

> [!Note]  
> <span data-ttu-id="12532-133">Die standardmäßigen MCI-CD-Audiodaten und Waveform-Audiotreiber unterstützen keine Volumen-oder Geschwindigkeitsänderungen.</span><span class="sxs-lookup"><span data-stu-id="12532-133">The standard MCI CD audio and waveform-audio drivers do not support volume or speed changes.</span></span>

 

 

 




