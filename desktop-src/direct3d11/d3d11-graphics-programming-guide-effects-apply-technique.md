---
title: Anwenden einer Technik (Direct3D 11)
description: Erfahren Sie, wie Sie den Effektzustand auf dem Gerät für Direct3D 11 festlegen, nachdem die Konstanten, Texturen und Shaderstatus deklariert und initialisiert wurden.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136d03f92957eaf1b3d501c0acd54aafde7e16d8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118945"
---
# <a name="apply-a-technique-direct3d-11"></a><span data-ttu-id="9df85-103">Anwenden einer Technik (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="9df85-103">Apply a Technique (Direct3D 11)</span></span>

<span data-ttu-id="9df85-104">Wenn die Konstanten, Texturen und der Shaderzustand deklariert und initialisiert sind, müssen Sie nur noch den Effektzustand auf dem Gerät festlegen.</span><span class="sxs-lookup"><span data-stu-id="9df85-104">With the constants, textures, and shader state declared and initialized, the only thing left to do is to set the effect state in the device.</span></span>

## <a name="set-non-shader-state-in-the-device"></a><span data-ttu-id="9df85-105">Festlegen des Zustands ohne Shader auf dem Gerät</span><span class="sxs-lookup"><span data-stu-id="9df85-105">Set Non-Shader State in the Device</span></span>

<span data-ttu-id="9df85-106">Ein Pipelinezustand wird nicht durch einen Effekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9df85-106">Some pipeline state is not set by an effect.</span></span> <span data-ttu-id="9df85-107">Wenn Sie beispielsweise ein Renderziel löschen, wird das Renderziel auf Daten vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="9df85-107">For example clearing a render target prepares the render target for data.</span></span> <span data-ttu-id="9df85-108">Vor dem Festlegen des Effektzustands auf dem Gerät finden Sie hier ein Beispiel für das Löschen von Ausgabepuffern.</span><span class="sxs-lookup"><span data-stu-id="9df85-108">Before setting the effect state in the device, here is an example of clearing output buffers.</span></span>


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a><span data-ttu-id="9df85-109">Festlegen des Effektzustands auf dem Gerät</span><span class="sxs-lookup"><span data-stu-id="9df85-109">Set Effect State in the Device</span></span>

<span data-ttu-id="9df85-110">Das Festlegen des Effektzustands erfolgt durch Anwenden des Effektzustands innerhalb der Renderschleife.</span><span class="sxs-lookup"><span data-stu-id="9df85-110">Setting effect state is done by applying the effect state within the render loop.</span></span> <span data-ttu-id="9df85-111">Dies erfolgt von außen in .</span><span class="sxs-lookup"><span data-stu-id="9df85-111">This is done from the outside in.</span></span> <span data-ttu-id="9df85-112">Das heißt, wählen Sie eine Technik aus, und legen Sie dann den Zustand für jeden der Durchläufe fest (je nach gewünschtem Ergebnis).</span><span class="sxs-lookup"><span data-stu-id="9df85-112">That is, select a technique, and then set the state for each of the passes (depending on your desired result).</span></span>


```
    D3D11_TECHNIQUE_DESC techDesc;
    pRenderTechnique->GetDesc( &techDesc );
    for( UINT p = 0; p < techDesc.Passes; ++p )
    {
        }
            ....
            pRenderTechnique->GetPassByIndex( p )->Apply(0);
            pd3dDevice->DrawIndexed( (UINT)pSubset->IndexCount, 0,  
                 (UINT)pSubset->VertexStart );
        }
    }
```



<span data-ttu-id="9df85-113">Ein Effekt rendert nichts, sondern legt einfach den Effektzustand auf das Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="9df85-113">An effect doesn't render anything, it simply sets effect state to the device.</span></span> <span data-ttu-id="9df85-114">Der Renderingcode wird aufgerufen, nachdem der Auswirkungsstatus den Gerätezustand aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="9df85-114">The rendering code is called after the effect state updates device state.</span></span> <span data-ttu-id="9df85-115">In diesem Beispiel führt der DrawIndexed-Aufruf das Rendering aus.</span><span class="sxs-lookup"><span data-stu-id="9df85-115">In this example, the DrawIndexed call performs the rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9df85-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9df85-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9df85-117">Rendern eines Effekts (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="9df85-117">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




