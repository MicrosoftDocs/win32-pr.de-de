---
description: Beschreibt die Präsentations Parameter.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: D3DPRESENT_PARAMETERS-Struktur (D3D9Types. h)
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
ms.openlocfilehash: f83ab03773356a01c8c6ac490bb099c6e7508be2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355057"
---
# <a name="d3dpresent_parameters-structure"></a><span data-ttu-id="ea95d-103">D3DPRESENT \_ Parameters-Struktur</span><span class="sxs-lookup"><span data-stu-id="ea95d-103">D3DPRESENT\_PARAMETERS structure</span></span>

<span data-ttu-id="ea95d-104">Beschreibt die Präsentations Parameter.</span><span class="sxs-lookup"><span data-stu-id="ea95d-104">Describes the presentation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea95d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea95d-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="ea95d-106">Member</span><span class="sxs-lookup"><span data-stu-id="ea95d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ea95d-107">**BackBufferWidth**</span><span class="sxs-lookup"><span data-stu-id="ea95d-107">**BackBufferWidth**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-109">Breite der Hintergrund Puffer der neuen Austausch Kette in Pixel.</span><span class="sxs-lookup"><span data-stu-id="ea95d-109">Width of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="ea95d-110">Wenn " **Windowed** " den Wert " **false** " hat (die Präsentation ist voll Bildschirm), muss dieser Wert mit der Breite eines der aufgelisteten Anzeigemodi identisch sein, die über [**enumadaptermodes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="ea95d-110">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the width of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="ea95d-111">Wenn **Windowed** den Wert **true** aufweist und entweder **BackBufferWidth** oder **BackBufferHeight** gleich NULL ist, wird die entsprechende Dimension des Client Bereichs von **hdevicewindow** (oder im Fokus Fenster, wenn **hdevicewindow** **null** ist) übernommen.</span><span class="sxs-lookup"><span data-stu-id="ea95d-111">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="ea95d-112">**BackBufferHeight**</span><span class="sxs-lookup"><span data-stu-id="ea95d-112">**BackBufferHeight**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-113">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-114">Die Höhe der Hintergrund Puffer der neuen Austausch Kette in Pixel.</span><span class="sxs-lookup"><span data-stu-id="ea95d-114">Height of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="ea95d-115">Wenn " **Windowed** " den Wert " **false** " hat (die Präsentation ist voll Bildschirm), muss dieser Wert mit der Höhe eines der aufgelisteten Anzeigemodi identisch sein, die über [**enumadaptermodes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="ea95d-115">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the height of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="ea95d-116">Wenn **Windowed** den Wert **true** aufweist und entweder **BackBufferWidth** oder **BackBufferHeight** gleich NULL ist, wird die entsprechende Dimension des Client Bereichs von **hdevicewindow** (oder im Fokus Fenster, wenn **hdevicewindow** **null** ist) übernommen.</span><span class="sxs-lookup"><span data-stu-id="ea95d-116">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="ea95d-117">**Backbufferformat**</span><span class="sxs-lookup"><span data-stu-id="ea95d-117">**BackBufferFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-118">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-119">Das Format des Hintergrund Puffers.</span><span class="sxs-lookup"><span data-stu-id="ea95d-119">The back buffer format.</span></span> <span data-ttu-id="ea95d-120">Weitere Informationen zu Formaten finden Sie unter [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="ea95d-120">For more information about formats, see [D3DFORMAT](d3dformat.md).</span></span> <span data-ttu-id="ea95d-121">Bei diesem Wert muss es sich um eines der renderzielformate handeln, die von [**CheckDeviceType**](/windows/desktop/api)überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="ea95d-121">This value must be one of the render-target formats as validated by [**CheckDeviceType**](/windows/desktop/api).</span></span> <span data-ttu-id="ea95d-122">Sie können [**getdisplaymode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) zum Abrufen des aktuellen Formats verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea95d-122">You can use [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) to obtain the current format.</span></span>

