---
description: Eine Kombination aus einem oder mehreren Flags, die das Erstellungs Verhalten des Geräts steuern.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14de345d6cb6d164ee5cd3067e1f38ff66d9795d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958487"
---
# <a name="d3dcreate"></a><span data-ttu-id="582ec-103">D3DCREATE</span><span class="sxs-lookup"><span data-stu-id="582ec-103">D3DCREATE</span></span>

<span data-ttu-id="582ec-104">Eine Kombination aus einem oder mehreren Flags, die das Erstellungs Verhalten des Geräts steuern.</span><span class="sxs-lookup"><span data-stu-id="582ec-104">A combination of one or more flags that control the device create behavior.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="582ec-105">#definieren</span><span class="sxs-lookup"><span data-stu-id="582ec-105">#define</span></span></td>
<td><span data-ttu-id="582ec-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="582ec-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="582ec-107">D3DCREATE_ADAPTERGROUP_DEVICE</span><span class="sxs-lookup"><span data-stu-id="582ec-107">D3DCREATE_ADAPTERGROUP_DEVICE</span></span></td>
<td><span data-ttu-id="582ec-108">Die Anwendung fordert das Gerät auf, alle Köpfe zu steuern, die dieser Master Adapter besitzt.</span><span class="sxs-lookup"><span data-stu-id="582ec-108">Application asks the device to drive all the heads that this master adapter owns.</span></span> <span data-ttu-id="582ec-109">Das Flag ist für nicht-Master Adapter unzulässig.</span><span class="sxs-lookup"><span data-stu-id="582ec-109">The flag is illegal on nonmaster adapters.</span></span> <span data-ttu-id="582ec-110">Wenn dieses Flag festgelegt ist, sollten die an " <a href="/windows/desktop/api"><strong>kreatedevice</strong></a> " übergeben Präsentations Parameter auf ein Array von <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>zeigen.</span><span class="sxs-lookup"><span data-stu-id="582ec-110">If this flag is set, the presentation parameters passed to <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> should point to an array of <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span></span> <span data-ttu-id="582ec-111">Die Anzahl der Elemente in <strong>D3DPRESENT_PARAMETERS</strong> sollte gleich der Anzahl von Adaptern sein, die durch den "zahlofadaptersingroup"-Member der <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> -Struktur definiert werden.</span><span class="sxs-lookup"><span data-stu-id="582ec-111">The number of elements in <strong>D3DPRESENT_PARAMETERS</strong> should equal the number of adapters defined by the NumberOfAdaptersInGroup member of the <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> structure.</span></span> <span data-ttu-id="582ec-112">Die DirectX-Laufzeit weist jedes Element jedem Kopf in der numerischen Reihenfolge zu, die durch den adapterordinalingroup-Member von <strong>D3DCAPS9</strong>angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="582ec-112">The DirectX runtime will assign each element to each head in the numerical order specified by the AdapterOrdinalInGroup member of <strong>D3DCAPS9</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="582ec-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="582ec-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span></span></td>
<td><span data-ttu-id="582ec-114">Direct3D verwaltet Ressourcen anstelle des Treibers.</span><span class="sxs-lookup"><span data-stu-id="582ec-114">Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="582ec-115">Direct3D-Aufrufe schlagen für Ressourcen Fehler wie nicht ausreichenden Video Arbeitsspeicher fehl.</span><span class="sxs-lookup"><span data-stu-id="582ec-115">Direct3D calls will not fail for resource errors such as insufficient video memory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="582ec-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span><span class="sxs-lookup"><span data-stu-id="582ec-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span></span></td>
<td><span data-ttu-id="582ec-117">Wie D3DCREATE_DISABLE_DRIVER_MANAGEMENT verwaltet Direct3D Ressourcen anstelle des Treibers.</span><span class="sxs-lookup"><span data-stu-id="582ec-117">Like D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="582ec-118">Im Gegensatz zu D3DCREATE_DISABLE_DRIVER_MANAGEMENT gibt D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX Fehler für Bedingungen zurück, wie z. b. unzureichenden Videospeicher.</span><span class="sxs-lookup"><span data-stu-id="582ec-118">Unlike D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX will return errors for conditions such as insufficient video memory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="582ec-119">D3DCREATE_DISABLE_PRINTSCREEN</span><span class="sxs-lookup"><span data-stu-id="582ec-119">D3DCREATE_DISABLE_PRINTSCREEN</span></span></td>
<td><span data-ttu-id="582ec-120">Bewirkt, dass die Laufzeit keine Hotkeys für PrintScreen, Ctrl-Printscreen und Alt-Printscreen registriert, um den Inhalt des Desktops oder Fensters zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="582ec-120">Causes the runtime not register hotkeys for Printscreen, Ctrl-Printscreen and Alt-Printscreen to capture the desktop or window content.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="582ec-121">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="582ec-121">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="582ec-122">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="582ec-122">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="582ec-123">D3DCREATE_DISABLE_PSGP_THREADING</span><span class="sxs-lookup"><span data-stu-id="582ec-123">D3DCREATE_DISABLE_PSGP_THREADING</span></span></td>
<td><span data-ttu-id="582ec-124">Beschränken Sie die Berechnung auf den Hauptanwendungs Thread.</span><span class="sxs-lookup"><span data-stu-id="582ec-124">Restrict computation to the main application thread.</span></span> <span data-ttu-id="582ec-125">Wenn das Flag nicht festgelegt ist, kann die Laufzeit die Verarbeitung von Software Scheitel Punkten und andere Berechnungen im Arbeits Thread durchführen, um die Leistung von Multiprozessorsystemen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="582ec-125">If the flag is not set, the runtime may perform software vertex processing and other computations in worker thread to improve performance on multi-processor systems.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="582ec-126">Unterschiede zwischen Windows XP und Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="582ec-126">Differences between Windows XP and Windows Vista:</span></span><br/> <span data-ttu-id="582ec-127">Dieses Flag ist unter Windows Vista, Windows Server 2008 und Windows 7 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="582ec-127">This flag is available on Windows Vista, Windows Server 2008, and Windows 7.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="582ec-128">D3DCREATE_ENABLE_PRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="582ec-128">D3DCREATE_ENABLE_PRESENTSTATS</span></span></td>
<td><span data-ttu-id="582ec-129">Ermöglicht das Sammeln der aktuellen Statistiken auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="582ec-129">Enables the gathering of present statistics on the device.</span></span> <span data-ttu-id="582ec-130">Aufrufe von <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>getpresentstatistics</strong></a> geben gültige Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="582ec-130">Calls to <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> will return valid data.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="582ec-131">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="582ec-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="582ec-132">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="582ec-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="582ec-133">D3DCREATE_FPU_PRESERVE</span><span class="sxs-lookup"><span data-stu-id="582ec-133">D3DCREATE_FPU_PRESERVE</span></span></td>
<td><span data-ttu-id="582ec-134">Legen Sie die Genauigkeit für Gleit Komma Berechnungen Direct3D auf die vom aufrufenden Thread verwendete Genauigkeit fest.</span><span class="sxs-lookup"><span data-stu-id="582ec-134">Set the precision for Direct3D floating-point calculations to the precision used by the calling thread.</span></span> <span data-ttu-id="582ec-135">Wenn Sie dieses Flag nicht angeben, ist Direct3D standardmäßig auf den Modus mit einfacher Genauigkeit und aus zwei Gründen festgelegt:</span><span class="sxs-lookup"><span data-stu-id="582ec-135">If you do not specify this flag, Direct3D defaults to single-precision round-to-nearest mode for two reasons:</span></span>
<ul>
<li><span data-ttu-id="582ec-136">Der Modus mit doppelter Genauigkeit führt zu einer Verringerung der Direct3D-Leistung.</span><span class="sxs-lookup"><span data-stu-id="582ec-136">Double-precision mode will reduce Direct3D performance.</span></span></li>
<li><span data-ttu-id="582ec-137">Teile von Direct3D gehen davon aus, dass Ausnahmen von Gleit Komma Einheiten maskiert werden. die Maskierung dieser Ausnahmen kann zu undefiniertem Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="582ec-137">Portions of Direct3D assume floating-point unit exceptions are masked; unmasking these exceptions may result in undefined behavior.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="582ec-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="582ec-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="582ec-139">Gibt die Vertex-Hardware Verarbeitung an.</span><span class="sxs-lookup"><span data-stu-id="582ec-139">Specifies hardware vertex processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="582ec-140">D3DCREATE_MIXED_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="582ec-140">D3DCREATE_MIXED_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="582ec-141">Gibt die Vertexverarbeitung von gemischten (sowohl Software-als auch Hardware) an.</span><span class="sxs-lookup"><span data-stu-id="582ec-141">Specifies mixed (both software and hardware) vertex processing.</span></span> <span data-ttu-id="582ec-142">Für Windows 10, Version 1607 und höher, wird die Verwendung dieser Einstellung nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="582ec-142">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="582ec-143">Siehe D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="582ec-143">See D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="582ec-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="582ec-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="582ec-145">Gibt die Verarbeitung von Software Scheitel Punkten an.</span><span class="sxs-lookup"><span data-stu-id="582ec-145">Specifies software vertex processing.</span></span> <span data-ttu-id="582ec-146">Für Windows 10, Version 1607 und höher, wird die Verwendung dieser Einstellung nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="582ec-146">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="582ec-147">Verwenden Sie D3DCREATE_HARDWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="582ec-147">Use D3DCREATE_HARDWARE_VERTEXPROCESSING.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="582ec-148">Wenn die Verarbeitung von Hardware Scheitel Punkten nicht verfügbar ist, wird die Verwendung der Verarbeitung von Software Scheitel Punkten in Windows 10, Version 1607 (und höheren Versionen), nicht empfohlen, da die Effizienz der Verarbeitung von Software Scheitel Punkten erheblich reduziert wurde und gleichzeitig die Sicherheit der Implementierung verbessert wurde.</span><span class="sxs-lookup"><span data-stu-id="582ec-148">Unless hardware vertex processing is not available, the usage of software vertex processing is not recommended in Windows 10, version 1607 (and later versions) because the efficiency of software vertex processing was significantly reduced while improving the security of the implementation.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="582ec-149">D3DCREATE_MULTITHREADED</span><span class="sxs-lookup"><span data-stu-id="582ec-149">D3DCREATE_MULTITHREADED</span></span></td>
<td><span data-ttu-id="582ec-150">Gibt an, dass die Anwendung Direct3D als multithreadsicher anfordert.</span><span class="sxs-lookup"><span data-stu-id="582ec-150">Indicates that the application requests Direct3D to be multithread safe.</span></span> <span data-ttu-id="582ec-151">Dadurch wird ein Direct3D-Thread häufiger in den Besitz seines globalen <a href="/windows/desktop/Sync/critical-section-objects">kritischen Abschnitts</a> übertragen, wodurch die Leistung beeinträchtigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="582ec-151">This makes a Direct3D thread take ownership of its global <a href="/windows/desktop/Sync/critical-section-objects">critical section</a> more frequently, which can degrade performance.</span></span> <span data-ttu-id="582ec-152">Wenn eine Anwendung Fenster Nachrichten in einem Thread verarbeitet, während Direct3D-API-Aufrufe in einer anderen vorgenommen werden, muss die Anwendung dieses Flag beim Erstellen des Geräts verwenden.</span><span class="sxs-lookup"><span data-stu-id="582ec-152">If an application processes window messages in one thread while making Direct3D API calls in another, the application must use this flag when creating the device.</span></span> <span data-ttu-id="582ec-153">Dieses Fenster muss vor dem Entladen d3d9.dll ebenfalls zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="582ec-153">This window must also be destroyed before unloading d3d9.dll.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="582ec-154">D3DCREATE_NOWINDOWCHANGES</span><span class="sxs-lookup"><span data-stu-id="582ec-154">D3DCREATE_NOWINDOWCHANGES</span></span></td>
<td><span data-ttu-id="582ec-155">Gibt an, dass Direct3D das Fokus Fenster in keiner Weise ändern darf.</span><span class="sxs-lookup"><span data-stu-id="582ec-155">Indicates that Direct3D must not alter the focus window in any way.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="582ec-156">Wenn dieses Flag festgelegt ist, muss die Anwendung alle Fokus Verwaltungs Ereignisse vollständig unterstützen, z. b. Alt + Tab-und Mausklicks-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="582ec-156">If this flag is set, the application must fully support all focus management events, such as ALT+TAB and mouse click events.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="582ec-157">D3DCREATE_PUREDEVICE</span><span class="sxs-lookup"><span data-stu-id="582ec-157">D3DCREATE_PUREDEVICE</span></span></td>
<td><span data-ttu-id="582ec-158">Gibt an, dass Direct3D Get \*-Aufrufe für Elemente, die in Zustands Blöcken gespeichert werden können, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="582ec-158">Specifies that Direct3D does not support Get\* calls for anything that can be stored in state blocks.</span></span> <span data-ttu-id="582ec-159">Es weist auch Direct3D an, keine Emulations Dienste für die Vertexverarbeitung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="582ec-159">It also tells Direct3D not to provide any emulation services for vertex processing.</span></span> <span data-ttu-id="582ec-160">Dies bedeutet Folgendes: Wenn das Gerät die Scheitelpunkt Verarbeitung nicht unterstützt, kann die Anwendung nur nachträglich transformierte Vertices verwenden.</span><span class="sxs-lookup"><span data-stu-id="582ec-160">This means that if the device does not support vertex processing, then the application can use only post-transformed vertices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="582ec-161">D3DCREATE_SCREENSAVER</span><span class="sxs-lookup"><span data-stu-id="582ec-161">D3DCREATE_SCREENSAVER</span></span></td>
<td><span data-ttu-id="582ec-162">Ermöglicht Screensaver während einer Vollbild-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="582ec-162">Allows screensavers during a fullscreen application.</span></span> <span data-ttu-id="582ec-163">Ohne dieses Flag deaktiviert Direct3D Screensaver so lange, wie es sich bei der aufrufenden Anwendung um Fullscreen handelt.</span><span class="sxs-lookup"><span data-stu-id="582ec-163">Without this flag, Direct3D will disable screensavers for as long as the calling application is fullscreen.</span></span> <span data-ttu-id="582ec-164">Wenn die aufrufenden Anwendung bereits ein Bildschirmschoner ist, hat dieses Flag keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="582ec-164">If the calling application is already a screensaver, this flag has no effect.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="582ec-165">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="582ec-165">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="582ec-166">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="582ec-166">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="582ec-167">D3DCREATE \_ Hardware \_ vertexprocessing, D3DCREATE \_ mixed \_ vertexprocessing und D3DCREATE \_ Software \_ vertexprocessing sind sich gegenseitig ausschließende Flags.</span><span class="sxs-lookup"><span data-stu-id="582ec-167">D3DCREATE\_HARDWARE\_VERTEXPROCESSING, D3DCREATE\_MIXED\_VERTEXPROCESSING, and D3DCREATE\_SOFTWARE\_VERTEXPROCESSING are mutually exclusive flags.</span></span> <span data-ttu-id="582ec-168">Beim Aufrufen von [**createdevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)muss mindestens eine dieser Scheitelpunkt-vertexflags angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="582ec-168">At least one of these vertex processing flags must be specified when calling [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span>

## <a name="constant-information"></a><span data-ttu-id="582ec-169">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="582ec-169">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="582ec-170">Header</span><span class="sxs-lookup"><span data-stu-id="582ec-170">Header</span></span>                   | <span data-ttu-id="582ec-171">D3d9. h</span><span class="sxs-lookup"><span data-stu-id="582ec-171">D3D9.h</span></span>     |
| <span data-ttu-id="582ec-172">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="582ec-172">Minimum operating system</span></span> | <span data-ttu-id="582ec-173">Windows 98</span><span class="sxs-lookup"><span data-stu-id="582ec-173">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="582ec-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="582ec-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="582ec-175">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="582ec-175">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
