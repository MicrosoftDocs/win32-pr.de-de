---
description: Sehen Sie sich eine Kombination aus einem oder mehrere Flags an, die das Verhalten beim Erstellen des Geräts steuern.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d89043ac49b72bccf6279ef3c9c8fa2c856c775
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343228"
---
# <a name="d3dcreate"></a><span data-ttu-id="6c80a-103">D3DCREATE</span><span class="sxs-lookup"><span data-stu-id="6c80a-103">D3DCREATE</span></span>

<span data-ttu-id="6c80a-104">Eine Kombination aus einem oder mehrere Flags, die das Verhalten beim Erstellen des Geräts steuern.</span><span class="sxs-lookup"><span data-stu-id="6c80a-104">A combination of one or more flags that control the device create behavior.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c80a-105">#Definieren</span><span class="sxs-lookup"><span data-stu-id="6c80a-105">#define</span></span></td>
<td><span data-ttu-id="6c80a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c80a-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c80a-107">D3DCREATE_ADAPTERGROUP_DEVICE</span><span class="sxs-lookup"><span data-stu-id="6c80a-107">D3DCREATE_ADAPTERGROUP_DEVICE</span></span></td>
<td><span data-ttu-id="6c80a-108">Die Anwendung fordert das Gerät auf, alle Kopfköpfe zu fahren, die dieser Masteradapter besitzt.</span><span class="sxs-lookup"><span data-stu-id="6c80a-108">Application asks the device to drive all the heads that this master adapter owns.</span></span> <span data-ttu-id="6c80a-109">Das Flag ist für Nichtmasteradapter ungültig.</span><span class="sxs-lookup"><span data-stu-id="6c80a-109">The flag is illegal on nonmaster adapters.</span></span> <span data-ttu-id="6c80a-110">Wenn dieses Flag festgelegt ist, sollten die an <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> übergebenen Präsentationsparameter auf ein Array <a href="d3dpresent-parameters.md"><strong>von</strong></a>D3DPRESENT_PARAMETERS.</span><span class="sxs-lookup"><span data-stu-id="6c80a-110">If this flag is set, the presentation parameters passed to <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> should point to an array of <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span></span> <span data-ttu-id="6c80a-111">Die Anzahl der Elemente in <strong>D3DPRESENT_PARAMETERS</strong> der Anzahl von Adaptern, die durch das NumberOfAdaptersInGroup-Element der <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9-Struktur definiert</strong></a> werden.</span><span class="sxs-lookup"><span data-stu-id="6c80a-111">The number of elements in <strong>D3DPRESENT_PARAMETERS</strong> should equal the number of adapters defined by the NumberOfAdaptersInGroup member of the <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> structure.</span></span> <span data-ttu-id="6c80a-112">Die DirectX-Laufzeit weist jedem Kopf jedes Element in der numerischen Reihenfolge zu, die vom AdapterOrdinalInGroup-Mitglied <strong>von D3DCAPS9 angegeben wird.</strong></span><span class="sxs-lookup"><span data-stu-id="6c80a-112">The DirectX runtime will assign each element to each head in the numerical order specified by the AdapterOrdinalInGroup member of <strong>D3DCAPS9</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c80a-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="6c80a-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span></span></td>
<td><span data-ttu-id="6c80a-114">Direct3D verwaltet Ressourcen anstelle des Treibers.</span><span class="sxs-lookup"><span data-stu-id="6c80a-114">Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="6c80a-115">Direct3D-Aufrufe treten bei Ressourcenfehlern wie unzureichendem Videospeicher nicht auf.</span><span class="sxs-lookup"><span data-stu-id="6c80a-115">Direct3D calls will not fail for resource errors such as insufficient video memory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c80a-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span><span class="sxs-lookup"><span data-stu-id="6c80a-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span></span></td>
<td><span data-ttu-id="6c80a-117">Wie D3DCREATE_DISABLE_DRIVER_MANAGEMENT verwaltet Direct3D Ressourcen anstelle des Treibers.</span><span class="sxs-lookup"><span data-stu-id="6c80a-117">Like D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="6c80a-118">Im Gegensatz D3DCREATE_DISABLE_DRIVER_MANAGEMENT gibt D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX Fehler für Bedingungen wie unzureichenden Videospeicher zurück.</span><span class="sxs-lookup"><span data-stu-id="6c80a-118">Unlike D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX will return errors for conditions such as insufficient video memory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c80a-119">D3DCREATE_DISABLE_PRINTSCREEN</span><span class="sxs-lookup"><span data-stu-id="6c80a-119">D3DCREATE_DISABLE_PRINTSCREEN</span></span></td>
<td><span data-ttu-id="6c80a-120">Bewirkt, dass die Runtime keine Hotkeys für Printscreen, Ctrl-Printscreen und Alt-Printscreen, um den Desktop- oder Fensterinhalt zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="6c80a-120">Causes the runtime not register hotkeys for Printscreen, Ctrl-Printscreen and Alt-Printscreen to capture the desktop or window content.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c80a-121">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="6c80a-121">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="6c80a-122">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c80a-122">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c80a-123">D3DCREATE_DISABLE_PSGP_THREADING</span><span class="sxs-lookup"><span data-stu-id="6c80a-123">D3DCREATE_DISABLE_PSGP_THREADING</span></span></td>
<td><span data-ttu-id="6c80a-124">Beschränken Sie die Berechnung auf den Hauptanwendungsthread.</span><span class="sxs-lookup"><span data-stu-id="6c80a-124">Restrict computation to the main application thread.</span></span> <span data-ttu-id="6c80a-125">Wenn das Flag nicht festgelegt ist, kann die Runtime softwarevertex processing and other computations in worker thread (Softwarevertexverarbeitung und andere Berechnungen im Arbeitsthread) ausführen, um die Leistung auf Systemen mit mehreren Prozessoren zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="6c80a-125">If the flag is not set, the runtime may perform software vertex processing and other computations in worker thread to improve performance on multi-processor systems.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c80a-126">Unterschiede zwischen Windows XP und Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="6c80a-126">Differences between Windows XP and Windows Vista:</span></span><br/> <span data-ttu-id="6c80a-127">Dieses Flag ist unter Windows Vista, Windows Server 2008 und Windows 7 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c80a-127">This flag is available on Windows Vista, Windows Server 2008, and Windows 7.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c80a-128">D3DCREATE_ENABLE_PRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="6c80a-128">D3DCREATE_ENABLE_PRESENTSTATS</span></span></td>
<td><span data-ttu-id="6c80a-129">Ermöglicht das Sammeln vorhandener Statistiken auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="6c80a-129">Enables the gathering of present statistics on the device.</span></span> <span data-ttu-id="6c80a-130">Aufrufe von <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> geben gültige Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="6c80a-130">Calls to <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> will return valid data.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c80a-131">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="6c80a-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="6c80a-132">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c80a-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c80a-133">D3DCREATE_FPU_PRESERVE</span><span class="sxs-lookup"><span data-stu-id="6c80a-133">D3DCREATE_FPU_PRESERVE</span></span></td>
<td><span data-ttu-id="6c80a-134">Legen Sie die Genauigkeit für Direct3D-Gleitkommaberechnungen auf die Genauigkeit fest, die vom aufrufenden Thread verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6c80a-134">Set the precision for Direct3D floating-point calculations to the precision used by the calling thread.</span></span> <span data-ttu-id="6c80a-135">Wenn Sie dieses Flag nicht angeben, verwendet Direct3D aus zwei Gründen standardmäßig den Modus "Round-to-Nearest" mit einfacher Genauigkeit:</span><span class="sxs-lookup"><span data-stu-id="6c80a-135">If you do not specify this flag, Direct3D defaults to single-precision round-to-nearest mode for two reasons:</span></span>
<ul>
<li><span data-ttu-id="6c80a-136">Der Modus mit doppelter Genauigkeit reduziert die Direct3D-Leistung.</span><span class="sxs-lookup"><span data-stu-id="6c80a-136">Double-precision mode will reduce Direct3D performance.</span></span></li>
<li><span data-ttu-id="6c80a-137">Bei Teilen von Direct3D wird davon ausgegangen, dass Gleitkommaeinheits-Ausnahmen maskiert sind. Das Aufheben derMaskatur dieser Ausnahmen kann zu undefiniertem Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="6c80a-137">Portions of Direct3D assume floating-point unit exceptions are masked; unmasking these exceptions may result in undefined behavior.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c80a-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="6c80a-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="6c80a-139">Gibt die Hardwarevertexverarbeitung an.</span><span class="sxs-lookup"><span data-stu-id="6c80a-139">Specifies hardware vertex processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c80a-140">D3DCREATE_MIXED_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="6c80a-140">D3DCREATE_MIXED_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="6c80a-141">Gibt die gemischte Vertexverarbeitung (software- und hardwareseitig) an.</span><span class="sxs-lookup"><span data-stu-id="6c80a-141">Specifies mixed (both software and hardware) vertex processing.</span></span> <span data-ttu-id="6c80a-142">Für Windows 10 Version 1607 und höher wird die Verwendung dieser Einstellung nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="6c80a-142">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="6c80a-143">Siehe D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="6c80a-143">See D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c80a-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="6c80a-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="6c80a-145">Gibt die Softwarevertexverarbeitung an.</span><span class="sxs-lookup"><span data-stu-id="6c80a-145">Specifies software vertex processing.</span></span> <span data-ttu-id="6c80a-146">Für Windows 10 Version 1607 und höher wird die Verwendung dieser Einstellung nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="6c80a-146">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="6c80a-147">Verwenden D3DCREATE_HARDWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="6c80a-147">Use D3DCREATE_HARDWARE_VERTEXPROCESSING.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6c80a-148">Sofern keine Hardwarevertexverarbeitung verfügbar ist, wird die Verwendung der Softwarevertexverarbeitung in Windows 10, Version 1607 (und höher), nicht empfohlen, da die Effizienz der Softwarevertexverarbeitung erheblich reduziert und gleichzeitig die Sicherheit der Implementierung verbessert wurde.</span><span class="sxs-lookup"><span data-stu-id="6c80a-148">Unless hardware vertex processing is not available, the usage of software vertex processing is not recommended in Windows 10, version 1607 (and later versions) because the efficiency of software vertex processing was significantly reduced while improving the security of the implementation.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c80a-149">D3DCREATE_MULTITHREADED</span><span class="sxs-lookup"><span data-stu-id="6c80a-149">D3DCREATE_MULTITHREADED</span></span></td>
<td><span data-ttu-id="6c80a-150">Gibt an, dass die Anwendung Direct3D als multithreadsicher angibt.</span><span class="sxs-lookup"><span data-stu-id="6c80a-150">Indicates that the application requests Direct3D to be multithread safe.</span></span> <span data-ttu-id="6c80a-151">Dadurch wird ein Direct3D-Thread <a href="/windows/desktop/Sync/critical-section-objects"></a> häufiger besitzer des globalen kritischen Abschnitts, was die Leistung beeinträchtigen kann.</span><span class="sxs-lookup"><span data-stu-id="6c80a-151">This makes a Direct3D thread take ownership of its global <a href="/windows/desktop/Sync/critical-section-objects">critical section</a> more frequently, which can degrade performance.</span></span> <span data-ttu-id="6c80a-152">Wenn eine Anwendung Fenstermeldungen in einem Thread verarbeitet, während sie Direct3D-API-Aufrufe in einem anderen threadt, muss die Anwendung dieses Flag beim Erstellen des Geräts verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c80a-152">If an application processes window messages in one thread while making Direct3D API calls in another, the application must use this flag when creating the device.</span></span> <span data-ttu-id="6c80a-153">Dieses Fenster muss auch zerstört werden, bevor sie d3d9.dll.</span><span class="sxs-lookup"><span data-stu-id="6c80a-153">This window must also be destroyed before unloading d3d9.dll.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c80a-154">D3DCREATE_NOWINDOWCHANGES</span><span class="sxs-lookup"><span data-stu-id="6c80a-154">D3DCREATE_NOWINDOWCHANGES</span></span></td>
<td><span data-ttu-id="6c80a-155">Gibt an, dass Direct3D das Fokusfenster nicht ändern darf.</span><span class="sxs-lookup"><span data-stu-id="6c80a-155">Indicates that Direct3D must not alter the focus window in any way.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6c80a-156">Wenn dieses Flag festgelegt ist, muss die Anwendung alle Fokusverwaltungsereignisse wie ALT+TAB und Mausklickereignisse vollständig unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6c80a-156">If this flag is set, the application must fully support all focus management events, such as ALT+TAB and mouse click events.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c80a-157">D3DCREATE_PUREDEVICE</span><span class="sxs-lookup"><span data-stu-id="6c80a-157">D3DCREATE_PUREDEVICE</span></span></td>
<td><span data-ttu-id="6c80a-158">Gibt an, dass Direct3D keine Get\*-Aufrufe für etwas unterstützt, das in Zustandsblöcken gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6c80a-158">Specifies that Direct3D does not support Get\* calls for anything that can be stored in state blocks.</span></span> <span data-ttu-id="6c80a-159">Außerdem weist direct3D an, keine Emulationsdienste für die Scheitelpunktverarbeitung zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="6c80a-159">It also tells Direct3D not to provide any emulation services for vertex processing.</span></span> <span data-ttu-id="6c80a-160">Dies bedeutet, dass die Anwendung nur nach transformierte Scheitelpunkte verwenden kann, wenn das Gerät die Scheitelpunktverarbeitung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c80a-160">This means that if the device does not support vertex processing, then the application can use only post-transformed vertices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c80a-161">D3DCREATE_SCREENSAVER</span><span class="sxs-lookup"><span data-stu-id="6c80a-161">D3DCREATE_SCREENSAVER</span></span></td>
<td><span data-ttu-id="6c80a-162">Ermöglicht Bildschirmschoner während einer Vollbildanwendung.</span><span class="sxs-lookup"><span data-stu-id="6c80a-162">Allows screensavers during a fullscreen application.</span></span> <span data-ttu-id="6c80a-163">Ohne dieses Flag deaktiviert Direct3D Bildschirmschoner, solange die aufrufende Anwendung vollbildig ist.</span><span class="sxs-lookup"><span data-stu-id="6c80a-163">Without this flag, Direct3D will disable screensavers for as long as the calling application is fullscreen.</span></span> <span data-ttu-id="6c80a-164">Wenn die aufrufende Anwendung bereits ein Bildschirmschoner ist, hat dieses Flag keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="6c80a-164">If the calling application is already a screensaver, this flag has no effect.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c80a-165">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="6c80a-165">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="6c80a-166">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c80a-166">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6c80a-167">D3DCREATE \_ HARDWARE \_ VERTEXPROCESSING, D3DCREATE \_ MIXED \_ VERTEXPROCESSING und D3DCREATE \_ SOFTWARE \_ VERTEXPROCESSING sind sich gegenseitig ausschließende Flags.</span><span class="sxs-lookup"><span data-stu-id="6c80a-167">D3DCREATE\_HARDWARE\_VERTEXPROCESSING, D3DCREATE\_MIXED\_VERTEXPROCESSING, and D3DCREATE\_SOFTWARE\_VERTEXPROCESSING are mutually exclusive flags.</span></span> <span data-ttu-id="6c80a-168">Mindestens eines dieser Scheitelpunktverarbeitungsflags muss beim Aufrufen von [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6c80a-168">At least one of these vertex processing flags must be specified when calling [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span>

## <a name="constant-information"></a><span data-ttu-id="6c80a-169">Konstanteninformationen</span><span class="sxs-lookup"><span data-stu-id="6c80a-169">Constant Information</span></span>



| <span data-ttu-id="6c80a-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c80a-170">Requirement</span></span>                         |  <span data-ttu-id="6c80a-171">Wert</span><span class="sxs-lookup"><span data-stu-id="6c80a-171">Value</span></span>          |
|--------------------------|------------|
| <span data-ttu-id="6c80a-172">Header</span><span class="sxs-lookup"><span data-stu-id="6c80a-172">Header</span></span>                   | <span data-ttu-id="6c80a-173">D3D9.h</span><span class="sxs-lookup"><span data-stu-id="6c80a-173">D3D9.h</span></span>     |
| <span data-ttu-id="6c80a-174">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="6c80a-174">Minimum operating system</span></span> | <span data-ttu-id="6c80a-175">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6c80a-175">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6c80a-176">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6c80a-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c80a-177">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="6c80a-177">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
