---
description: Multihead-Karten sind solche, die über einen gemeinsamen Frame Puffer und eine Zugriffstaste, unabhängige Digital-zu-Analog-Konverter (DACs) und Monitor Ausgaben verfügen.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Multihead (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4617666ca623795d33bf1dafcaafeabe73323253
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481299"
---
# <a name="multihead-direct3d-9"></a><span data-ttu-id="0299c-103">Multihead (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0299c-103">Multihead (Direct3D 9)</span></span>

<span data-ttu-id="0299c-104">Multihead-Karten sind solche, die über einen gemeinsamen Frame Puffer und eine Zugriffstaste, unabhängige Digital-zu-Analog-Konverter (DACs) und Monitor Ausgaben verfügen.</span><span class="sxs-lookup"><span data-stu-id="0299c-104">Multihead cards are those that have a common frame buffer and accelerator, independent digital-to-analog converters (DACs), and monitor outputs.</span></span> <span data-ttu-id="0299c-105">Diese Geräte können eine viel nützlichere Unterstützung für mehrere Monitore bieten als eine ähnliche Anzahl heterogener Anzeige Adapter.</span><span class="sxs-lookup"><span data-stu-id="0299c-105">Such devices can offer much more usable multiple monitor support than a similar number of heterogeneous display adapters.</span></span>

<span data-ttu-id="0299c-106">Multihead-Karten sind in der API als einzelnes Gerät auf API-Ebene verfügbar, das mehrere voll Bildaustausch Ketten steuern kann.</span><span class="sxs-lookup"><span data-stu-id="0299c-106">Multihead cards are exposed in the API as a single API-level device that can drive several full-screen swap chains.</span></span> <span data-ttu-id="0299c-107">Folglich werden alle Ressourcen für alle Köpfe freigegeben, und jeder Head hat genau die gleichen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="0299c-107">Consequently, all resources are shared with all the heads, and each head has exactly the same capabilities.</span></span> <span data-ttu-id="0299c-108">Jeder Head kann auf unabhängige Anzeigemodi festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0299c-108">Each head can be set to independent display modes.</span></span> <span data-ttu-id="0299c-109">Sie können separate Aufrufe von [**IDirect3DSwapChain9::P Resent**](/windows/desktop/api) zum Aktualisieren der einzelnen Köpfe verwenden.</span><span class="sxs-lookup"><span data-stu-id="0299c-109">You can use separate calls to [**IDirect3DSwapChain9::Present**](/windows/desktop/api) to refresh each head.</span></span> <span data-ttu-id="0299c-110">Sie können auch einen [**:P IDirect3DDevice9**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) -aufrufbefehl verwenden, um die einzelnen Kopfzeile nacheinander zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0299c-110">You can also use one call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) to refresh each head sequentially.</span></span>

