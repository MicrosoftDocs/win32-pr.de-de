---
description: Wenn tiefen Tests auf einer Renderingoberfläche durchgeführt werden, aktualisiert das Direct3D-System standardmäßig die Renderziel-Oberfläche, wenn der entsprechende tiefen Wert (z oder w) für jeden Punkt kleiner ist als der Wert im tiefen Puffer.
ms.assetid: e9243c05-e943-4a42-ab73-e684900fc81d
title: Ändern von tiefen Puffer Vergleichsfunktionen (d3d9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7589ea0035376c6e73bcb70a73fcca3b913c9ecc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749064"
---
# <a name="changing-depth-buffer-comparison-functions-d3d9"></a><span data-ttu-id="db5d8-103">Ändern von tiefen Puffer Vergleichsfunktionen (d3d9)</span><span class="sxs-lookup"><span data-stu-id="db5d8-103">Changing Depth Buffer Comparison Functions (D3D9)</span></span>

<span data-ttu-id="db5d8-104">Wenn tiefen Tests auf einer Renderingoberfläche durchgeführt werden, aktualisiert das Direct3D-System standardmäßig die Renderziel-Oberfläche, wenn der entsprechende tiefen Wert (z oder w) für jeden Punkt kleiner ist als der Wert im tiefen Puffer.</span><span class="sxs-lookup"><span data-stu-id="db5d8-104">By default, when depth-testing is performed on a rendering surface, the Direct3D system updates the render-target surface if the corresponding depth value (z or w) for each point is less than the value in the depth buffer.</span></span> <span data-ttu-id="db5d8-105">In einer C++-Anwendung ändern Sie, wie das Systemvergleiche für tiefen Werte durchführt, indem Sie die [**IDirect3DDevice9:: setrenderstate**](/windows/desktop/api) -Methode aufrufen, wobei der *State* -Parameter auf D3DRS \_ zfunc festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="db5d8-105">In a C++ application, you change how the system performs comparisons on depth values by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method with the *State* parameter set to D3DRS\_ZFUNC.</span></span> <span data-ttu-id="db5d8-106">Der *value* -Parameter muss auf einen Wert im [**D3DCMPFUNC**](./d3dcmpfunc.md) -enumerierten Typ festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="db5d8-106">The *Value* parameter should be set to a value in the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db5d8-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db5d8-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db5d8-108">Tiefen Puffer</span><span class="sxs-lookup"><span data-stu-id="db5d8-108">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
