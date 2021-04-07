---
description: Eine Oberfläche stellt einen linearen Bereich des Anzeige Speichers dar und befindet sich normalerweise im Anzeige Speicher der Anzeigekarte, obwohl die Oberfläche im Systemspeicher vorhanden sein kann. Oberflächen werden von der IDirect3DSurface9-Schnittstelle verwaltet.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Direct3D-Oberflächen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08729cc7252c39ddf71048991a796469f2e8b0b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745400"
---
# <a name="direct3d-surfaces-direct3d-9"></a><span data-ttu-id="b0e5e-104">Direct3D-Oberflächen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0e5e-104">Direct3D Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="b0e5e-105">Eine Oberfläche stellt einen linearen Bereich des Anzeige Speichers dar und befindet sich normalerweise im Anzeige Speicher der Anzeigekarte, obwohl die Oberfläche im Systemspeicher vorhanden sein kann.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-105">A surface represents a linear area of display memory and usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span> <span data-ttu-id="b0e5e-106">Oberflächen werden von der [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-106">Surfaces are managed by the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span>

-   <span data-ttu-id="b0e5e-107">Vorder-Puffer.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-107">Front Buffer.</span></span> <span data-ttu-id="b0e5e-108">Ein Rechteck des Arbeitsspeichers, der vom Grafikadapter übersetzt und auf dem Monitor angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-108">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span> <span data-ttu-id="b0e5e-109">In Direct3D schreibt eine Anwendung niemals direkt in den Vorder-Puffer.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-109">In Direct3D an application never writes directly to the front buffer.</span></span>
-   <span data-ttu-id="b0e5e-110">Hintergrund Puffer.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-110">Back Buffer.</span></span> <span data-ttu-id="b0e5e-111">Ein Rechteck des Arbeitsspeichers, in den eine Anwendung direkt schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-111">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="b0e5e-112">Der Hintergrund Puffer wird nie direkt auf dem Monitor angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-112">The back buffer is never directly displayed on the monitor.</span></span>
-   <span data-ttu-id="b0e5e-113">Flipping-Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-113">Flipping surfaces.</span></span> <span data-ttu-id="b0e5e-114">Der Prozess, bei dem der Hintergrund Puffer in den Vordergrund Puffer verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-114">The process of moving the back buffer to the front buffer.</span></span>
-   <span data-ttu-id="b0e5e-115">Austausch Kette.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-115">Swap chain.</span></span> <span data-ttu-id="b0e5e-116">Eine Auflistung von einem oder mehreren Back Puffern, die seriell dem Vorder-Puffer angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-116">A collection of one or more back buffers that can be serially presented to the front buffer.</span></span>

## <a name="getting-a-surface"></a><span data-ttu-id="b0e5e-117">Erhalten einer Oberfläche</span><span class="sxs-lookup"><span data-stu-id="b0e5e-117">Getting a Surface</span></span>

<span data-ttu-id="b0e5e-118">Erstellen Sie eine Oberfläche, indem Sie eine der folgenden Methoden aufrufen:</span><span class="sxs-lookup"><span data-stu-id="b0e5e-118">Create a surface by calling any of these methods:</span></span>

