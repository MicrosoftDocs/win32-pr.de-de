---
description: Das Vollbild-Antialiasing bezieht sich auf das Verwischen der Kanten der einzelnen Polygon in der Szene, wenn es in einem einzigen Durchlauf gerragt wird. Es ist kein zweiter Durchlauf erforderlich.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Full-Scene Antialiasing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73d559c4b4fec060efbff7468ee29e6c83b64c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520912"
---
# <a name="full-scene-antialiasing-direct3d-9"></a><span data-ttu-id="15d11-103">Full-Scene Antialiasing (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="15d11-103">Full-Scene Antialiasing (Direct3D 9)</span></span>

<span data-ttu-id="15d11-104">Das Vollbild-Antialiasing bezieht sich auf das Verwischen der Kanten der einzelnen Polygon in der Szene, wenn es in einem einzigen Durchlauf gerragt wird. Es ist kein zweiter Durchlauf erforderlich.</span><span class="sxs-lookup"><span data-stu-id="15d11-104">Full-scene antialiasing refers to blurring the edges of each polygon in the scene as it is rasterized in a single pass; no second pass is required.</span></span> <span data-ttu-id="15d11-105">Das Vollbild-Antialiasing wirkt sich bei Unterstützung nur auf Dreiecke und Gruppen von Dreiecken aus.</span><span class="sxs-lookup"><span data-stu-id="15d11-105">Full-scene antialiasing, when supported, affects only triangles and groups of triangles.</span></span> <span data-ttu-id="15d11-106">Zeilen können nicht mithilfe von Direct3D Services als Antialiasing verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15d11-106">Lines cannot be antialiased by using Direct3D services.</span></span> <span data-ttu-id="15d11-107">Das Vollbild-Antialiasing erfolgt in Direct3D mithilfe von multisamplinggrad auf den einzelnen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="15d11-107">Full-scene antialiasing is done in Direct3D by using multisampling on each pixel.</span></span> <span data-ttu-id="15d11-108">Wenn die multisamplinggrad-Funktion aktiviert ist, werden alle Teil Beispiele eines Pixels in einem Durchlauf aktualisiert. Wenn Sie jedoch für andere Effekte verwendet werden, die mehrere Renderingdurchläufen einschließen, kann die Anwendung angeben, dass nur einige unter Beispiele von einem gegebenen Renderingdurchlauf betroffen sein sollen.</span><span class="sxs-lookup"><span data-stu-id="15d11-108">When multisampling is enabled, all subsamples of a pixel are updated in one pass but when used for other effects that involve multiple rendering passes, the application can specify that only some subsamples are to be affected by a given rendering pass.</span></span> <span data-ttu-id="15d11-109">Mit diesem letzteren Ansatz wird die Simulation von Bewegungsunschärfe, tiefen Fokus Effekten, reflektionstypen usw. ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="15d11-109">This latter approach enables simulation of motion blur, depth-of-field focus effects, reflection blur, and so on.</span></span>

<span data-ttu-id="15d11-110">In beiden Fällen werden die verschiedenen für jedes Pixel aufgezeichneten Beispiele kombiniert und auf dem Bildschirm ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="15d11-110">In both cases, the various samples recorded for each pixel are blended together and output to the screen.</span></span> <span data-ttu-id="15d11-111">Dies ermöglicht die verbesserte Bildqualität von Antialiasing oder anderen Effekten.</span><span class="sxs-lookup"><span data-stu-id="15d11-111">This enables the improved image quality of antialiasing or other effects.</span></span>

<span data-ttu-id="15d11-112">Vor dem Erstellen eines Geräts mit der [**IDirect3D9:: kreatedevice**](/windows/desktop/api) -Methode müssen Sie bestimmen, ob das Vollbild-Antialiasing unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="15d11-112">Before creating a device with the [**IDirect3D9::CreateDevice**](/windows/desktop/api) method, you need to determine if full-scene antialiasing is supported.</span></span> <span data-ttu-id="15d11-113">Rufen Sie dazu die [**IDirect3D9:: checkdevicemultisampletype**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) -Methode auf, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="15d11-113">Do this by calling the [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) method as shown in the code example below.</span></span>


```
/*
* The code below assumes that pD3D is a valid pointer 
*   to a IDirect3D9 interface.
*/

if( SUCCEEDED(pD3D->CheckDeviceMultiSampleType( D3DADAPTER_DEFAULT, 
                    D3DDEVTYPE_HAL , D3DFMT_R8G8B8, FALSE, 
                    D3DMULTISAMPLE_2_SAMPLES, NULL ) ) )
// Full-scene antialiasing is supported. Enable it here.
```



