---
title: Benutzeroberfläche des mciwnd-Fensters
description: Benutzeroberfläche des mciwnd-Fensters
ms.assetid: 422c5acb-bce5-4be2-96ba-5ab7f9dcc826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98c0b11b6868828625c6c6e605f005fe842d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036578"
---
# <a name="mciwnd-window-user-interface"></a><span data-ttu-id="f4844-103">Benutzeroberfläche des mciwnd-Fensters</span><span class="sxs-lookup"><span data-stu-id="f4844-103">MCIWnd Window User Interface</span></span>

<span data-ttu-id="f4844-104">Mciwnd bietet zusätzliche Features zum Anpassen des Erscheinungsbild des mciwnd-Fensters, zum Anpassen des Verhaltens der Anwendung und zum Optimieren der Wiedergabe Leistung.</span><span class="sxs-lookup"><span data-stu-id="f4844-104">MCIWnd provides additional features to adjust the look of the MCIWnd window, customize the behavior of your application, and tune playback performance.</span></span> <span data-ttu-id="f4844-105">Im mciwnd-Fenster sind folgende Features enthalten:</span><span class="sxs-lookup"><span data-stu-id="f4844-105">The following features are included in the MCIWnd window:</span></span>

-   <span data-ttu-id="f4844-106">Eine Symbolleiste **mit** **Menü** Schaltflächen zum wiedergeben, **Abbrechen**, **aufzeichnen**</span><span class="sxs-lookup"><span data-stu-id="f4844-106">A toolbar with **Play**, **Stop**, **Record** and **Menu** buttons</span></span>
-   <span data-ttu-id="f4844-107">Eine TrackBar, die die Positionierung innerhalb des Wiedergabe Inhalts steuert.</span><span class="sxs-lookup"><span data-stu-id="f4844-107">A trackbar that controls positioning within the playback content</span></span>
-   <span data-ttu-id="f4844-108">Ein Popup Menü mit allgemeinen Befehlen</span><span class="sxs-lookup"><span data-stu-id="f4844-108">A pop-up menu containing common commands</span></span>
-   <span data-ttu-id="f4844-109">Ein Wiedergabe Bereich für Videos und andere Geräte, die Bilder anzeigen</span><span class="sxs-lookup"><span data-stu-id="f4844-109">A playback area for video and other devices that display images</span></span>

<span data-ttu-id="f4844-110">In der folgenden Abbildung wird der anfängliche Status der benutzergesteuerten Videowiedergabe dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f4844-110">The following illustration shows the initial state of user-controlled video playback.</span></span> <span data-ttu-id="f4844-111">Die Beispieldatei wird CLOCK.AVI verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4844-111">The sample file used is CLOCK.AVI.</span></span>

![Bild clock.avi](images/mciwnd1.gif)

<span data-ttu-id="f4844-113">Das mciwnd-Fenster enthält einen Wiedergabe Bereich für Videos und andere Geräte, auf denen Bilder während der Wiedergabe angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f4844-113">The MCIWnd window includes a playback area for video and other devices that display images during playback.</span></span> <span data-ttu-id="f4844-114">Mciwnd lässt den Wiedergabe Bereich von Waveform-Audiogeräten, von MIDI-Sequencern und anderen Geräten aus, die nicht in die Anzeige schreiben.</span><span class="sxs-lookup"><span data-stu-id="f4844-114">MCIWnd omits the playback area from waveform-audio devices, MIDI sequencers, and other devices that do not write to the display.</span></span> <span data-ttu-id="f4844-115">In der folgenden Abbildung wird der Wiedergabe Bereich von Waveform-Audiodaten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f4844-115">The following illustration shows the waveform-audio playback area.</span></span>

![Bild des mciwnd-Fensters](images/mciwnd4.gif)

<span data-ttu-id="f4844-117">Die **Wiedergabe** Schaltfläche befindet sich in der unteren linken Ecke des mciwnd-Fensters.</span><span class="sxs-lookup"><span data-stu-id="f4844-117">The **Play** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="f4844-118">Sie wird angezeigt, wenn der Inhalt angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="f4844-118">It appears when the content is stopped.</span></span> <span data-ttu-id="f4844-119">Der Benutzer kann den Inhalt auf folgende Weise wiedergeben:</span><span class="sxs-lookup"><span data-stu-id="f4844-119">The user can play the content in the following ways:</span></span>

-   <span data-ttu-id="f4844-120">Um den Inhalt von der aktuellen Wiedergabe Position wiederzugeben, wählen Sie **die Wiedergabe Schaltfläche aus** .</span><span class="sxs-lookup"><span data-stu-id="f4844-120">To play the content from the current playback position, select the **Play** button.</span></span>
-   <span data-ttu-id="f4844-121">Um den Inhalts Vollbild von der aktuellen Wiedergabe Position wiederzugeben, wählen Sie **die Wiedergabe Schaltfläche aus** , während Sie die STRG-Taste gedrückt halten.</span><span class="sxs-lookup"><span data-stu-id="f4844-121">To play the content full-screen from the current playback position, select the **Play** button while holding down the CTRL key.</span></span>
-   <span data-ttu-id="f4844-122">Um den Inhalt von der aktuellen Wiedergabe Position rückwärts wiederzugeben, wählen Sie **die Wiedergabe Schaltfläche aus** , während Sie die UMSCHALTTASTE gedrückt halten.</span><span class="sxs-lookup"><span data-stu-id="f4844-122">To play the content backward from the current playback position, select the **Play** button while holding down the SHIFT key.</span></span>

