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
# <a name="multiple-pass-rendering"></a>Multiple-Pass Rendering

Das Rendering mehrerer Pässe ist ein Prozess, bei dem eine Anwendung das Szene Diagramm mehrmals durchläuft, um eine Ausgabe zum Rendern der Anzeige zu erzeugen. Das Rendering mehrerer Pässe verbessert die Leistung, da es komplexe Szenen in Aufgaben unterteilt, die gleichzeitig ausgeführt werden können.

Um das Rendering mehrerer Pässe auszuführen, erstellen Sie für jeden zusätzlichen Durchlauf einen verzögerten Kontext und eine Befehlsliste. Während die Anwendung das Szenen Diagramm durchläuft, zeichnet Sie Befehle (z. b. das Rendern von Befehlen, z. b. [**Zeichnen**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) in einem verzögerten Kontext auf. Nachdem die Anwendung den Durchlauf abgeschlossen hat, ruft Sie die [**finishcommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) -Methode für den verzögerten Kontext auf. Schließlich ruft die Anwendung die [**executecommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) -Methode im unmittelbaren Kontext auf, um die Befehle in den einzelnen Befehlslisten auszuführen.

Der folgende Pseudo Code zeigt, wie das Rendering mehrerer Pässe durchgeführt wird:

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
> Der unmittelbare Kontext ändert eine Ressource, die an den unmittelbaren Kontext als renderzielansicht (RTV) gebunden ist. im Gegensatz dazu verwendet jeder verzögerte Kontext einfach die Ressource, die als Shader-Ressourcen Ansicht (SRV) an den verzögerten Kontext gebunden ist. Weitere Informationen zu sofortigen und verzögerten Kontexten finden Sie unter [sofortiges und verzögertes Rendering](overviews-direct3d-11-render-multi-thread-render.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Darstellung](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




