---
title: Aufzeichnen einer Befehlsliste
description: In diesem Thema wird gezeigt, wie eine Befehlsliste erstellt und aufgezeichnet wird.
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712f48386e0625c58a1f11c122d105064477ca8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711544"
---
# <a name="how-to-record-a-command-list"></a>Gewusst wie: Aufzeichnen einer Befehlsliste

Eine [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md) ist eine aufgezeichnete Liste von renderingbefehlen. In diesem Thema wird gezeigt, wie eine [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md)erstellt und aufgezeichnet wird. Verwenden Sie eine Befehlsliste, um Rendering-Befehle aufzuzeichnen und Sie später wiederzugeben. Eine Befehlsliste ist praktisch für das Aufteilen von renderingtasks zwischen Threads.

**So zeichnen Sie eine Befehlsliste auf**

1.  Eine Befehlsliste muss aus einem verzögerten Kontext erstellt werden, der Geräte Zustands-und renderingaktionen enthält. Wenn Sie ein Gerät haben, erstellen Sie einen verzögerten Kontext durch Aufrufen von [**ID3D11Device:: createdeferredcontext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  Verwenden Sie den verzögerten Kontext zum Rendering.

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    In diesem einfachen Beispiel wird ein Renderziel gelöscht, aber Sie können zusätzliche renderbefehle hinzufügen.

3.  Erstellen Sie eine Befehlsliste, und zeichnen Sie Sie auf, indem Sie [**Verknüpfung id3d11devicecontext aus:: finishcommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) aufrufen und einen Zeiger auf eine nicht initialisierte [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) -Schnittstelle übergeben.

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    Wenn die-Methode zurückgibt, wird eine Befehlsliste erstellt, die alle Rendering-Befehle enthält, und eine Schnittstelle wird an die Anwendung zurückgegeben.

    Der boolesche Parameter teilt der Laufzeit mit, was mit dem Pipeline Zustand im verzögerten Kontext zu tun ist. " **True** " bedeutet, dass der Zustand des Geräte Kontexts in der vorbefehls Listen Bedingung wieder hergestellt wird, wenn die Aufzeichnung abgeschlossen ist. " **false** " bedeutet, dass der Status nach der Aufzeichnung nicht geändert Dies bedeutet, dass der Gerätekontext die in der Befehlsliste enthaltenen Zustandsänderungen widerspiegelt.

Ein Beispiel für die Wiedergabe einer Befehlsliste finden Sie unter Gewusst [wie: Wiedergeben einer Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list-play.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




