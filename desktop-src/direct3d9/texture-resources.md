---
description: Textur Ressourcen werden in der IDirect3DTexture9-Schnittstelle implementiert. Um einen Zeiger auf eine Textur Schnittstelle zu erhalten, rufen Sie die IDirect3DDevice9::-Methode oder eine der folgenden D3DX-Funktionen auf.
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Textur Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14134ca53b7735426e3f01340308282858da5516
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213975"
---
# <a name="texture-resources-direct3d-9"></a><span data-ttu-id="515f1-104">Textur Ressourcen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="515f1-104">Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="515f1-105">Textur Ressourcen werden in der [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="515f1-105">Texture resources are implemented in the [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface.</span></span> <span data-ttu-id="515f1-106">Um einen Zeiger auf eine Textur Schnittstelle zu erhalten, rufen Sie die [**IDirect3DDevice9::**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) -Methode oder eine der folgenden D3DX-Funktionen auf.</span><span class="sxs-lookup"><span data-stu-id="515f1-106">To obtain a pointer to a texture interface, call the [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) method or any of the following D3DX functions.</span></span>

-   [<span data-ttu-id="515f1-107">**D3DXCreateTexture**</span><span class="sxs-lookup"><span data-stu-id="515f1-107">**D3DXCreateTexture**</span></span>](d3dxcreatetexture.md)
-   [<span data-ttu-id="515f1-108">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="515f1-108">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
-   [<span data-ttu-id="515f1-109">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="515f1-109">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
-   [<span data-ttu-id="515f1-110">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="515f1-110">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
-   [<span data-ttu-id="515f1-111">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="515f1-111">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
-   [<span data-ttu-id="515f1-112">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="515f1-112">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
-   [<span data-ttu-id="515f1-113">**D3DXCreateTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="515f1-113">**D3DXCreateTextureFromResourceEx**</span></span>](d3dxcreatetexturefromresourceex.md)

<span data-ttu-id="515f1-114">Im folgenden Codebeispiel wird [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) verwendet, um eine Textur aus Tiger.bmp zu laden.</span><span class="sxs-lookup"><span data-stu-id="515f1-114">The following code example uses [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) to load a texture from Tiger.bmp.</span></span>


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



<span data-ttu-id="515f1-115">Der erste Parameter, den [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) annimmt, ist ein Zeiger auf eine [**IDirect3DDevice9**](/windows/desktop/api) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="515f1-115">The first parameter that [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) accepts is a pointer to an [**IDirect3DDevice9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="515f1-116">Der zweite Parameter teilt Direct3D den Namen der Datei, aus der die Textur geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="515f1-116">The second parameter tells Direct3D the name of the file from which to load the texture.</span></span> <span data-ttu-id="515f1-117">Der dritte Parameter übernimmt die Adresse eines Zeigers auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="515f1-117">The third parameter takes the address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

## <a name="rendering-with-texture-resources"></a><span data-ttu-id="515f1-118">Rendering mit Textur Ressourcen</span><span class="sxs-lookup"><span data-stu-id="515f1-118">Rendering with Texture Resources</span></span>

<span data-ttu-id="515f1-119">Direct3D unterstützt mehrere Textur-Mischungen durch das Konzept von Textur Stufen.</span><span class="sxs-lookup"><span data-stu-id="515f1-119">Direct3D supports multiple texture blending through the concept of texture stages.</span></span> <span data-ttu-id="515f1-120">Jede Textur Phase enthält eine Textur und Vorgänge, die für die Textur ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="515f1-120">Each texture stage contains a texture and operations that can be performed on the texture.</span></span> <span data-ttu-id="515f1-121">Die Texturen in den Textur Stufen bilden den Satz der aktuellen Texturen.</span><span class="sxs-lookup"><span data-stu-id="515f1-121">The textures in the texture stages form the set of current textures.</span></span> <span data-ttu-id="515f1-122">Weitere Informationen finden Sie unter [Textur blending (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="515f1-122">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="515f1-123">Der Zustand jeder Textur wird in der Textur Phase gekapselt.</span><span class="sxs-lookup"><span data-stu-id="515f1-123">The state of each texture is encapsulated in its texture stage.</span></span>

<span data-ttu-id="515f1-124">In einer C++-Anwendung muss der Zustand jeder Textur mit der [**IDirect3DDevice9:: settexturestagestate**](/windows/desktop/api) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="515f1-124">In a C++ application, the state of each texture must be set with the [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="515f1-125">Übergeben Sie die Phasen Nummer (0-7) als Wert des ersten Parameters.</span><span class="sxs-lookup"><span data-stu-id="515f1-125">Pass the stage number (0-7) as the value of the first parameter.</span></span> <span data-ttu-id="515f1-126">Legen Sie den Wert des zweiten Parameters auf einen Member des [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) -Enumerationstyps fest.</span><span class="sxs-lookup"><span data-stu-id="515f1-126">Set the value of the second parameter to a member of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="515f1-127">Der letzte Parameter ist der Zustandswert für den jeweiligen Textur Zustand.</span><span class="sxs-lookup"><span data-stu-id="515f1-127">The final parameter is the state value for the particular texture state.</span></span>

<span data-ttu-id="515f1-128">Mithilfe von Textur Schnittstellen Zeigern kann die Anwendung eine Mischung von bis zu acht Texturen darstellen.</span><span class="sxs-lookup"><span data-stu-id="515f1-128">Using texture interface pointers, your application can render a blend of up to eight textures.</span></span> <span data-ttu-id="515f1-129">Legen Sie die aktuellen Texturen fest, indem Sie die [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="515f1-129">Set the current textures by invoking the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="515f1-130">Direct3D vermischt alle aktuellen Texturen mit den primitiven, die Sie rendert.</span><span class="sxs-lookup"><span data-stu-id="515f1-130">Direct3D blends all current textures onto the primitives that it renders.</span></span>

> [!Note]  
> <span data-ttu-id="515f1-131">Die [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -Methode erhöht den Verweis Zähler der zugewiesenen Textur Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="515f1-131">The [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method increments the reference count of the texture surface being assigned.</span></span> <span data-ttu-id="515f1-132">Wenn die Textur nicht mehr benötigt wird, sollten Sie die Textur in der entsprechenden Phase auf **null** festlegen.</span><span class="sxs-lookup"><span data-stu-id="515f1-132">When the texture is no longer needed, you should set the texture at the appropriate stage to **NULL**.</span></span> <span data-ttu-id="515f1-133">Wenn Sie dies nicht tun, wird die Oberfläche nicht freigegeben, was zu einem Speicherfehler führt.</span><span class="sxs-lookup"><span data-stu-id="515f1-133">If you fail to do this, the surface will not be released, resulting in a memory leak.</span></span>

 

<span data-ttu-id="515f1-134">Die Anwendung kann den texturwrapping Zustand für die aktuellen Texturen durch Aufrufen der [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode festlegen.</span><span class="sxs-lookup"><span data-stu-id="515f1-134">Your application can set the texture wrapping state for the current textures by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method.</span></span> <span data-ttu-id="515f1-135">Übergeben Sie einen Wert von D3DRS \_ WRAP0 bis D3DRS \_ WRAP7 als Wert des ersten Parameters, und verwenden Sie eine Kombination der \_ Flags D3DWRAPCOORD 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD \_ 2 und D3DWRAPCOORD \_ 3, um das Umleiten in den Richtungen u, v oder w zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="515f1-135">Pass a value from D3DRS\_WRAP0 through D3DRS\_WRAP7 as the value of the first parameter, and use a combination of the D3DWRAPCOORD\_0, D3DWRAPCOORD\_1, D3DWRAPCOORD\_2, and D3DWRAPCOORD\_3 flags to enable wrapping in the u, v, or w directions.</span></span>

<span data-ttu-id="515f1-136">Die Anwendung kann auch die Textur Perspektive und die Textur Filter Zustände festlegen.</span><span class="sxs-lookup"><span data-stu-id="515f1-136">Your application can also set the texture perspective and texture filtering states.</span></span> <span data-ttu-id="515f1-137">Weitere Informationen finden Sie unter [Textur Filterung (Direct3D 9)](texture-filtering.md).</span><span class="sxs-lookup"><span data-stu-id="515f1-137">See [Texture Filtering (Direct3D 9)](texture-filtering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="515f1-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="515f1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="515f1-139">Direct3D-Texturen</span><span class="sxs-lookup"><span data-stu-id="515f1-139">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
