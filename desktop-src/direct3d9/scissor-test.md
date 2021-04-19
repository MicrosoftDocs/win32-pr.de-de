---
description: Der Scheren-Test das Culling-Pixel, die sich außerhalb des Scheren Rechtecks befinden, ein benutzerdefinierter rechteckiger unter Abschnitt des Renderziels.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Scissor-Test (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c4298182ab2bb6302c19111e2970d23cef311d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338884"
---
# <a name="scissor-test-direct3d-9"></a><span data-ttu-id="05326-103">Scissor-Test (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="05326-103">Scissor Test (Direct3D 9)</span></span>

<span data-ttu-id="05326-104">Der Scheren-Test das Culling-Pixel, die sich außerhalb des Scheren Rechtecks befinden, ein benutzerdefinierter rechteckiger unter Abschnitt des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="05326-104">The scissor test culls pixels that are outside of the scissor rectangle, a user-defined rectangular sub-section of the render target.</span></span>

<span data-ttu-id="05326-105">Das Scheren-Rechteck kann verwendet werden, um den Bereich des Renderziels anzugeben, in dem die Spiel Welt gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="05326-105">The scissor rectangle could be used to indicate the area of the render target where the game world is drawn.</span></span> <span data-ttu-id="05326-106">Der Bereich außerhalb des Rechtecks ist ein herausgefiltert werden und kann für die GUI eines Spiels verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05326-106">The area outside the rectangle is culled and could be devoted to a game's GUI.</span></span> <span data-ttu-id="05326-107">Der Scheren-Test kann nicht rechteckige Bereiche umkreisen.</span><span class="sxs-lookup"><span data-stu-id="05326-107">The scissor test cannot cull non-rectangular areas.</span></span>

<span data-ttu-id="05326-108">Scissor-Rechtecke können nicht größer als das Renderziel festgelegt werden, Sie können jedoch größer als der Viewport festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="05326-108">Scissor rectangles cannot be set larger than the render target, but they can be set larger than the viewport.</span></span>

<span data-ttu-id="05326-109">Das Scheren Rechteck wird von einem Geräte-Rendering-Zustand verwaltet.</span><span class="sxs-lookup"><span data-stu-id="05326-109">The scissor rectangle is managed by a device render state.</span></span> <span data-ttu-id="05326-110">Ein Scheren Test wird aktiviert oder deaktiviert, indem renderstate auf " **true** " oder " **false**" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="05326-110">A scissor test is enabled or disabled by setting the renderstate to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="05326-111">Dieser Test wird nach dem Berechnen der fragmentfarbe, aber vor dem Alpha Test ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05326-111">This test is performed after the fragment color is computed but before alpha testing.</span></span> <span data-ttu-id="05326-112">[**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) setzt das Scheren Rechteck auf das vollständige Renderziel zurück, analog zum Zurücksetzen des Viewports.</span><span class="sxs-lookup"><span data-stu-id="05326-112">[**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) resets the scissor rectangle to the full render target, analogous to the viewport reset.</span></span> <span data-ttu-id="05326-113">[**IDirect3DDevice9:: czcissorrect**](/windows/desktop/api) wird von stateblocks aufgezeichnet, und [**IDirect3DDevice9:: kreatestateblock**](/windows/desktop/api) mit der Einstellung All State (D3DSBT \_ all Value in [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)).</span><span class="sxs-lookup"><span data-stu-id="05326-113">[**IDirect3DDevice9::SetScissorRect**](/windows/desktop/api) is recorded by stateblocks, and [**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) with the all state setting (D3DSBT\_ALL value in [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)).</span></span> <span data-ttu-id="05326-114">Der Scheren-Test wirkt sich auch auf den Device [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) -Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="05326-114">The scissor test also affects the device [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) operation.</span></span>


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



<span data-ttu-id="05326-115">Das standardmäßige Scheren-Rechteck ist der vollständige Viewport.</span><span class="sxs-lookup"><span data-stu-id="05326-115">The default scissor rectangle is the full viewport.</span></span>

<span data-ttu-id="05326-116">Das Testen von Scissor erfolgt erst, nachdem die Pixel Verarbeitung von einem Pixelshader oder der Fixed-Funktions Pipeline abgeschlossen wurde. Dies ist im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="05326-116">Scissor testing is done just after pixel processing is completed by a pixel shader or the fixed function pipeline, as shown in the following diagram.</span></span>

![Diagramm der Ausführung von Scheren Tests in Bezug auf andere Schritte](images/scissor-test.png)

## <a name="related-topics"></a><span data-ttu-id="05326-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="05326-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05326-119">Pixel Pipeline</span><span class="sxs-lookup"><span data-stu-id="05326-119">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