<span data-ttu-id="15d11-114">Der erste Parameter, den [**IDirect3D9:: checkdevicemultisampletype**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) annimmt, ist eine Ordinalzahl, die den abzufragenden Anzeige Adapter angibt.</span><span class="sxs-lookup"><span data-stu-id="15d11-114">The first parameter that [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) accepts is an ordinal number that denotes the display adapter to query.</span></span> <span data-ttu-id="15d11-115">In diesem Beispiel wird D3DADAPTER \_ default verwendet, um den primären Anzeige Adapter anzugeben.</span><span class="sxs-lookup"><span data-stu-id="15d11-115">This sample uses D3DADAPTER\_DEFAULT to specify the primary display adapter.</span></span> <span data-ttu-id="15d11-116">Der zweite Parameter ist ein Wert aus dem [**D3DDEVTYPE**](./d3ddevtype.md) -Enumerationstyp, der den Gerätetyp angibt.</span><span class="sxs-lookup"><span data-stu-id="15d11-116">The second parameter is a value from the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type, specifying the device type.</span></span> <span data-ttu-id="15d11-117">Der dritte Parameter gibt das Format der-Oberfläche an.</span><span class="sxs-lookup"><span data-stu-id="15d11-117">The third parameter specifies the format of the surface.</span></span> <span data-ttu-id="15d11-118">Der vierte Parameter gibt Direct3D an, ob die multisamplinggrad-Funktion (**true**) oder das Vollbild-Antialiasing (**false**) vollständig im Fenster beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="15d11-118">The fourth parameter tells Direct3D whether to inquire about full-windowed multisampling (**TRUE**) or full-scene antialiasing (**FALSE**).</span></span> <span data-ttu-id="15d11-119">In diesem Beispiel wird **false** verwendet, um Direct3D zu sagen, dass es sich um das Antialiasing in der vollständigen Szene handelt.</span><span class="sxs-lookup"><span data-stu-id="15d11-119">This sample uses **FALSE** to tell Direct3D that it is inquiring about full-scene antialiasing.</span></span> <span data-ttu-id="15d11-120">Der letzte Parameter gibt die multisamplinggrad-Methode an, die Sie testen möchten.</span><span class="sxs-lookup"><span data-stu-id="15d11-120">The last parameter specifies the multisampling technique that you want to test.</span></span> <span data-ttu-id="15d11-121">Verwenden Sie einen Wert aus dem enumerierten Typ [**D3DMULTISAMPLE \_ Type**](./d3dmultisample-type.md) .</span><span class="sxs-lookup"><span data-stu-id="15d11-121">Use a value from the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="15d11-122">In diesem Beispiel wird getestet, ob zwei Ebenen von multisamplinggrad unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="15d11-122">This sample tests to see if two levels of multisampling are supported.</span></span>

<span data-ttu-id="15d11-123">Wenn das Gerät die gewünschte multisamplinggrad-Ebene unterstützt, besteht der nächste Schritt darin, die Präsentations Parameter festzulegen, indem die entsprechenden Member der [**D3DPRESENT \_ Parameters**](d3dpresent-parameters.md) -Struktur ausgefüllt werden, um eine Multisampling-Renderingoberfläche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="15d11-123">If the device supports the level of multisampling that you want to use, the next step is to set the presentation parameters by filling in the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to create a multisample rendering surface.</span></span> <span data-ttu-id="15d11-124">Danach können Sie das Gerät erstellen.</span><span class="sxs-lookup"><span data-stu-id="15d11-124">After that, you can create the device.</span></span> <span data-ttu-id="15d11-125">Der folgende Beispielcode zeigt, wie Sie ein Gerät mit einer multisamplinggrad-Renderoberfläche einrichten.</span><span class="sxs-lookup"><span data-stu-id="15d11-125">The sample code below shows how to set up a device with a multisampling render surface.</span></span>


```
/*
* The example below assumes that pD3D is a valid pointer 
* to a IDirect3D9 interface, d3dDevice is a pointer to a 
* IDirect3DDevice9 interface, and hWnd is a valid handle
* to a window.
*/

D3DPRESENT_PARAMETER d3dPP
ZeroMemory( &d3dPP, sizeof( d3dPP ) );
d3dPP.Windowed        = FALSE
d3dPP.SwapEffect      = D3DSWAPEFFECT_DISCARD;
d3dPP.MultiSampleType = D3DMULTISAMPLE_2_SAMPLES;
pD3D->CreateDevice(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                    &d3dpp, &d3dDevice)
```



<span data-ttu-id="15d11-126">Zum Verwenden von Multisampling muss das Member-Element von "D3DPRESENT" \_ auf "D3DSWAPEFFECT verwerfen" festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="15d11-126">To use multisampling, the SwapEffect member of D3DPRESENT\_PARAMETER must be set to D3DSWAPEFFECT\_DISCARD.</span></span>

<span data-ttu-id="15d11-127">Der letzte Schritt besteht darin, das multisamplinggrad-Antialiasing zu aktivieren, indem die [**IDirect3DDevice9:: btrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode aufgerufen und der D3DRS \_ multisampleantialias auf **true** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="15d11-127">The last step is to enable multisampling antialiasing by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method and setting the D3DRS\_MULTISAMPLEANTIALIAS to **TRUE**.</span></span> <span data-ttu-id="15d11-128">Nachdem Sie diesen Wert auf " **true**" festgelegt haben, wird für jedes Rendering, das Sie ausführen, eine multisamplinggrad-Funktion angewendet.</span><span class="sxs-lookup"><span data-stu-id="15d11-128">After setting this value to **TRUE**, any rendering that you do will have multisampling applied to it.</span></span> <span data-ttu-id="15d11-129">Je nachdem, was Sie rendern, empfiehlt es sich, Multisampling zu aktivieren und zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="15d11-129">You might want to enable and disable multisampling, depending on what you are rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15d11-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15d11-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15d11-131">Antialiasing</span><span class="sxs-lookup"><span data-stu-id="15d11-131">Antialiasing</span></span>](antialiasing.md)
</dt> </dl>

 

 
