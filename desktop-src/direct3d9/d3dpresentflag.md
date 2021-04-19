---
description: Von D3DPRESENT- \_ Parametern verwendete Konstanten.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3b7fe950a6fe09425aa47a79ce8f803eb81298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346225"
---
# <a name="d3dpresentflag"></a><span data-ttu-id="ec810-103">D3DPRESENTFLAG</span><span class="sxs-lookup"><span data-stu-id="ec810-103">D3DPRESENTFLAG</span></span>

<span data-ttu-id="ec810-104">Von D3DPRESENT- [**\_ Parametern**](d3dpresent-parameters.md)verwendete Konstanten.</span><span class="sxs-lookup"><span data-stu-id="ec810-104">Constants used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec810-105">#definieren</span><span class="sxs-lookup"><span data-stu-id="ec810-105">#define</span></span></td>
<td><span data-ttu-id="ec810-106">Wert</span><span class="sxs-lookup"><span data-stu-id="ec810-106">Value</span></span></td>
<td><span data-ttu-id="ec810-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec810-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec810-108">D3DPRESENTFLAG_DEVICECLIP</span><span class="sxs-lookup"><span data-stu-id="ec810-108">D3DPRESENTFLAG_DEVICECLIP</span></span></td>
<td><span data-ttu-id="ec810-109">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ec810-109">0x00000004</span></span></td>
<td><span data-ttu-id="ec810-110">Schneiden Sie ein Fenster <a href="/windows/desktop/api"><strong></strong></a> aus, das sich im Fenster Client Bereich befindet, und zwar im Bildschirmbereich des Monitors der Grafikkarte, von der das Direct3D-Gerät erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ec810-110">Clip a windowed <a href="/windows/desktop/api"><strong>Present</strong></a> blit into the window client area, within the monitor screen area of the video adapter that created the Direct3D device.</span></span> <span data-ttu-id="ec810-111">D3DPRESENTFLAG_DEVICECLIP ist mit D3DSWAPEFFECT_FLIPEX ungültig.</span><span class="sxs-lookup"><span data-stu-id="ec810-111">D3DPRESENTFLAG_DEVICECLIP is not valid with D3DSWAPEFFECT_FLIPEX.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec810-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span><span class="sxs-lookup"><span data-stu-id="ec810-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span></span></td>
<td><span data-ttu-id="ec810-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ec810-113">0x00000002</span></span></td>
<td><span data-ttu-id="ec810-114">Legen Sie dieses Flag fest, wenn das Gerät oder die Swapkette erstellt wird, um z-Puffer-verwerfen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ec810-114">Set this flag when the device or swap chain is created to enable z-buffer discarding.</span></span> <span data-ttu-id="ec810-115">Wenn dieses Flag festgelegt ist, ist der Inhalt des tiefen Schablone-Puffers nach dem Aufrufen von " <a href="/windows/desktop/api"><strong>Present</strong></a>" oder " <a href="/windows/desktop/api"><strong>setdepthstencilsurface</strong></a> " mit einer anderen tiefen Oberfläche ungültig.</span><span class="sxs-lookup"><span data-stu-id="ec810-115">If this flag is set, the contents of the depth stencil buffer will be invalid after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span> <span data-ttu-id="ec810-116">Das Verwerfen von z-Puffer Daten kann die Leistung erhöhen und ist Treiber abhängig.</span><span class="sxs-lookup"><span data-stu-id="ec810-116">Discarding z-buffer data can increase performance and is driver dependent.</span></span> <span data-ttu-id="ec810-117">Die Debug-Laufzeit erzwingt das verwerfen, indem Sie den z-Puffer auf einen konstanten Wert nach dem Aufruf von " <a href="/windows/desktop/api"><strong>Present</strong></a>" oder " <a href="/windows/desktop/api"><strong>setdepthstencilsurface</strong></a> " mit einer anderen tiefen Oberfläche löscht.</span><span class="sxs-lookup"><span data-stu-id="ec810-117">The debug runtime will enforce discarding by clearing the z-buffer to some constant value after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span><br/> <span data-ttu-id="ec810-118">Das Verwerfen von z-Puffer Daten ist für alle Sperr baren Formate, D3DFMT_D16_LOCKABLE und D3DFMT_D32F_LOCKABLE nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ec810-118">Discarding z-buffer data is illegal for all lockable formats, D3DFMT_D16_LOCKABLE and D3DFMT_D32F_LOCKABLE.</span></span> <span data-ttu-id="ec810-119">Jede Verwendung von " <a href="/windows/desktop/api"><strong>kreatedevice</strong></a> ", die ein Sperr bares Format und z-Puffer-verwerfen angibt, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="ec810-119">Any use of <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> specifying a lockable format and z-buffer discarding will fail.</span></span> <span data-ttu-id="ec810-120">Weitere Informationen zu Formaten finden Sie unter <a href="d3dformat.md">D3DFORMAT</a>.</span><span class="sxs-lookup"><span data-stu-id="ec810-120">For more information about formats, see <a href="d3dformat.md">D3DFORMAT</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec810-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="ec810-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span></span></td>
<td><span data-ttu-id="ec810-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ec810-122">0x00000001</span></span></td>
<td><span data-ttu-id="ec810-123">Legen Sie dieses Flag fest, wenn die Anwendung die Möglichkeit erfordert, den Hintergrund Puffer direkt zu sperren.</span><span class="sxs-lookup"><span data-stu-id="ec810-123">Set this flag if the application requires the ability to lock the back buffer directly.</span></span> <span data-ttu-id="ec810-124">Beachten Sie, dass die Back Puffer nicht sperrbar sind, es sei denn, die Anwendung gibt D3DPRESENTFLAG_LOCKABLE_BACKBUFFER beim Aufrufen von <a href="/windows/desktop/api"><strong>createdevice</strong></a> <a href="/windows/desktop/api"><strong>an oder setzt</strong></a></span><span class="sxs-lookup"><span data-stu-id="ec810-124">Note that back buffers are not lockable unless the application specifies D3DPRESENTFLAG_LOCKABLE_BACKBUFFER when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> or <a href="/windows/desktop/api"><strong>Reset</strong></a>.</span></span> <span data-ttu-id="ec810-125">Sperr Bare Sicherungs Puffer verursachen bei manchen Grafikhardware Konfigurationen Leistungseinbußen.</span><span class="sxs-lookup"><span data-stu-id="ec810-125">Lockable back buffers incur a performance cost on some graphics hardware configurations.</span></span> <span data-ttu-id="ec810-126">Durch das Ausführen eines Sperr Vorgangs (oder mithilfe von <a href="/windows/desktop/api"><strong>updatesurface</strong></a> zum Schreiben) auf dem Sperr baren Hintergrund wird die Leistung auf vielen Karten verringert.</span><span class="sxs-lookup"><span data-stu-id="ec810-126">Performing a lock operation (or using <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> to write) on the lockable back buffer decreases performance on many cards.</span></span> <span data-ttu-id="ec810-127">In diesem Fall sollten Sie die Verwendung von Text Dreiecken zum Verschieben von Daten in den Hintergrund Puffer in Erwägung ziehen.</span><span class="sxs-lookup"><span data-stu-id="ec810-127">In this case, consider using textured triangles to move data to the back buffer.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec810-128">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ec810-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ec810-129">In Direct3D9Ex kann dieses Flag nicht festgelegt werden, wenn der D3DSWAPEFFECT-Wert D3DSWAPEFFECT_FLIPEX ist, da das Flip-Modell dem Desktopfenster-Manager den Zugriff auf den Hintergrund Puffer einer Anwendung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ec810-129">In Direct3D9Ex this flag cannot be set if the D3DSWAPEFFECT is D3DSWAPEFFECT_FLIPEX, since the flip model enables the Desktop Window Manager to access an application's back buffer.</span></span> <span data-ttu-id="ec810-130">Eine prozessübergreifende, freigegebene Oberfläche sollte nicht gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="ec810-130">A cross-process shared-surface should not be locked.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec810-131">D3DPRESENTFLAG_NOAUTOROTATE</span><span class="sxs-lookup"><span data-stu-id="ec810-131">D3DPRESENTFLAG_NOAUTOROTATE</span></span></td>
<td><span data-ttu-id="ec810-132">0x00000020</span><span class="sxs-lookup"><span data-stu-id="ec810-132">0x00000020</span></span></td>
<td><span data-ttu-id="ec810-133">Gedrehte Monitore werden bei der Präsentation automatisch mit einer rotierenden Kopie behandelt, was nicht sehr effizient ist.</span><span class="sxs-lookup"><span data-stu-id="ec810-133">Rotated monitors are handled automatically with a rotating copy during presentation, which is not very efficient.</span></span> <span data-ttu-id="ec810-134">Dieses Flag bedeutet, dass die Anwendung die eigene Anzeigedrehung ausführt.</span><span class="sxs-lookup"><span data-stu-id="ec810-134">This flag means the application will perform it's own display rotation.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec810-135">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ec810-135">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ec810-136">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec810-136">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="ec810-137">Anwendungen können eine eigene Drehung erzielen, indem Sie möglicherweise eine gedrehte Ansichts Matrix verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec810-137">Applications can achieve their own rotation possibly by using a rotated view matrix.</span></span> <span data-ttu-id="ec810-138">Die Methoden <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>getdisplaymodeex</strong></a> und <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>getadapterdisplaymodeex</strong></a> sollten verwendet werden, um die aktuelle Rotations Einstellung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="ec810-138">The methods <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> should be used to to find the current rotation setting.</span></span> <span data-ttu-id="ec810-139">Die Parameter "width" und "Height" in " <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>kreatedeviceex</strong></a> " und " <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>rectex</strong></a> " müssen in der Querformat Ausrichtung verwendet werden, während die Struktur des Vollbild-Anzeigemodus identisch mit der Rückgabe von " <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>enumadaptermodesex</strong></a> " ist (d. h., wenn 90 und 270 Grad gedreht werden, werden Breite und Höhe ausgetauscht).</span><span class="sxs-lookup"><span data-stu-id="ec810-139">The backbuffer Width and Height parameters in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> must be use landscape orientation, while the fullscreen display mode structure should be the same as what is returned from <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (i.e. Width and Height are swapped when rotated 90 and 270 degrees).</span></span></p>
<p><span data-ttu-id="ec810-140">Bei Verwendung der Lock-Klausel für gedrehte Renderziele sind linke obere Ecke nicht mehr true. Das Renderziel SURFACE_DESC bleibt Querformat (wie durch die Erstellungs Parameter impliziert) und GDI-Fenster, Maus Koordinaten und muss bei Verwendung mit dem Direct3D-Renderziel und der Szene ordnungsgemäß übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="ec810-140">When using Lock on rotated render targets, upper-left corner assumptions no longer hold true, the render target SURFACE_DESC will remain landscape (as implied by the creation parameters), and GDI window, mouse coordinates, and such need to be properly translated when used with the Direct3D render target and scene.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec810-141">D3DPRESENTFLAG_UNPRUNEDMODE</span><span class="sxs-lookup"><span data-stu-id="ec810-141">D3DPRESENTFLAG_UNPRUNEDMODE</span></span></td>
<td><span data-ttu-id="ec810-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="ec810-142">0x00000040</span></span></td>
<td><span data-ttu-id="ec810-143">Verwenden Sie dieses Flag, um alle vom Anzeige Adapter aufgelisteten unformatierten Anzeigemodi anzugeben, auch wenn Direct3D möglicherweise angibt, dass der Modus ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="ec810-143">Use this flag to specify any RAW display mode enumerated by the display adapter even though Direct3D may have indicated the mode is invalid.</span></span> <span data-ttu-id="ec810-144">Die Anwendung sollte dies auf robuste Weise implementieren, falls der gewünschte Modus wirklich ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="ec810-144">The application should implement this in a robust manner in case the desired mode really is invalid.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec810-145">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ec810-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ec810-146">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec810-146">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec810-147">D3DPRESENTFLAG_VIDEO</span><span class="sxs-lookup"><span data-stu-id="ec810-147">D3DPRESENTFLAG_VIDEO</span></span></td>
<td><span data-ttu-id="ec810-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec810-148">0x00000010</span></span></td>
<td><span data-ttu-id="ec810-149">Dies ist ein Hinweis für den Treiber, dass die Hintergrund Puffer Videodaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="ec810-149">This is a hint to the driver that the back buffers will contain video data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec810-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span><span class="sxs-lookup"><span data-stu-id="ec810-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span></span></td>
<td><span data-ttu-id="ec810-151">0x00000080</span><span class="sxs-lookup"><span data-stu-id="ec810-151">0x00000080</span></span></td>
<td><span data-ttu-id="ec810-152">Gibt an, ob die Überlagerung den vollen Bereich RGB oder den begrenzten Bereich RGB hat.</span><span class="sxs-lookup"><span data-stu-id="ec810-152">Specifies whether the overlay is full range RGB or limited range RGB.</span></span> <span data-ttu-id="ec810-153">Das Festlegen dieses Flags gibt den begrenzten Bereich RGB an.</span><span class="sxs-lookup"><span data-stu-id="ec810-153">Setting this flag indicates limited range RGB.</span></span> <span data-ttu-id="ec810-154">Im begrenzten Bereich RGB wird der RGB-Bereich so komprimiert, dass 16:16:16 schwarz und 235:235:235 weiß ist.</span><span class="sxs-lookup"><span data-stu-id="ec810-154">In limited range RGB, the RGB range is compressed such that 16:16:16 is black and 235:235:235 is white.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec810-155">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ec810-155">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ec810-156">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec810-156">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec810-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span><span class="sxs-lookup"><span data-stu-id="ec810-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span></span></td>
<td><span data-ttu-id="ec810-158">0x00000100</span><span class="sxs-lookup"><span data-stu-id="ec810-158">0x00000100</span></span></td>
<td><span data-ttu-id="ec810-159">Gibt an, ob die Überlagerung BT. 601 oder BT. 709 ist.</span><span class="sxs-lookup"><span data-stu-id="ec810-159">Specifies whether the overlay is BT.601 or BT.709.</span></span> <span data-ttu-id="ec810-160">Wenn dieses Flag festgelegt wird, wird "BT. 709" für High-Definition TV (HDTV) angegeben.</span><span class="sxs-lookup"><span data-stu-id="ec810-160">Setting this flag indicates BT.709, for high-definition TV (HDTV).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec810-161">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ec810-161">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ec810-162">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec810-162">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec810-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span><span class="sxs-lookup"><span data-stu-id="ec810-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span></span></td>
<td><span data-ttu-id="ec810-164">0x00000200</span><span class="sxs-lookup"><span data-stu-id="ec810-164">0x00000200</span></span></td>
<td><span data-ttu-id="ec810-165">Gibt an, ob die Überlagerung konventionelle YCbCr oder Extended YCbCr (xwycc) ist.</span><span class="sxs-lookup"><span data-stu-id="ec810-165">Specifies whether the overlay is conventional YCbCr or extended YCbCr (xvYCC).</span></span> <span data-ttu-id="ec810-166">Wenn dieses Flag festgelegt wird, wird der erweiterte YCbCr (xwycc) angegeben.</span><span class="sxs-lookup"><span data-stu-id="ec810-166">Setting this flag indicates extended YCbCr (xvYCC).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec810-167">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ec810-167">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ec810-168">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec810-168">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec810-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span><span class="sxs-lookup"><span data-stu-id="ec810-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span></span></td>
<td><span data-ttu-id="ec810-170">0x00000400</span><span class="sxs-lookup"><span data-stu-id="ec810-170">0x00000400</span></span></td>
<td><span data-ttu-id="ec810-171">Das Festlegen dieses Flags gibt an, dass die vorhandenes SwapChain geschützte Inhalte enthält und automatisch bewirkt, dass die Laufzeit den Zugriff auf die vorhandenes SwapChain einschränkt, sodass nur der Desktop-Windows-Manager (DWM) vorhandenes SwapChain verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="ec810-171">Setting this flag indicates that the swapchain contains protected content and automatically causes the runtime to restrict access to the swapchain so that only the Desktop Windows Manager (DWM) can use the swapchain.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec810-172">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ec810-172">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ec810-173">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec810-173">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec810-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span><span class="sxs-lookup"><span data-stu-id="ec810-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span></span></td>
<td><span data-ttu-id="ec810-175">0x00000800</span><span class="sxs-lookup"><span data-stu-id="ec810-175">0x00000800</span></span></td>
<td><span data-ttu-id="ec810-176">Wenn dieses Flag festgelegt wird, wird der Zugriff auf freigegebene Ressourcen, die für die DWM-Interaktion erstellt werden, durch den Treiber eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="ec810-176">Setting this flag indicates that the driver should restrict access to any shared resources that are created for DWM interaction.</span></span> <span data-ttu-id="ec810-177">Der Aufrufer muss einen authentifizierten Kanal mit dem Treiber erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec810-177">The caller must create an authenticated channel with the driver.</span></span> <span data-ttu-id="ec810-178">Der Treiber sollte dann den Zugriff auf Prozesse zulassen, die versuchen, diese freigegebenen Ressourcen zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ec810-178">The driver should then allow access to processes that attempt to open those shared resources.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec810-179">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ec810-179">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ec810-180">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec810-180">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ec810-181">Diese Konstanten werden von [**D3DPRESENT- \_ Parametern**](d3dpresent-parameters.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="ec810-181">These constants are used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="ec810-182">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="ec810-182">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="ec810-183">Header</span><span class="sxs-lookup"><span data-stu-id="ec810-183">Header</span></span>                   | <span data-ttu-id="ec810-184">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="ec810-184">d3d9types.h</span></span> |
| <span data-ttu-id="ec810-185">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="ec810-185">Minimum operating system</span></span> | <span data-ttu-id="ec810-186">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ec810-186">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="ec810-187">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec810-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec810-188">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ec810-188">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




