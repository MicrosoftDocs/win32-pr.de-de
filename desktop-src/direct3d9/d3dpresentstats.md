---
description: Beschreibt vorhandenes SwapChain-Statistiken im Zusammenhang mit presentex-aufrufen.
ms.assetid: aa100b83-6fbf-442d-9891-7fc034a5b1d5
title: D3DPRESENTSTATS-Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENTSTATS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b49a589fa1702f61e5a5daef806a5b36d464d0ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219566"
---
# <a name="d3dpresentstats-structure"></a><span data-ttu-id="5a6c8-103">D3DPRESENTSTATS-Struktur</span><span class="sxs-lookup"><span data-stu-id="5a6c8-103">D3DPRESENTSTATS structure</span></span>

<span data-ttu-id="5a6c8-104">Beschreibt vorhandenes SwapChain-Statistiken im Zusammenhang mit [**presentex**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) -aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-104">Describes swapchain statistics relating to [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a6c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a6c8-105">Syntax</span></span>


```C++
typedef struct _D3DPRESENTSTATS {
  UINT          PresentCount;
  UINT          PresentRefreshCount;
  UINT          SyncRefreshCount;
  LARGE_INTEGER SyncQPCTime;
  LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```



## <a name="members"></a><span data-ttu-id="5a6c8-106">Member</span><span class="sxs-lookup"><span data-stu-id="5a6c8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5a6c8-107">**Presentcount**</span><span class="sxs-lookup"><span data-stu-id="5a6c8-107">**PresentCount**</span></span>
</dt> <dd>

<span data-ttu-id="5a6c8-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a6c8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5a6c8-109">Anzahl erfolgreicher Aufrufe, die von einem Anzeigegerät ausgeführt werden, das derzeit auf den Bildschirm aussteht.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-109">Running count of successful Present calls made by a display device that is currently outputting to screen.</span></span> <span data-ttu-id="5a6c8-110">Dieser Parameter ist tatsächlich die aktuelle ID des letzten aktuellen Aufrufs und ist nicht notwendigerweise die Gesamtzahl der vorhandenen API-Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-110">This parameter is really the Present ID of the last Present call and is not necessarily the total number of Present API calls made.</span></span>

</dd> <dt>

<span data-ttu-id="5a6c8-111">**Presenterfrischend-Anzahl**</span><span class="sxs-lookup"><span data-stu-id="5a6c8-111">**PresentRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="5a6c8-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a6c8-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5a6c8-113">Die vblank-Anzahl, bei der das letzte vorhanden sein auf dem Bildschirm angezeigt wurde, die vblank-Anzahl wird nach jedem vblank-Intervall erhöht.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-113">The vblank count at which the last Present was displayed on screen, the vblank count increments once every vblank interval.</span></span>

</dd> <dt>

<span data-ttu-id="5a6c8-114">**Synkrefreshcount**</span><span class="sxs-lookup"><span data-stu-id="5a6c8-114">**SyncRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="5a6c8-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a6c8-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5a6c8-116">Die vblank-Anzahl, wenn der Planer die Zeit des Zeit Planungs Moduls zuletzt durch Aufrufen von QueryPerformanceCounter erfasst hat.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-116">The vblank count when the scheduler last sampled the machine time by calling QueryPerformanceCounter.</span></span>

</dd> <dt>

<span data-ttu-id="5a6c8-117">**Syncqpctime**</span><span class="sxs-lookup"><span data-stu-id="5a6c8-117">**SyncQPCTime**</span></span>
</dt> <dd>

