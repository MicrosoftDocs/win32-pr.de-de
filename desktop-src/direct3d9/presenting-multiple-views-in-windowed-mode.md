---
description: Zusätzlich zu der Swapkette, die über die IDirect3DDevice9-Schnittstelle gehört und manipuliert wird, kann eine Anwendung zusätzliche Austausch Ketten erstellen, um mehrere Ansichten desselben Geräts darzustellen.
ms.assetid: 4fc09b9c-7adb-4f5d-80e0-2d39bc10420e
title: Darstellung mehrerer Ansichten im Fenstermodus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 039b02c487e06c7464dc8163c719371dc2b23706
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522768"
---
# <a name="presenting-multiple-views-in-windowed-mode-direct3d-9"></a><span data-ttu-id="6eee8-103">Darstellung mehrerer Ansichten im Fenstermodus (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6eee8-103">Presenting Multiple Views in Windowed Mode (Direct3D 9)</span></span>

<span data-ttu-id="6eee8-104">Zusätzlich zu der Swapkette, die über die [**IDirect3DDevice9**](/windows/desktop/api) -Schnittstelle gehört und manipuliert wird, kann eine Anwendung zusätzliche Austausch Ketten erstellen, um mehrere Ansichten desselben Geräts darzustellen.</span><span class="sxs-lookup"><span data-stu-id="6eee8-104">In addition to the swap chain that is owned and manipulated through the [**IDirect3DDevice9**](/windows/desktop/api) interface, an application can create additional swap chains in order to present multiple views from the same device.</span></span> <span data-ttu-id="6eee8-105">Die Anwendung erstellt in der Regel eine Austausch Kette pro Ansicht mithilfe der [**IDirect3DDevice9:: forateadditionalswapchain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) -Methode und ordnet jede Swapkette einem bestimmten Fenster zu.</span><span class="sxs-lookup"><span data-stu-id="6eee8-105">The application typically creates one swap chain per view by using the [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) method, and associates each swap chain with a particular window.</span></span> <span data-ttu-id="6eee8-106">Die Anwendung rendert Bilder in den backpuffern jeder SwapChain und zeigt Sie dann einzeln an.</span><span class="sxs-lookup"><span data-stu-id="6eee8-106">The application renders images into the back buffers of each swap chain, and then presents them individually.</span></span>

<span data-ttu-id="6eee8-107">Jeweils nur eine SwapChain kann auf jedem Adapter voll Bildschirm sein.</span><span class="sxs-lookup"><span data-stu-id="6eee8-107">Only one swap chain at a time can be full-screen on each adapter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6eee8-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6eee8-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6eee8-109">Programmiertipps</span><span class="sxs-lookup"><span data-stu-id="6eee8-109">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
