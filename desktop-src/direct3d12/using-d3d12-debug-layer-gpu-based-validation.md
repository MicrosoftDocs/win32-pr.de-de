---
title: GPU-basierte Validierung und die Direct3D 12-Debugebene
description: In diesem Thema wird beschrieben, wie Sie die Direct3D 12-Debugebene optimal nutzen. GPU-basierte Validierung (GBV) ermöglicht Validierungsszenarien auf der GPU-Zeitachse, die während API-Aufrufen auf der CPU nicht möglich sind.
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 63e1ebbe34bbb94fbdf52b374b10283100e3bfa432338521a9807497b236d868
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952740"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a>GPU-basierte Validierung und die Direct3D 12-Debugebene

In diesem Thema wird beschrieben, wie Sie die Direct3D 12-Debugebene optimal nutzen. GPU-basierte Validierung (GBV) ermöglicht Validierungsszenarien auf der GPU-Zeitachse, die während API-Aufrufen auf der CPU nicht möglich sind. GBV ist ab den Grafiktools für Windows 10 Anniversary Update verfügbar.

## <a name="purpose-of-gpu-based-validation"></a>Zweck der GPU-basierten Überprüfung

Die GPU-basierte Überprüfung hilft bei der Identifizierung der folgenden Fehler:

- Verwendung von nicht initialisierten oder inkompatiblen Deskriptoren in einem Shader.
- Verwendung von Deskriptoren, die auf gelöschte Ressourcen in einem Shader verweisen.
- Überprüfung der heraufgestuften Ressourcenzustände und des Ressourcenzustandsverfalls.
- Indizierung nach dem Ende des Deskriptorheaps in einem Shader.
- Shader greift auf Ressourcen im inkompatiblen Zustand zu.
- Verwendung von nicht initialisierten oder inkompatiblen Samplern in einem Shader.

GbV erstellt gepatchte Shader, deren Validierung direkt dem Shader hinzugefügt wurde. Die gepatchten Shader überprüfen Stammargumente und Ressourcen, auf die während der Ausführung des Shaders zugegriffen wird, und melden Fehler an einen Protokollpuffer. GbV fügt auch zusätzliche Vorgänge und Dispatch-Aufrufe in die Anwendungsbefehlslisten ein, um Änderungen am Ressourcenzustand zu überprüfen und nachzuverfolgen, die von der Befehlsliste auf der GPU-Zeitachse vorgegeben werden.

Da GBV die Möglichkeit zum Ausführen von Shadern erfordert, werden COPY-Befehlslisten durch eine COMPUTE-Befehlsliste emuliert. Dies kann möglicherweise die Art und Weise ändern, in der Hardware Kopien ausführt, obwohl das Endergebnis nicht geändert werden sollte. Die Anwendung erkennt weiterhin, dass es sich hierbei um COPY-Befehlslisten handelt, und die Debugebene überprüft sie als solche.

## <a name="turning-on-gpu-based-validation"></a>Aktivieren der GPU-basierten Überprüfung

GBV kann für die Verwendung des DirectX-Systemsteuerung (DXCPL) erzwungen werden, indem die Direct3D 12-Debugebene erzwungen und zusätzlich die GPU-basierte Validierung erzwungen wird (neue Registerkarte in der Systemsteuerung). Nach der Aktivierung bleibt GBV aktiviert, bis das Direct3D 12-Gerät freigegeben wird. Alternativ kann GBV vor dem Erstellen des Direct3D 12-Geräts programmgesteuert aktiviert werden:

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

Im Allgemeinen sollten Sie Ihren Code mit aktivierter Debugebene ausführen. GbV kann dies jedoch erheblich verlangsamen. Entwickler können erwägen, GBV mit kleineren Datensätzen zu aktivieren (z. B. Engine-Demos oder kleine Spielebenen mit weniger PSO und Ressourcen) oder während einer frühen Anwendungsinbetriebszeit, um Leistungsprobleme zu reduzieren. Bei größeren Inhalten sollten Sie gbv auf einem oder zwei Testcomputern in einem nachts ausgeführten Testdurchlauf aktivieren.

## <a name="debug-output"></a>Debugausgabe

GBV erzeugt eine Debugausgabe, nachdem ein Aufruf von [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) die Ausführung auf der GPU abgeschlossen hat. Da sich dies auf der GPU-Zeitachse befindet, kann die Debugausgabe mit einer anderen CPU-Zeitachsenüberprüfung asynchron sein. Anwendungsentwickler möchten möglicherweise ihre eigene Wait-After-Execute-Anweisung einfügen, um die Debugausgabe zu synchronisieren.

Die GBV-Ausgabe gibt an, wo in einem Shader ein Fehler aufgetreten ist, zusammen mit der aktuellen Draw/Dispatch-Anzahl und Identitäten verwandter Objekte (z. B. Befehlsliste, Warteschlange, PSO usw.).

## <a name="example-debug-message"></a>Beispiel für eine Debugmeldung

Die folgende Fehlermeldung gibt an, dass auf eine Ressource mit dem Namen "Hauptfarbpuffer" in einem Shader als Shaderressource zugegriffen wurde, sich aber im ungeordneten Zugriffsstatus befand, als der Shader auf der GPU ausgeführt wurde. Zusätzliche Informationen, z. B. die Position in der Shaderquelle, der Name der Befehlsliste und die Draw-Anzahl (Draw Index) sowie die Namen der zugehörigen D3D-Schnittstellenobjekte werden ebenfalls bereitgestellt.

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

## <a name="debug-layer-apis"></a>Debugebenen-APIs

Um die Debugebene zu aktivieren, rufen [**Sie EnableDebugLayer auf.**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)

Um die GPU-basierte Validierung zu aktivieren, rufen [**Sie SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)auf, und verweisen Sie auf die Methoden der folgenden Schnittstellen:

- [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

Weitere Informationen finden Sie in den folgenden Enumerationen und Strukturen:

- [**PARAMETERTYP DER \_ D3D12-DEBUGBEFEHLSLISTE \_ \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [**D3D12 \_ DEBUG \_ DEVICE \_ PARAMETER \_ TYPE**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [**D3D12 \_ \_ GPU-BASIERTE \_ \_ \_ VALIDIERUNGSPIPELINE – \_ \_ ZUSTANDSERSTELLUNGSFLAGS**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [**D3D12 \_ \_ GPU-BASIERTER \_ \_ VALIDIERUNGS-SHADER-PATCHMODUS \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [**D3D12 \_ \_ \_ DEBUGBEFEHLSLISTE \_ \_ GPU-BASIERTE \_ \_ VALIDIERUNGSEINSTELLUNGEN**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [**D3D12– \_ \_ DEBUGGEN VON \_ \_ GPU-BASIERTEN \_ \_ ÜBERPRÜFUNGSEINSTELLUNGEN FÜR GERÄTE**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a>Zugehörige Themen

* [Grundlegendes zur Direct3D 12-Debugebene](understanding-the-d3d12-debug-layer.md)
