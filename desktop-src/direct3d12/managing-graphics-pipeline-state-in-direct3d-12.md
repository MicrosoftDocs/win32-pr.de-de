---
title: Verwalten des Grafik Pipeline Status in Direct3D 12
description: In diesem Thema wird beschrieben, wie der Status der Grafik Pipeline in Direct3D 12 festgelegt wird.
ms.assetid: AAF97BD2-D532-469D-9242-CC94C06727C3
keywords:
- Pipeline Status
- Pipeline Zustands Objekt
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7564b5863d3efebdf8a335e2c46945aeebea93e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548761"
---
# <a name="managing-graphics-pipeline-state-in-direct3d-12"></a>Verwalten des Grafik Pipeline Status in Direct3D 12

In diesem Thema wird beschrieben, wie der Status der Grafik Pipeline in Direct3D 12 festgelegt wird.

## <a name="pipeline-state-overview"></a>Übersicht über den Pipeline Status

Wenn Geometry an die zu Zeichnungsende GPU (Graphics Processing Unit) übermittelt wird, gibt es eine Vielzahl von Hardware Einstellungen, die bestimmen, wie die Eingabedaten interpretiert und gerendert werden. Gemeinsam werden diese Einstellungen als Grafik Pipeline Status bezeichnet und umfassen allgemeine Einstellungen wie den Status des Rasterizers, den Blend-Status und den Status der tiefen Schablone sowie den primitiven Topologietyp der übermittelten Geometrie und der Shader, die für das Rendering verwendet werden. In Microsoft Direct3D 12 wird der größte Grafik Pipeline Status mithilfe von Pipeline Zustands Objekten (PSO) festgelegt. Eine APP kann eine unbegrenzte Anzahl von Objekten erstellen, die von der [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) -Schnittstelle dargestellt wird, in der Regel zur Initialisierungs Zeit. Zum Zeitpunkt der Wiedergabe können Befehlslisten schnell mehrere Einstellungen des Pipeline Zustands umschalten, indem Sie [**ID3D12GraphicsCommandList:: setpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate) in einer direkten Befehlsliste oder einem Paket aufrufen, um die aktive PSO festzulegen.

In Direct3D 11 wurde der Grafik Pipeline Zustand in große, grob abgestimmte Zustands Objekte wie [**ID3D11BlendState**](/windows/win32/api/d3d11/nn-d3d11-id3d11blendstate) gebündelt, die zur Renderingzeit im unmittelbaren Kontext mit Methoden wie [**Verknüpfung id3d11devicecontext aus:: omsetblendstate**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-omsetblendstate)erstellt und festgelegt werden konnten. Die Idee dahinter war, dass die GPU durch das Festlegen verwandter Einstellungen (z. b. die Blend-Zustands Einstellungen) gleichzeitig Effizienz erzielen konnte. Mit der aktuellen Grafikhardware gibt es jedoch Abhängigkeiten zwischen den verschiedenen Hardware Einheiten. Beispielsweise kann der Hardware-Blend-Status Abhängigkeiten vom Raster Status und dem Blend-Status aufweisen. PSOs in Direct3D 12 wurden so konzipiert, dass die GPU alle abhängigen Einstellungen in den einzelnen Pipeline Zuständen Vorverarbeiten kann (in der Regel während der Initialisierung), um so effizient wie möglich zwischen den Zuständen zu wechseln.

Beachten Sie, dass zwar die meisten Einstellungen des Pipeline Zustands mithilfe von PSOs festgelegt werden, aber einige Zustands Einstellungen festgelegt werden, die separat mithilfe der von [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)bereitgestellten APIs festgelegt werden. Diese Einstellungen und die zugehörigen APIs werden im folgenden ausführlich erläutert. Außerdem gibt es Unterschiede in der Art und Weise, in der der Grafik Pipeline Zustand von der direkten Befehlsliste und den Paketen geerbt und beibehalten wird. Dieses Thema enthält ausführliche Informationen zu den beiden folgenden Themen.

## <a name="graphics-pipeline-states-set-with-pipeline-state-objects"></a>Mit Pipeline Zustands Objekten festgelegte Grafik Pipeline Zustände

Am einfachsten können Sie alle unterschiedlichen Pipeline Zustände anzeigen, die mithilfe eines Pipeline Zustands Objekts festgelegt werden können, indem Sie sich das Referenz Thema für den [**D3D12- \_ Grafik \_ Pipeline Status- \_ \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) ansehen, den Sie beim Initialisieren des Objekts an [**ID3D12Device:: aliategraphicspipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) übergeben. Eine kurze Zusammenfassung der Zustände, die festgelegt werden können, umfasst:

-   Der Bytecode für alle Shader, einschließlich Scheitelpunkt-, Pixel-, Domänen-, Hull-und Geometry-Shadern.
-   Das Format für die Eingabe des Scheitel Punkts.
-   Der primitive Topologietyp. Beachten Sie, dass der primitive Topologietyp des Eingabe-Assemblers (Point, Line, Dreieck, Patch) innerhalb des PSO festgelegt wird, indem die [**D3D12 \_ primitive \_ \_ Topologietyp**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) -Enumeration verwendet wird. Die grundlegende und die Reihenfolge (Zeilen Liste, Zeilen Streifen, Zeilen Streifen mit Informationsdaten usw.) werden in einer Befehlsliste mithilfe der [**ID3D12GraphicsCommandList:: iasetprimitivetopology**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology) -Methode festgelegt.
-   Der Blend-Zustand, der Status des Rasterizers, der Status der tiefen Schablone.
-   Die tiefen Schablone und renderzielformate sowie die Anzahl der Renderziele.
-   Parameter für mehrere Stichproben.
-   Ein Ausgabepuffer für das Streaming.
-   Die Stamm Signatur. Weitere Informationen finden Sie unter [root Signature](root-signatures.md).

## <a name="graphics-pipeline-states-set-outside-of-the-pipeline-state-object"></a>Außerhalb des Pipeline Zustands Objekts festgelegte Grafik Pipeline Zustände

Die meisten Grafik Pipeline Zustände werden mithilfe von PSOs festgelegt. Es gibt jedoch einen Satz von Pipeline Zustands Parametern, die durch den Aufruf von Methoden der [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) -Schnittstelle innerhalb einer Befehlsliste festgelegt werden. In der folgenden Tabelle sind die Zustände, die auf diese Weise festgelegt werden, und die entsprechenden Methoden aufgeführt.

|Zustand|Methode|
|-|-|
|Ressourcen Bindungen|[**Iasetindexbuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)<br/>[**Iasetvertexbuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)<br/>[**Sosettargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)<br/>[**Omantrendertargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)<br/>[**Setdescriptorheaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)<br/>Alle **setgraphicsroot...** -Methoden<br/>Alle **setcomputeroot...** -Methoden<br/>
|Viewports|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports">**Rssetviewports**</a>|
|Scissor-Rechtecke|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects">**Rssezcissorrects**</a>|
|Blend-Faktor|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetblendfactor">**Omsetblendfactor**</a>|
|Der Verweis Wert der tiefen Schablone.|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref">**Omsetstencilref**</a>|
|Die primitive topologiereihen Folge und der Typ der Eingabe Assembler|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology">**Iasetprimitivetopology**</a>|

## <a name="graphics-pipeline-state-inheritance"></a>Vererbung von Grafik Pipeline Zuständen

Da direkte Befehlslisten in der Regel für eine Verwendung gleichzeitig vorgesehen sind und Pakete mehrmals gleichzeitig verwendet werden sollen, gibt es verschiedene Regeln für die Vererbung des Grafik Pipeline Zustands, der von vorherigen Befehlslisten oder Paketen festgelegt wurde.

Für die Grafik Pipeline Zustände, die mithilfe von PSOs festgelegt werden, wird keiner dieser Zustände entweder durch direkte Befehlslisten oder Bündel geerbt. Der anfängliche Status der Grafik Pipeline für direkte Befehlslisten und Pakete wird zum Zeitpunkt der Erstellung mit dem [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) -Parameter auf [**ID3D12Device:: | atecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)festgelegt. Wenn im-Befehl kein PSO angegeben ist, wird ein Standard Anfangszustand verwendet. Sie können das aktuelle PSO in einer Befehlsliste durch Aufrufen von [**ID3D12GraphicsCommandList:: setpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)ändern.

Direkte Befehlslisten Erben auch keinen Zustand, der mit Befehlslisten Methoden wie [**rssetviewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)festgelegt wird. Ausführliche Informationen zu den Standard Anfangswerten für nicht-PSO-Zustände finden Sie unter [**ID3D12GraphicsCommandList:: clearstate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate).

Pakete erben den gesamten Grafik Pipeline Status, der nicht mit PSOs festgelegt ist, mit Ausnahme des primitiven topologietyps. Die primitive Topologie wird immer auf [**D3D12 \_ primitiver \_ \_ Topologietyp \_ undefiniert**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) festgelegt, wenn ein Paket mit der Ausführung beginnt. Jeder Status, der in einem Bündel festgelegt wird (der PSO selbst, der nicht PSO-basierte Zustand und Ressourcen Bindungen), wirkt sich auf den Status der übergeordneten direkten Befehlsliste aus. Wenn z. b. ein [**rssetviewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports) innerhalb eines Pakets aufgerufen wird, werden die angegebenen Viewports weiterhin in der übergeordneten direkten Befehlsliste für Aufrufe festgelegt, die sich nach dem [**executebundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) -Aufruf befinden, der die Viewports festgelegt hat.

Ressourcen Bindungen, die in einer Befehlsliste oder einem Bundle festgelegt sind, bleiben erhalten. In einer direkten Befehlsliste geänderte Ressourcen Bindungen werden also weiterhin innerhalb der nachfolgenden untergeordneten Paket Ausführung festgelegt. Und Ressourcen Bindungen, die innerhalb eines Pakets geändert wurden, werden weiterhin für nachfolgende Aufrufe innerhalb der übergeordneten direkten Befehlsliste festgelegt.

Weitere Informationen zu Bindungen finden Sie im Abschnitt **Paket Semantik** unter [Verwenden einer Stamm Signatur](using-a-root-signature.md).

## <a name="related-topics"></a>Verwandte Themen

* [Arbeits Übermittlung in Direct3D 12](command-queues-and-command-lists.md)