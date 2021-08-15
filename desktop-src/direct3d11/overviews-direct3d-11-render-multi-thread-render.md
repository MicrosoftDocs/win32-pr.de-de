---
title: Sofortiges und verzögertes Rendering
description: Direct3D 11 unterstützt zwei Arten von sofortigem und verzögerten Rendering. Beide werden mithilfe der ID3D11DeviceContext-Schnittstelle implementiert.
ms.assetid: 8991be9f-c882-4752-9048-704fe4ae1725
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740a957ec4b7f2edacb4b753c7f68230494b10cf33721ef6c2d869de334517b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912932"
---
# <a name="immediate-and-deferred-rendering"></a>Sofortiges und verzögertes Rendering

Direct3D 11 unterstützt zwei Arten von Rendering: direkt und verzögert. Beide werden mithilfe der [**ID3D11DeviceContext-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) implementiert.

## <a name="immediate-rendering"></a>Sofortiges Rendering

Sofortiges Rendering bezieht sich auf das Aufrufen von Rendering-APIs oder -Befehlen von einem Gerät, das die Befehle in einem Puffer zur Ausführung auf der GPU in die Warteschlange einreiht. Verwenden Sie einen unmittelbaren Kontext zum Rendern, Festlegen des Pipelinezustands und Wiedergeben einer Befehlsliste.

Erstellen Sie mithilfe von [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)einen unmittelbaren Kontext.

## <a name="deferred-rendering"></a>Verzögertes Rendering

Beim verzögerten Rendering werden Grafikbefehle in einem Befehlspuffer aufgezeichnet, sodass sie zu einem anderen Zeitpunkt wiedergegeben werden können. Verwenden Sie einen verzögerten Kontext, um Befehle (Rendering und Zustandseinstellung) in einer Befehlsliste aufzuzeichnen. Verzögertes Rendering ist ein neues Konzept in Direct3D 11. Das verzögerte Rendering ist so konzipiert, dass das Rendering in einem Thread unterstützt wird, während Befehle zum Rendern in zusätzlichen Threads aufgezeichnet werden. Mit dieser parallelen Multithreadstrategie können Sie komplexe Szenen in gleichzeitige Aufgaben aufgliedern. Weitere Informationen zum Rendern komplexer Szenen finden Sie unter [Multiple-Pass Rendering](overviews-direct3d-11-render-multipass.md).

Erstellen Sie mit [**id3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext)einen verzögerten Kontext.

Direct3D generiert Renderingaufwand, wenn Befehle im Befehlspuffer in die Warteschlange eingereiht werden. Im Gegensatz dazu wird eine [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md) während der Wiedergabe viel effizienter ausgeführt. Um eine Befehlsliste zu verwenden, zeichnen Sie Renderingbefehle mit einem verzögerten Kontext auf und wiedergeben sie mithilfe eines unmittelbaren Kontexts.

Sie können nur eine einzelne Befehlsliste auf Singlethread-Weise generieren. Sie können jedoch mehrere verzögerte Kontexte gleichzeitig erstellen und verwenden, jeweils in einem separaten Thread. Anschließend können Sie diese mehreren verzögerten Kontexte verwenden, um gleichzeitig mehrere Befehlslisten zu erstellen.

Sie können nicht zwei oder mehr Befehlslisten gleichzeitig im unmittelbaren Kontext wiedergeben.

Rufen Sie [**ID3D11DeviceContext::GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gettype)auf, um zu bestimmen, ob es sich bei einem Gerätekontext um einen unmittelbaren oder verzögerten Kontext handelt.

Die [**ID3D11DeviceContext::Map-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) wird nur in einem verzögerten Kontext für dynamische Ressourcen ([**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) unterstützt, wobei der erste Aufruf in der Befehlsliste [**D3D11 \_ MAP WRITE \_ \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)ist. **D3D11 \_ MAP \_ WRITE \_ NO \_ OVERWRITE** wird bei nachfolgenden Aufrufen unterstützt, sofern für den angegebenen Ressourcentyp verfügbar.

Abfragen in einem verzögerten Kontext sind auf die Datengenerierung und prädikatierte Zeichnung beschränkt. Sie können [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) nicht für einen verzögerten Kontext aufrufen, um Daten zu einer Abfrage abzurufen. Sie können **GetData** nur im unmittelbaren Kontext aufrufen, um Daten zu einer Abfrage abzurufen. Sie können ein Renderingprädikat (einen Abfragetyp) festlegen, indem Sie [**D3D11DeviceContext::SetPredication**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-setpredication) aufrufen, um Abfrageergebnisse auf der GPU zu verwenden. Sie können Abfragedaten durch Aufrufe von [**ID3D11DeviceContext::Begin**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-begin) und [**ID3D11DeviceContext::End**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-end)generieren. Die Abfragedaten sind jedoch erst verfügbar, wenn Sie [**ID3D11DeviceContext::ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) im unmittelbaren Kontext aufrufen, um die Befehlsliste des verzögerten Kontexts zu übermitteln. Die Abfragedaten werden dann von der GPU verarbeitet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




