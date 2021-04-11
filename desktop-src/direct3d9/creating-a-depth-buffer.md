---
description: Ein tiefen Puffer ist eine Eigenschaft des Geräts. Zum Erstellen eines tiefen Puffers, der von Direct3D verwaltet wird, legen Sie die entsprechenden Member der D3DPRESENT- \_ Parameter Struktur fest, wie im folgenden Codebeispiel gezeigt.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Erstellen eines tiefen Puffers (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa30ccba6c44d3582201ea96017a16cc903fecce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126158"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a><span data-ttu-id="05690-104">Erstellen eines tiefen Puffers (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05690-104">Creating a Depth Buffer (Direct3D 9)</span></span>

<span data-ttu-id="05690-105">Ein tiefen Puffer ist eine Eigenschaft des Geräts.</span><span class="sxs-lookup"><span data-stu-id="05690-105">A depth buffer is a property of the device.</span></span> <span data-ttu-id="05690-106">Zum Erstellen eines tiefen Puffers, der von Direct3D verwaltet wird, legen Sie die entsprechenden Member der [**D3DPRESENT- \_ Parameter**](d3dpresent-parameters.md) Struktur fest, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="05690-106">To create a depth buffer that is managed by Direct3D, set the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure as shown in the following code example.</span></span>


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



<span data-ttu-id="05690-107">Indem Sie den enableautodepthstencil-Member auf " **true**" festlegen, weisen Sie Direct3D an, die tiefen Puffer für die Anwendung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="05690-107">By setting the EnableAutoDepthStencil member to **TRUE**, you instruct Direct3D to manage depth buffers for the application.</span></span> <span data-ttu-id="05690-108">Beachten Sie, dass autodepthstencilformat auf ein gültiges Tiefe Puffer Format festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="05690-108">Note that AutoDepthStencilFormat must be set to a valid depth buffer format.</span></span> <span data-ttu-id="05690-109">Das \_ Flag D3DFMT D16 gibt einen 16-Bit-Tiefen Puffer an, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="05690-109">The D3DFMT\_D16 flag specifies a 16-bit depth buffer, if one is available.</span></span>

<span data-ttu-id="05690-110">Mit dem folgenden Aufrufen der [**IDirect3D9:: kreatedevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) -Methode wird ein Gerät erstellt, das dann einen tiefen Puffer erstellt.</span><span class="sxs-lookup"><span data-stu-id="05690-110">The following call to the [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) method creates a device that then creates a depth buffer.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



<span data-ttu-id="05690-111">Der tiefen Puffer wird automatisch als Renderziel des Geräts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="05690-111">The depth buffer is automatically set as the render target of the device.</span></span> <span data-ttu-id="05690-112">Wenn das Gerät zurückgesetzt wird, wird der tiefen Puffer automatisch zerstört und in der neuen Größe neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="05690-112">When the device is reset, the depth buffer is automatically destroyed and re-created in the new size.</span></span>

<span data-ttu-id="05690-113">Verwenden Sie die [**IDirect3DDevice9:: foatedepthstencilsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) -Methode, um eine neue tiefen Puffer Oberfläche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="05690-113">To create a new depth buffer surface, use the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) method.</span></span>

<span data-ttu-id="05690-114">Verwenden Sie die [**IDirect3DDevice9:: setdepthstencilsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) -Methode, um eine neue tiefen Puffer Oberfläche für das Gerät festzulegen.</span><span class="sxs-lookup"><span data-stu-id="05690-114">To set a new depth-buffer surface for the device, use the [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) method.</span></span>

<span data-ttu-id="05690-115">Um den tiefen Puffer in der Anwendung zu verwenden, müssen Sie den tiefen Puffer aktivieren.</span><span class="sxs-lookup"><span data-stu-id="05690-115">To use the depth buffer in your application, you need to enable the depth buffer.</span></span> <span data-ttu-id="05690-116">Weitere Informationen finden Sie unter [Aktivieren der tiefen Pufferung (Direct3D 9)](enabling-depth-buffering.md).</span><span class="sxs-lookup"><span data-stu-id="05690-116">For details, see [Enabling Depth Buffering (Direct3D 9)](enabling-depth-buffering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="05690-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="05690-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05690-118">Tiefen Puffer</span><span class="sxs-lookup"><span data-stu-id="05690-118">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
