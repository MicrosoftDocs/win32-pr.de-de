---
title: Multiple-Pass Rendering
description: Das Rendering mehrerer Pässe ist ein Prozess, bei dem eine Anwendung das Szene Diagramm mehrmals durchläuft, um eine Ausgabe zum Rendern der Anzeige zu erzeugen.
ms.assetid: 9a11686a-fd99-4d40-8b02-6f8ec18346e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fcf7f3f04bd641fdf82c9cf317e8a2ec99e85c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310443"
---
# <a name="multiple-pass-rendering"></a><span data-ttu-id="39c81-103">Multiple-Pass Rendering</span><span class="sxs-lookup"><span data-stu-id="39c81-103">Multiple-Pass Rendering</span></span>

<span data-ttu-id="39c81-104">Das Rendering mehrerer Pässe ist ein Prozess, bei dem eine Anwendung das Szene Diagramm mehrmals durchläuft, um eine Ausgabe zum Rendern der Anzeige zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="39c81-104">Multiple-pass rendering is a process in which an application traverses its scene graph multiple times in order to produce an output to render to the display.</span></span> <span data-ttu-id="39c81-105">Das Rendering mehrerer Pässe verbessert die Leistung, da es komplexe Szenen in Aufgaben unterteilt, die gleichzeitig ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="39c81-105">Multiple-pass rendering improves performance because it breaks up complex scenes into tasks that can run concurrently.</span></span>

<span data-ttu-id="39c81-106">Um das Rendering mehrerer Pässe auszuführen, erstellen Sie für jeden zusätzlichen Durchlauf einen verzögerten Kontext und eine Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="39c81-106">To perform multiple-pass rendering, you create a deferred context and command list for each additional pass.</span></span> <span data-ttu-id="39c81-107">Während die Anwendung das Szenen Diagramm durchläuft, zeichnet Sie Befehle (z. b. das Rendern von Befehlen, z. b. [**Zeichnen**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) in einem verzögerten Kontext auf.</span><span class="sxs-lookup"><span data-stu-id="39c81-107">While the application traverses the scene graph, it records commands (for example, rendering commands such as [**Draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) into a deferred context.</span></span> <span data-ttu-id="39c81-108">Nachdem die Anwendung den Durchlauf abgeschlossen hat, ruft Sie die [**finishcommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) -Methode für den verzögerten Kontext auf.</span><span class="sxs-lookup"><span data-stu-id="39c81-108">After the application finishes the traversal, it calls the [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) method on the deferred context.</span></span> <span data-ttu-id="39c81-109">Schließlich ruft die Anwendung die [**executecommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) -Methode im unmittelbaren Kontext auf, um die Befehle in den einzelnen Befehlslisten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="39c81-109">Finally, the application calls the [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) method on the immediate context to execute the commands in each command list.</span></span>

<span data-ttu-id="39c81-110">Der folgende Pseudo Code zeigt, wie das Rendering mehrerer Pässe durchgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="39c81-110">The following pseudocode shows how to perform multiple-pass rendering:</span></span>

``` syntax
{
 ImmCtx->SetRenderTarget( pRTViewOfResourceX );
 DefCtx1->SetTexture( pSRView1OfResourceX );
 DefCtx2->SetTexture( pSRView2OfResourceX );

 for () // Traverse the scene graph.
  {
    ImmCtx->Draw(); // Pass 0: immediate context renders primitives into resource X.

    // The following texturing by the deferred contexts occurs after the 
    // immediate context makes calls to ExecuteCommandList. 
    // Resource X is then comletely updated by the immediate context. 
    DefCtx1->Draw(); // Pass 1: deferred context 1 performs texturing from resource X.
    DefCtx2->Draw(); // Pass 2: deferred context 2 performs texturing from resource X.
      }

  // Create command lists and record commands into them.
  DefCtx1->FinishCommandList( &pCL1 ); 
  DefCtx2->FinishCommandList( &pCL2 );

  ImmCtx->ExecuteCommandList( pCL1 ); // Execute pass 1.
  ImmCtx->ExecuteCommandList( pCL2 ); // Exeucte pass 2.
}
```

> [!Note]  
> <span data-ttu-id="39c81-111">Der unmittelbare Kontext ändert eine Ressource, die an den unmittelbaren Kontext als renderzielansicht (RTV) gebunden ist. im Gegensatz dazu verwendet jeder verzögerte Kontext einfach die Ressource, die als Shader-Ressourcen Ansicht (SRV) an den verzögerten Kontext gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="39c81-111">The immediate context modifies a resource, which is bound to the immediate context as a render target view (RTV); in contrast, each deferred context simply uses the resource, which is bound to the deferred context as a shader resource view (SRV).</span></span> <span data-ttu-id="39c81-112">Weitere Informationen zu sofortigen und verzögerten Kontexten finden Sie unter [sofortiges und verzögertes Rendering](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="39c81-112">For more information about immediate and deferred contexts, see [Immediate and Deferred Rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="39c81-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39c81-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39c81-114">Darstellung</span><span class="sxs-lookup"><span data-stu-id="39c81-114">Rendering</span></span>](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