<span data-ttu-id="ea95d-123">Tatsächlich \_ kann D3DFMT Unknown für das **backbufferformat** im Fenstermodus angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ea95d-123">In fact, D3DFMT\_UNKNOWN can be specified for the **BackBufferFormat** while in windowed mode.</span></span> <span data-ttu-id="ea95d-124">Dadurch wird der Laufzeit mitgeteilt, dass das aktuelle Anzeigemodus-Format verwendet wird, und es entfällt, dass [**getdisplaymode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="ea95d-124">This tells the runtime to use the current display-mode format and eliminates the need to call [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span></span>

<span data-ttu-id="ea95d-125">Für Fenster Anwendungen muss das Hintergrund Puffer Format nicht mehr dem Anzeigemodus entsprechen, da die Farbkonvertierung nun von der Hardware durchgeführt werden kann (wenn die Hardware Farbkonvertierung unterstützt).</span><span class="sxs-lookup"><span data-stu-id="ea95d-125">For windowed applications, the back buffer format no longer needs to match the display-mode format because color conversion can now be done by the hardware (if the hardware supports color conversion).</span></span> <span data-ttu-id="ea95d-126">Der Satz möglicher backpufferformate ist eingeschränkt, aber die Laufzeit lässt zu, dass jedes beliebige gültige Hintergrund Puffer Format allen Desktop Formaten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ea95d-126">The set of possible back buffer formats is constrained, but the runtime will allow any valid back buffer format to be presented to any desktop format.</span></span> <span data-ttu-id="ea95d-127">(Es ist erforderlich, dass das Gerät auf dem Desktop betriebsbereit ist. Geräte funktionieren in der Regel nicht im Modus von 8 Bits pro Pixel.)</span><span class="sxs-lookup"><span data-stu-id="ea95d-127">(There is the additional requirement that the device be operable in the desktop; devices typically do not operate in 8 bits per pixel modes.)</span></span>

<span data-ttu-id="ea95d-128">Vollbildanwendungen können keine Farbkonvertierung durchführen.</span><span class="sxs-lookup"><span data-stu-id="ea95d-128">Full-screen applications cannot do color conversion.</span></span>

</dd> <dt>

<span data-ttu-id="ea95d-129">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="ea95d-129">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-130">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-131">Dieser Wert kann zwischen 0 und [D3DPRESENT \_ Back \_ Puffern \_ Max](d3dpresent-back-buffers.md) (oder [D3DPRESENT \_ Back \_ Puffern \_ Max \_ Ex](d3dpresent-back-buffers.md) bei Verwendung von Direct3D 9Ex) liegen.</span><span class="sxs-lookup"><span data-stu-id="ea95d-131">This value can be between 0 and [D3DPRESENT\_BACK\_BUFFERS\_MAX](d3dpresent-back-buffers.md) (or [D3DPRESENT\_BACK\_BUFFERS\_MAX\_EX](d3dpresent-back-buffers.md) when using Direct3D 9Ex).</span></span> <span data-ttu-id="ea95d-132">Werte von 0 werden als 1 behandelt.</span><span class="sxs-lookup"><span data-stu-id="ea95d-132">Values of 0 are treated as 1.</span></span> <span data-ttu-id="ea95d-133">Wenn die Anzahl der Back Puffer nicht erstellt werden kann, misslingt die Laufzeit den Methoden Aufrufvorgang und füllen diesen Wert mit der Anzahl der zu erstellenden Sicherungs Puffer aus.</span><span class="sxs-lookup"><span data-stu-id="ea95d-133">If the number of back buffers cannot be created, the runtime will fail the method call and fill this value with the number of back buffers that could be created.</span></span> <span data-ttu-id="ea95d-134">Daher kann eine Anwendung die Methode zweimal mit der gleichen D3DPRESENT \_ Parameters-Struktur abrufen und erwarten, dass Sie beim zweiten Mal funktioniert.</span><span class="sxs-lookup"><span data-stu-id="ea95d-134">As a result, an application can call the method twice with the same D3DPRESENT\_PARAMETERS structure and expect it to work the second time.</span></span>