<span data-ttu-id="5a6c8-118">Typ: **[ **große \_ ganze Zahl**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="5a6c8-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="5a6c8-119">Die Zeit des Zeit Planungs Moduls für den letzten Sampling, abgerufen durch Aufrufen von [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="5a6c8-119">The scheduler's last sampled machine time, obtained by calling [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

</dd> <dt>

<span data-ttu-id="5a6c8-120">**Syncgputime**</span><span class="sxs-lookup"><span data-stu-id="5a6c8-120">**SyncGPUTime**</span></span>
</dt> <dd>

<span data-ttu-id="5a6c8-121">Typ: **[ **große \_ ganze Zahl**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="5a6c8-121">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="5a6c8-122">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a6c8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a6c8-123">Remarks</span></span>

<span data-ttu-id="5a6c8-124">Wenn eine 9Ex-Anwendung den Flip-Modus annimmt (D3DSWAPEFFECT \_ flipex), können Anwendungen das Löschen von Frames erkennen, indem Sie getpresentstatistics zu einem beliebigen Zeitpunkt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-124">When a 9Ex application adopts Flip Mode present (D3DSWAPEFFECT\_FLIPEX), applications can detect frame dropping by calling GetPresentStatistics at any point in time.</span></span> <span data-ttu-id="5a6c8-125">In der Tat können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="5a6c8-125">In effect, they can do the following.</span></span>

1.  <span data-ttu-id="5a6c8-126">In den Hintergrund Puffer Rendering</span><span class="sxs-lookup"><span data-stu-id="5a6c8-126">Render to the back buffer</span></span>
2.  <span data-ttu-id="5a6c8-127">Aufrufe vorhanden</span><span class="sxs-lookup"><span data-stu-id="5a6c8-127">Call Present</span></span>
3.  <span data-ttu-id="5a6c8-128">Getpresentstats aufrufen und die resultierende D3DPRESENTSTATS-Struktur speichern</span><span class="sxs-lookup"><span data-stu-id="5a6c8-128">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="5a6c8-129">Den nächsten Frame in den Hintergrund Puffer Rendering</span><span class="sxs-lookup"><span data-stu-id="5a6c8-129">Render the next frame to the back buffer</span></span>
5.  <span data-ttu-id="5a6c8-130">Aufrufe vorhanden</span><span class="sxs-lookup"><span data-stu-id="5a6c8-130">Call Present</span></span>
6.  <span data-ttu-id="5a6c8-131">Wiederholen Sie die Schritte 4 und 5 1 oder mehrmals.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-131">Repeat steps 4 and 5 one or more times</span></span>
7.  <span data-ttu-id="5a6c8-132">Getpresentstats aufrufen und die resultierende D3DPRESENTSTATS-Struktur speichern</span><span class="sxs-lookup"><span data-stu-id="5a6c8-132">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
8.  <span data-ttu-id="5a6c8-133">Vergleichen Sie die Werte von presenterfrischendes count aus den beiden gespeicherten D3DPRESENTSTATS-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-133">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="5a6c8-134">Die Anwendung kann die entsprechende presenterfrischend-Anzahl eines bestimmten presentcount-Parameters basierend auf den Annahmen der presenterfrischendes count Inkrement-und presentcount-Zuweisung von Frame-Vorstellungen berechnen.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-134">The application can calculate the corresponding PresentRefreshCount of a particular PresentCount parameter based on the assumptions of PresentRefreshCount increment and PresentCount assignment of frame presents.</span></span> <span data-ttu-id="5a6c8-135">Wenn die Anzahl der zuletzt erfassten Präsentationen nicht mit der presentcount-Entsprechung identisch ist (d. h., wenn die presentaktuationszahl inkrementiert wurde, aber presentcount nicht, gab es einen Frame, der gelöscht wurde</span><span class="sxs-lookup"><span data-stu-id="5a6c8-135">If the PresentRefreshCount last sampled does not match the PresentCount (i.e. if the PresentRefreshCount has incremented but PresentCount has not, then there was frame dropping.)</span></span>

<span data-ttu-id="5a6c8-136">Anwendungen können bestimmen, ob ein Frame durch Sampling zweier Instanzen von presentcount und getpresentstats (durch Aufrufen der getpresentstats-API zu einem beliebigen Zeitpunkt) gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-136">Applications can determine whether a frame has been dropped by sampling any two instances of PresentCount and GetPresentStats (by calling GetPresentStats API at any two points in time).</span></span> <span data-ttu-id="5a6c8-137">Beispielsweise möchte eine Medien Anwendung, die mit derselben Rate wie die Aktualisierungsrate des Monitors (z. b. Monitor Aktualisierungsrate ist 60Hz), die Anwendung einen Frame alle 1/60 Sekunden anzeigt, die Frames a, B, C, D, E darstellen, die jeweils den vorhandenen IDs entsprechen (presentcount) 1, 2, 3, 7, 8.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-137">For example, a media application that is presenting at the same rate as the monitor refresh rate (for example, monitor refresh rate is 60Hz, the application presents a frame every 1/60 seconds) wants to present frames A, B, C, D, E, each corresponding to Present IDs (PresentCount) 1, 2, 3, 7, 8.</span></span>

<span data-ttu-id="5a6c8-138">Der Anwendungscode sieht wie die folgende Sequenz aus.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-138">The application code looks like the following sequence.</span></span>

1.  <span data-ttu-id="5a6c8-139">Rendering von Frame A in den Hintergrund Puffer</span><span class="sxs-lookup"><span data-stu-id="5a6c8-139">Render frame A to the back buffer</span></span>
2.  <span data-ttu-id="5a6c8-140">Aufrufe vorhanden, presentcount = 1</span><span class="sxs-lookup"><span data-stu-id="5a6c8-140">Call Present, PresentCount = 1</span></span>
3.  <span data-ttu-id="5a6c8-141">Getpresentstats aufrufen und die resultierende D3DPRESENTSTATS-Struktur speichern</span><span class="sxs-lookup"><span data-stu-id="5a6c8-141">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="5a6c8-142">Rendering der nächsten 4 Frames, B, C, D, E bzw.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-142">Render the next 4 frames, B, C, D, E, respectively</span></span>
5.  <span data-ttu-id="5a6c8-143">Der-Rückruf ist viermal verfügbar, presentcounts = 2, 3, 7, 8.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-143">Call Present 4 times, PresentCounts = 2, 3, 7, 8, respectively</span></span>
6.  <span data-ttu-id="5a6c8-144">Getpresentstats aufrufen und die resultierende D3DPRESENTSTATS-Struktur speichern</span><span class="sxs-lookup"><span data-stu-id="5a6c8-144">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
7.  <span data-ttu-id="5a6c8-145">Vergleichen Sie die Werte von presenterfrischendes count aus den beiden gespeicherten D3DPRESENTSTATS-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-145">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="5a6c8-146">Wenn der Unterschied 2 ist, d. h. zwei vblank-Intervalle zwischen den beiden getpresentstats-API-aufrufen verstrichen sind, sollte der letzte dargestellte Frame Frame C lauten. Da die Anwendung ein sehr vleeres Intervall (die Aktualisierungsrate des Monitors) darstellt, ist die verstrichene Zeit zwischen dem Zeitpunkt, an dem Frame A dargestellt wird, und dem Zeitpunkt, an dem Frame C dargestellt wird, 2 vblank.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-146">If the difference is 2, i.e. 2 vblank intervals has elapsed between the two GetPresentStats API calls, then the last presented frame should be frame C. Because the application presents once very vblank interval (the refresh rate of the monitor), the time elapsed between when frame A is presented and when frame C is presented should be 2 vblanks.</span></span>
8.  <span data-ttu-id="5a6c8-147">Vergleichen Sie die Werte von presentcount aus den beiden gespeicherten D3DPRESENTSTATS-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-147">Compare the values of PresentCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="5a6c8-148">Wenn der erste presentcount 1 ist (entspricht Frame A) und der zweite presentcount 3 (entsprechend Frame C), wurden keine Frames gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-148">If the first PresentCount is 1 (corresponding to frame A) and the second PresentCount is 3 (corresponding to frame C), then no frames have been dropped.</span></span> <span data-ttu-id="5a6c8-149">Wenn das zweite presentcount-Element 3 ist, das Frame D entspricht, weiß die Anwendung, dass ein Frame gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-149">If the second PresentCount is 3, which corresponds to frame D, then the application knows that one frame has been dropped.</span></span>

<span data-ttu-id="5a6c8-150">Beachten Sie, dass getpresentstatistics nach dem Aufruf verarbeitet wird, unabhängig vom Status der Ansichts Aufrufe des flipex-Modus.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-150">Note that GetPresentStatistics will be processed after it is called, regardless of the state of FLIPEX mode PresentEx calls.</span></span>

<span data-ttu-id="5a6c8-151">**Windows Vista:** Die aktuellen Aufrufe werden in die Warteschlange eingereiht und dann verarbeitet, bevor der getpresentstats-Aufruf verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-151">**Windows Vista:** The Present calls will be queued and then processed before GetPresentStats call will be processed.</span></span>

<span data-ttu-id="5a6c8-152">Wenn eine Anwendung erkennt, dass die Darstellung bestimmter Frames dahinter steht, können diese Frames übersprungen und die Präsentation korrigiert werden, um die erneute Synchronisierung mit vblank durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-152">When an application detects that the presentation of certain frames are behind, it can skip those frames and correct the presentation to re-synchronize with the vblank.</span></span> <span data-ttu-id="5a6c8-153">Zu diesem Zweck kann eine Anwendung die späten Frames einfach nicht Rendern und das Rendering mit dem nächsten richtigen Frame in der Warteschlange starten.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-153">To do this, an application can simply not render the late frames and start rendering with the next correct frame in the queue.</span></span> <span data-ttu-id="5a6c8-154">Wenn eine Anwendung jedoch bereits mit dem Rendern von späten Frames begonnen hat, kann Sie einen neuen Present-Parameter in D3D9Ex namens D3DPRESENT \_ forceimvermittler verwenden.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-154">However, if an application has already started the rendering of late frames, it can use a new Present parameter in D3D9Ex called D3DPRESENT\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="5a6c8-155">Das Flag wird in den Parametern des aktuellen API-Aufrufes ausgegeben und gibt der Laufzeit an, dass der Frame direkt innerhalb des nächsten vblank-Intervalls verarbeitet wird, was auf dem Bildschirm überhaupt nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-155">The flag will be passed in the parameters of Present API call and indicates to the runtime that the frame will be processed immediately within the next vblank interval, effectively not visible on screen at all.</span></span> <span data-ttu-id="5a6c8-156">Im folgenden finden Sie das Beispiel für die Anwendungs Verwendung nach dem letzten Schritt im vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-156">Here is the application usage example after the last step in the previous example.</span></span>

1.  <span data-ttu-id="5a6c8-157">Den nächsten Frame in den Hintergrund Puffer Rendering</span><span class="sxs-lookup"><span data-stu-id="5a6c8-157">Render the next frame to the back buffer</span></span>
2.  <span data-ttu-id="5a6c8-158">Entdecken Sie aus presenterfrischen count, dass der nächste Frame bereits spät ist.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-158">Discover from PresentRefreshCount that the next frame is already late</span></span>
3.  <span data-ttu-id="5a6c8-159">Festlegen des aktuellen Intervalls auf D3DPRESENT \_ forceimvermittler</span><span class="sxs-lookup"><span data-stu-id="5a6c8-159">Set Present interval to D3DPRESENT\_FORCEIMMEDIATE</span></span>
4.  <span data-ttu-id="5a6c8-160">Auf dem nächsten Frame vorhandener aufzurufen</span><span class="sxs-lookup"><span data-stu-id="5a6c8-160">Call Present on the next frame</span></span>

<span data-ttu-id="5a6c8-161">Anwendungen können Video-und Audiostreams auf die gleiche Weise synchronisieren, da sich das Verhalten von getpresentstatistics in diesem Szenario nicht ändert.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-161">Applications can synchronize video and audio streams in the same manner because the behavior of GetPresentStatistics does not change in that scenario.</span></span>

<span data-ttu-id="5a6c8-162">Der D3D9Ex Flip-Modus stellt Frame Statistik Informationen für Fenster Anwendungen und Vollbild-9Ex-Anwendungen bereit.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-162">D3D9Ex Flip Mode provides frame statistics information to windowed applications and full screen 9Ex applications.</span></span>

<span data-ttu-id="5a6c8-163">**Windows Vista:** Verwenden Sie die DWM-APIs zum Abrufen der aktuellen Statistik.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-163">**Windows Vista:** Use the DWM APIs for retrieving present statistics.</span></span>

<span data-ttu-id="5a6c8-164">Wenn Desktopfenster-Manager ausgeschaltet ist, erhalten die Anwendungen im Fenstermodus 9Ex, die den Flip-Modus verwenden, die Statistik Informationen mit eingeschränkter Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-164">When Desktop Window Manager is turned off, windowed mode 9Ex applications using flip mode will receive present statistics information of limited accuracy.</span></span>

<span data-ttu-id="5a6c8-165">\* \* Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="5a6c8-165">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="5a6c8-166">Wenn eine Anwendung nicht schnell genug ist, um mit der Aktualisierungsrate des Monitors Schritt zu halten, möglicherweise aufgrund langsamer Hardware oder fehlender Systemressourcen, kann ein Grafik-glitch angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-166">If an application is not fast enough to keep up with the monitor's refresh rate, possibly due to slow hardware or lack of system resources, then it can experience a graphics glitch.</span></span> <span data-ttu-id="5a6c8-167">Ein Störung ist ein so genanntes visuelles Element.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-167">A glitch is a so-called visual hiccup.</span></span> <span data-ttu-id="5a6c8-168">Wenn ein Monitor bei 60 Hz auf Refresh festgelegt ist und die Anwendung nur 30 FPS verwalten kann, werden für die Hälfte der Rahmen ein Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-168">If a monitor is set to refresh at 60 Hz, and the application can only manage 30 fps, then half of the frames will have glitches.</span></span>

<span data-ttu-id="5a6c8-169">Anwendungen können einen Fehler erkennen, indem Sie die synchrone Anzahl verfolgen.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-169">Applications can detect a glitch by keeping track of SynchRefreshCount.</span></span> <span data-ttu-id="5a6c8-170">Beispielsweise kann eine Anwendung die folgende Sequenz von Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-170">For example, an application might perform the following sequence of actions.</span></span>

1.  <span data-ttu-id="5a6c8-171">In den Hintergrund Puffer Rendering.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-171">Render to the back buffer.</span></span>
2.  <span data-ttu-id="5a6c8-172">Aufrufe vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-172">Call Present.</span></span>
3.  <span data-ttu-id="5a6c8-173">Getpresentstats aufrufen und die resultierende D3DPRESENTSTATS-Struktur speichern.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-173">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
4.  <span data-ttu-id="5a6c8-174">Den nächsten Frame in den Hintergrund Puffer Rendering.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-174">Render the next frame to the back buffer.</span></span>
5.  <span data-ttu-id="5a6c8-175">Aufrufe vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-175">Call Present.</span></span>
6.  <span data-ttu-id="5a6c8-176">Getpresentstats aufrufen und die resultierende D3DPRESENTSTATS-Struktur speichern.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-176">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
7.  <span data-ttu-id="5a6c8-177">Vergleichen Sie die Werte von synkrefreshcount aus den beiden gespeicherten D3DPRESENTSTATS-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-177">Compare the values of SyncRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="5a6c8-178">Wenn der Unterschied größer als 1 ist, wurde ein Frame übersprungen.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-178">If the difference is greater than one, then a frame was skipped.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a6c8-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a6c8-179">Requirements</span></span>



| <span data-ttu-id="5a6c8-180">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a6c8-180">Requirement</span></span> | <span data-ttu-id="5a6c8-181">Wert</span><span class="sxs-lookup"><span data-stu-id="5a6c8-181">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a6c8-182">Header</span><span class="sxs-lookup"><span data-stu-id="5a6c8-182">Header</span></span><br/> | <dl> <span data-ttu-id="5a6c8-183"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a6c8-183"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a6c8-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a6c8-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a6c8-185">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="5a6c8-185">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
