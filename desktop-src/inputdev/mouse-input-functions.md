---
title: 'Mauseingabefunktionen '
description: .
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47437458cc8ad2bf85ecfa0d8676af8d26c67b89
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734976"
---
# <a name="mouse-input-functions"></a><span data-ttu-id="f80dc-103">Mauseingabefunktionen </span><span class="sxs-lookup"><span data-stu-id="f80dc-103">Mouse Input Functions</span></span>


## <a name="in-this-section"></a><span data-ttu-id="f80dc-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f80dc-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f80dc-105">Thema</span><span class="sxs-lookup"><span data-stu-id="f80dc-105">Topic</span></span></th>
<th><span data-ttu-id="f80dc-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f80dc-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f80dc-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80dc-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="f80dc-108">Sendet Nachrichten, wenn der Mauszeiger ein Fenster verlässt oder für einen bestimmten Zeitraum auf ein Fenster zeigt.</span><span class="sxs-lookup"><span data-stu-id="f80dc-108">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span> <span data-ttu-id="f80dc-109">Diese Funktion ruft <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>trackmougevent</strong></a> auf, wenn Sie vorhanden ist, andernfalls emuliert sie.</span><span class="sxs-lookup"><span data-stu-id="f80dc-109">This function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise it emulates it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80dc-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>Dragdetect</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80dc-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span></span><br/></td>
<td><span data-ttu-id="f80dc-111">Erfasst die Maus und zeichnet ihre Bewegung auf, bis der Benutzer die linke Maustaste loslässt, die ESC-Taste drückt oder die Maus so bewegt, dass sie sich außerhalb des Ziehrechtecks um den angegebenen Punkt herum befindet.</span><span class="sxs-lookup"><span data-stu-id="f80dc-111">Captures the mouse and tracks its movement until the user releases the left button, presses the ESC key, or moves the mouse outside the drag rectangle around the specified point.</span></span> <span data-ttu-id="f80dc-112">Die Breite und Höhe des Zieh Rechtecks werden durch die <strong>SM_CXDRAG</strong> -und <strong>SM_CYDRAG</strong> Werte angegeben, die von der <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f80dc-112">The width and height of the drag rectangle are specified by the <strong>SM_CXDRAG</strong> and <strong>SM_CYDRAG</strong> values returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80dc-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80dc-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="f80dc-114">Ruft ein Handle für das Fenster (sofern vorhanden) ab, das die Maus erfasst hat.</span><span class="sxs-lookup"><span data-stu-id="f80dc-114">Retrieves a handle to the window (if any) that has captured the mouse.</span></span> <span data-ttu-id="f80dc-115">Die Maus kann nur von einem Fenster erfasst werden. Dieses Fenster empfängt Maus Eingaben, unabhängig davon, ob sich der Cursor innerhalb seines Rahmens befindet.</span><span class="sxs-lookup"><span data-stu-id="f80dc-115">Only one window at a time can capture the mouse; this window receives mouse input whether or not the cursor is within its borders.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80dc-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>Getdoubleclicktime</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80dc-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="f80dc-117">Ruft die aktuelle Doppelklick Zeit für die Maus ab.</span><span class="sxs-lookup"><span data-stu-id="f80dc-117">Retrieves the current double-click time for the mouse.</span></span> <span data-ttu-id="f80dc-118">Ein Doppelklick ist eine Reihe von zwei Klicks der Maustaste, die zweite innerhalb eines angegebenen Zeitraums nach dem ersten.</span><span class="sxs-lookup"><span data-stu-id="f80dc-118">A double-click is a series of two clicks of the mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="f80dc-119">Bei der Doppelklick Zeit handelt es sich um die maximale Anzahl von Millisekunden, die zwischen dem ersten und zweiten Klick auf einen Doppelklick auftreten können.</span><span class="sxs-lookup"><span data-stu-id="f80dc-119">The double-click time is the maximum number of milliseconds that may occur between the first and second click of a double-click.</span></span> <span data-ttu-id="f80dc-120">Die maximale Doppelklick Zeit beträgt 5000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="f80dc-120">The maximum double-click time is 5000 milliseconds.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80dc-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>Getmoucmuvepointsex</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80dc-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="f80dc-122">Ruft einen Verlauf von bis zu 64 vorherigen Koordinaten der Maus oder des Stifts ab.</span><span class="sxs-lookup"><span data-stu-id="f80dc-122">Retrieves a history of up to 64 previous coordinates of the mouse or pen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80dc-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80dc-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span></span><br/></td>
<td><span data-ttu-id="f80dc-124">Die <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> -Funktion synthetisiert die Mausbewegung und Schaltflächen Klicks.</span><span class="sxs-lookup"><span data-stu-id="f80dc-124">The <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> function synthesizes mouse motion and button clicks.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f80dc-125">Diese Funktion wurde abgelöst.</span><span class="sxs-lookup"><span data-stu-id="f80dc-125">This function has been superseded.</span></span> <span data-ttu-id="f80dc-126">Verwenden Sie stattdessen <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f80dc-126">Use <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80dc-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>Releasecapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80dc-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="f80dc-128">Gibt die Maus Aufzeichnung von einem Fenster im aktuellen Thread frei und stellt die normale Verarbeitung der Maus Eingaben wieder her.</span><span class="sxs-lookup"><span data-stu-id="f80dc-128">Releases the mouse capture from a window in the current thread and restores normal mouse input processing.</span></span> <span data-ttu-id="f80dc-129">Ein Fenster, das die Maus erfasst hat, erhält unabhängig von der Position des Cursors alle Maus Eingaben, außer wenn auf eine Maustaste geklickt wird, während sich der Cursor-Hotspot im Fenster eines anderen Threads befindet.</span><span class="sxs-lookup"><span data-stu-id="f80dc-129">A window that has captured the mouse receives all mouse input, regardless of the position of the cursor, except when a mouse button is clicked while the cursor hot spot is in the window of another thread.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80dc-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80dc-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="f80dc-131">Legt die Maus Aufzeichnung auf das angegebene Fenster fest, das zum aktuellen Thread gehört.</span><span class="sxs-lookup"><span data-stu-id="f80dc-131">Sets the mouse capture to the specified window belonging to the current thread.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80dc-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>Setdoubleclicktime</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80dc-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="f80dc-133">Legt die Doppelklick Zeit für die Maus fest.</span><span class="sxs-lookup"><span data-stu-id="f80dc-133">Sets the double-click time for the mouse.</span></span> <span data-ttu-id="f80dc-134">Ein Doppelklick ist eine Reihe von zwei Mausklicks, die jeweils innerhalb eines angegebenen Zeitraums nach dem ersten auftreten.</span><span class="sxs-lookup"><span data-stu-id="f80dc-134">A double-click is a series of two clicks of a mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="f80dc-135">Der Doppelklick Zeitraum ist die maximale Anzahl von Millisekunden, die zwischen dem ersten und dem zweiten Mausklick eines Doppelklicks auftreten können.</span><span class="sxs-lookup"><span data-stu-id="f80dc-135">The double-click time is the maximum number of milliseconds that may occur between the first and second clicks of a double-click.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80dc-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>Austausch Schaltfläche</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80dc-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span></span><br/></td>
<td><span data-ttu-id="f80dc-137">Kehrt die Bedeutung der linken und rechten Maustaste um und stellt diese wieder her.</span><span class="sxs-lookup"><span data-stu-id="f80dc-137">Reverses or restores the meaning of the left and right mouse buttons.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80dc-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80dc-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="f80dc-139">Sendet Nachrichten, wenn der Mauszeiger ein Fenster verlässt oder für einen bestimmten Zeitraum auf ein Fenster zeigt.</span><span class="sxs-lookup"><span data-stu-id="f80dc-139">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f80dc-140">Die <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> -Funktion ruft <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>trackmouserevent</strong></a> auf, wenn Sie vorhanden ist, andernfalls emuliert <strong>_TrackMouseEvent</strong> <strong>trackmousevent</strong>.</span><span class="sxs-lookup"><span data-stu-id="f80dc-140">The <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise <strong>_TrackMouseEvent</strong> emulates <strong>TrackMouseEvent</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

