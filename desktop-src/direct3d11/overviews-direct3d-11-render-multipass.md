---
title: Multiple-Pass Rendering
description: Das Mehrfachdurchlaufrendering ist ein Prozess, bei dem eine Anwendung ihren Szenengraphen mehrmals durchläuft, um eine Ausgabe zum Rendern auf der Anzeige zu erzeugen.
ms.assetid: 9a11686a-fd99-4d40-8b02-6f8ec18346e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242573dea2982f3525082187aad536a407e446c4ce59f116f53b8fa0d40fc582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124208"
---
# <a name="multiple-pass-rendering"></a>Multiple-Pass Rendering

Das Mehrfachdurchlaufrendering ist ein Prozess, bei dem eine Anwendung ihren Szenengraphen mehrmals durchläuft, um eine Ausgabe zum Rendern auf der Anzeige zu erzeugen. Das Rendering mit mehreren Durchläufen verbessert die Leistung, da komplexe Szenen in Aufgaben unterteilt werden, die gleichzeitig ausgeführt werden können.

Um das Rendering mit mehreren Durchlauf durchzuführen, erstellen Sie einen verzögerten Kontext und eine Befehlsliste für jeden zusätzlichen Durchlauf. Während die Anwendung das Szenendiagramm durchläuft, zeichnet sie Befehle (z. B. Renderingbefehle wie [**Zeichnen)**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)in einen verzögerten Kontext auf. Nachdem die Anwendung den Durchlauf abgeschlossen hat, ruft sie die [**FinishCommandList-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) für den verzögerten Kontext auf. Schließlich ruft die Anwendung die [**ExecuteCommandList-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) im unmittelbaren Kontext auf, um die Befehle in jeder Befehlsliste auszuführen.

Der folgende Pseudocode zeigt, wie Das Rendering mit mehreren Kennungen ausgeführt wird:

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
> Der direkte Kontext ändert eine Ressource, die als Renderzielansicht (RTV) an den unmittelbaren Kontext gebunden ist. Im Gegensatz dazu verwendet jeder verzögerte Kontext einfach die Ressource, die an den verzögerten Kontext als Shaderressourcenansicht (SRV) gebunden ist. Weitere Informationen zu unmittelbaren und verzögerten Kontexten finden Sie unter [Sofortiges und verzögertes Rendering.](overviews-direct3d-11-render-multi-thread-render.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendering](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