<span data-ttu-id="ea95d-135">Die Methode schlägt fehl, wenn ein BackBuffer nicht erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ea95d-135">The method fails if one back buffer cannot be created.</span></span> <span data-ttu-id="ea95d-136">Der Wert von **BackBufferCount** wirkt sich darauf aus, welche Gruppe von Swap-Effekten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ea95d-136">The value of **BackBufferCount** influences what set of swap effects are allowed.</span></span> <span data-ttu-id="ea95d-137">Insbesondere ist es erforderlich, dass für jeden D3DSWAPEFFECT-Auslagerungs \_ Effekt genau ein Hintergrund Puffer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ea95d-137">Specifically, any D3DSWAPEFFECT\_COPY swap effect requires that there be exactly one back buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ea95d-138">**MultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="ea95d-138">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-139">Type: **[ **D3DMULTISAMPLE- \_ Typ**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-139">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-140">Member des [**D3DMULTISAMPLE \_ Type**](./d3dmultisample-type.md) -enumerierten Typs.</span><span class="sxs-lookup"><span data-stu-id="ea95d-140">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="ea95d-141">Der Wert muss D3DMULTISAMPLE \_ None lauten, es sei denn, für " **Swap** " wurde "D3DSWAPEFFECT DISCARD" festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="ea95d-141">The value must be D3DMULTISAMPLE\_NONE unless **SwapEffect** has been set to D3DSWAPEFFECT\_DISCARD.</span></span> <span data-ttu-id="ea95d-142">Multisampling wird nur unterstützt, wenn der Auslagerungs Effekt D3DSWAPEFFECT \_ verwerfen ist.</span><span class="sxs-lookup"><span data-stu-id="ea95d-142">Multisampling is supported only if the swap effect is D3DSWAPEFFECT\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="ea95d-143">**Multisamplequality**</span><span class="sxs-lookup"><span data-stu-id="ea95d-143">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-144">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-145">Qualitätsstufe.</span><span class="sxs-lookup"><span data-stu-id="ea95d-145">Quality level.</span></span> <span data-ttu-id="ea95d-146">Der gültige Bereich liegt zwischen 0 (null) und einem niedrigeren Wert als der von " [**checkdevicemultisampletype**](/windows/desktop/api)" verwendeten pqualitylevels.</span><span class="sxs-lookup"><span data-stu-id="ea95d-146">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span></span> <span data-ttu-id="ea95d-147">Wenn Sie einen größeren Wert übergeben, wird der Fehler D3DERR \_ invalidcallzurück gegeben.</span><span class="sxs-lookup"><span data-stu-id="ea95d-147">Passing a larger value returns the error D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="ea95d-148">Gekoppelte Werte von renderzielen oder tiefen Schablonen und der [**D3DMULTISAMPLE- \_ Typ**](./d3dmultisample-type.md) müssen mit identisch sein.</span><span class="sxs-lookup"><span data-stu-id="ea95d-148">Paired values of render targets or of depth stencil surfaces and [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) must match.</span></span>

</dd> <dt>

