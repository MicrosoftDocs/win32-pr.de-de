---
title: GPU-basierte Validierung und die Direct3D 12-Debugebene
description: In diesem Thema wird beschrieben, wie die Direct3D 12-Debugebene optimal genutzt wird. Die GPU-basierte Validierung (GBV) ermöglicht Validierungs Szenarien auf der GPU-Zeitachse, die bei API-aufrufen auf der CPU nicht möglich sind.
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 3160df3faf994df2abf9cf878088e84564bb5fe1
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548731"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a>GPU-basierte Validierung und die Direct3D 12-Debugebene

In diesem Thema wird beschrieben, wie die Direct3D 12-Debugebene optimal genutzt wird. Die GPU-basierte Validierung (GBV) ermöglicht Validierungs Szenarien auf der GPU-Zeitachse, die bei API-aufrufen auf der CPU nicht möglich sind. GBV ist ab dem Grafik Tool für Windows 10 Anniversary Update verfügbar.

## <a name="purpose-of-gpu-based-validation"></a>Zweck der GPU-basierten Validierung

Die GPU-basierte Überprüfung hilft bei der Identifizierung der folgenden Fehler:

- Verwendung von nicht initialisierten oder inkompatiblen Deskriptoren in einem Shader.
- Verwendung von Deskriptoren, die auf gelöschte Ressourcen in einem Shader verweisen.
- Validierung der höher gestuften Ressourcen Zustände und des Zustands des Ressourcen Zustands.
- Indizierung über das Ende des deskriptorheaps in einem Shader hinaus.
- Shader-Zugriffe von Ressourcen im inkompatiblen Zustand.
- Verwendung von nicht initialisierten oder inkompatiblen Samplern in einem Shader.

GBV funktioniert, indem gepatchte Shader erstellt werden, deren Validierung dem Shader direkt hinzugefügt wurde. Die gepatchten Shader überprüfen Stamm Argumente und Ressourcen, auf die während der shaderausführung zugegriffen wurde, und melden Fehler an einen Protokollpuffer GBV fügt auch zusätzliche Vorgänge und Dispatch-Aufrufe in die Anwendungs Befehlslisten ein, um Änderungen am Ressourcen Status zu überprüfen und nachverfolgen, die von der Befehlsliste auf der GPU-Zeitachse erhoben werden.

Da GBV die Fähigkeit zum Ausführen von Shadern erfordert, werden Kopier Befehlslisten durch eine COMPUTE-Befehlsliste emuliert. Dies kann möglicherweise die Art und Weise ändern, wie Hardware Kopien ausführt, obwohl das Endergebnis nicht geändert werden sollte. Diese werden von der Anwendung weiterhin als Kopier Befehlslisten wahrgenommen, und die debugschicht überprüft sie als solche.

## <a name="turning-on-gpu-based-validation"></a>Aktivieren der GPU-basierten Validierung

GBV kann bei der Verwendung der DirectX-Systemsteuerung (dxcpl) erzwungen werden, indem auf der Direct3D 12-debugschicht erzwungen und zusätzlich die GPU-basierte Validierung erzwungen wird (neue Registerkarte in der Systemsteuerung). Nach der Aktivierung bleibt GBV aktiviert, bis das Direct3D 12-Gerät freigegeben wird. Alternativ kann GBV auch Programm gesteuert aktiviert werden, bevor das Direct3D 12-Gerät erstellt wird:

```cpp
void EnableShaderBasedValidation()
{
    CComPtr<ID3D12Debug> spDebugController0;
    CComPtr<ID3D12Debug1> spDebugController1;
    VERIFY(D3D12GetDebugInterface(IID_PPV_ARGS(&spDebugController0)));
    VERIFY(spDebugController0->QueryInterface(IID_PPV_ARGS(&spDebugController1)));
    spDebugController1->SetEnableGPUBasedValidation(true);
}
```

## <a name="recommended-usage"></a>Empfohlene Verwendung

Im Allgemeinen sollten Sie den Code in den meisten Fällen mit aktivierter debugschicht ausführen. GBV kann jedoch eine große Anzahl von Aufgaben beeinträchtigen. Entwickler könnten GBV mit kleineren Datasets aktivieren (z. b. Engine-Demos oder kleine Spielebenen mit weniger PSO-und-Ressourcen) oder während der frühen Anwendungs Bereitstellung, um Leistungsprobleme zu verringern. Bei größeren Inhalten empfiehlt es sich, GBV in einem nächtlichen Test Durchlauf auf einem oder zwei Testcomputern zu aktivieren.