-   [<span data-ttu-id="b0e5e-119">**"Kreatedepthstencilsurface"**</span><span class="sxs-lookup"><span data-stu-id="b0e5e-119">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="b0e5e-120">**"Kreateoffscreenplainsurface"**</span><span class="sxs-lookup"><span data-stu-id="b0e5e-120">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [<span data-ttu-id="b0e5e-121">**"Kreaterendertarget"**</span><span class="sxs-lookup"><span data-stu-id="b0e5e-121">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

<span data-ttu-id="b0e5e-122">Oberflächen Formate legen fest, wie Daten für die einzelnen Pixel im Oberflächen Speicher interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-122">Surface formats determine how data for each pixel in surface memory is interpreted.</span></span> <span data-ttu-id="b0e5e-123">Direct3D verwendet das [D3DFORMAT](d3dformat.md) -Member der [**D3DSURFACE \_ DESC**](d3dsurface-desc.md) -Struktur, um das Oberflächen Format zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-123">Direct3D uses the [D3DFORMAT](d3dformat.md) member of the [**D3DSURFACE\_DESC**](d3dsurface-desc.md) structure to describe the surface format.</span></span> <span data-ttu-id="b0e5e-124">Sie können das Format einer vorhandenen Oberfläche abrufen, indem Sie die [**getdesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-124">You can retrieve the format of an existing surface by calling the [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) method.</span></span>

<span data-ttu-id="b0e5e-125">Nachdem eine Oberfläche erstellt wurde, können Sie einen Zeiger darauf abrufen, indem Sie eine der folgenden Methoden aufrufen:</span><span class="sxs-lookup"><span data-stu-id="b0e5e-125">Once a surface is created, you can get a pointer to it by calling any of these methods:</span></span>

-   [<span data-ttu-id="b0e5e-126">**Getcubemapsurface**</span><span class="sxs-lookup"><span data-stu-id="b0e5e-126">**GetCubeMapSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [<span data-ttu-id="b0e5e-127">**GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="b0e5e-127">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="b0e5e-128">**Getdepthstencilsurface**</span><span class="sxs-lookup"><span data-stu-id="b0e5e-128">**GetDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [<span data-ttu-id="b0e5e-129">**Getfrontbufferdata**</span><span class="sxs-lookup"><span data-stu-id="b0e5e-129">**GetFrontBufferData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [<span data-ttu-id="b0e5e-130">**GetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="b0e5e-130">**GetRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [<span data-ttu-id="b0e5e-131">**GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="b0e5e-131">**GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [<span data-ttu-id="b0e5e-132">**Getsurfakelevel**</span><span class="sxs-lookup"><span data-stu-id="b0e5e-132">**GetSurfaceLevel**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

<span data-ttu-id="b0e5e-133">Die [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle ermöglicht Ihnen den indirekten Zugriff auf den Arbeitsspeicher über die [**updatesurface**](/windows/desktop/api) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-133">The [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface enables you to indirectly access memory through the [**UpdateSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="b0e5e-134">Mit dieser Methode können Sie einen rechteckigen Bereich von Pixeln von einer **IDirect3DSurface9** -Schnittstelle in eine andere **IDirect3DSurface9** -Schnittstelle kopieren.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-134">This method allows you to copy a rectangular region of pixels from one **IDirect3DSurface9** interface to another **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="b0e5e-135">Die Oberflächen Schnittstelle verfügt auch über Methoden, um direkt auf den Anzeige Speicher zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-135">The surface interface also has methods to directly access display memory.</span></span> <span data-ttu-id="b0e5e-136">Beispielsweise können Sie die [**lockrect**](/windows/desktop/api) -Methode verwenden, um einen rechteckigen Bereich des Anzeige Speichers zu sperren.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-136">For example, you can use the [**LockRect**](/windows/desktop/api) method to lock a rectangular region of display memory.</span></span> <span data-ttu-id="b0e5e-137">Es ist wichtig, [**unlockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) aufzurufen, nachdem Sie die Arbeit mit dem gesperrten rechteckigen Bereich auf der-Oberfläche abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="b0e5e-137">It is important to call [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) after you are done working with the locked rectangular region on the surface.</span></span>

## <a name="additional-surface-topics"></a><span data-ttu-id="b0e5e-138">Zusätzliche Oberflächen Themen</span><span class="sxs-lookup"><span data-stu-id="b0e5e-138">Additional Surface Topics</span></span>

<span data-ttu-id="b0e5e-139">Weitere Informationen zur Verwendung von Oberflächen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b0e5e-139">Find out more about how to use surfaces with any of these topics:</span></span>

-   [<span data-ttu-id="b0e5e-140">Oberflächen Formate (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0e5e-140">Surface Formats (Direct3D 9)</span></span>](surface-formats.md)
-   [<span data-ttu-id="b0e5e-141">Was ist eine austauschkette? (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0e5e-141">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
-   [<span data-ttu-id="b0e5e-142">Breite und Tonhöhe (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0e5e-142">Width vs. Pitch (Direct3D 9)</span></span>](width-vs--pitch.md)
-   [<span data-ttu-id="b0e5e-143">Flipping-Oberflächen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0e5e-143">Flipping Surfaces (Direct3D 9)</span></span>](flipping-surfaces.md)
-   [<span data-ttu-id="b0e5e-144">Seiten kippen und zurück Pufferung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0e5e-144">Page Flipping and Back Buffering (Direct3D 9)</span></span>](page-flipping-and-back-buffering.md)
-   [<span data-ttu-id="b0e5e-145">Kopieren auf Oberflächen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0e5e-145">Copying to Surfaces (Direct3D 9)</span></span>](copying-to-surfaces.md)
-   [<span data-ttu-id="b0e5e-146">Kopieren von Oberflächen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0e5e-146">Copying Surfaces (Direct3D 9)</span></span>](copying-surfaces.md)
-   [<span data-ttu-id="b0e5e-147">Direktes Zugreifen auf den Surface-Speicher (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0e5e-147">Accessing Surface Memory Directly (Direct3D 9)</span></span>](accessing-surface-memory-directly.md)
-   [<span data-ttu-id="b0e5e-148">Private Oberflächendaten (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0e5e-148">Private Surface Data (Direct3D 9)</span></span>](private-surface-data.md)
-   [<span data-ttu-id="b0e5e-149">Gamma Steuerelemente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0e5e-149">Gamma Controls (Direct3D 9)</span></span>](gamma-controls.md)

## <a name="related-topics"></a><span data-ttu-id="b0e5e-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0e5e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0e5e-151">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="b0e5e-151">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
