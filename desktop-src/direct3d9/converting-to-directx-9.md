---
description: Die folgenden Features wurden in Microsoft Direct3D 9 geändert. Wenn Sie diese Features verwenden, sehen Sie sich die unten aufgeführten Änderungen an, um Ihre Anwendung auf Direct3D 9 zu portieren.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Wandeln in Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becdb878ad462bfc0157fb15b3c9c1ef2ba158dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346858"
---
# <a name="converting-to-direct3d-9"></a><span data-ttu-id="10eed-104">Wandeln in Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="10eed-104">Converting to Direct3D 9</span></span>

<span data-ttu-id="10eed-105">Die folgenden Features wurden in Microsoft Direct3D 9 geändert.</span><span class="sxs-lookup"><span data-stu-id="10eed-105">The following features were changed in Microsoft Direct3D 9.</span></span> <span data-ttu-id="10eed-106">Wenn Sie diese Features verwenden, sehen Sie sich die unten aufgeführten Änderungen an, um Ihre Anwendung auf Direct3D 9 zu portieren.</span><span class="sxs-lookup"><span data-stu-id="10eed-106">If you are using these features, see the changes listed below to help you port your application to Direct3D 9.</span></span>

-   [<span data-ttu-id="10eed-107">Basevertexindex-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-107">BaseVertexIndex Changes</span></span>](#basevertexindex-changes)
-   [<span data-ttu-id="10eed-108">"Kreateimagesurface"-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-108">CreateImageSurface Changes</span></span>](#createimagesurface-changes)
-   [<span data-ttu-id="10eed-109">D3DENUM \_ keine \_ Änderungen an WHQL- \_ Ebene</span><span class="sxs-lookup"><span data-stu-id="10eed-109">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>](/windows)
-   [<span data-ttu-id="10eed-110">Erstellen von Ressourcen Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-110">Create Resource Changes</span></span>](#create-resource-changes)
-   [<span data-ttu-id="10eed-111">Enumadaptermodes-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-111">EnumAdapterModes Changes</span></span>](#enumadaptermodes-changes)
-   [<span data-ttu-id="10eed-112">Get/SetStreamSource- \_ Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-112">Get/SetStreamSource\_Changes</span></span>](#getsetstreamsource-changes)
-   [<span data-ttu-id="10eed-113">Qualitätsänderungen bei der Multisampling</span><span class="sxs-lookup"><span data-stu-id="10eed-113">Multisampling Quality Changes</span></span>](#multisampling-quality-changes)
-   [<span data-ttu-id="10eed-114">Resourcemanagerverwerdbytes-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-114">ResourceManagerDiscardBytes Changes</span></span>](#resourcemanagerdiscardbytes-changes)
-   [<span data-ttu-id="10eed-115">Setsoftwarevertexprocessing-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-115">SetSoftwareVertexProcessing Changes</span></span>](#setsoftwarevertexprocessing-changes)
-   [<span data-ttu-id="10eed-116">Textursampler-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-116">Texture Sampler Changes</span></span>](#texture-sampler-changes)
-   [<span data-ttu-id="10eed-117">Vertex-Deklarations Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-117">Vertex Declaration Changes</span></span>](#vertex-declaration-changes)
-   [<span data-ttu-id="10eed-118">Intervalle \_ und \_ austauschen von \_ Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-118">Intervals,\_and\_SwapEffects\_Changes</span></span>](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a><span data-ttu-id="10eed-119">Basevertexindex-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-119">BaseVertexIndex Changes</span></span>

<span data-ttu-id="10eed-120">In DirectX 8. x erforderte IDirect3DDevice8:: setindexes einen Zeiger auf den Index Puffer und einen basevertexindex für die Anfangsposition im Vertex-Puffer.</span><span class="sxs-lookup"><span data-stu-id="10eed-120">In DirectX 8.x, IDirect3DDevice8::SetIndices required a pointer to the index buffer and a BaseVertexIndex for the starting position in the vertex buffer.</span></span> <span data-ttu-id="10eed-121">Eine Anwendung, die unterschiedliche Objekte in den Vertex-Puffer unterteilt, musste den Index Puffer wechseln (oder IDirect3DDevice8:: setindexes aufrufen), bevor IDirect3DDevice8::D rawindexedprimitiv aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="10eed-121">An application batching different objects into the vertex buffer had to switch the index buffer (or make a call to IDirect3DDevice8::SetIndices) before calling IDirect3DDevice8::DrawIndexedPrimitive.</span></span>

<span data-ttu-id="10eed-122">In Direct3D 9 wurde die Anfangsposition im Vertex-Puffer *basevertexindex* nach IDirect3DDevice9::D rawindexedprimitiv verschoben, und der Datentyp des Datentyps wurde von DWORD in int geändert.</span><span class="sxs-lookup"><span data-stu-id="10eed-122">In Direct3D 9, the starting position in the vertex buffer, *BaseVertexIndex*, has been moved to IDirect3DDevice9::DrawIndexedPrimitive, and its data type changed from a DWORD to an INT.</span></span>


```
HRESULT IDirect3DDevice9::DrawIndexedPrimitive( 
    D3DPRIMITIVETYPE PrimType, 
    INT BaseVertexIndex, 
    UINT minIndex, 
    UINT NumVertices, 
    UINT startIndex, 
    UINT primCount); 

HRESULT SetIndices(IDirect3DIndexBuffer9* pIndexData); 
```



## <a name="createimagesurface-changes"></a><span data-ttu-id="10eed-123">"Kreateimagesurface"-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-123">CreateImageSurface Changes</span></span>

<span data-ttu-id="10eed-124">IDirect3DDevice8:: kreateimagesurface wurde in " [**kreateoffscreenplainsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)" umbenannt.</span><span class="sxs-lookup"><span data-stu-id="10eed-124">IDirect3DDevice8::CreateImageSurface was renamed [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface).</span></span> <span data-ttu-id="10eed-125">Ein zusätzlicher Parameter, der einen D3DPOOL-Typ annimmt, wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="10eed-125">An additional parameter that takes a D3DPOOL type was added.</span></span> <span data-ttu-id="10eed-126">D3DPOOL \_ Scratch gibt eine Oberfläche mit identischen Merkmalen für eine Oberfläche zurück, die von IDirect3DDevice8:: kreateimagesurface erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="10eed-126">D3DPOOL\_SCRATCH will return a surface that has identical characteristics to a surface created by IDirect3DDevice8::CreateImageSurface.</span></span> <span data-ttu-id="10eed-127">D3DPOOL \_ Default ist der geeignete Pool für die Verwendung mit [**stretchrect**](/windows/desktop/api) und [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).</span><span class="sxs-lookup"><span data-stu-id="10eed-127">D3DPOOL\_DEFAULT is the appropriate pool for use with [**StretchRect**](/windows/desktop/api) and [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).</span></span>

## <a name="d3denum_no_whql_level-changes"></a><span data-ttu-id="10eed-128">D3DENUM \_ keine \_ Änderungen an WHQL- \_ Ebene</span><span class="sxs-lookup"><span data-stu-id="10eed-128">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>

<span data-ttu-id="10eed-129">Anwendungen müssen nun explizit Microsoft Windows Hardware Quality Labs (WHQL) anfordern, da die Antwort relativ lange dauert (einige Sekunden).</span><span class="sxs-lookup"><span data-stu-id="10eed-129">Applications now have to explicitly ask for the Microsoft Windows Hardware Quality Labs (WHQL) because the response takes relatively long (a few seconds).</span></span> <span data-ttu-id="10eed-130">D3DENUM es wurde \_ keine \_ WHQL \_ -Ebene entfernt, und die D3DENUM \_ WHQL- \_ Ebene wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="10eed-130">D3DENUM\_NO\_WHQL\_LEVEL has been removed and D3DENUM\_WHQL\_LEVEL has been added.</span></span>

## <a name="create-resource-changes"></a><span data-ttu-id="10eed-131">Erstellen von Ressourcen Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-131">Create Resource Changes</span></span>

<span data-ttu-id="10eed-132">Ein Handle wurde mehreren Methoden hinzugefügt und sollte auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="10eed-132">A handle has been added to several methods and should be set to **NULL**.</span></span> <span data-ttu-id="10eed-133">Folgende Methoden sind betroffen:</span><span class="sxs-lookup"><span data-stu-id="10eed-133">The methods affected include:</span></span>

-   [<span data-ttu-id="10eed-134">**"Kreatetexture"**</span><span class="sxs-lookup"><span data-stu-id="10eed-134">**CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="10eed-135">**"Kreatevolumetexture"**</span><span class="sxs-lookup"><span data-stu-id="10eed-135">**CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [<span data-ttu-id="10eed-136">**"Kreatecubetexture"**</span><span class="sxs-lookup"><span data-stu-id="10eed-136">**CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="10eed-137">**"Kreatevertexbuffer"**</span><span class="sxs-lookup"><span data-stu-id="10eed-137">**CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [<span data-ttu-id="10eed-138">**"Kreateingedexbuffer"**</span><span class="sxs-lookup"><span data-stu-id="10eed-138">**CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [<span data-ttu-id="10eed-139">**"Kreaterendertarget"**</span><span class="sxs-lookup"><span data-stu-id="10eed-139">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [<span data-ttu-id="10eed-140">**"Kreatedepthstencilsurface"**</span><span class="sxs-lookup"><span data-stu-id="10eed-140">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="10eed-141">**"Kreateoffscreenplainsurface"**</span><span class="sxs-lookup"><span data-stu-id="10eed-141">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a><span data-ttu-id="10eed-142">Enumadaptermodes-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-142">EnumAdapterModes Changes</span></span>

<span data-ttu-id="10eed-143">[**Enumadaptermodes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) nimmt nun eine D3DFORMAT-Datei an.</span><span class="sxs-lookup"><span data-stu-id="10eed-143">The [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) now takes a D3DFORMAT.</span></span>


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



<span data-ttu-id="10eed-144">Das Format unterstützt eine erweiternde Gruppe von Anzeigemodi.</span><span class="sxs-lookup"><span data-stu-id="10eed-144">The format supports an expanding set of display modes.</span></span> <span data-ttu-id="10eed-145">Um Anwendungen vor dem Auflisten von Formaten zu schützen, die beim Versand der Anwendung nicht erfunden wurden, muss die Anwendung Direct3D das Format für die Anzeigemodi angeben, die aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="10eed-145">To protect applications from enumerating formats that were not invented when the application shipped, the application must tell Direct3D the format for the display modes that should be enumerated.</span></span> <span data-ttu-id="10eed-146">Das resultierende Array der Anzeigemodi unterscheidet sich nur durch die Breite, die Höhe und die Aktualisierungsrate.</span><span class="sxs-lookup"><span data-stu-id="10eed-146">The resulting array of display modes will differ only by width, height, and refresh rate.</span></span>

<span data-ttu-id="10eed-147">Die Anwendung gibt ein Pixel Format an, und die Enumeration ist auf die Anzeigemodi beschränkt, die exakt mit dem Format übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="10eed-147">The application specifies a pixel format and the enumeration is restricted to those display modes that exactly match the format.</span></span> <span data-ttu-id="10eed-148">Im folgenden finden Sie eine Liste der zulässigen Formate:</span><span class="sxs-lookup"><span data-stu-id="10eed-148">The following is a list of the allowed formats:</span></span>

-   <span data-ttu-id="10eed-149">D3DFMT \_ A1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="10eed-149">D3DFMT\_A1R5G5B5</span></span>
-   <span data-ttu-id="10eed-150">D3DFMT \_ A2B10G10R10</span><span class="sxs-lookup"><span data-stu-id="10eed-150">D3DFMT\_A2B10G10R10</span></span>
-   <span data-ttu-id="10eed-151">D3DFMT \_ A8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="10eed-151">D3DFMT\_A8R8G8B8</span></span>
-   <span data-ttu-id="10eed-152">D3DFMT \_ R5G6B5</span><span class="sxs-lookup"><span data-stu-id="10eed-152">D3DFMT\_R5G6B5</span></span>
-   <span data-ttu-id="10eed-153">D3DFMT \_ X1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="10eed-153">D3DFMT\_X1R5G5B5</span></span>
-   <span data-ttu-id="10eed-154">D3DFMT \_ X8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="10eed-154">D3DFMT\_X8R8G8B8</span></span>

<span data-ttu-id="10eed-155">Die Enumeration ist äquivalent zu Alpha-und nonalpha-Versionen desselben Formats.</span><span class="sxs-lookup"><span data-stu-id="10eed-155">Enumeration is equivalent for alpha and nonalpha versions of the same format.</span></span> <span data-ttu-id="10eed-156">Das zurückgegebene Format wird immer mit dem von der Anwendung bereitgestellten Format ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="10eed-156">The returned Format will always be filled with the same format supplied by the application.</span></span>

<span data-ttu-id="10eed-157">Diese Methode behandelt 565 und 555 als gleichwertig und gibt die richtige Version im-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="10eed-157">This method treats 565 and 555 as equivalent, and returns the correct version in the Format.</span></span> <span data-ttu-id="10eed-158">Der Unterschied wird nur wiedergegeben, wenn die Anwendung den Hintergrund Puffer sperrt, und es gibt ein explizites Flag, das von der Anwendung festgelegt werden muss, um dies zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="10eed-158">The difference comes into play only when the application locks the back buffer, and there is an explicit flag that the application must set in order to accomplish this.</span></span>

## <a name="getsetstreamsource-changes"></a><span data-ttu-id="10eed-159">Get/SetStreamSource-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-159">Get/SetStreamSource Changes</span></span>

<span data-ttu-id="10eed-160">Der [**getstreamsource**](/windows/desktop/api) -Methode und der [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) -Methode wurde ein Parameter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="10eed-160">One parameter has been added to the [**GetStreamSource**](/windows/desktop/api) and [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) methods.</span></span> <span data-ttu-id="10eed-161">Der Offset ist die Anzahl von Bytes zwischen dem Anfang des Streams und dem Anfang der Scheitelpunkt Daten.</span><span class="sxs-lookup"><span data-stu-id="10eed-161">The offset is the number of bytes between the beginning of the stream and the beginning of the vertex data.</span></span> <span data-ttu-id="10eed-162">Der entsprechende Wert wird in „Bytes“ angegeben.</span><span class="sxs-lookup"><span data-stu-id="10eed-162">It is measured in bytes.</span></span> <span data-ttu-id="10eed-163">Dadurch kann die Pipeline streamoffsets unterstützen.</span><span class="sxs-lookup"><span data-stu-id="10eed-163">This enables the pipeline to support stream offsets.</span></span> <span data-ttu-id="10eed-164">Informationen dazu, ob das Gerät streamoffsets unterstützt, finden Sie unter D3DDEVCAPS2 \_ Streamoffset.</span><span class="sxs-lookup"><span data-stu-id="10eed-164">To find out if the device supports stream offsets, see D3DDEVCAPS2\_STREAMOFFSET.</span></span>


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a><span data-ttu-id="10eed-165">Qualitätsänderungen bei der Multisampling</span><span class="sxs-lookup"><span data-stu-id="10eed-165">Multisampling Quality Changes</span></span>

<span data-ttu-id="10eed-166">Bisher gab es nur die D3DMULTISAMPLE \_ Type-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="10eed-166">Previously, there was only the D3DMULTISAMPLE\_TYPE enumeration.</span></span> <span data-ttu-id="10eed-167">Direct3D 9 behält diese Enumeration bei und fügt die Idee einer Qualitätsstufe für jedes Element der Enumeration hinzu.</span><span class="sxs-lookup"><span data-stu-id="10eed-167">Direct3D 9 retains this enumeration and adds the idea of a quality level for each element of the enumeration.</span></span> <span data-ttu-id="10eed-168">Die Qualitätsstufe gibt einen Kompromiss zwischen visueller Qualität und Leistung an, indem die Anzahl der hervor hefbaren Stichproben (im Sinne von D3DRS \_ multisamplemask) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10eed-168">The quality level indicates a trade-off between visual quality and performance by indicating the number of maskable samples (in the sense of D3DRS\_MULTISAMPLEMASK).</span></span>

<span data-ttu-id="10eed-169">Eine Anwendung sollte auswählen, wie viele für Sie erforderliche Beispiele benötigt werden, und Sie sollten sich dann pqualitylevels ansehen.</span><span class="sxs-lookup"><span data-stu-id="10eed-169">An application should choose how many maskable samples it requires, and then consult pQualityLevels.</span></span> <span data-ttu-id="10eed-170">Wenn ungleich 0 (null) angegeben ist, gibt dieser Wert die Anzahl der Qualitätsstufen an, die die Anwendung über multisamplequality an die verschiedenen Erstellungs Funktionen übergeben kann.</span><span class="sxs-lookup"><span data-stu-id="10eed-170">If nonzero, this value indicates the number of quality levels the application can pass to the various creation functions through MultiSampleQuality.</span></span> <span data-ttu-id="10eed-171">Da Treiber alle Ihre multibeispielschemas als Qualitäts Ebenen bei D3DMULTISAMPLE nicht \_ MASKABLE verfügbar machen, können Sie alle verfügbaren multisamplinggrad-Schemas über diesen Typ auflisten, wenn die Anwendung keine Beispiele maskieren muss.</span><span class="sxs-lookup"><span data-stu-id="10eed-171">Because drivers expose all their multisample schemes as quality levels at D3DMULTISAMPLE\_NONMASKABLE, you can enumerate all available multisampling schemes through this one type if your application does not need to mask samples.</span></span>

<span data-ttu-id="10eed-172">Das D3DPRASTERCAPS \_ StretchBltMultisample Caps-Bit wurde eingestellt.</span><span class="sxs-lookup"><span data-stu-id="10eed-172">The D3DPRASTERCAPS\_STRETCHBLTMULTISAMPLE caps bit has been retired.</span></span> <span data-ttu-id="10eed-173">Dieses Bit bedeutete, dass die multisamplinggrad-Methode Schreib Masken nicht unterstützte und zwischen [**BeginScene**](/windows/desktop/api) und [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene)nicht ein-und ausgeschaltet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="10eed-173">This bit used to mean that the multisampling method did not support write masks, and could not be toggled on and off between [**BeginScene**](/windows/desktop/api) and [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene).</span></span> <span data-ttu-id="10eed-174">Solche nicht masretisierbaren Methoden werden nun über D3DMULTISAMPLE \_ Nonmaskable verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="10eed-174">Such nonmaskable methods are now exposed through D3DMULTISAMPLE\_NONMASKABLE.</span></span>


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



<span data-ttu-id="10eed-175">Es gibt ein anderes Maximum für jede Anzahl von für das Paar baren Stichproben.</span><span class="sxs-lookup"><span data-stu-id="10eed-175">There is a different maximum for each number of maskable samples.</span></span> <span data-ttu-id="10eed-176">Beispielsweise können D3DMULTISAMPLE \_ 4- \_ Beispiele drei Qualitätsstufen aufweisen, während D3DMULTISAMPLE- \_ \_ Stichproben möglicherweise nur eine Qualität aufweisen.</span><span class="sxs-lookup"><span data-stu-id="10eed-176">For example, D3DMULTISAMPLE\_4\_SAMPLES might have three levels of quality, while D3DMULTISAMPLE\_2\_SAMPLES might have only one.</span></span> <span data-ttu-id="10eed-177">Es gibt höchstens acht Qualitätsstufen für jede Anzahl von durchsuchbaren Beispielen (der Treiber ist nicht berechtigt, mehr auszudrücken).</span><span class="sxs-lookup"><span data-stu-id="10eed-177">There are at most eight levels of quality for each number of maskable samples (the driver is not allowed to express more).</span></span> <span data-ttu-id="10eed-178">Die Qualität reicht von 0 (NULL \* ) bis (pqualitylevels-1).</span><span class="sxs-lookup"><span data-stu-id="10eed-178">The quality ranges from zero to (\*pQualityLevels - 1).</span></span>

## <a name="resourcemanagerdiscardbytes-changes"></a><span data-ttu-id="10eed-179">Resourcemanagerverwerdbytes-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-179">ResourceManagerDiscardBytes Changes</span></span>

<span data-ttu-id="10eed-180">Resourcemanagerverwerdbytes wurde durch IDirect3DDevice9:: evictmanagedresources ersetzt.</span><span class="sxs-lookup"><span data-stu-id="10eed-180">ResourceManagerDiscardBytes has been replaced by IDirect3DDevice9::EvictManagedResources.</span></span> <span data-ttu-id="10eed-181">Sie kann alle Ressourcen entfernen, sowohl Direct3D als auch Treiber Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="10eed-181">It can evict all resources, both Direct3D and driver resources.</span></span>

<span data-ttu-id="10eed-182">Der Ressourcen-Manager wird jetzt bei der Erstellung einer Ressource (ob verwaltet oder nicht verwaltet) nicht ausgeführt, weil nicht genügend Videospeicher verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="10eed-182">The resource manager is now consulted when a resource (whether managed or nonmanaged) fails creation because there is insufficient video memory.</span></span> <span data-ttu-id="10eed-183">Der Manager wird automatisch aufgefordert, genügend Ressourcen freizugeben, damit die Erstellung erfolgreich durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="10eed-183">The manager will automatically be asked to free enough resources for the creation to succeed.</span></span> <span data-ttu-id="10eed-184">In DirectX 8,0 war dies kein automatisierter Prozess.</span><span class="sxs-lookup"><span data-stu-id="10eed-184">In DirectX 8.0, this was not an automated process.</span></span>

## <a name="setsoftwarevertexprocessing-changes"></a><span data-ttu-id="10eed-185">Setsoftwarevertexprocessing-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-185">SetSoftwareVertexProcessing Changes</span></span>

<span data-ttu-id="10eed-186">Eine Anwendung kann ein Gerät im gemischten Modus erstellen, um die Verarbeitung von Software-und Hardware Scheitel Punkten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="10eed-186">An application can create a mixed-mode device to use software and hardware vertex processing.</span></span>

<span data-ttu-id="10eed-187">Um zwischen den beiden Scheitelpunkt Verarbeitungsmodi in DirectX 8. x zu wechseln, wird IDirect3DDevice8:: Server State aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="10eed-187">To switch between the two vertex processing modes in DirectX 8.x, call IDirect3DDevice8::SetRenderState.</span></span> <span data-ttu-id="10eed-188">Dies wurde durch [**setsoftwarevertexprocessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) ersetzt, um Probleme zu vereinfachen, die durch Zustands Blöcke verursacht wurden.</span><span class="sxs-lookup"><span data-stu-id="10eed-188">This has been replaced with [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) to ease problems caused by state blocks.</span></span> <span data-ttu-id="10eed-189">Diese neue Methode wird nicht von Zustands Blöcken aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="10eed-189">This new method is not recorded by state blocks.</span></span>

## <a name="texture-sampler-changes"></a><span data-ttu-id="10eed-190">Textursampler-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-190">Texture Sampler Changes</span></span>

<span data-ttu-id="10eed-191">Direct3D 9 unterstützt bis zu sechzehn Textur Oberflächen in einem Durchlauf mithilfe des Pixels-Shader 2 \_ 0-Modells. die Anzahl der Texturkoordinaten bleibt jedoch auf acht beschränkt.</span><span class="sxs-lookup"><span data-stu-id="10eed-191">Direct3D 9 supports up to sixteen texture surfaces in one pass using the pixel shader 2\_0 model; however, the number of texture coordinates remains limited to eight.</span></span> <span data-ttu-id="10eed-192">Der Textur Stufen Zustand ist mit Oberflächen, Koordinaten Sätzen, Vertexverarbeitung und Pixel Verarbeitung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="10eed-192">Texture stage state is associated with surfaces, coordinate sets, vertex processing, and pixel processing.</span></span> <span data-ttu-id="10eed-193">Um diese Unterschiede zur Kompilierzeit zu verwalten, wurde [**settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) in zwei Methoden unterteilt:</span><span class="sxs-lookup"><span data-stu-id="10eed-193">To manage these differences at compile time, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) has been broken into two methods:</span></span>

-   <span data-ttu-id="10eed-194">IDirect3DDevice9:: settexturestagestate wird weiterhin für den Texturkoordinaten Zustand verwendet, wie z. b. Umbruch Modi und Texturkoordinaten Generierung.</span><span class="sxs-lookup"><span data-stu-id="10eed-194">IDirect3DDevice9::SetTextureStageState will still be used for texture coordinate state, such as wrap modes and texture coordinate generation.</span></span>
-   <span data-ttu-id="10eed-195">" [**Setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) " wurde hinzugefügt und wird jetzt zum Filtern, ticken, spannen, miplod usw. verwendet.</span><span class="sxs-lookup"><span data-stu-id="10eed-195">[**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) has been added and will now be used for filtering, tiling, clamping, MIPLOD, and so forth.</span></span> <span data-ttu-id="10eed-196">Dies funktioniert für bis zu sechzehn samplz.</span><span class="sxs-lookup"><span data-stu-id="10eed-196">This will work for up to sixteen samplers.</span></span>

### <a name="settexturestagestate-changes"></a><span data-ttu-id="10eed-197">Settexturestagestate-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-197">SetTextureStageState Changes</span></span>

<span data-ttu-id="10eed-198">IDirect3DDevice9:: settexturestagestate legt nun die folgenden Zustände fest:</span><span class="sxs-lookup"><span data-stu-id="10eed-198">IDirect3DDevice9::SetTextureStageState now sets the following states:</span></span>

-   <span data-ttu-id="10eed-199">Verarbeitungs Status des Scheitelpunkt Status der Funktion.</span><span class="sxs-lookup"><span data-stu-id="10eed-199">Fixed function vertex processing state.</span></span> <span data-ttu-id="10eed-200">Dieser Zustand steuert die Bearbeitung von Texturkoordinaten D3DTSS \_ texturetransformflags und D3DTSS \_ texcoordindex.</span><span class="sxs-lookup"><span data-stu-id="10eed-200">This state controls the manipulation of texture coordinates D3DTSS\_TEXTURETRANSFORMFLAGS and D3DTSS\_TEXCOORDINDEX.</span></span> <span data-ttu-id="10eed-201">Es können bis zu acht von jedem festgelegt werden (da acht Texturkoordinaten immer unterstützt werden).</span><span class="sxs-lookup"><span data-stu-id="10eed-201">Up to eight of each can be set (because eight texture coordinates are always supported).</span></span> <span data-ttu-id="10eed-202">D3DTSS \_ texcoordindex ist ein Status der Vertex-Verarbeitung fester Funktionen.</span><span class="sxs-lookup"><span data-stu-id="10eed-202">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="10eed-203">Wenn ein programmierbarer Vertex-Shader verwendet wird, wird dieser Zustand ignoriert.</span><span class="sxs-lookup"><span data-stu-id="10eed-203">If a programmable vertex shader is used, this state is ignored.</span></span>
-   <span data-ttu-id="10eed-204">Fester funktionspixelshader-Zustand (Legacy texturestagestate).</span><span class="sxs-lookup"><span data-stu-id="10eed-204">Fixed function pixel shader state (the legacy TextureStageState).</span></span>

    -   <span data-ttu-id="10eed-205">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="10eed-205">D3DTSS\_ALPHAARG0</span></span>
    -   <span data-ttu-id="10eed-206">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="10eed-206">D3DTSS\_ALPHAARG1</span></span>
    -   <span data-ttu-id="10eed-207">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="10eed-207">D3DTSS\_ALPHAARG2</span></span>
    -   <span data-ttu-id="10eed-208">D3DTSS \_ alphaop</span><span class="sxs-lookup"><span data-stu-id="10eed-208">D3DTSS\_ALPHAOP</span></span>
    -   <span data-ttu-id="10eed-209">D3DTSS \_ bumpenvloffset</span><span class="sxs-lookup"><span data-stu-id="10eed-209">D3DTSS\_BUMPENVLOFFSET</span></span>
    -   <span data-ttu-id="10eed-210">D3DTSS \_ bumpendvlscale</span><span class="sxs-lookup"><span data-stu-id="10eed-210">D3DTSS\_BUMPENVLSCALE</span></span>
    -   <span data-ttu-id="10eed-211">D3DTSS \_ BUMPENVMAT00</span><span class="sxs-lookup"><span data-stu-id="10eed-211">D3DTSS\_BUMPENVMAT00</span></span>
    -   <span data-ttu-id="10eed-212">D3DTSS \_ BUMPENVMAT01</span><span class="sxs-lookup"><span data-stu-id="10eed-212">D3DTSS\_BUMPENVMAT01</span></span>
    -   <span data-ttu-id="10eed-213">D3DTSS \_ BUMPENVMAT10</span><span class="sxs-lookup"><span data-stu-id="10eed-213">D3DTSS\_BUMPENVMAT10</span></span>
    -   <span data-ttu-id="10eed-214">D3DTSS \_ BUMPENVMAT11</span><span class="sxs-lookup"><span data-stu-id="10eed-214">D3DTSS\_BUMPENVMAT11</span></span>
    -   <span data-ttu-id="10eed-215">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="10eed-215">D3DTSS\_COLORARG0</span></span>
    -   <span data-ttu-id="10eed-216">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="10eed-216">D3DTSS\_COLORARG1</span></span>
    -   <span data-ttu-id="10eed-217">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="10eed-217">D3DTSS\_COLORARG2</span></span>
    -   <span data-ttu-id="10eed-218">D3DTSS \_ colorop</span><span class="sxs-lookup"><span data-stu-id="10eed-218">D3DTSS\_COLOROP</span></span>
    -   <span data-ttu-id="10eed-219">D3DTSS \_ resultarg</span><span class="sxs-lookup"><span data-stu-id="10eed-219">D3DTSS\_RESULTARG</span></span>

    <span data-ttu-id="10eed-220">Die Anzahl der festzulegenden Pixel-Shader-Zustände fester Funktionen ist kleiner oder gleich der durch MaxTextureBlendStages dargestellten Zahl.</span><span class="sxs-lookup"><span data-stu-id="10eed-220">The number of fixed function pixel shader states that can be set is less than or equal to the number represented by MaxTextureBlendStages.</span></span>

<span data-ttu-id="10eed-221">Die Anzahl der für die Anwendung verfügbaren Textur Samplern wird durch die Pixel-Shader-Version bestimmt, wie in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="10eed-221">The number of texture samplers available to the application is determined by the pixel shader version, as indicated in the following table.</span></span>



| <span data-ttu-id="10eed-222">Name</span><span class="sxs-lookup"><span data-stu-id="10eed-222">Name</span></span>                    | <span data-ttu-id="10eed-223">Number</span><span class="sxs-lookup"><span data-stu-id="10eed-223">Number</span></span>                                                         |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="10eed-224">PS \_ 1 1 \_ bis PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="10eed-224">ps\_1\_1 to ps\_1\_3</span></span>    | <span data-ttu-id="10eed-225">vier Textur-Samplern</span><span class="sxs-lookup"><span data-stu-id="10eed-225">4 texture samplers</span></span>                                             |
| <span data-ttu-id="10eed-226">PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="10eed-226">ps\_1\_4</span></span>                | <span data-ttu-id="10eed-227">6 Textur-Samplern</span><span class="sxs-lookup"><span data-stu-id="10eed-227">6 texture samplers</span></span>                                             |
| <span data-ttu-id="10eed-228">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="10eed-228">ps\_2\_0</span></span>                | <span data-ttu-id="10eed-229">16 Textur-Samplern</span><span class="sxs-lookup"><span data-stu-id="10eed-229">16 texture samplers</span></span>                                            |
| <span data-ttu-id="10eed-230">Fixed-Funktions Pipeline</span><span class="sxs-lookup"><span data-stu-id="10eed-230">fixed function pipeline</span></span> | <span data-ttu-id="10eed-231">MaxTextureBlendStages/maxdie oustextures Textur-Samplern</span><span class="sxs-lookup"><span data-stu-id="10eed-231">MaxTextureBlendStages/MaxSimultaneousTextures texture samplers</span></span> |



 

<span data-ttu-id="10eed-232">Geräte, die die Verschiebungs Zuordnung in Direct3D 9 unterstützen, unterstützen einen zusätzlichen Sampler (D3DDMAPSAMPLER), der die Verschiebungs Zuordnungen in der Mosaik Einheit abbildet.</span><span class="sxs-lookup"><span data-stu-id="10eed-232">Devices that support displacement mapping in Direct3D 9 will support an additional sampler (D3DDMAPSAMPLER), which samples the displacement maps in the tessellator unit.</span></span>

### <a name="setsamplerstate-changes"></a><span data-ttu-id="10eed-233">Setsamplerstate-Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-233">SetSamplerState Changes</span></span>

<span data-ttu-id="10eed-234">IDirect3DDevice9:: setsamplerstate legt den samplerstatus fest (einschließlich der in der Mosaik Einheit verwendeten Beispiel Verschiebungs Karten).</span><span class="sxs-lookup"><span data-stu-id="10eed-234">IDirect3DDevice9::SetSamplerState sets the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="10eed-235">Diese wurden mit einem D3DSAMP- \_ Präfix umbenannt, um die Kompilierzeit-Fehlererkennung beim Portieren aus DirectX 8. x zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="10eed-235">These have been renamed with a D3DSAMP\_ prefix to enable compile-time error detection when porting from DirectX 8.x.</span></span> <span data-ttu-id="10eed-236">Die Zustände umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="10eed-236">The states include:</span></span>

-   <span data-ttu-id="10eed-237">D3DSAMP \_ adressu</span><span class="sxs-lookup"><span data-stu-id="10eed-237">D3DSAMP\_ADDRESSU</span></span>
-   <span data-ttu-id="10eed-238">D3DSAMP \_ adressssv</span><span class="sxs-lookup"><span data-stu-id="10eed-238">D3DSAMP\_ADDRESSV</span></span>
-   <span data-ttu-id="10eed-239">D3DSAMP \_ AddressW</span><span class="sxs-lookup"><span data-stu-id="10eed-239">D3DSAMP\_ADDRESSW</span></span>
-   <span data-ttu-id="10eed-240">D3DSAMP \_ BorderColor</span><span class="sxs-lookup"><span data-stu-id="10eed-240">D3DSAMP\_BORDERCOLOR</span></span>
-   <span data-ttu-id="10eed-241">D3DSAMP- \_ MagFilter</span><span class="sxs-lookup"><span data-stu-id="10eed-241">D3DSAMP\_MAGFILTER</span></span>
-   <span data-ttu-id="10eed-242">D3DSAMP \_ MaxAnisotropy</span><span class="sxs-lookup"><span data-stu-id="10eed-242">D3DSAMP\_MAXANISOTROPY</span></span>
-   <span data-ttu-id="10eed-243">D3DSAMP \_ MaxMipLevel</span><span class="sxs-lookup"><span data-stu-id="10eed-243">D3DSAMP\_MAXMIPLEVEL</span></span>
-   <span data-ttu-id="10eed-244">D3DSAMP \_ MinFilter</span><span class="sxs-lookup"><span data-stu-id="10eed-244">D3DSAMP\_MINFILTER</span></span>
-   <span data-ttu-id="10eed-245">D3DSAMP \_ MipFilter</span><span class="sxs-lookup"><span data-stu-id="10eed-245">D3DSAMP\_MIPFILTER</span></span>
-   <span data-ttu-id="10eed-246">D3DSAMP \_ mipmaplodbias</span><span class="sxs-lookup"><span data-stu-id="10eed-246">D3DSAMP\_MIPMAPLODBIAS</span></span>

## <a name="vertex-declaration-changes"></a><span data-ttu-id="10eed-247">Vertex-Deklarations Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-247">Vertex Declaration Changes</span></span>

<span data-ttu-id="10eed-248">Vertex-Deklarationen werden nun von der Vertex-Shader-Erstellung entkoppelt.</span><span class="sxs-lookup"><span data-stu-id="10eed-248">Vertex declarations are now decoupled from vertex shader creation.</span></span> <span data-ttu-id="10eed-249">Vertex-Deklarationen verwenden jetzt eine Component Object Model (com)-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="10eed-249">Vertex declarations now use a Component Object Model (COM) interface.</span></span>

<span data-ttu-id="10eed-250">Bei DirectX 8. x sind Scheitelpunkt Deklarationen an Scheitelpunkt-Shader gebunden.</span><span class="sxs-lookup"><span data-stu-id="10eed-250">For DirectX 8.x, vertex declarations are tied to vertex shaders.</span></span>

-   <span data-ttu-id="10eed-251">Bei der Fixed-Funktions Pipeline wird [**setvertexshader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) mit dem Code des flexiblen Scheitelpunkt Formats (FVF) des Scheitelpunkt Puffers aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="10eed-251">For the fixed function pipeline, call [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) with the flexible vertex format (FVF) code of the vertex buffer.</span></span>
-   <span data-ttu-id="10eed-252">Rufen Sie für Vertex-Shader IDirect3DDevice9:: setvertexshader mit einem Handle für einen zuvor erstellten Scheitelpunkt-Shader auf.</span><span class="sxs-lookup"><span data-stu-id="10eed-252">For vertex shaders, call IDirect3DDevice9::SetVertexShader with a handle to a previously create vertex shader.</span></span> <span data-ttu-id="10eed-253">Der Shader enthält eine Scheitelpunkt Deklaration.</span><span class="sxs-lookup"><span data-stu-id="10eed-253">The shader includes a vertex declaration.</span></span>

<span data-ttu-id="10eed-254">Bei Direct3D 9 sind Scheitelpunkt Deklarationen von Vertex-Shadern entkoppelt und können mit der Fixed-Funktions Pipeline oder mit Shadern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10eed-254">For Direct3D 9, vertex declarations are decoupled from vertex shaders and they can be used with either the fixed function pipeline or with shaders.</span></span>

-   <span data-ttu-id="10eed-255">Bei der Fixed-Funktions Pipeline muss IDirect3DDevice9:: setvertexshader nicht aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="10eed-255">For the fixed function pipeline, there is no need to call IDirect3DDevice9::SetVertexShader.</span></span> <span data-ttu-id="10eed-256">Wenn Sie jedoch zur Fixed-Funktions Pipeline wechseln und zuvor einen Vertex-Shader verwendet haben, aufrufen Sie IDirect3DDevice9:: setvertexshader (**null**).</span><span class="sxs-lookup"><span data-stu-id="10eed-256">If, however, you want to switch to the fixed function pipeline and have previously used a vertex shader, call IDirect3DDevice9::SetVertexShader(**NULL**).</span></span> <span data-ttu-id="10eed-257">Wenn dies der Fall ist, müssen Sie auch [**setfvf**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) aufrufen, um den FVF-Code zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="10eed-257">When this is done, you will still need to call [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) to declare the FVF code.</span></span>
-   <span data-ttu-id="10eed-258">Beim Verwenden von Vertex-Shadern wird IDirect3DDevice9:: setvertexshader mit dem Vertex-Shader-Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="10eed-258">When using vertex shaders, call IDirect3DDevice9::SetVertexShader with the vertex shader object.</span></span> <span data-ttu-id="10eed-259">Außerdem müssen Sie IDirect3DDevice9:: setfvf aufrufen, um eine Scheitelpunkt Deklaration einzurichten.</span><span class="sxs-lookup"><span data-stu-id="10eed-259">Additionally, call IDirect3DDevice9::SetFVF to set up a vertex declaration.</span></span> <span data-ttu-id="10eed-260">Dabei werden die Informationen verwendet, die in der "f" implizit sind.</span><span class="sxs-lookup"><span data-stu-id="10eed-260">This uses the information implicit in the FVF.</span></span> <span data-ttu-id="10eed-261">[**Setvertexdeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) kann anstelle von IDirect3DDevice9:: setfvf aufgerufen werden, da es Scheitelpunkt Deklarationen unterstützt, die nicht mit einem FVF ausgedrückt werden können.</span><span class="sxs-lookup"><span data-stu-id="10eed-261">[**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) can be called in place of IDirect3DDevice9::SetFVF because it supports vertex declarations that cannot be expressed with an FVF.</span></span>

## <a name="intervals-and-swapeffects-changes"></a><span data-ttu-id="10eed-262">Intervalle und Austauschen von Änderungen</span><span class="sxs-lookup"><span data-stu-id="10eed-262">Intervals, and SwapEffects Changes</span></span>

<span data-ttu-id="10eed-263">Es wurden mehrere Änderungen vorgenommen, um dem Benutzer eine bessere Kontrolle über die Aktualisierungsrate des Monitors, die Präsentations Rate und den Vorder-und Hintergrund Puffer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="10eed-263">Several changes were made to give the user more control over monitor refresh rate, presentation rate, and front-buffer versus back-buffer drawing.</span></span> <span data-ttu-id="10eed-264">Dies sind:</span><span class="sxs-lookup"><span data-stu-id="10eed-264">They are as follows:</span></span>

-   <span data-ttu-id="10eed-265">Ein Auslagerungs Effekt, D3DSWAPEFFECT \_ Copy \_ VSYNC und eine Präsentations Rate, D3DPRESENT \_ Rate \_ Unlimited, wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="10eed-265">Removed one swap effect, D3DSWAPEFFECT\_COPY\_VSYNC, and one presentation rate, D3DPRESENT\_RATE\_UNLIMITED.</span></span>
-   <span data-ttu-id="10eed-266">Umbenannte D3DPRESENT- \_ Parameter. Vollbild- \_ presentationinterval zu presentationinterval.</span><span class="sxs-lookup"><span data-stu-id="10eed-266">Renamed D3DPRESENT\_PARAMETERS.FullScreen\_PresentationInterval to PresentationIntervals.</span></span>
-   <span data-ttu-id="10eed-267">D3DPRESENT \_ Interval \_ wurde sofort hinzugefügt, was bedeutet, dass die Präsentation nicht mit der vertikalen Synchronisierung synchronisiert wird. Wie in DirectX 8. x ist D3DPRESENT \_ Interval \_ Default als 0 (null) definiert und entspricht D3DPRESENT \_ Interval \_ 1.</span><span class="sxs-lookup"><span data-stu-id="10eed-267">Added D3DPRESENT\_INTERVAL\_IMMEDIATE, which means that the presentation is not synchronized with the vertical sync. As in DirectX 8.x, D3DPRESENT\_INTERVAL\_DEFAULT is defined as zero and is equivalent to D3DPRESENT\_INTERVAL\_ONE.</span></span> <span data-ttu-id="10eed-268">D3DPRESENT \_ Interval \_ Default ist eine einfache Initialisierung von D3DPRESENT- \_ Parametern mit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="10eed-268">D3DPRESENT\_INTERVAL\_DEFAULT is a convenience for initializing D3DPRESENT\_PARAMETERS to zero.</span></span>

<span data-ttu-id="10eed-269">Eine ausführliche Erläuterung der Modi und der unterstützten Intervalle finden Sie unter D3DPRESENT.</span><span class="sxs-lookup"><span data-stu-id="10eed-269">For a detailed explanation of the modes and the intervals that are supported, see D3DPRESENT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10eed-270">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="10eed-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10eed-271">Direct3D 9-Grafiken</span><span class="sxs-lookup"><span data-stu-id="10eed-271">Direct3D 9 Graphics</span></span>](dx9-graphics.md)
</dt> </dl>

 

 
