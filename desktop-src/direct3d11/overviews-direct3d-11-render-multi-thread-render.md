---
title: Sofortiges und verzögertes Rendering
description: Direct3D 11 unterstützt zwei renderingtypen direkt und verzögert. Beide werden mithilfe der Verknüpfung id3d11devicecontext aus-Schnittstelle implementiert.
ms.assetid: 8991be9f-c882-4752-9048-704fe4ae1725
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef954a8e794755e1405c8e1e07505a5f39189b03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992822"
---
# <a name="immediate-and-deferred-rendering"></a>Sofortiges und verzögertes Rendering

Direct3D 11 unterstützt zwei renderingtypen: direkt und verzögert. Beide werden mithilfe der [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Schnittstelle implementiert.

## <a name="immediate-rendering"></a>Sofortiges Rendering

Sofortiges Rendering bezieht sich auf das Aufrufen von Rendering-APIs oder-Befehlen von einem Gerät, das die Befehle in einem Puffer zur Ausführung auf der GPU in die Warteschlange stellt. Verwenden Sie einen unmittelbaren Kontext zum Rendering, zum Festlegen des Pipeline Zustands und zum Wiedergeben einer Befehlsliste.

Erstellen Sie einen unmittelbaren Kontext mithilfe von [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="deferred-rendering"></a>Verzögertes Rendering

Das verzögerte Rendering zeichnet Grafikbefehle in einem Befehls Puffer auf, damit Sie zu einem späteren Zeitpunkt wiedergegeben werden können. Verwenden Sie einen verzögerten Kontext zum Aufzeichnen von Befehlen (Rendering und Zustands Einstellung) in einer Befehlsliste. Verzögertes Rendering ist ein neues Konzept in Direct3D 11; das verzögerte Rendering unterstützt das Rendering in einem Thread beim Aufzeichnen von Befehlen für das Rendering in weiteren Threads. Diese parallele multithreadstrategie ermöglicht es Ihnen, komplexe Szenen in gleichzeitige Aufgaben zu unterbrechen. Weitere Informationen zum Rendern komplexer Szenen finden Sie unter [Multi-Pass-Rendering](overviews-direct3d-11-render-multipass.md).

Erstellen Sie einen verzögerten Kontext mithilfe von [**ID3D11Device:: kreatedeferredcontext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

Direct3D generiert renderingaufwand, wenn Befehle im Befehls Puffer in die Warteschlange eingereiht werden. Im Gegensatz dazu wird eine [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md) während der Wiedergabe wesentlich effizienter ausgeführt. Zum Verwenden einer Befehlsliste zeichnen Sie renderingbefehle mit einem verzögerten Kontext auf und wiedergeben Sie mithilfe eines unmittelbaren Kontexts wieder.

Sie können nur eine einzige Befehlsliste im Single Thread-Stil generieren. Sie können jedoch mehrere verzögerte Kontexte gleichzeitig erstellen und verwenden, jeweils in einem separaten Thread. Anschließend können Sie diese mehrere verzögerte Kontexte verwenden, um mehrere Befehlslisten gleichzeitig zu erstellen.

Sie können zwei oder mehr Befehlslisten nicht gleichzeitig im unmittelbaren Kontext wiedergeben.

Um zu ermitteln, ob ein Gerätekontext ein unmittelbarer oder ein verzögerter Kontext ist, müssen Sie [**Verknüpfung id3d11devicecontext aus:: GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gettype)aufrufen.

Die [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) -Methode wird nur in einem verzögerten Kontext für dynamische Ressourcen ([**D3D11 \_ Usage \_ Dynamic**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) unterstützt, wobei der erste Befehl in der Befehlsliste [**D3D11 Map- \_ \_ Schreib \_ Verwerfungs**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)Wert ist. **D3D11 \_ Das \_ schreiben \_ \_** von Zuordnungen wird für nachfolgende Aufrufe nicht unterstützt, sofern diese für den angegebenen Ressourcentyp verfügbar sind.

Abfragen in einem verzögerten Kontext sind auf die Datengenerierung und die Prädikat Zeichnung beschränkt. Sie können [**Verknüpfung id3d11devicecontext aus:: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) nicht in einem verzögerten Kontext aufrufen, um Daten zu einer Abfrage abzurufen. Sie können **GetData** nur im unmittelbaren Kontext aufrufen, um Daten zu einer Abfrage abzurufen. Sie können ein Rendering-Prädikat (einen Abfragetyp) festlegen, indem Sie [**D3D11DeviceContext:: setprediation**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-setpredication) aufrufen, um Abfrageergebnisse auf der GPU zu verwenden. Sie können Abfrage Daten durch Aufrufe von [**Verknüpfung id3d11devicecontext aus:: begin**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-begin) und [**Verknüpfung id3d11devicecontext aus:: End**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-end)generieren. Die Abfrage Daten sind jedoch erst verfügbar, wenn Sie [**Verknüpfung id3d11devicecontext aus:: executecommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) im unmittelbaren Kontext aufrufen, um die verzögerte Kontext Befehlsliste zu übermitteln. Die Abfrage Daten werden dann von der GPU verarbeitet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




