---
title: Anwenden einer Technik (Direct3D 11)
description: Wenn die Konstanten, Texturen und der Shader-Zustand deklariert und initialisiert sind, besteht die einzige Aufgabe darin, den Effekt Zustand im Gerät festzulegen.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e67668b27c1f0271974f20edc62619a7b1ae8ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037051"
---
# <a name="apply-a-technique-direct3d-11"></a><span data-ttu-id="d9b19-103">Anwenden einer Technik (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="d9b19-103">Apply a Technique (Direct3D 11)</span></span>

<span data-ttu-id="d9b19-104">Wenn die Konstanten, Texturen und der Shader-Zustand deklariert und initialisiert sind, besteht die einzige Aufgabe darin, den Effekt Zustand im Gerät festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d9b19-104">With the constants, textures, and shader state declared and initialized, the only thing left to do is to set the effect state in the device.</span></span>

## <a name="set-non-shader-state-in-the-device"></a><span data-ttu-id="d9b19-105">Festlegen des Zustands eines nicht-Shader im Gerät</span><span class="sxs-lookup"><span data-stu-id="d9b19-105">Set Non-Shader State in the Device</span></span>

<span data-ttu-id="d9b19-106">Der Pipeline Zustand wird nicht durch einen Effekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9b19-106">Some pipeline state is not set by an effect.</span></span> <span data-ttu-id="d9b19-107">Beispielsweise bereitet das Löschen eines Renderziels das Renderziel für Daten vor.</span><span class="sxs-lookup"><span data-stu-id="d9b19-107">For example clearing a render target prepares the render target for data.</span></span> <span data-ttu-id="d9b19-108">Im folgenden finden Sie ein Beispiel für das Löschen von Ausgabe Puffern, bevor Sie den Effekt Zustand im Gerät festlegen.</span><span class="sxs-lookup"><span data-stu-id="d9b19-108">Before setting the effect state in the device, here is an example of clearing output buffers.</span></span>


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a><span data-ttu-id="d9b19-109">Festlegen des Wirkungs Zustands im Gerät</span><span class="sxs-lookup"><span data-stu-id="d9b19-109">Set Effect State in the Device</span></span>

<span data-ttu-id="d9b19-110">Der Effekt Zustand wird durch Anwenden des Effekt Zustands innerhalb der Renderschleife festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9b19-110">Setting effect state is done by applying the effect state within the render loop.</span></span> <span data-ttu-id="d9b19-111">Dies erfolgt von außerhalb von in.</span><span class="sxs-lookup"><span data-stu-id="d9b19-111">This is done from the outside in.</span></span> <span data-ttu-id="d9b19-112">Das heißt, wählen Sie eine Technik aus, und legen Sie dann den Status für jeden der Durchläufen fest (je nach gewünschtem Ergebnis).</span><span class="sxs-lookup"><span data-stu-id="d9b19-112">That is, select a technique, and then set the state for each of the passes (depending on your desired result).</span></span>


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



<span data-ttu-id="d9b19-113">Ein Effekt führt nichts aus, sondern legt einfach den Effekt auf das Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="d9b19-113">An effect doesn't render anything, it simply sets effect state to the device.</span></span> <span data-ttu-id="d9b19-114">Der Renderingcode wird aufgerufen, nachdem der Status des Effekts den Gerätezustand aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="d9b19-114">The rendering code is called after the effect state updates device state.</span></span> <span data-ttu-id="d9b19-115">In diesem Beispiel führt der drawinentxed-Befehl das Rendering aus.</span><span class="sxs-lookup"><span data-stu-id="d9b19-115">In this example, the DrawIndexed call performs the rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9b19-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d9b19-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9b19-117">Rendern eines Effekts (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="d9b19-117">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




