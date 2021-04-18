---
description: Der Begriff Blit ist eine \# Kurznotiz für &0034, Bitblock Übertragung, &\# 0034. dabei handelt es sich um den Prozess, bei dem Datenblöcke von einem Speicherort im Arbeitsspeicher auf einen anderen übertragen werden.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Kopieren von Oberflächen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344372"
---
# <a name="copying-surfaces-direct3d-9"></a><span data-ttu-id="667c6-103">Kopieren von Oberflächen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="667c6-103">Copying Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="667c6-104">Der Begriff Blit ist eine Kurznotiz für "Bitblock Übertragung", bei der es sich um den Prozess der Übertragung von Datenblöcken von einem Speicherort im Arbeitsspeicher auf einen anderen handelt.</span><span class="sxs-lookup"><span data-stu-id="667c6-104">The term blit is shorthand for "bit block transfer," which is the process of transferring blocks of data from one place in memory to another.</span></span> <span data-ttu-id="667c6-105">Die blitinggeräte Treiberschnittstelle (DDI) wird weiterhin in Direct3D 9 als primärer Mechanismus zum Verschieben großer Rechtecke von Pixeln pro Frame verwendet, der Mechanismus hinter der Kopier orientierten [**IDirect3DDevice9::P Resent**](/windows/desktop/api) -Methode.</span><span class="sxs-lookup"><span data-stu-id="667c6-105">The blitting device driver interface (DDI) continues to be used in Direct3D 9 as the primary mechanism for moving large rectangles of pixels on a per-frame basis, the mechanism behind the copy-oriented [**IDirect3DDevice9::Present**](/windows/desktop/api) method.</span></span> <span data-ttu-id="667c6-106">Der Transport von Grafiken im Blit-Vorgang wird von der [**IDirect3DDevice9:: UpdateTexture**](/windows/desktop/api) -Methode durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="667c6-106">The transportation of artwork in the blit operation is performed by the [**IDirect3DDevice9::UpdateTexture**](/windows/desktop/api) method.</span></span> <span data-ttu-id="667c6-107">Mithilfe der [**IDirect3DDevice9:: updatesurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) -Methode kann auch das Artwork in Direct3D 9 kopiert werden, das eine rechteckige Teilmenge von Pixeln kopiert.</span><span class="sxs-lookup"><span data-stu-id="667c6-107">Artwork can also be copied in Direct3D 9 by using the [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) method, which copies a rectangular subset of pixels.</span></span>

> [!Note]  
> <span data-ttu-id="667c6-108">Direct3D 9 stellt D3DX-Funktionen bereit, mit denen Sie Grafiken aus Dateien laden, Farb Konvertierungen anwenden und die Größe von Grafiken ändern können.</span><span class="sxs-lookup"><span data-stu-id="667c6-108">Direct3D 9 provides D3DX functions that enable you to load artwork from files, apply color conversion, and resize artwork.</span></span> <span data-ttu-id="667c6-109">Weitere Informationen zu den verfügbaren Funktionen finden Sie unter [Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).</span><span class="sxs-lookup"><span data-stu-id="667c6-109">For more information about the available functions see [Texture Functions in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="667c6-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="667c6-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="667c6-111">Direct3D-Oberflächen</span><span class="sxs-lookup"><span data-stu-id="667c6-111">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="667c6-112">**IDirect3DDevice9:: stretchrect**</span><span class="sxs-lookup"><span data-stu-id="667c6-112">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

<span data-ttu-id="667c6-113">**IDirect3DDevice9:: stretchrect**</span><span class="sxs-lookup"><span data-stu-id="667c6-113">**IDirect3DDevice9::StretchRect**</span></span>
</dt> </dl>

 

 
