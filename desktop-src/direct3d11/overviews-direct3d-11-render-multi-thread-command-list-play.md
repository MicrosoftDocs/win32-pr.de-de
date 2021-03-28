---
title: Wiedergeben einer Befehlsliste
description: In diesem Thema wird gezeigt, wie eine Befehlsliste wiedergegeben wird.
ms.assetid: 4e6c0a98-85ff-45ca-963b-7d5c55f47195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d04df73b481adea17e1f985e2c1851039fd016a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992799"
---
# <a name="how-to-play-back-a-command-list"></a>Gewusst wie: Wiedergeben einer Befehlsliste

Eine [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md) ist eine aufgezeichnete Liste von renderingbefehlen. Verwenden Sie eine Befehlsliste, um Zeichnungs Befehle vorab aufzuzeichnen und Sie später wiederzugeben. In diesem Thema wird gezeigt, wie eine [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md)wiedergegeben wird. Eine Befehlsliste kann verwendet werden, um renderingtasks zwischen Threads aufzuteilen.

In diesem Abschnitt wird beschrieben, wie eine Befehlsliste wiedergegeben wird. Informationen zum Aufzeichnen einer Befehlsliste finden [Sie unter Gewusst wie: Aufzeichnen einer Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list-record.md).

**Wiedergeben einer Befehlsliste**

-   Aufrufen von [**Verknüpfung id3d11devicecontext aus:: executecommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) und übergeben eines gültigen [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) -Objekts.
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

[**Executecommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) muss im [unmittelbaren Kontext](overviews-direct3d-11-devices-intro.md) ausgeführt werden, damit aufgezeichnete Befehle auf der Grafikverarbeitungseinheit (Graphics Processing Unit, GPU) ausgeführt werden. Verwenden Sie den unmittelbaren Kontext zum Übertragen von Befehlen an die GPU zur Ausführung. verwenden Sie einen verzögerten Kontext zum Aufzeichnen von Befehlen für die Wiedergabe in einer anderen Befehlsliste. Wenn Sie **executecommandlist** in einem anderen verzögerten Kontext aufrufen, erstellen Sie eine verzögerte, verzögerte Befehlsliste. Wenn Sie die Befehle für die zusammengeführte verzögerte Befehlsliste ausführen möchten, müssen Sie diese im unmittelbaren Kontext ausführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