## <a name="debug-output"></a>Ausgabe Debuggen

GBV erzeugt eine Debugausgabe, nachdem bei der Ausführung von [**executecommandlists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) die Ausführung auf der GPU abgeschlossen wurde. Da sich dies auf der GPU-Zeitachse befindet, kann die Debugausgabe mit einer anderen CPU-Zeitachsen Validierung asynchron sein. Anwendungsentwickler möchten möglicherweise Ihre eigene Wait-after-Execute-Datei einfügen, um die Debugausgabe zu synchronisieren.

Die GBV-Ausgabe gibt an, wo ein Fehler in einem Shader aufgetreten ist, zusammen mit der aktuellen Draw-/Dispatch-Anzahl und den Identitäten verwandter Objekte (z. b. Befehlsliste, Warteschlange, PSO usw.).

## <a name="example-debug-message"></a>Beispiel für Debugmeldung

Die folgende Fehlermeldung gibt an, dass auf eine Ressource mit dem Namen "Haupt Farb Puffer" in einem Shader als Shaderressource zugegriffen wurde, sich jedoch im ungeordneten Zugriffs Zustand befunden hat, als der Shader auf der GPU ausgeführt wurde. Weitere Informationen, wie z. b. der Speicherort in der Shader-Quelle, der Name der Befehlsliste und der Zeichnungs Zähler (Index zeichnen) und die Namen von verknüpften D3D-Schnittstellen Objekten werden ebenfalls bereitgestellt.

```cmd
D3D12 ERROR: Incompatible resource state: Resource: 0x0000016F61A6EA80:'Main Color Buffer', 
Subresource Index: [0], 
Descriptor heap index: [0], 
Binding Type In Descriptor: SRV, 
Resource State: D3D12_RESOURCE_STATE_UNORDERED_ACCESS(0x8), 
Shader Stage: PIXEL, 
Root Parameter Index: [0], 
Draw Index: [0], 
Shader Code: E:\FileShare\MiniEngine_GitHub_160128\MiniEngine_GitHub\Core\Shaders\SharpeningUpsamplePS.hlsl(37,2-59), 
Asm Instruction Range: [0x138-0x16b], 
Asm Operand Index: [3], 
Command List: 0x0000016F6F75F740:'CommandList', SRV/UAV/CBV Descriptor Heap: 0x0000016F6F76F280:'Unnamed ID3D12DescriptorHeap Object', 
Sampler Descriptor Heap: <not set>, 
Pipeline State: 0x0000016F572C89F0:'Unnamed ID3D12PipelineState Object',  
[ EXECUTION ERROR #942: GPU_BASED_VALIDATION_INCOMPATIBLE_RESOURCE_STATE]
```

## <a name="debug-layer-apis"></a>Debug-ebenenapis

Um die Debug-Ebene zu aktivieren, müssen Sie [**enabledebuglayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)aufzurufen.

Um die GPU-basierte Validierung zu aktivieren [**, geben**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)Sie "*" an, und verweisen Sie auf die Methoden der folgenden Schnittstellen:

- [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

Weitere Informationen finden Sie in den folgenden Enumerationen und Strukturen:

- [**D3D12 \_ Debug- \_ Befehls \_ Listen- \_ \_ Parametertyp**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [**D3D12 \_ Debug \_ - \_ Geräte \_ Parametertyp**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [**D3D12 \_ GPU- \_ basierter \_ Validierungs \_ Pipeline \_ Status \_ Create \_ Flags**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [**D3D12 \_ GPU- \_ basierter \_ Validierungs- \_ Shader- \_ \_ patchmodus**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [**D3D12 \_ Debug- \_ Befehls \_ Liste GPU- \_ \_ basierte \_ Validierungs \_ Einstellungen**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [**D3D12 \_ Debuggen von \_ \_ GPU-basierten Überprüfungs \_ \_ \_ Einstellungen für Geräte**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a>Verwandte Themen

* [Grundlegendes zur Direct3D 12-Debugebene](understanding-the-d3d12-debug-layer.md)
