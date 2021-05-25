---
description: Beschreibt die Präsentationsparameter.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: D3DPRESENT_PARAMETERS-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENT_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f113b3df247765b958dfe47bb04fafb6c9a13bbe
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343105"
---
# <a name="d3dpresent_parameters-structure"></a><span data-ttu-id="c96ba-103">D3DPRESENT \_ PARAMETERS-Struktur</span><span class="sxs-lookup"><span data-stu-id="c96ba-103">D3DPRESENT\_PARAMETERS structure</span></span>

<span data-ttu-id="c96ba-104">Beschreibt die Präsentationsparameter.</span><span class="sxs-lookup"><span data-stu-id="c96ba-104">Describes the presentation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="c96ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c96ba-105">Syntax</span></span>


```C++
typedef struct D3DPRESENT_PARAMETERS {
  UINT                BackBufferWidth;
  UINT                BackBufferHeight;
  D3DFORMAT           BackBufferFormat;
  UINT                BackBufferCount;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  D3DSWAPEFFECT       SwapEffect;
  HWND                hDeviceWindow;
  BOOL                Windowed;
  BOOL                EnableAutoDepthStencil;
  D3DFORMAT           AutoDepthStencilFormat;
  DWORD               Flags;
  UINT                FullScreen_RefreshRateInHz;
  UINT                PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="c96ba-106">Member</span><span class="sxs-lookup"><span data-stu-id="c96ba-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c96ba-107">**BackBufferWidth**</span><span class="sxs-lookup"><span data-stu-id="c96ba-107">**BackBufferWidth**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-109">Breite der Rückpuffer der neuen Swapkette in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c96ba-109">Width of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="c96ba-110">Wenn **Windowed** auf **FALSE** festgelegt ist (die Präsentation ist vollbildbereit), muss dieser Wert der Breite eines der aufzählten Anzeigemodi entsprechen, die über [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c96ba-110">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the width of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="c96ba-111">Wenn **Windowed** **true** ist und entweder **BackBufferWidth** oder **BackBufferHeight** 0 (null) ist, wird die entsprechende Dimension des Clientbereichs von **hDeviceWindow** (oder das Fokusfenster, wenn **hDeviceWindow** **NULL** ist) übernommen.</span><span class="sxs-lookup"><span data-stu-id="c96ba-111">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="c96ba-112">**BackBufferHeight**</span><span class="sxs-lookup"><span data-stu-id="c96ba-112">**BackBufferHeight**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-113">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-114">Höhe der Rückpuffer der neuen Swapkette in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c96ba-114">Height of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="c96ba-115">Wenn **Windowed** auf **FALSE** festgelegt ist (die Darstellung im Vollbildmodus), muss dieser Wert der Höhe eines der aufzählten Anzeigemodi entsprechen, die über [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c96ba-115">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the height of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="c96ba-116">Wenn **Windowed** **true** ist und entweder **BackBufferWidth** oder **BackBufferHeight** 0 (null) ist, wird die entsprechende Dimension des Clientbereichs von **hDeviceWindow** (oder das Fokusfenster, wenn **hDeviceWindow** **NULL** ist) übernommen.</span><span class="sxs-lookup"><span data-stu-id="c96ba-116">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="c96ba-117">**BackBufferFormat**</span><span class="sxs-lookup"><span data-stu-id="c96ba-117">**BackBufferFormat**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-118">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-119">Das Backpufferformat.</span><span class="sxs-lookup"><span data-stu-id="c96ba-119">The back buffer format.</span></span> <span data-ttu-id="c96ba-120">Weitere Informationen zu Formaten finden Sie unter [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="c96ba-120">For more information about formats, see [D3DFORMAT](d3dformat.md).</span></span> <span data-ttu-id="c96ba-121">Dieser Wert muss eines der Renderzielformate sein, wie von [**CheckDeviceType**](/windows/desktop/api)überprüft.</span><span class="sxs-lookup"><span data-stu-id="c96ba-121">This value must be one of the render-target formats as validated by [**CheckDeviceType**](/windows/desktop/api).</span></span> <span data-ttu-id="c96ba-122">Sie können [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) verwenden, um das aktuelle Format abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c96ba-122">You can use [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) to obtain the current format.</span></span>

<span data-ttu-id="c96ba-123">Tatsächlich kann D3DFMT UNKNOWN für \_ **das BackBufferFormat** im Fenstermodus angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c96ba-123">In fact, D3DFMT\_UNKNOWN can be specified for the **BackBufferFormat** while in windowed mode.</span></span> <span data-ttu-id="c96ba-124">Dies weist die Runtime an, das aktuelle Anzeigemodusformat zu verwenden, und macht es nicht mehr notwendig, [**GetDisplayMode auf aufruft.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)</span><span class="sxs-lookup"><span data-stu-id="c96ba-124">This tells the runtime to use the current display-mode format and eliminates the need to call [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span></span>

<span data-ttu-id="c96ba-125">Bei Anwendungen mit Fenstern muss das Format des Hintergrundpuffers nicht mehr mit dem Anzeigemodusformat übereinstimmen, da die Farbkonvertierung jetzt von der Hardware durchgeführt werden kann (wenn die Hardware die Farbkonvertierung unterstützt).</span><span class="sxs-lookup"><span data-stu-id="c96ba-125">For windowed applications, the back buffer format no longer needs to match the display-mode format because color conversion can now be done by the hardware (if the hardware supports color conversion).</span></span> <span data-ttu-id="c96ba-126">Der Satz möglicher Backpufferformate ist eingeschränkt, aber die Laufzeit lässt zu, dass jedes gültige Backpufferformat in jedem Desktopformat dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c96ba-126">The set of possible back buffer formats is constrained, but the runtime will allow any valid back buffer format to be presented to any desktop format.</span></span> <span data-ttu-id="c96ba-127">(Es gibt die zusätzliche Anforderung, dass das Gerät auf dem Desktop ausgeführt werden kann. Geräte arbeiten in der Regel nicht mit 8 Bits pro Pixelmodus.)</span><span class="sxs-lookup"><span data-stu-id="c96ba-127">(There is the additional requirement that the device be operable in the desktop; devices typically do not operate in 8 bits per pixel modes.)</span></span>

<span data-ttu-id="c96ba-128">Vollbildanwendungen können keine Farbkonvertierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="c96ba-128">Full-screen applications cannot do color conversion.</span></span>

</dd> <dt>

<span data-ttu-id="c96ba-129">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="c96ba-129">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-130">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-131">Dieser Wert kann zwischen 0 und [D3DPRESENT \_ BACK \_ BUFFERS \_ MAX](d3dpresent-back-buffers.md) (oder [D3DPRESENT \_ BACK \_ BUFFERS MAX \_ \_ EX](d3dpresent-back-buffers.md) bei Verwendung von Direct3D 9Ex) liegen.</span><span class="sxs-lookup"><span data-stu-id="c96ba-131">This value can be between 0 and [D3DPRESENT\_BACK\_BUFFERS\_MAX](d3dpresent-back-buffers.md) (or [D3DPRESENT\_BACK\_BUFFERS\_MAX\_EX](d3dpresent-back-buffers.md) when using Direct3D 9Ex).</span></span> <span data-ttu-id="c96ba-132">Werte von 0 werden als 1 behandelt.</span><span class="sxs-lookup"><span data-stu-id="c96ba-132">Values of 0 are treated as 1.</span></span> <span data-ttu-id="c96ba-133">Wenn die Anzahl der Backpuffer nicht erstellt werden kann, erzeugt die Laufzeit einen Fehler beim Methodenaufruf und füllt diesen Wert mit der Anzahl der Backpuffer auf, die erstellt werden könnten.</span><span class="sxs-lookup"><span data-stu-id="c96ba-133">If the number of back buffers cannot be created, the runtime will fail the method call and fill this value with the number of back buffers that could be created.</span></span> <span data-ttu-id="c96ba-134">Daher kann eine Anwendung die -Methode zweimal mit derselben D3DPRESENT PARAMETERS-Struktur aufrufen und erwarten, dass sie beim \_ zweiten Mal funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c96ba-134">As a result, an application can call the method twice with the same D3DPRESENT\_PARAMETERS structure and expect it to work the second time.</span></span>

<span data-ttu-id="c96ba-135">Die Methode schlägt fehl, wenn kein Backpuffer erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c96ba-135">The method fails if one back buffer cannot be created.</span></span> <span data-ttu-id="c96ba-136">Der Wert von **BackBufferCount beeinflusst,** welche Swapeffekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c96ba-136">The value of **BackBufferCount** influences what set of swap effects are allowed.</span></span> <span data-ttu-id="c96ba-137">Insbesondere erfordert jeder D3DSWAPEFFECT \_ COPY-Auslagerungseffekt genau einen Hintergrundpuffer.</span><span class="sxs-lookup"><span data-stu-id="c96ba-137">Specifically, any D3DSWAPEFFECT\_COPY swap effect requires that there be exactly one back buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c96ba-138">**MultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="c96ba-138">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-139">Typ: **[ **D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-139">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-140">Member des [**aufzählten D3DMULTISAMPLE \_ TYPE-Typs.**](./d3dmultisample-type.md)</span><span class="sxs-lookup"><span data-stu-id="c96ba-140">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="c96ba-141">Der Wert muss D3DMULTISAMPLE NONE sein, es sei \_ **denn, SwapEffect** wurde auf D3DSWAPEFFECT \_ DISCARD festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c96ba-141">The value must be D3DMULTISAMPLE\_NONE unless **SwapEffect** has been set to D3DSWAPEFFECT\_DISCARD.</span></span> <span data-ttu-id="c96ba-142">Multisampling wird nur unterstützt, wenn der Swapeffekt D3DSWAPEFFECT \_ DISCARD ist.</span><span class="sxs-lookup"><span data-stu-id="c96ba-142">Multisampling is supported only if the swap effect is D3DSWAPEFFECT\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="c96ba-143">**MultiSampleQuality**</span><span class="sxs-lookup"><span data-stu-id="c96ba-143">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-144">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-145">Qualitätsstufe.</span><span class="sxs-lookup"><span data-stu-id="c96ba-145">Quality level.</span></span> <span data-ttu-id="c96ba-146">Der gültige Bereich liegt zwischen 0 (null) und 1 kleiner als die von "pQualityLevels" zurückgegebene Ebene, die von [**CheckDeviceMultiSampleType**](/windows/desktop/api)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c96ba-146">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span></span> <span data-ttu-id="c96ba-147">Wenn Sie einen größeren Wert übergeben, wird der Fehler D3DERR \_ INVALIDCALL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c96ba-147">Passing a larger value returns the error D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="c96ba-148">Gekoppelte Werte von Renderzielen oder Tiefenschablonenoberflächen und [**D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md) müssen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c96ba-148">Paired values of render targets or of depth stencil surfaces and [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) must match.</span></span>

</dd> <dt>

<span data-ttu-id="c96ba-149">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="c96ba-149">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-150">Typ: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-150">Type: **[**D3DSWAPEFFECT**](./d3dswapeffect.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-151">Member des [**D3DSWAPEFFECT-Enumerationstyps.**](./d3dswapeffect.md)</span><span class="sxs-lookup"><span data-stu-id="c96ba-151">Member of the [**D3DSWAPEFFECT**](./d3dswapeffect.md) enumerated type.</span></span> <span data-ttu-id="c96ba-152">Die Laufzeit garantiert die implizite Semantik in Bezug auf das Pufferaustauschverhalten. Wenn **Windowed** daher **TRUE** ist und **SwapEffect** auf D3DSWAPEFFECT FLIP festgelegt \_ ist, erstellt die Laufzeit einen zusätzlichen Backpuffer und kopiert den Puffer, der zur Präsentationszeit zum Frontpuffer wird.</span><span class="sxs-lookup"><span data-stu-id="c96ba-152">The runtime will guarantee the implied semantics concerning buffer swap behavior; therefore, if **Windowed** is **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIP, the runtime will create one extra back buffer and copy whichever becomes the front buffer at presentation time.</span></span>

<span data-ttu-id="c96ba-153">D3DSWAPEFFECT \_ COPY erfordert, dass **BackBufferCount** auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c96ba-153">D3DSWAPEFFECT\_COPY requires that **BackBufferCount** be set to 1.</span></span>

<span data-ttu-id="c96ba-154">D3DSWAPEFFECT \_ DISCARD wird in der Debuglaufzeit erzwungen, indem nach der Darstellung ein beliebiger Puffer mit Rauschen gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="c96ba-154">D3DSWAPEFFECT\_DISCARD will be enforced in the debug runtime by filling any buffer with noise after it is presented.</span></span>

<span data-ttu-id="c96ba-155">Unterschiede zwischen Direct3D9 und Direct3D9Ex:</span><span class="sxs-lookup"><span data-stu-id="c96ba-155">Differences between Direct3D9 and Direct3D9Ex:</span></span>

- <span data-ttu-id="c96ba-156">In Direct3D9Ex wird D3DSWAPEFFECT \_ FLIPEX hinzugefügt, um festzulegen, wann eine Anwendung den Flip-Modus einnimmt.</span><span class="sxs-lookup"><span data-stu-id="c96ba-156">In Direct3D9Ex, D3DSWAPEFFECT\_FLIPEX is added to designate when an application is adopting flip mode.</span></span> <span data-ttu-id="c96ba-157">Das heißt, der Frame einer Anwendung wird im Fenstermodus (statt kopiert) zur Komposition an den Desktopfenster-Manager (DWM) übergeben.</span><span class="sxs-lookup"><span data-stu-id="c96ba-157">That is, whan an application's frame is passed in window's mode (instead of copied) to the Desktop Window Manager(DWM) for composition.</span></span> <span data-ttu-id="c96ba-158">Der Flip-Modus bietet eine effizientere Speicherbandbreite und ermöglicht einer Anwendung die Nutzung von Statistiken im Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="c96ba-158">Flip mode provides more efficient memory bandwidth and enables an application to take advantage of full-screen-present statistics.</span></span> <span data-ttu-id="c96ba-159">Das Vollbildverhalten wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="c96ba-159">It does not change full screen behavior.</span></span> <span data-ttu-id="c96ba-160">Das Flipmodusverhalten ist ab Windows 7 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c96ba-160">Flip mode behavior is available beginning with Windows 7.</span></span>



 

</dd> <dt>

<span data-ttu-id="c96ba-161">**hDeviceWindow**</span><span class="sxs-lookup"><span data-stu-id="c96ba-161">**hDeviceWindow**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-162">Typ: **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-162">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-163">Das Gerätefenster bestimmt den Speicherort und die Größe des Hintergrundpuffers auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="c96ba-163">The device window determines the location and size of the back buffer on screen.</span></span> <span data-ttu-id="c96ba-164">Dies wird von Direct3D verwendet, wenn der Inhalt des Hintergrundpuffers während present in den Frontpuffer [**kopiert wird.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)</span><span class="sxs-lookup"><span data-stu-id="c96ba-164">This is used by Direct3D when the back buffer contents are copied to the front buffer during [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

-   <span data-ttu-id="c96ba-165">Bei einer Vollbildanwendung ist dies ein Handle für das obere Fenster (das Fokusfenster).</span><span class="sxs-lookup"><span data-stu-id="c96ba-165">For a full-screen application, this is a handle to the top window (which is the focus window).</span></span>

    <span data-ttu-id="c96ba-166">Für Anwendungen, die mehrere Vollbildgeräte verwenden (z. B. ein System mit mehreren Monitoren), kann genau ein Gerät das Fokusfenster als Gerätefenster verwenden.</span><span class="sxs-lookup"><span data-stu-id="c96ba-166">For applications that use multiple full-screen devices (such as a multimonitor system), exactly one device can use the focus window as the device window.</span></span> <span data-ttu-id="c96ba-167">Alle anderen Geräte müssen über eindeutige Gerätefenster verfügen.</span><span class="sxs-lookup"><span data-stu-id="c96ba-167">All other devices must have unique device windows.</span></span>

-   <span data-ttu-id="c96ba-168">Für eine Anwendung im Fenstermodus ist dieses Handle das Standardzielfenster für [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="c96ba-168">For a windowed-mode application, this handle will be the default target window for [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="c96ba-169">Wenn dieses Handle NULL **ist,** wird das Fokusfenster verwendet.</span><span class="sxs-lookup"><span data-stu-id="c96ba-169">If this handle is **NULL**, the focus window will be taken.</span></span>

<span data-ttu-id="c96ba-170">Beachten Sie, dass die Runtime nicht versucht, Benutzeränderungen in der Fenstergröße widerzu spiegeln.</span><span class="sxs-lookup"><span data-stu-id="c96ba-170">Note that no attempt is made by the runtime to reflect user changes in window size.</span></span> <span data-ttu-id="c96ba-171">Der Hintergrundpuffer wird nicht implizit zurückgesetzt, wenn dieses Fenster zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c96ba-171">The back buffer is not implicitly reset when this window is reset.</span></span> <span data-ttu-id="c96ba-172">Die [**Present-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) verfolgt änderungen an der Fensterposition jedoch automatisch nach.</span><span class="sxs-lookup"><span data-stu-id="c96ba-172">However, the [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method does automatically track window position changes.</span></span>

</dd> <dt>

<span data-ttu-id="c96ba-173">**Fenstermodus**</span><span class="sxs-lookup"><span data-stu-id="c96ba-173">**Windowed**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-174">Typ: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-174">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-175">**TRUE,** wenn die Anwendung im Fenster ausgeführt wird; **FALSE,** wenn die Anwendung im Vollbildmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c96ba-175">**TRUE** if the application runs windowed; **FALSE** if the application runs full-screen.</span></span>

</dd> <dt>

<span data-ttu-id="c96ba-176">**EnableAutoDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="c96ba-176">**EnableAutoDepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-177">Typ: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-177">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-178">Wenn dieser Wert **TRUE ist,** verwaltet Direct3D Tiefenpuffer für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c96ba-178">If this value is **TRUE**, Direct3D will manage depth buffers for the application.</span></span> <span data-ttu-id="c96ba-179">Das Gerät erstellt einen Tiefen-Schablonenpuffer, wenn es erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c96ba-179">The device will create a depth-stencil buffer when it is created.</span></span> <span data-ttu-id="c96ba-180">Der Tiefen-Schablonenpuffer wird automatisch als Renderziel des Geräts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c96ba-180">The depth-stencil buffer will be automatically set as the render target of the device.</span></span> <span data-ttu-id="c96ba-181">Wenn das Gerät zurückgesetzt wird, wird der Tiefen-Schablonenpuffer automatisch zerstört und in der neuen Größe neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="c96ba-181">When the device is reset, the depth-stencil buffer will be automatically destroyed and recreated in the new size.</span></span>

<span data-ttu-id="c96ba-182">Wenn EnableAutoDepthStencil **true** ist, muss AutoDepthStencilFormat ein gültiges Tiefen-Schablonenformat sein.</span><span class="sxs-lookup"><span data-stu-id="c96ba-182">If EnableAutoDepthStencil is **TRUE**, then AutoDepthStencilFormat must be a valid depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="c96ba-183">**AutoDepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="c96ba-183">**AutoDepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-184">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-184">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-185">Member des [D3DFORMAT-Enumerationstyps.](d3dformat.md)</span><span class="sxs-lookup"><span data-stu-id="c96ba-185">Member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="c96ba-186">Das Format der automatischen Tiefenschablonenoberfläche, die das Gerät erstellt.</span><span class="sxs-lookup"><span data-stu-id="c96ba-186">The format of the automatic depth-stencil surface that the device will create.</span></span> <span data-ttu-id="c96ba-187">Dieser Member wird ignoriert, es sei **denn, EnableAutoDepthStencil** ist **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="c96ba-187">This member is ignored unless **EnableAutoDepthStencil** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="c96ba-188">**Flags**</span><span class="sxs-lookup"><span data-stu-id="c96ba-188">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-189">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-189">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-190">Eine der [D3DPRESENTFLAG-Konstanten.](d3dpresentflag.md)</span><span class="sxs-lookup"><span data-stu-id="c96ba-190">One of the [D3DPRESENTFLAG](d3dpresentflag.md) constants.</span></span>

</dd> <dt>

<span data-ttu-id="c96ba-191">**FullScreen \_ RefreshRateInHz**</span><span class="sxs-lookup"><span data-stu-id="c96ba-191">**FullScreen\_RefreshRateInHz**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-192">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-192">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-193">Die Rate, mit der der Anzeigeadapter den Bildschirm aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c96ba-193">The rate at which the display adapter refreshes the screen.</span></span> <span data-ttu-id="c96ba-194">Der Wert hängt vom Modus ab, in dem die Anwendung ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="c96ba-194">The value depends on the mode in which the application is running:</span></span>

-   <span data-ttu-id="c96ba-195">Für den Fenstermodus muss die Aktualisierungsrate 0 sein.</span><span class="sxs-lookup"><span data-stu-id="c96ba-195">For windowed mode, the refresh rate must be 0.</span></span>
-   <span data-ttu-id="c96ba-196">Für den Vollbildmodus ist die Aktualisierungsrate eine der Aktualisierungsraten, die von [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c96ba-196">For full-screen mode, the refresh rate is one of the refresh rates returned by [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>

</dd> <dt>

<span data-ttu-id="c96ba-197">**PresentationInterval**</span><span class="sxs-lookup"><span data-stu-id="c96ba-197">**PresentationInterval**</span></span>
</dt> <dd>

<span data-ttu-id="c96ba-198">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c96ba-198">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c96ba-199">Die maximale Rate, mit der die Hintergrundpuffer der Swapkette dem Frontpuffer angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="c96ba-199">The maximum rate at which the swap chain's back buffers can be presented to the front buffer.</span></span> <span data-ttu-id="c96ba-200">Eine ausführliche Erläuterung der unterstützten Modi und Intervalle finden Sie unter [D3DPRESENT](d3dpresent.md).</span><span class="sxs-lookup"><span data-stu-id="c96ba-200">For a detailed explanation of the modes and the intervals that are supported, see [D3DPRESENT](d3dpresent.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c96ba-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c96ba-201">Requirements</span></span>



| <span data-ttu-id="c96ba-202">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c96ba-202">Requirement</span></span> | <span data-ttu-id="c96ba-203">Wert</span><span class="sxs-lookup"><span data-stu-id="c96ba-203">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c96ba-204">Header</span><span class="sxs-lookup"><span data-stu-id="c96ba-204">Header</span></span><br/> | <dl> <span data-ttu-id="c96ba-205"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="c96ba-205"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c96ba-206">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c96ba-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c96ba-207">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c96ba-207">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="c96ba-208">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="c96ba-208">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="c96ba-209">**CreateAdditionalSwapChain**</span><span class="sxs-lookup"><span data-stu-id="c96ba-209">**CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[<span data-ttu-id="c96ba-210">**Present**</span><span class="sxs-lookup"><span data-stu-id="c96ba-210">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[<span data-ttu-id="c96ba-211">**Reset**</span><span class="sxs-lookup"><span data-stu-id="c96ba-211">**Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
