---
description: Von D3DPRESENT PARAMETERS verwendete \_ Konstanten.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 578d41119980719e69b9eb0e502c025414018f73
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343095"
---
# <a name="d3dpresentflag"></a><span data-ttu-id="36bc8-103">D3DPRESENTFLAG</span><span class="sxs-lookup"><span data-stu-id="36bc8-103">D3DPRESENTFLAG</span></span>

<span data-ttu-id="36bc8-104">Konstanten, die von [**D3DPRESENT PARAMETERS \_ verwendet werden.**](d3dpresent-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="36bc8-104">Constants used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36bc8-105">#Definieren</span><span class="sxs-lookup"><span data-stu-id="36bc8-105">#define</span></span></td>
<td><span data-ttu-id="36bc8-106">Wert</span><span class="sxs-lookup"><span data-stu-id="36bc8-106">Value</span></span></td>
<td><span data-ttu-id="36bc8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36bc8-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36bc8-108">D3DPRESENTFLAG_DEVICECLIP</span><span class="sxs-lookup"><span data-stu-id="36bc8-108">D3DPRESENTFLAG_DEVICECLIP</span></span></td>
<td><span data-ttu-id="36bc8-109">0x00000004</span><span class="sxs-lookup"><span data-stu-id="36bc8-109">0x00000004</span></span></td>
<td><span data-ttu-id="36bc8-110">Clip a windowed <a href="/windows/desktop/api"><strong>Present</strong></a> blit into the window client area, within the monitor screen area of the video adapter that created the Direct3D device.</span><span class="sxs-lookup"><span data-stu-id="36bc8-110">Clip a windowed <a href="/windows/desktop/api"><strong>Present</strong></a> blit into the window client area, within the monitor screen area of the video adapter that created the Direct3D device.</span></span> <span data-ttu-id="36bc8-111">D3DPRESENTFLAG_DEVICECLIP ist mit dem -D3DSWAPEFFECT_FLIPEX.</span><span class="sxs-lookup"><span data-stu-id="36bc8-111">D3DPRESENTFLAG_DEVICECLIP is not valid with D3DSWAPEFFECT_FLIPEX.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36bc8-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span><span class="sxs-lookup"><span data-stu-id="36bc8-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span></span></td>
<td><span data-ttu-id="36bc8-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="36bc8-113">0x00000002</span></span></td>
<td><span data-ttu-id="36bc8-114">Legen Sie dieses Flag fest, wenn das Gerät oder die Auslagerungskette erstellt wird, um das Z-Buffer-Verwerfen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="36bc8-114">Set this flag when the device or swap chain is created to enable z-buffer discarding.</span></span> <span data-ttu-id="36bc8-115">Wenn dieses Flag festgelegt ist, ist der Inhalt des Tiefen-Schablonenpuffers nach dem Aufruf von <a href="/windows/desktop/api"><strong>Present</strong></a>oder <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> mit einer anderen Tiefenoberfläche ungültig.</span><span class="sxs-lookup"><span data-stu-id="36bc8-115">If this flag is set, the contents of the depth stencil buffer will be invalid after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span> <span data-ttu-id="36bc8-116">Das Verwerfen von Z-Buffer-Daten kann die Leistung erhöhen und ist treiberabhängig.</span><span class="sxs-lookup"><span data-stu-id="36bc8-116">Discarding z-buffer data can increase performance and is driver dependent.</span></span> <span data-ttu-id="36bc8-117">Die Debuglaufzeit erzwingt das Verwerfen, indem der Z-Puffer auf einen konstanten Wert gelöscht wird, nachdem entweder <a href="/windows/desktop/api"><strong>Present</strong></a>oder <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> mit einer anderen Tiefenoberfläche aufruft.</span><span class="sxs-lookup"><span data-stu-id="36bc8-117">The debug runtime will enforce discarding by clearing the z-buffer to some constant value after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span><br/> <span data-ttu-id="36bc8-118">Das Verwerfen von Z-Buffer-Daten ist für alle sperrbaren Formate, Formate D3DFMT_D16_LOCKABLE und D3DFMT_D32F_LOCKABLE.</span><span class="sxs-lookup"><span data-stu-id="36bc8-118">Discarding z-buffer data is illegal for all lockable formats, D3DFMT_D16_LOCKABLE and D3DFMT_D32F_LOCKABLE.</span></span> <span data-ttu-id="36bc8-119">Bei jeder Verwendung <a href="/windows/desktop/api"><strong>von CreateDevice,</strong></a> die ein sperrbares Format und Z-Buffer-Verwerfen anknt, kommt es zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="36bc8-119">Any use of <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> specifying a lockable format and z-buffer discarding will fail.</span></span> <span data-ttu-id="36bc8-120">Weitere Informationen zu Formaten finden Sie unter <a href="d3dformat.md">D3DFORMAT</a>.</span><span class="sxs-lookup"><span data-stu-id="36bc8-120">For more information about formats, see <a href="d3dformat.md">D3DFORMAT</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36bc8-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="36bc8-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span></span></td>
<td><span data-ttu-id="36bc8-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="36bc8-122">0x00000001</span></span></td>
<td><span data-ttu-id="36bc8-123">Legen Sie dieses Flag fest, wenn die Anwendung die Möglichkeit benötigt, den Hintergrundpuffer direkt zu sperren.</span><span class="sxs-lookup"><span data-stu-id="36bc8-123">Set this flag if the application requires the ability to lock the back buffer directly.</span></span> <span data-ttu-id="36bc8-124">Beachten Sie, dass Rückpuffer nur dann gesperrt werden können, wenn die Anwendung D3DPRESENTFLAG_LOCKABLE_BACKBUFFER <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> oder <a href="/windows/desktop/api"><strong>Reset angibt.</strong></a></span><span class="sxs-lookup"><span data-stu-id="36bc8-124">Note that back buffers are not lockable unless the application specifies D3DPRESENTFLAG_LOCKABLE_BACKBUFFER when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> or <a href="/windows/desktop/api"><strong>Reset</strong></a>.</span></span> <span data-ttu-id="36bc8-125">Sperrbare Hintergrundpuffer führen bei einigen Grafikhardwarekonfigurationen zu Leistungskosten.</span><span class="sxs-lookup"><span data-stu-id="36bc8-125">Lockable back buffers incur a performance cost on some graphics hardware configurations.</span></span> <span data-ttu-id="36bc8-126">Das Ausführen eines Sperrvorgangs (oder Verwenden von <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> zum Schreiben) für den sperrbaren Hintergrundpuffer verringert die Leistung auf vielen Karten.</span><span class="sxs-lookup"><span data-stu-id="36bc8-126">Performing a lock operation (or using <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> to write) on the lockable back buffer decreases performance on many cards.</span></span> <span data-ttu-id="36bc8-127">Ziehen Sie in diesem Fall die Verwendung von strukturierten Dreiecken in Betracht, um Daten in den Hintergrundpuffer zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="36bc8-127">In this case, consider using textured triangles to move data to the back buffer.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36bc8-128">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="36bc8-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="36bc8-129">In Direct3D9Ex kann dieses Flag nicht festgelegt werden, wenn D3DSWAPEFFECT D3DSWAPEFFECT_FLIPEX ist, da das Flip-Modell dem Desktopfenster-Manager den Zugriff auf den Backpuffer einer Anwendung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="36bc8-129">In Direct3D9Ex this flag cannot be set if the D3DSWAPEFFECT is D3DSWAPEFFECT_FLIPEX, since the flip model enables the Desktop Window Manager to access an application's back buffer.</span></span> <span data-ttu-id="36bc8-130">Eine prozessübergreifende freigegebene Oberfläche sollte nicht gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="36bc8-130">A cross-process shared-surface should not be locked.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36bc8-131">D3DPRESENTFLAG_NOAUTOROTATE</span><span class="sxs-lookup"><span data-stu-id="36bc8-131">D3DPRESENTFLAG_NOAUTOROTATE</span></span></td>
<td><span data-ttu-id="36bc8-132">0x00000020</span><span class="sxs-lookup"><span data-stu-id="36bc8-132">0x00000020</span></span></td>
<td><span data-ttu-id="36bc8-133">Gedrehte Monitore werden automatisch mit einer rotierenden Kopie während der Präsentation verarbeitet, was nicht sehr effizient ist.</span><span class="sxs-lookup"><span data-stu-id="36bc8-133">Rotated monitors are handled automatically with a rotating copy during presentation, which is not very efficient.</span></span> <span data-ttu-id="36bc8-134">Dieses Flag bedeutet, dass die Anwendung ihre eigene Anzeigerotation ausführt.</span><span class="sxs-lookup"><span data-stu-id="36bc8-134">This flag means the application will perform it's own display rotation.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36bc8-135">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="36bc8-135">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="36bc8-136">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="36bc8-136">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="36bc8-137">Anwendungen können ihre eigene Drehung erreichen, möglicherweise mithilfe einer gedrehten Ansichtsmatrix.</span><span class="sxs-lookup"><span data-stu-id="36bc8-137">Applications can achieve their own rotation possibly by using a rotated view matrix.</span></span> <span data-ttu-id="36bc8-138">Die Methoden <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> und <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> sollten verwendet werden, um die aktuelle Rotationseinstellung zu finden.</span><span class="sxs-lookup"><span data-stu-id="36bc8-138">The methods <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> should be used to to find the current rotation setting.</span></span> <span data-ttu-id="36bc8-139">Die Backbufferparameter Width und Height in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> und <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> müssen querformatiert sein, während die Struktur des Vollbildanzeigemodus mit der von <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> zurückgegebenen Struktur identisch sein sollte (d. h. Breite und Höhe werden ausgetauscht, wenn sie um 90 und 270 Grad gedreht werden).</span><span class="sxs-lookup"><span data-stu-id="36bc8-139">The backbuffer Width and Height parameters in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> must be use landscape orientation, while the fullscreen display mode structure should be the same as what is returned from <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (i.e. Width and Height are swapped when rotated 90 and 270 degrees).</span></span></p>
<p><span data-ttu-id="36bc8-140">Bei Verwendung von Lock on rotated render targets (Sperren für gedrehte Renderziele) gelten annahmen in der linken oberen Ecke nicht mehr als true, das Renderziel SURFACE_DESC bleibt (wie durch die Erstellungsparameter impliziert) und GDI-Fenster, Mauskoordinaten und solche müssen ordnungsgemäß übersetzt werden, wenn sie mit dem Direct3D-Renderziel und der -Szene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36bc8-140">When using Lock on rotated render targets, upper-left corner assumptions no longer hold true, the render target SURFACE_DESC will remain landscape (as implied by the creation parameters), and GDI window, mouse coordinates, and such need to be properly translated when used with the Direct3D render target and scene.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36bc8-141">D3DPRESENTFLAG_UNPRUNEDMODE</span><span class="sxs-lookup"><span data-stu-id="36bc8-141">D3DPRESENTFLAG_UNPRUNEDMODE</span></span></td>
<td><span data-ttu-id="36bc8-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="36bc8-142">0x00000040</span></span></td>
<td><span data-ttu-id="36bc8-143">Verwenden Sie dieses Flag, um einen beliebigen RAW-Anzeigemodus anzugeben, der vom Anzeigeadapter aufzählt, obwohl Direct3D möglicherweise angegeben hat, dass der Modus ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="36bc8-143">Use this flag to specify any RAW display mode enumerated by the display adapter even though Direct3D may have indicated the mode is invalid.</span></span> <span data-ttu-id="36bc8-144">Die Anwendung sollte dies auf stabile Weise implementieren, falls der gewünschte Modus tatsächlich ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="36bc8-144">The application should implement this in a robust manner in case the desired mode really is invalid.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36bc8-145">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="36bc8-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="36bc8-146">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="36bc8-146">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36bc8-147">D3DPRESENTFLAG_VIDEO</span><span class="sxs-lookup"><span data-stu-id="36bc8-147">D3DPRESENTFLAG_VIDEO</span></span></td>
<td><span data-ttu-id="36bc8-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36bc8-148">0x00000010</span></span></td>
<td><span data-ttu-id="36bc8-149">Dies ist ein Hinweis an den Treiber, dass die Hintergrundpuffer Videodaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="36bc8-149">This is a hint to the driver that the back buffers will contain video data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36bc8-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span><span class="sxs-lookup"><span data-stu-id="36bc8-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span></span></td>
<td><span data-ttu-id="36bc8-151">0x00000080</span><span class="sxs-lookup"><span data-stu-id="36bc8-151">0x00000080</span></span></td>
<td><span data-ttu-id="36bc8-152">Gibt an, ob es sich bei der Überlagerung um einen RGB-Vollbereich oder um rgb-Bereich mit eingeschränktem Bereich handelt.</span><span class="sxs-lookup"><span data-stu-id="36bc8-152">Specifies whether the overlay is full range RGB or limited range RGB.</span></span> <span data-ttu-id="36bc8-153">Das Festlegen dieses Flags gibt den begrenzten Bereich RGB an.</span><span class="sxs-lookup"><span data-stu-id="36bc8-153">Setting this flag indicates limited range RGB.</span></span> <span data-ttu-id="36bc8-154">In einem begrenzten Bereich von RGB wird der RGB-Bereich so komprimiert, dass 16:16:16 schwarz und 235:235:235 weiß ist.</span><span class="sxs-lookup"><span data-stu-id="36bc8-154">In limited range RGB, the RGB range is compressed such that 16:16:16 is black and 235:235:235 is white.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36bc8-155">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="36bc8-155">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="36bc8-156">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="36bc8-156">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36bc8-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span><span class="sxs-lookup"><span data-stu-id="36bc8-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span></span></td>
<td><span data-ttu-id="36bc8-158">0x00000100</span><span class="sxs-lookup"><span data-stu-id="36bc8-158">0x00000100</span></span></td>
<td><span data-ttu-id="36bc8-159">Gibt an, ob die Überlagerung BT.601 oder BT.709 ist.</span><span class="sxs-lookup"><span data-stu-id="36bc8-159">Specifies whether the overlay is BT.601 or BT.709.</span></span> <span data-ttu-id="36bc8-160">Wenn Sie dieses Flag festlegen, wird BT.709 für high-definition TV (GS) angegeben.</span><span class="sxs-lookup"><span data-stu-id="36bc8-160">Setting this flag indicates BT.709, for high-definition TV (HDTV).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36bc8-161">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="36bc8-161">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="36bc8-162">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="36bc8-162">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36bc8-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span><span class="sxs-lookup"><span data-stu-id="36bc8-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span></span></td>
<td><span data-ttu-id="36bc8-164">0x00000200</span><span class="sxs-lookup"><span data-stu-id="36bc8-164">0x00000200</span></span></td>
<td><span data-ttu-id="36bc8-165">Gibt an, ob die Überlagerung konventioneller YCbCr oder erweiterter YCbCr (xvYCC) ist.</span><span class="sxs-lookup"><span data-stu-id="36bc8-165">Specifies whether the overlay is conventional YCbCr or extended YCbCr (xvYCC).</span></span> <span data-ttu-id="36bc8-166">Das Festlegen dieses Flags gibt die erweiterte YCbCr (xvYCC) an.</span><span class="sxs-lookup"><span data-stu-id="36bc8-166">Setting this flag indicates extended YCbCr (xvYCC).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36bc8-167">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="36bc8-167">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="36bc8-168">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="36bc8-168">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36bc8-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span><span class="sxs-lookup"><span data-stu-id="36bc8-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span></span></td>
<td><span data-ttu-id="36bc8-170">0x00000400</span><span class="sxs-lookup"><span data-stu-id="36bc8-170">0x00000400</span></span></td>
<td><span data-ttu-id="36bc8-171">Das Festlegen dieses Flags gibt an, dass die Swapkette geschützte Inhalte enthält und automatisch bewirkt, dass die Laufzeit den Zugriff auf die Swapkette einschränkt, sodass nur der Desktop-Windows-Manager (DWM) die Swapkette verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="36bc8-171">Setting this flag indicates that the swapchain contains protected content and automatically causes the runtime to restrict access to the swapchain so that only the Desktop Windows Manager (DWM) can use the swapchain.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36bc8-172">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="36bc8-172">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="36bc8-173">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="36bc8-173">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36bc8-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span><span class="sxs-lookup"><span data-stu-id="36bc8-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span></span></td>
<td><span data-ttu-id="36bc8-175">0x00000800</span><span class="sxs-lookup"><span data-stu-id="36bc8-175">0x00000800</span></span></td>
<td><span data-ttu-id="36bc8-176">Das Festlegen dieses Flags gibt an, dass der Treiber den Zugriff auf alle freigegebenen Ressourcen einschränken soll, die für die DWM-Interaktion erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="36bc8-176">Setting this flag indicates that the driver should restrict access to any shared resources that are created for DWM interaction.</span></span> <span data-ttu-id="36bc8-177">Der Aufrufer muss einen authentifizierten Kanal mit dem Treiber erstellen.</span><span class="sxs-lookup"><span data-stu-id="36bc8-177">The caller must create an authenticated channel with the driver.</span></span> <span data-ttu-id="36bc8-178">Der Treiber sollte dann den Zugriff auf Prozesse zulassen, die versuchen, diese freigegebenen Ressourcen zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="36bc8-178">The driver should then allow access to processes that attempt to open those shared resources.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36bc8-179">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="36bc8-179">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="36bc8-180">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="36bc8-180">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="36bc8-181">Diese Konstanten werden von [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="36bc8-181">These constants are used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="36bc8-182">Konstanteninformationen</span><span class="sxs-lookup"><span data-stu-id="36bc8-182">Constant Information</span></span>



| <span data-ttu-id="36bc8-183">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36bc8-183">Requirement</span></span>                         | <span data-ttu-id="36bc8-184">Wert</span><span class="sxs-lookup"><span data-stu-id="36bc8-184">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="36bc8-185">Header</span><span class="sxs-lookup"><span data-stu-id="36bc8-185">Header</span></span>                   | <span data-ttu-id="36bc8-186">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="36bc8-186">d3d9types.h</span></span> |
| <span data-ttu-id="36bc8-187">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="36bc8-187">Minimum operating system</span></span> | <span data-ttu-id="36bc8-188">Windows 98</span><span class="sxs-lookup"><span data-stu-id="36bc8-188">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="36bc8-189">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36bc8-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36bc8-190">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="36bc8-190">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