<span data-ttu-id="f4844-123">Mit der **Menü** Schaltfläche neben der **Wiedergabe** Schaltfläche wird ein Menü aktiviert, das es dem Benutzer ermöglicht, Audiovideo-überlappende (AVI)-Dateien zu öffnen und zu schließen und die Bildgröße, Wiedergabegeschwindigkeit und das Volume anzupassen.</span><span class="sxs-lookup"><span data-stu-id="f4844-123">The **Menu** button, located next to the **Play** button, activates a menu that allows the user to open and close audio-video interleaved (AVI) files, and to adjust the image size, playback speed, and volume.</span></span> <span data-ttu-id="f4844-124">(Der Benutzer kann das Menü auch aktivieren, indem er immer dann auf die Rechte Maustaste klickt, wenn sich der Cursor im Client Bereich des Fensters befindet.) Das Menü enthält auch Befehle, mit denen Sie die Konfiguration des aktuellen Geräts ändern, den Wiedergabe Inhalt in die Zwischenablage kopieren und MCI-Befehle ausgeben können.</span><span class="sxs-lookup"><span data-stu-id="f4844-124">(The user can also activate the menu by clicking the right mouse button whenever the cursor is in the client area of the window.) The menu also includes commands to change the configuration of the current device, to copy the playback content to the clipboard, and to issue MCI commands.</span></span>

<span data-ttu-id="f4844-125">Die TrackBar rechts neben der **Menü** Schaltfläche stellt die Dauer des Wiedergabe-(oder aufgezeichneten) Inhalts dar.</span><span class="sxs-lookup"><span data-stu-id="f4844-125">The trackbar to the right of the **Menu** button represents the duration of the playback (or recorded) content.</span></span> <span data-ttu-id="f4844-126">Der Schieberegler auf der TrackBar stellt die aktuelle Wiedergabe Position innerhalb des Inhalts dar.</span><span class="sxs-lookup"><span data-stu-id="f4844-126">The slider on the trackbar represents the current playback position within the content.</span></span> <span data-ttu-id="f4844-127">Wenn sich der Schieberegler am linken Ende der Trackleiste befindet, ist die aktuelle Wiedergabe Position der Anfang des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="f4844-127">When the slider is positioned at the left end of the trackbar, the current playback position is the beginning of the content.</span></span> <span data-ttu-id="f4844-128">Der Benutzer kann an verschiedene Positionen im Inhalt wechseln, indem er den Schieberegler entlang der TrackBar zieht.</span><span class="sxs-lookup"><span data-stu-id="f4844-128">The user can move to different locations in the content by dragging the slider along the trackbar.</span></span> <span data-ttu-id="f4844-129">Die Schaltfläche " **Abbrechen** " befindet sich in der unteren linken Ecke des mciwnd-Fensters.</span><span class="sxs-lookup"><span data-stu-id="f4844-129">The **Stop** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="f4844-130">Sie wird angezeigt, wenn der Inhalt wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f4844-130">It appears when the content is played.</span></span> <span data-ttu-id="f4844-131">In der folgenden Abbildung wird die Wiedergabe des Videos gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f4844-131">The following illustration shows video playback in progress.</span></span>

![Videowiedergabe Bild](images/mciwnd2.gif)

<span data-ttu-id="f4844-133">Die mciwnd-Steuerelemente können auch eine **Datensatz** -Schaltfläche für Geräte enthalten, die aufzeichnen können.</span><span class="sxs-lookup"><span data-stu-id="f4844-133">The MCIWnd controls can also include a **Record** button for devices that can record.</span></span> <span data-ttu-id="f4844-134">Die Schaltfläche **Datensatz** ist mit einem roten Kreis gekennzeichnet und wird nur angezeigt, wenn das Gerät aufgezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4844-134">The **Record** button is marked with a red circle and appears only when the device is capable of recording.</span></span>

> [!Note]  
> <span data-ttu-id="f4844-135">Das Wiedergabe Fenster muss an einer Grenze von vier Pixeln ausgerichtet werden, um die beste Videowiedergabe Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="f4844-135">The playback window must be aligned on a four-pixel boundary for the best video playback performance.</span></span> <span data-ttu-id="f4844-136">In der Regel richtet Windows das Fenster automatisch aus, wenn es erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f4844-136">Typically, Windows aligns the window automatically when it is created.</span></span> <span data-ttu-id="f4844-137">Wenn ein Benutzer das Fenster von seiner ursprünglichen Position aus bewegt oder verschiebt, wird die Videowiedergabegeschwindigkeit möglicherweise um die Hälfte reduziert.</span><span class="sxs-lookup"><span data-stu-id="f4844-137">If a user moves or stretches the window from its initial position, video playback speed might be reduced by half.</span></span>

 

 

 