<span data-ttu-id="ea95d-149">**SwapEffect verwenden**</span><span class="sxs-lookup"><span data-stu-id="ea95d-149">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-150">Typ: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-150">Type: **[**D3DSWAPEFFECT**](./d3dswapeffect.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-151">Member des [**D3DSWAPEFFECT**](./d3dswapeffect.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="ea95d-151">Member of the [**D3DSWAPEFFECT**](./d3dswapeffect.md) enumerated type.</span></span> <span data-ttu-id="ea95d-152">Die Laufzeit gewährleistet die implizite Semantik bezüglich des Puffer Austausch Verhaltens. Wenn " **Windowed** " auf " **true** " festgelegt ist und " **Swap** " auf "D3DSWAPEFFECT Flip" festgelegt ist \_ , erstellt die Laufzeit einen zusätzlichen Hintergrund Puffer und kopiert, je nachdem, welcher der vordere Puffer zur Präsentationszeit wird.</span><span class="sxs-lookup"><span data-stu-id="ea95d-152">The runtime will guarantee the implied semantics concerning buffer swap behavior; therefore, if **Windowed** is **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIP, the runtime will create one extra back buffer and copy whichever becomes the front buffer at presentation time.</span></span>

<span data-ttu-id="ea95d-153">D3DSWAPEFFECT \_ Copy erfordert, dass **BackBufferCount** auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ea95d-153">D3DSWAPEFFECT\_COPY requires that **BackBufferCount** be set to 1.</span></span>

<span data-ttu-id="ea95d-154">D3DSWAPEFFECT \_ verwerfen wird in der Debug-Laufzeit erzwungen, indem jeder Puffer mit Rauschen aufgefüllt wird, nachdem er angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ea95d-154">D3DSWAPEFFECT\_DISCARD will be enforced in the debug runtime by filling any buffer with noise after it is presented.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea95d-155">Unterschiede zwischen von Direct3D9 und Direct3D9Ex</span><span class="sxs-lookup"><span data-stu-id="ea95d-155">Differences between Direct3D9 and Direct3D9Ex</span></span><br/> <span data-ttu-id="ea95d-156">In Direct3D9Ex wird D3DSWAPEFFECT \_ flipex hinzugefügt, um zu bestimmen, wann eine Anwendung den Flip-Modus annimmt.</span><span class="sxs-lookup"><span data-stu-id="ea95d-156">In Direct3D9Ex, D3DSWAPEFFECT\_FLIPEX is added to designate when an application is adopting flip mode.</span></span> <span data-ttu-id="ea95d-157">Das heißt, der Rahmen einer Anwendung wird im Fenstermodus (anstelle von kopiert) zur Komposition an den Desktopfenster-Manager (DWM) übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ea95d-157">That is, whan an application's frame is passed in window's mode (instead of copied) to the Desktop Window Manager(DWM) for composition.</span></span> <span data-ttu-id="ea95d-158">Der Flip-Modus sorgt für eine effizientere Arbeitsspeicher Bandbreite und ermöglicht einer Anwendung, die Vollbildansicht von Statistiken zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="ea95d-158">Flip mode provides more efficient memory bandwidth and enables an application to take advantage of full-screen-present statistics.</span></span> <span data-ttu-id="ea95d-159">Das Verhalten der voll Bild Anzeige wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="ea95d-159">It does not change full screen behavior.</span></span> <span data-ttu-id="ea95d-160">Das Verhalten des Flip-Modus ist ab Windows 7 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ea95d-160">Flip mode behavior is available beginning with Windows 7.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ea95d-161">**hdevicewindow**</span><span class="sxs-lookup"><span data-stu-id="ea95d-161">**hDeviceWindow**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-162">Typ: **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-162">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-163">Das Geräte Fenster bestimmt den Speicherort und die Größe des Hintergrund Puffers auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="ea95d-163">The device window determines the location and size of the back buffer on screen.</span></span> <span data-ttu-id="ea95d-164">Diese wird von Direct3D verwendet, wenn der Hintergrund Pufferinhalt während der [**Anwesenheit**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)in den Vorder-Puffer kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="ea95d-164">This is used by Direct3D when the back buffer contents are copied to the front buffer during [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

-   <span data-ttu-id="ea95d-165">Bei einer Vollbildanwendung handelt es sich hierbei um ein Handle für das obere Fenster (das Fokus Fenster).</span><span class="sxs-lookup"><span data-stu-id="ea95d-165">For a full-screen application, this is a handle to the top window (which is the focus window).</span></span>

    <span data-ttu-id="ea95d-166">Bei Anwendungen mit mehreren voll Bild Geräten (z. b. einem Multimonitor-System) kann genau ein Gerät das Fokus Fenster als Geräte Fenster verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea95d-166">For applications that use multiple full-screen devices (such as a multimonitor system), exactly one device can use the focus window as the device window.</span></span> <span data-ttu-id="ea95d-167">Alle anderen Geräte müssen über eindeutige Geräte Fenster verfügen.</span><span class="sxs-lookup"><span data-stu-id="ea95d-167">All other devices must have unique device windows.</span></span>

-   <span data-ttu-id="ea95d-168">Bei einer Anwendung im Windowed-Modus ist dieses handle das Standardziel Fenster für das [**vorhanden**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)sein.</span><span class="sxs-lookup"><span data-stu-id="ea95d-168">For a windowed-mode application, this handle will be the default target window for [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="ea95d-169">Wenn dieses Handle **null** ist, wird das Fokus Fenster übernommen.</span><span class="sxs-lookup"><span data-stu-id="ea95d-169">If this handle is **NULL**, the focus window will be taken.</span></span>

<span data-ttu-id="ea95d-170">Beachten Sie, dass die Laufzeit keinen Versuch hat, Benutzer Änderungen in der Fenstergröße widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="ea95d-170">Note that no attempt is made by the runtime to reflect user changes in window size.</span></span> <span data-ttu-id="ea95d-171">Der Hintergrund Puffer wird beim Zurücksetzen dieses Fensters nicht implizit zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="ea95d-171">The back buffer is not implicitly reset when this window is reset.</span></span> <span data-ttu-id="ea95d-172">Allerdings werden die Änderungen an der Fensterposition von der [**aktuellen**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) Methode automatisch nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="ea95d-172">However, the [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method does automatically track window position changes.</span></span>

</dd> <dt>

<span data-ttu-id="ea95d-173">**Fenster**</span><span class="sxs-lookup"><span data-stu-id="ea95d-173">**Windowed**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-174">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-174">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-175">**True** , wenn die Anwendung ausgeführt wird. **False** , wenn die Anwendung voll Bildschirm ausführt.</span><span class="sxs-lookup"><span data-stu-id="ea95d-175">**TRUE** if the application runs windowed; **FALSE** if the application runs full-screen.</span></span>

</dd> <dt>

<span data-ttu-id="ea95d-176">**Enableautodepthstencil**</span><span class="sxs-lookup"><span data-stu-id="ea95d-176">**EnableAutoDepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-177">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-177">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-178">Wenn dieser Wert **true** ist, verwaltet Direct3D Tiefe Puffer für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ea95d-178">If this value is **TRUE**, Direct3D will manage depth buffers for the application.</span></span> <span data-ttu-id="ea95d-179">Das Gerät erstellt einen tiefen Schablone-Puffer, wenn er erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ea95d-179">The device will create a depth-stencil buffer when it is created.</span></span> <span data-ttu-id="ea95d-180">Der tiefen Schablone-Puffer wird automatisch als Renderziel des Geräts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ea95d-180">The depth-stencil buffer will be automatically set as the render target of the device.</span></span> <span data-ttu-id="ea95d-181">Wenn das Gerät zurückgesetzt wird, wird der tiefen Schablone-Puffer automatisch zerstört und in der neuen Größe neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="ea95d-181">When the device is reset, the depth-stencil buffer will be automatically destroyed and recreated in the new size.</span></span>

<span data-ttu-id="ea95d-182">Wenn enableautodepthstencil den Wert **true** hat, muss autodepthstencilformat ein gültiges tiefen Schablone-Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ea95d-182">If EnableAutoDepthStencil is **TRUE**, then AutoDepthStencilFormat must be a valid depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="ea95d-183">**Autodepthstencilformat**</span><span class="sxs-lookup"><span data-stu-id="ea95d-183">**AutoDepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-184">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-184">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-185">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="ea95d-185">Member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="ea95d-186">Das Format der automatischen tiefen Schablone, die vom Gerät erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ea95d-186">The format of the automatic depth-stencil surface that the device will create.</span></span> <span data-ttu-id="ea95d-187">Dieser Member wird ignoriert, es sei denn, **enableautodepthstencil** ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="ea95d-187">This member is ignored unless **EnableAutoDepthStencil** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="ea95d-188">**Flags**</span><span class="sxs-lookup"><span data-stu-id="ea95d-188">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-189">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-189">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-190">Eine der [D3DPRESENTFLAG](d3dpresentflag.md) -Konstanten.</span><span class="sxs-lookup"><span data-stu-id="ea95d-190">One of the [D3DPRESENTFLAG](d3dpresentflag.md) constants.</span></span>

</dd> <dt>

<span data-ttu-id="ea95d-191">**Vollbild- \_ aktuscreenshrateingehz**</span><span class="sxs-lookup"><span data-stu-id="ea95d-191">**FullScreen\_RefreshRateInHz**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-192">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-192">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-193">Die Rate, mit der der Anzeige Adapter den Bildschirm aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ea95d-193">The rate at which the display adapter refreshes the screen.</span></span> <span data-ttu-id="ea95d-194">Der Wert hängt vom Modus ab, in dem die Anwendung ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="ea95d-194">The value depends on the mode in which the application is running:</span></span>

-   <span data-ttu-id="ea95d-195">Für den Fenstermodus muss die Aktualisierungsrate 0 betragen.</span><span class="sxs-lookup"><span data-stu-id="ea95d-195">For windowed mode, the refresh rate must be 0.</span></span>
-   <span data-ttu-id="ea95d-196">Für den Vollbildmodus ist die Aktualisierungsrate einer der von [**enumadaptermodes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)zurückgegebenen Aktualisierungs Raten.</span><span class="sxs-lookup"><span data-stu-id="ea95d-196">For full-screen mode, the refresh rate is one of the refresh rates returned by [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>

</dd> <dt>

<span data-ttu-id="ea95d-197">**Presentationinterval**</span><span class="sxs-lookup"><span data-stu-id="ea95d-197">**PresentationInterval**</span></span>
</dt> <dd>

<span data-ttu-id="ea95d-198">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea95d-198">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ea95d-199">Die maximale Rate, mit der die Hintergrund Puffer der Swapkette dem Vorder Puffer angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="ea95d-199">The maximum rate at which the swap chain's back buffers can be presented to the front buffer.</span></span> <span data-ttu-id="ea95d-200">Eine ausführliche Erläuterung der Modi und der unterstützten Intervalle finden Sie unter [D3DPRESENT](d3dpresent.md).</span><span class="sxs-lookup"><span data-stu-id="ea95d-200">For a detailed explanation of the modes and the intervals that are supported, see [D3DPRESENT](d3dpresent.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea95d-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea95d-201">Requirements</span></span>



| <span data-ttu-id="ea95d-202">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea95d-202">Requirement</span></span> | <span data-ttu-id="ea95d-203">Wert</span><span class="sxs-lookup"><span data-stu-id="ea95d-203">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea95d-204">Header</span><span class="sxs-lookup"><span data-stu-id="ea95d-204">Header</span></span><br/> | <dl> <span data-ttu-id="ea95d-205"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea95d-205"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea95d-206">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea95d-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea95d-207">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ea95d-207">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="ea95d-208">**"Kreatedevice"**</span><span class="sxs-lookup"><span data-stu-id="ea95d-208">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="ea95d-209">**"Kreateadditionalswapchain"**</span><span class="sxs-lookup"><span data-stu-id="ea95d-209">**CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[<span data-ttu-id="ea95d-210">**Anzahl**</span><span class="sxs-lookup"><span data-stu-id="ea95d-210">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[<span data-ttu-id="ea95d-211">**Reset**</span><span class="sxs-lookup"><span data-stu-id="ea95d-211">**Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
