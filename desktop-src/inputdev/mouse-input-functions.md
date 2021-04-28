---
title: 'Mauseingabefunktionen '
description: 'Mauseingabefunktionen '
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a952a9ce90284f284b176c608228c0b852f5f4c8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112878"
---
# <a name="mouse-input-functions"></a><span data-ttu-id="d1752-103">Mauseingabefunktionen </span><span class="sxs-lookup"><span data-stu-id="d1752-103">Mouse Input Functions</span></span>


## <a name="in-this-section"></a><span data-ttu-id="d1752-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d1752-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d1752-105">Thema</span><span class="sxs-lookup"><span data-stu-id="d1752-105">Topic</span></span></th>
<th><span data-ttu-id="d1752-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1752-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d1752-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1752-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="d1752-108">Sendet Meldungen, wenn der Mauszeiger ein Fenster verlässt oder für einen bestimmten Zeitraum auf ein Fenster zeigt.</span><span class="sxs-lookup"><span data-stu-id="d1752-108">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span> <span data-ttu-id="d1752-109">Diese Funktion ruft <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> auf, sofern vorhanden, andernfalls emuliert sie es.</span><span class="sxs-lookup"><span data-stu-id="d1752-109">This function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise it emulates it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1752-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1752-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span></span><br/></td>
<td><span data-ttu-id="d1752-111">Erfasst die Maus und zeichnet ihre Bewegung auf, bis der Benutzer die linke Maustaste loslässt, die ESC-Taste drückt oder die Maus so bewegt, dass sie sich außerhalb des Ziehrechtecks um den angegebenen Punkt herum befindet.</span><span class="sxs-lookup"><span data-stu-id="d1752-111">Captures the mouse and tracks its movement until the user releases the left button, presses the ESC key, or moves the mouse outside the drag rectangle around the specified point.</span></span> <span data-ttu-id="d1752-112">Die Breite und Höhe des Ziehrechtecks wird durch die <strong>SM_CXDRAG</strong> und <strong>SM_CYDRAG</strong> Werte angegeben, die von der <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics-Funktion</strong></a> zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d1752-112">The width and height of the drag rectangle are specified by the <strong>SM_CXDRAG</strong> and <strong>SM_CYDRAG</strong> values returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1752-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1752-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="d1752-114">Ruft ein Handle für das Fenster ab (sofern vorhanden), das die Maus erfasst hat.</span><span class="sxs-lookup"><span data-stu-id="d1752-114">Retrieves a handle to the window (if any) that has captured the mouse.</span></span> <span data-ttu-id="d1752-115">Nur jeweils ein Fenster kann die Maus erfassen. Dieses Fenster empfängt Mauseingaben, unabhängig davon, ob sich der Cursor innerhalb seiner Rahmen befindet.</span><span class="sxs-lookup"><span data-stu-id="d1752-115">Only one window at a time can capture the mouse; this window receives mouse input whether or not the cursor is within its borders.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1752-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1752-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="d1752-117">Ruft die aktuelle Doppelklickzeit für die Maus ab.</span><span class="sxs-lookup"><span data-stu-id="d1752-117">Retrieves the current double-click time for the mouse.</span></span> <span data-ttu-id="d1752-118">Bei einem Doppelklick handelt es sich um eine Reihe von zwei Mausklicks, der zweite klickt innerhalb eines angegebenen Zeitraums nach dem ersten Klick.</span><span class="sxs-lookup"><span data-stu-id="d1752-118">A double-click is a series of two clicks of the mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="d1752-119">Die Doppelklickzeit ist die maximale Anzahl von Millisekunden, die zwischen dem ersten und zweiten Klick eines Doppelklicks auftreten können.</span><span class="sxs-lookup"><span data-stu-id="d1752-119">The double-click time is the maximum number of milliseconds that may occur between the first and second click of a double-click.</span></span> <span data-ttu-id="d1752-120">Die maximale Doppelklickzeit beträgt 5.000 Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="d1752-120">The maximum double-click time is 5000 milliseconds.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1752-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1752-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="d1752-122">Ruft einen Verlauf von bis zu 64 vorherigen Koordinaten der Maus oder des Stifts ab.</span><span class="sxs-lookup"><span data-stu-id="d1752-122">Retrieves a history of up to 64 previous coordinates of the mouse or pen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1752-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1752-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span></span><br/></td>
<td><span data-ttu-id="d1752-124">Die <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> Funktion synthetisiert Mausbewegungen und Schaltflächenklicks.</span><span class="sxs-lookup"><span data-stu-id="d1752-124">The <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> function synthesizes mouse motion and button clicks.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d1752-125">Diese Funktion wurde abgelöst.</span><span class="sxs-lookup"><span data-stu-id="d1752-125">This function has been superseded.</span></span> <span data-ttu-id="d1752-126">Verwenden Sie stattdessen <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput.</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1752-126">Use <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1752-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1752-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="d1752-128">Gibt die Mauserfassung aus einem Fenster im aktuellen Thread frei und stellt die normale Verarbeitung der Mauseingabe wieder auf.</span><span class="sxs-lookup"><span data-stu-id="d1752-128">Releases the mouse capture from a window in the current thread and restores normal mouse input processing.</span></span> <span data-ttu-id="d1752-129">Ein Fenster, das die Maus erfasst hat, empfängt unabhängig von der Position des Cursors alle Mauseingaben, es sei denn, es wird auf eine Maustaste geklickt, während sich der Cursor im Fenster eines anderen Threads befindet.</span><span class="sxs-lookup"><span data-stu-id="d1752-129">A window that has captured the mouse receives all mouse input, regardless of the position of the cursor, except when a mouse button is clicked while the cursor hot spot is in the window of another thread.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1752-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1752-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="d1752-131">Legt die Mauserfassung auf das angegebene Fenster fest, das zum aktuellen Thread gehört.</span><span class="sxs-lookup"><span data-stu-id="d1752-131">Sets the mouse capture to the specified window belonging to the current thread.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1752-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1752-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="d1752-133">Legt die Doppelklickzeit für die Maus fest.</span><span class="sxs-lookup"><span data-stu-id="d1752-133">Sets the double-click time for the mouse.</span></span> <span data-ttu-id="d1752-134">Bei einem Doppelklick handelt es sich um eine Reihe von zwei Mausklicks, bei der der zweite innerhalb eines angegebenen Zeitpunkts nach dem ersten klickt.</span><span class="sxs-lookup"><span data-stu-id="d1752-134">A double-click is a series of two clicks of a mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="d1752-135">Die Doppelklickzeit ist die maximale Anzahl von Millisekunden, die zwischen dem ersten und zweiten Klick eines Doppelklicks auftreten können.</span><span class="sxs-lookup"><span data-stu-id="d1752-135">The double-click time is the maximum number of milliseconds that may occur between the first and second clicks of a double-click.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1752-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1752-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span></span><br/></td>
<td><span data-ttu-id="d1752-137">Kehrt die Bedeutung der linken und rechten Maustaste um oder stellt sie wieder wieder auf.</span><span class="sxs-lookup"><span data-stu-id="d1752-137">Reverses or restores the meaning of the left and right mouse buttons.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1752-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1752-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="d1752-139">Gibt Meldungen aus, wenn der Mauszeiger ein Fenster verlässt oder für einen angegebenen Zeitraum mit dem Mauszeiger auf ein Fenster zeigt.</span><span class="sxs-lookup"><span data-stu-id="d1752-139">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d1752-140">Die <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent-Funktion</strong></a> ruft <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> auf, sofern vorhanden, andernfalls _TrackMouseEvent <strong>TrackMouseEvent emuliert.</strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="d1752-140">The <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise <strong>_TrackMouseEvent</strong> emulates <strong>TrackMouseEvent</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

