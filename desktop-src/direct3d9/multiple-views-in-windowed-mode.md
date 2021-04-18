---
description: Neben der Swapkette, die im Besitz des Direct3DDevice-Objekts ist, kann eine Anwendung die IDirect3DDevice9::-Methode verwenden, um zusätzliche Austausch Ketten zu erstellen, um mehrere Ansichten desselben Geräts darzustellen.
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Mehrere Ansichten im Fenstermodus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed750472d1816c0365298630cfb426982743b11a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338859"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a><span data-ttu-id="caea5-103">Mehrere Ansichten im Fenstermodus (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="caea5-103">Multiple Views in Windowed Mode (Direct3D 9)</span></span>

<span data-ttu-id="caea5-104">Neben der Swapkette, die im Besitz des Direct3DDevice-Objekts ist, kann eine Anwendung die [**IDirect3DDevice9::**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) -Methode verwenden, um zusätzliche Austausch Ketten zu erstellen, um mehrere Ansichten desselben Geräts darzustellen.</span><span class="sxs-lookup"><span data-stu-id="caea5-104">In addition to the swap chain that is owned and manipulated through the Direct3DDevice object, an application can use the [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) method to create additional swap chains to present multiple views from the same device.</span></span>

<span data-ttu-id="caea5-105">In der Regel erstellt die Anwendung eine austauschkette pro Ansicht und ordnet jede Austausch Kette einer bestimmten Ansicht zu.</span><span class="sxs-lookup"><span data-stu-id="caea5-105">Typically, the application creates one swap chain per view, and it associates each swap chain with a particular view.</span></span> <span data-ttu-id="caea5-106">Die Anwendung rendert Bilder in den backpuffern jeder SwapChain und verwendet dann die [**IDirect3DDevice9::P Resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) -Methode, um Sie einzeln darzustellen.</span><span class="sxs-lookup"><span data-stu-id="caea5-106">The application renders images in the back buffers of each swap chain, and then uses the [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method to present them individually.</span></span> <span data-ttu-id="caea5-107">Beachten Sie, dass auf jedem Adapter jeweils nur eine SwapChain auf dem Bildschirm angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="caea5-107">Note that only one swap chain at a time can be full-screen on each adapter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="caea5-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="caea5-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caea5-109">Präsentieren einer Szene</span><span class="sxs-lookup"><span data-stu-id="caea5-109">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 