> [!Note]  
> <span data-ttu-id="0299c-111">Die Aktualisierung der einzelnen Köpfe erfolgt nicht gleichzeitig mit einem einzelnen IDirect3DDevice9-Rückruf [**::P erneut gesendet**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="0299c-111">The refresh of each head does not occur simultaneously with a single call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="0299c-112">Die aktuellen Statistiken in Direct3D 9Ex können die [**D3DPRESENTSTATS**](d3dpresentstats.md) -Struktur verwenden, um die Aktualisierungen auf den einzelnen Köpfen zu belassen, um die Auswirkungen auf mehrere Köpfe von Adaptern zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="0299c-112">Present statistics in Direct3D 9Ex can use the [**D3DPRESENTSTATS**](d3dpresentstats.md) structure to keep the refreshes to each head close to each other to limit tearing effects across multiple heads of adapters.</span></span> <span data-ttu-id="0299c-113">Informationen zum Synchronisieren von Frames von Direct3D 9Ex-Flip-Modell Anwendungen finden Sie unter [Direct3D 9Ex-Verbesserungen](../direct3darticles/direct3d-9ex-improvements.md).</span><span class="sxs-lookup"><span data-stu-id="0299c-113">For information about synchronizing frames of Direct3D 9Ex flip model applications, see [Direct3D 9Ex Improvements](../direct3darticles/direct3d-9ex-improvements.md).</span></span>

 

<span data-ttu-id="0299c-114">Jede austauschkette für ein multiheadgerät muss voll Bildschirm sein.</span><span class="sxs-lookup"><span data-stu-id="0299c-114">Each swap chain for a multihead device must be full screen.</span></span> <span data-ttu-id="0299c-115">Wenn ein Gerät in den multiheadmodus gewechselt ist, muss es im Vollbildmodus bleiben.</span><span class="sxs-lookup"><span data-stu-id="0299c-115">When a device has entered multihead mode, it must remain full screen.</span></span> <span data-ttu-id="0299c-116">Bei der Umstellung auf den Fenstermodus muss das Gerät (außer dem normalen Alt + Tab-bis-minimieren-Vorgang) zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="0299c-116">The transition back to windowed mode requires the destruction of the device (except for the normal ALT+TAB-to-minimize operation).</span></span>

<span data-ttu-id="0299c-117">Die alte Methode zum Aufteilen von Videospeicher zwischen den Köpfen und die Behandlung der einzelnen Köpfe als vollständig unabhängige Zugriffstaste ist weiterhin ein häufiges Verwendungs Szenario.</span><span class="sxs-lookup"><span data-stu-id="0299c-117">The old method of dividing video memory between the heads and treating each head as a fully independent accelerator will still be a common usage scenario.</span></span> <span data-ttu-id="0299c-118">Dieser Mechanismus wird nicht durch diesen Vorschlag ersetzt, es sei denn, die Anwendung wurde speziell für die Funktionsweise im Direct3D 9-multiheadmodus programmiert.</span><span class="sxs-lookup"><span data-stu-id="0299c-118">This proposal does not replace that mechanism unless the application has been specifically coded to function in the Direct3D 9 multihead mode.</span></span>

<span data-ttu-id="0299c-119">Die Treiber verfügen über ausreichende Kenntnisse, um zwischen den beiden Betriebsmodi zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="0299c-119">Drivers are given adequate knowledge to switch between the two modes of operation.</span></span>

<span data-ttu-id="0299c-120">Eine Kopfzeile wird als Haupt Kopfzeile bezeichnet, und alle anderen Köpfe auf derselben Karte werden als untergeordnete Köpfe bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0299c-120">One head will be called the master head, and all other heads on the same card be called subordinate heads.</span></span> <span data-ttu-id="0299c-121">Wenn mehr als ein multiheadadapter in einem System vorhanden ist, werden der Master und seine untergeordneten Elemente von einem Multihead-Adapter als Gruppe bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0299c-121">If more than one multihead adapter is present in a system, the master and its subordinates from one multihead adapter are called a group.</span></span> <span data-ttu-id="0299c-122">Gruppen werden durch die Ordnungszahl des Adapters Ihrer Haupt Kopfzeile bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0299c-122">Groups are denoted by the adapter ordinal of their master head.</span></span>

<span data-ttu-id="0299c-123">Die [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur wurde aktualisiert, um die folgenden neuen Hardware-Caps verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="0299c-123">The [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure has been updated to expose the following new hardware caps.</span></span>


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   <span data-ttu-id="0299c-124">"Numofadaptersingroup" ist 1 für herkömmliche Adapter und größer als 1 für den Master Adapter einer Multihead-Karte.</span><span class="sxs-lookup"><span data-stu-id="0299c-124">NumberOfAdaptersInGroup is 1 for conventional adapters, and greater than 1 for the master adapter of a multihead card.</span></span> <span data-ttu-id="0299c-125">Der Wert ist 0 für einen untergeordneten Adapter einer Multihead-Karte.</span><span class="sxs-lookup"><span data-stu-id="0299c-125">The value will be 0 for a subordinate adapter of a multihead card.</span></span> <span data-ttu-id="0299c-126">Jede Karte kann höchstens über einen Master verfügen, kann aber auch über viele untergeordnete Elemente verfügen.</span><span class="sxs-lookup"><span data-stu-id="0299c-126">Each card can have at most one master, but might have many subordinates.</span></span>
-   <span data-ttu-id="0299c-127">Masteradapterordinal gibt an, welches Gerät der Master für diese untergeordnete ist.</span><span class="sxs-lookup"><span data-stu-id="0299c-127">MasterAdapterOrdinal indicates which device is the master for this subordinate.</span></span>
-   <span data-ttu-id="0299c-128">Adapterordinalingroup gibt die Reihenfolge an, in der die Kopfzeilen von der API referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="0299c-128">AdapterOrdinalInGroup indicates the order in which heads are referenced by the API.</span></span> <span data-ttu-id="0299c-129">Der Master Adapter hat immer adapterordinalingroup 0.</span><span class="sxs-lookup"><span data-stu-id="0299c-129">The master adapter always has AdapterOrdinalInGroup 0.</span></span> <span data-ttu-id="0299c-130">Diese Werte entsprechen nicht den Adapter Ordinalzahlen, die an die IDirect3D9-Methoden übergebenen werden, sondern nur für Köpfe innerhalb einer Gruppe gelten.</span><span class="sxs-lookup"><span data-stu-id="0299c-130">These values do not correspond to the adapter ordinals passed to the IDirect3D9 methods, but apply only to heads within a group.</span></span>

<span data-ttu-id="0299c-131">Mit dieser Definition können Multihead-Karten weiterhin mehrere Adapter wie in DirectX 8 als unabhängige Karten darstellen.</span><span class="sxs-lookup"><span data-stu-id="0299c-131">This definition allows multihead cards to continue to present multiple adapters as if they were independent cards, just as they did in DirectX 8.</span></span>

<span data-ttu-id="0299c-132">Um ein multiheadgerät zu erstellen, geben Sie das verhaltenflag D3DCREATE \_ adaptergroup \_ Device in [**IDirect3D9:: kreatedevice**](/windows/desktop/api)an.</span><span class="sxs-lookup"><span data-stu-id="0299c-132">To create a multihead device, specify the behavior flag D3DCREATE\_ADAPTERGROUP\_DEVICE in [**IDirect3D9::CreateDevice**](/windows/desktop/api).</span></span> <span data-ttu-id="0299c-133">Die Darstellungs Parameter (ein Array von [**D3DPRESENT- \_ Parametern**](d3dpresent-parameters.md)) sollten "numofadaptersingroup"-Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="0299c-133">The presentation parameters (an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md)) should contain NumberOfAdaptersInGroup elements.</span></span> <span data-ttu-id="0299c-134">Die Laufzeit weist jedes Element jedem Kopf in der numerischen adapterordinalingroup-Reihenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="0299c-134">The runtime will assign each element to each head in AdapterOrdinalInGroup numerical order.</span></span> <span data-ttu-id="0299c-135">Wenn das D3DCREATE \_ adaptergroup- \_ Gerät festgelegt ist, muss für jeden Präsentations Parameter Folgendes vorhanden sein:</span><span class="sxs-lookup"><span data-stu-id="0299c-135">When D3DCREATE\_ADAPTERGROUP\_DEVICE is set, each presentation parameter must have:</span></span>

-   <span data-ttu-id="0299c-136">Der Windowed-Member ist auf **false** festgelegt (mit anderen Worten: Vollbild).</span><span class="sxs-lookup"><span data-stu-id="0299c-136">The Windowed member set to **FALSE** (in other words, be full screen).</span></span>
-   <span data-ttu-id="0299c-137">Der gleiche Wert für den enableautodepthstencil-Member der [**D3DPRESENT- \_ Parameter**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0299c-137">The same value for the EnableAutoDepthStencil member of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="0299c-138">Wenn enableautodepthstencil den Wert **true** hat, muss jedes der folgenden Felder für jeden [**D3DPRESENT- \_ Parameter**](d3dpresent-parameters.md)denselben Wert aufweisen:</span><span class="sxs-lookup"><span data-stu-id="0299c-138">In addition, if EnableAutoDepthStencil is **TRUE**, then each of the following fields must have the same value for each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md):</span></span>

-   <span data-ttu-id="0299c-139">Autodepthstencilformat</span><span class="sxs-lookup"><span data-stu-id="0299c-139">AutoDepthStencilFormat</span></span>
-   <span data-ttu-id="0299c-140">BackBufferWidth</span><span class="sxs-lookup"><span data-stu-id="0299c-140">BackBufferWidth</span></span>
-   <span data-ttu-id="0299c-141">BackBufferHeight</span><span class="sxs-lookup"><span data-stu-id="0299c-141">BackBufferHeight</span></span>
-   <span data-ttu-id="0299c-142">Backbufferformat</span><span class="sxs-lookup"><span data-stu-id="0299c-142">BackBufferFormat</span></span>

<span data-ttu-id="0299c-143">Wenn die DAC festgelegt ist, sind zusätzliche Aufrufe an [**IDirect3DDevice9:: deateadditionalswapchain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) unzulässig.</span><span class="sxs-lookup"><span data-stu-id="0299c-143">If DAC is set, additional calls to [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) are illegal.</span></span>

<span data-ttu-id="0299c-144">Wenn das Gerät mit der DAC erstellt wurde, erwartet [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) ein Array von [**D3DPRESENT- \_ Parametern**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0299c-144">If the device was created with the DAC, [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) will expect an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="0299c-145">Jede [**D3DPRESENT \_ Parameter**](d3dpresent-parameters.md) -Struktur, die an [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) übermittelt wird, muss voll Bildschirm sein.</span><span class="sxs-lookup"><span data-stu-id="0299c-145">Each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure passed to [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) must be full screen.</span></span> <span data-ttu-id="0299c-146">Wenn Sie wieder in den Fenstermodus wechseln möchten, muss die Anwendung das Gerät zerstören und im Fenstermodus ein nicht-Multihead-Gerät neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0299c-146">To switch back to windowed mode, the application must destroy the device and re-create a non-multihead device in windowed mode.</span></span>

<span data-ttu-id="0299c-147">Im folgenden finden Sie ein grundlegendes Verwendungs Szenario:</span><span class="sxs-lookup"><span data-stu-id="0299c-147">Here is a basic usage scenario:</span></span>


```
1. Create multihead device 
2. For each swap chain of device:
   3. Call GetBackBuffer for the i-th swapchain
   4. Call SetRenderTarget 
   5. Call DrawPrimitive 
   6. Optionally call swapchain::Present (or wait until 
all swap chains are drawn and present outside of loop)
7. End the for loop
8. Optionally present all swap chains with device::Present
```



<span data-ttu-id="0299c-148">Weitere Informationen finden Sie unter [**IDirect3D9:: kreatedevice**](/windows/desktop/api) und [**IDirect3DDevice9:: getnumofswapchain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).</span><span class="sxs-lookup"><span data-stu-id="0299c-148">For more information, see [**IDirect3D9::CreateDevice**](/windows/desktop/api) and [**IDirect3DDevice9::GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0299c-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0299c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0299c-150">Programmiertipps</span><span class="sxs-lookup"><span data-stu-id="0299c-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
