---
description: 'Wenn IDirect3DDevice9:: updatesurface verwendet wird, übergeben Sie ein Rechteck auf der Quell Oberfläche, oder verwenden Sie NULL, um die gesamte Oberfläche anzugeben.'
ms.assetid: 2219d037-8480-4c36-b04e-0c23406a2e7e
title: Kopieren auf Oberflächen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163907aada5b2396a2a103d94af49d7ddd01d5ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483838"
---
# <a name="copying-to-surfaces-direct3d-9"></a><span data-ttu-id="99d51-103">Kopieren auf Oberflächen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="99d51-103">Copying to Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="99d51-104">Wenn [**IDirect3DDevice9:: updatesurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)verwendet wird, übergeben Sie ein Rechteck auf der Quell Oberfläche, oder verwenden Sie **null** , um die gesamte Oberfläche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="99d51-104">When using [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), pass a rectangle on the source surface, or use **NULL** to specify the entire surface.</span></span> <span data-ttu-id="99d51-105">Außerdem übergeben Sie einen Punkt auf der Ziel Oberfläche, auf den die obere linke Position des Rechtecks im Quellbild kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="99d51-105">You also pass a point on the destination surface to which the upper left position of the rectangle on the source image is copied.</span></span> <span data-ttu-id="99d51-106">Diese Methode unterstützt kein Clipping.</span><span class="sxs-lookup"><span data-stu-id="99d51-106">This method does not support clipping.</span></span> <span data-ttu-id="99d51-107">Der Vorgang schlägt fehl, es sei denn, das Quell Rechteck und das zugehörige Ziel Rechteck sind vollständig in den Quell-und Ziel Oberflächen enthalten.</span><span class="sxs-lookup"><span data-stu-id="99d51-107">The operation will fail unless the source rectangle and the corresponding destination rectangle are completely contained within the source and destination surfaces respectively.</span></span> <span data-ttu-id="99d51-108">Diese Methode unterstützt keine Alpha Blending, Farbtasten oder Formatkonvertierung.</span><span class="sxs-lookup"><span data-stu-id="99d51-108">This method does not support alpha blending, color keys, or format conversion.</span></span> <span data-ttu-id="99d51-109">Beachten Sie, dass sich die Ziel-und Quell Oberflächen unterscheiden müssen.</span><span class="sxs-lookup"><span data-stu-id="99d51-109">Note that the destination and source surfaces must be distinct.</span></span>

<span data-ttu-id="99d51-110">Weitere Einschränkungen bei der Verwendung von updatesurface finden Sie unter [**IDirect3DDevice9:: updatesurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).</span><span class="sxs-lookup"><span data-stu-id="99d51-110">For other restrictions when using UpdateSurface, see [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).</span></span>

<span data-ttu-id="99d51-111">Die folgenden Methoden sind auch in C++/C zum Kopieren von Bildern auf eine Direct3D-Oberfläche verfügbar.</span><span class="sxs-lookup"><span data-stu-id="99d51-111">The following methods are also available in C++/C for copying images to a Direct3D surface.</span></span>

-   [<span data-ttu-id="99d51-112">**D3DXLoadSurfaceFromFile**</span><span class="sxs-lookup"><span data-stu-id="99d51-112">**D3DXLoadSurfaceFromFile**</span></span>](d3dxloadsurfacefromfile.md)
-   [<span data-ttu-id="99d51-113">**D3DXLoadSurfaceFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="99d51-113">**D3DXLoadSurfaceFromFileInMemory**</span></span>](d3dxloadsurfacefromfileinmemory.md)
-   [<span data-ttu-id="99d51-114">**D3DXLoadSurfaceFromMemory**</span><span class="sxs-lookup"><span data-stu-id="99d51-114">**D3DXLoadSurfaceFromMemory**</span></span>](d3dxloadsurfacefrommemory.md)
-   [<span data-ttu-id="99d51-115">**D3DXLoadSurfaceFromResource**</span><span class="sxs-lookup"><span data-stu-id="99d51-115">**D3DXLoadSurfaceFromResource**</span></span>](d3dxloadsurfacefromresource.md)
-   [<span data-ttu-id="99d51-116">**D3DXLoadSurfaceFromSurface**</span><span class="sxs-lookup"><span data-stu-id="99d51-116">**D3DXLoadSurfaceFromSurface**</span></span>](d3dxloadsurfacefromsurface.md)
-   [<span data-ttu-id="99d51-117">**IDirect3DDevice9:: updatesurface**</span><span class="sxs-lookup"><span data-stu-id="99d51-117">**IDirect3DDevice9::UpdateSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a><span data-ttu-id="99d51-118">Updatesurface-Beispiel</span><span class="sxs-lookup"><span data-stu-id="99d51-118">UpdateSurface Example</span></span>

<span data-ttu-id="99d51-119">Im folgenden Beispiel werden zwei Rechtecke von der Quell Oberfläche auf eine Ziel Oberfläche kopiert.</span><span class="sxs-lookup"><span data-stu-id="99d51-119">The following example copies two rectangles from the source surface to a destination surface.</span></span> <span data-ttu-id="99d51-120">Das erste Rechteck wird von (0, 0, 50, 50) auf der Quell Oberfläche an denselben Speicherort auf der Ziel Oberfläche kopiert, und das zweite Rechteck wird von (50, 50, 100, 100) auf der Quell Oberfläche in (150, 150, 200, 200) auf der Ziel Oberfläche kopiert.</span><span class="sxs-lookup"><span data-stu-id="99d51-120">The first rectangle is copied from (0, 0, 50, 50) on the source surface to the same location on the destination surface, and the second rectangle is copied from (50, 50, 100, 100) on the source surface to (150, 150, 200, 200) on the destination surface.</span></span>


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a><span data-ttu-id="99d51-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99d51-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99d51-122">Direct3D-Oberflächen</span><span class="sxs-lookup"><span data-stu-id="99d51-122">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="99d51-123">**IDirect3DDevice9:: stretchrect**</span><span class="sxs-lookup"><span data-stu-id="99d51-123">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
