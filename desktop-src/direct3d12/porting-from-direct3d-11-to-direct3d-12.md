---
title: Portieren von Direct3D 11 zu Direct3D 12
description: Dieser Abschnitt enthält einige Anleitungen zum Portieren von einer benutzerdefinierten Direct3D 11-Grafik-Engine zu Direct3D 12.
ms.assetid: 9EB4AC6B-AFDD-4673-8EB3-54272C151784
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ccf4a0bd10032d94ecaf4a88cc442f3a7ad516
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812558"
---
# <a name="porting-from-direct3d-11-to-direct3d-12"></a>Portieren von Direct3D 11 zu Direct3D 12

Dieser Abschnitt enthält einige Anleitungen zum Portieren von einer benutzerdefinierten Direct3D 11-Grafik-Engine zu Direct3D 12.

-   [Geräteerstellung](#device-creation)
-   [Ressourcen, für die ein Committed (Ressourcen](#committed-resources)
-   [Reservierte Ressourcen](#reserved-resources)
-   [Hochladen von Daten](#uploading-data)
-   [Shader und Shaderobjekte](#shaders-and-shader-objects)
-   [Übermitteln von Arbeit an die GPU](#submitting-work-to-the-gpu)
-   [CPU-/GPU-Synchronisierung](#cpugpu-synchronization)
-   [Ressourcenbindung](#resource-binding)
-   [Ressourcenzustand](#resource-state)
-   [Swapchains](#swapchains)
-   [Funktionsrendering korrigiert](#fixed-function-rendering)
-   [Wahrscheinlichkeit und Ende](#odds-and-ends)
-   [Zugehörige Themen](#related-topics)

## <a name="device-creation"></a>Geräteerstellung

Sowohl Direct3D 11 als auch Direct3D 12 verwenden ein ähnliches Muster für die Geräteerstellung. Vorhandene Direct3D 12-Treiber sind D3D_FEATURE_LEVEL_11_0 oder besser, sodass Sie die älteren Featureebenen und die damit verbundenen Einschränkungen ignorieren können. 

Beachten Sie außerdem, dass Sie mit Direct3D 12 Geräteinformationen explizit mit dxgi-Schnittstellen aufzählen sollten. In Direct3D 11  können Sie vom Direct3D-Gerät zurück zum DXGI-Gerät verketten, was für Direct3D 12 nicht unterstützt wird.

Zum Erstellen eines WARP-Softwaregeräts auf Direct3D 12 wird ein expliziter Adapter von **IDXGIFactory4::EnumWarpAdapter angegeben.** Das WARP-Gerät für Direct3D 12 ist nur auf Systemen verfügbar, auf dem das **optionale Feature** Grafiktools aktiviert ist.

> [!NOTE]
> Es gibt keine Entsprechung zu **D3D11CreateDeviceAndSwapChain.** Selbst bei Direct3D 11 raten wir von der Verwendung dieser Funktion ab, da es oft besser ist, das Gerät zu erstellen und die Swapchain in unterschiedlichen Schritten zu verwenden.

## <a name="committed-resources"></a>Ressourcen, für die ein Committed (Ressourcen

Objekte, die mit den folgenden Schnittstellen in Direct3D 11 erstellt wurden, werden in Direct3D 12 in sogenannte "übertragene Ressourcen" übersetzt. Eine Ressource, für die ein Committed ausgeführt wurde, ist eine Ressource, der sowohl virtueller Adressraum als auch physische Seiten zugeordnet sind. Dies ist ein Konzept des Arbeitsspeichermodells von Microsoft Windows Device Driver 2 (WDD2), auf dem Direct3D 12 basiert.

Direct3D 11-Ressourcen:

-   [**ID3D11Resource**](/windows/win32/api/d3d11/nn-d3d11-id3d11resource)
-   [**ID3D11Buffer**](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) und [ **ID3D11Device::CreateBuffer**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createbuffer)
-   [**ID3D11Texture1D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture1d) und [ **ID3D11Device:CreateTexture1D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture1d)
-   [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) und [ **ID3D11Device::CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d)
-   [**ID3D11Texture3D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture3d) und [ **ID3D11Device::CreateTexture3D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture3d)

In Direct3D 12 werden diese alle durch [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) und [**ID3D12Device::CreateCommittedResource dargestellt.**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)

## <a name="reserved-resources"></a>Reservierte Ressourcen

Reservierte Ressourcen sind Ressourcen, bei denen nur virtueller Adressraum zugeordnet wurde, physischer Speicher erst dann zugeordnet wird, wenn [**ID3D12Device::CreateHeap aufruft.**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap) Dies ist im Wesentlichen das gleiche Konzept wie bei gekachelten Ressourcen in Direct3D 11.

Die Flags ([**D3D11 \_ RESOURCE \_ MISC \_ FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)), die in Direct3D 11 zum Einrichten von gekachelten Ressourcen verwendet werden, und ordnen sie dann dem physischen Speicher zu.

-   D3D11 \_ RESSOURCE \_ FALSCH \_ GEKACHELT
-   D3D11 \_ RESOURCE \_ MISC \_ TILE \_ POOL

## <a name="uploading-data"></a>Hochladen von Daten

In Direct3D 11 wird eine einzelne Zeitachse angezeigt (Aufrufe nach einer Sequenz, z. B. Daten, die mit [**D3D11 \_ SUBRESOURCE \_ DATA**](/windows/win32/api/d3d11/ns-d3d11-d3d11_subresource_data)initialisiert wurden), dann erfolgt ein Aufruf von [**ID3D11DeviceContext::UpdateSubresource**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource)und dann ein Aufruf von [**ID3D11DeviceContext::Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)). Die Anzahl der erstellten Kopien der Daten ist für einen Direct3D 11-Entwickler nicht offensichtlich.

In Direct3D 12 gibt es zwei Zeitachsen: die GPU-Zeitachse (eingerichtet durch Aufrufe von [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)und [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) aus zuordnungsfähigem Arbeitsspeicher) und die CPU-Zeitachse (bestimmt durch Aufrufe von [**Map).**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map) Hilfsfunktionen werden (in der Datei d3dx12.h) mit dem Namen [**Updatesubresources**](updatesubresources1.md) bereitgestellt, die eine freigegebene Zeitachse verwenden. Es gibt mehrere Variationen dieser Hilfsfunktion, eine, die [**ID3D12Device::GetCopyableFootprints**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)verwendet, eine andere, die einen Heapzuweisungsmechanismus verwendet, und eine andere, die einen Stapelzuweisungsmechanismus verwendet. Diese Hilfsfunktionen kopieren Ressourcen über einen zwischengeschalteten Stagingbereich des Arbeitsspeichers sowohl auf die GPU als auch auf die CPU.

In der Regel verfügen GPU und CPU jeweils über eine eigene Kopie einer Ressource, die an ihre eigene Zeitachse gebunden ist. Der Ansatz für die gemeinsame Zeitachse verwaltet auf ähnliche Weise zwei Kopien.

## <a name="shaders-and-shader-objects"></a>Shader und Shaderobjekte

In Direct3D 11 werden viele Shader- und Zustandsobjekte erstellt und der Zustand dieser Objekte mithilfe der [**Id3D11Device-Erstellungsmethoden**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) und der [**Set-Methoden ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) festgelegt. In der Regel wird eine große Anzahl von Aufrufen an diese Methoden durchgeführt, die dann zur Zeichnen-Zeit vom Treiber kombiniert werden, um den richtigen Pipelinezustand zu festlegen.

In Direct3D 12 wurde diese Einstellung des Pipelinezustands zu einem einzelnen Objekt kombiniert ([**CreateComputePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) für eine Compute-Engine und [**CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) für eine Grafik-Engine), das dann vor dem Zeichnen-Aufruf mit einem Aufruf von [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)an eine Befehlsliste angefügt wird.

Diese Aufrufe ersetzen alle einzelnen Aufrufe zum Festlegen von Shadern, Eingabelayout, Überblendungszustand, Rasterizerzustand, Tiefenschablonenzustand und so weiter in Direct3D 11.

- Device 11-Methoden: ``CreateInputLayout`` , ``CreateXShader`` , ``CreateDepthStencilState`` undD ``CreateRasterizerState`` .
- Gerätekontext 11-Methoden:  ``IASetInputLayout`` , , , und ``xxSetShader`` ``OMSetBlendState`` ``OMSetDepthStencilState`` ``RSSetState`` .

Während Direct3D 12 ältere kompilierte Shaderblobs unterstützen kann, sollten Shader entweder mit shader Model 5.1 mit den FXC/D3DCompile-APIs oder mithilfe des DXIL DXC-Compilers mit shader Model 6 erstellt werden. Überprüfen Sie die Shadermodell 6-Unterstützung mit [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) und **D3D12_FEATURE_SHADER_MODEL**.

## <a name="submitting-work-to-the-gpu"></a>Übermitteln von Arbeit an die GPU

In Direct3D 11 gibt es nur wenig Kontrolle darüber, wie die Arbeit übermittelt wird. Sie wird größtenteils vom Treiber verarbeitet, obwohl ein gewisses Steuerelement über die Aufrufe [**ID3D11DeviceContext::Flush**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-flush) und [**IDXGISwapChain1::P resent1 aktiviert**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) wird.

In Direct3D 12 erfolgt die Übermittlung von Arbeit sehr explizit und wird von der App gesteuert. Das primäre Konstrukt zum Übermitteln von Arbeit ist [**die ID3D12GraphicsCommandList,**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)die zum Aufzeichnen aller Apps-Befehle verwendet wird (und im Konzept dem verzögerten KONTEXT ID3D11 sehr ähnlich ist). Der Unterstützungsspeicher für eine Befehlsliste wird von [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)bereitgestellt, wodurch die App die Speicherauslastung der Befehlsliste verwalten kann, indem tatsächlich der Arbeitsspeicher verfügbar ist, den der Direct3D 12-Treiber zum Speichern der Befehlsliste verwenden wird.

Schließlich ist [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) eine First-in-First-Out-Warteschlange, in der die richtige Reihenfolge der Befehlslisten für die Übermittlung an die GPU gespeichert wird. Nur wenn eine Befehlsliste die Ausführung auf der GPU abgeschlossen hat, wird die nächste Befehlsliste aus der Warteschlange vom Treiber übermittelt.

In Direct3D 11 gibt es kein explizites Konzept einer Befehlswarteschlange. Beim allgemeinen Setup für Direct3D 12  kann die derzeit geöffnete D3D12_COMMAND_LIST_TYPE_DIRECT-Befehlsliste für den aktuellen Frame analog zum direkten Direct3D 11-Kontext betrachtet werden. Dies stellt viele der gleichen Funktionen zur Verfügung.


| D3D11DeviceContext                  | ID3D12GraphicsCommand List     |
|-------------------------------------|--------------------------------|
| ClearDepthStencilView               | ClearDepthStencilView          |
| ClearRenderTargetView               | ClearRenderTargetView          |
| ClearUnorderedAccess*               | ClearUnorderedAccess*          |
| Draw, DrawInstanced                 | DrawInstanced                  |
| DrawIndexed, DrawIndexedInstanced   | DrawIndexedInstanced           |
| Dispatch                            | Dispatch                       |
| IASetInputLayout, xxSetShader usw. | SetPipelineState               |
| OMSetBlendState                     | OMSetBlendFactor               |
| OMSetDepthStencilState              | OMSetStencilRef                |
| OMSetRenderTargets                  | OMSetRenderTargets             |
| RSSetViewports                      | RSSetViewports                 |
| RSSetScissorRects                   | RSSetScissorRects              |
| IASetPrimitiveTopology              | IASetPrimitiveTopology         |
| IASetVertexBuffers                  | IASetVertexBuffers             |
| IASetIndexBuffer                    | IASetIndexBuffer               |
| ResolveSubresource                  | ResolveSubresource             |
| CopySubresourceRegion               | CopyBufferRegion               |
| UpdateSubresource                   | CopyTextureRegion              |
| CopyResource                        | CopyResource                   |

> [!NOTE]
> Eine befehlsliste, die mit **D3D12_COMMAND_LIST_TYPE_BUNDLE** erstellt wurde, ist mit einem verzögerten Kontext gleichgestellt. Direct3D 12 unterstützt auch die Abiilty für den Zugriff  auf einige Features  eines unmittelbaren Kontexts gleichzeitig mit dem Rendering über D3D12_COMMAND_LIST_TYPE_COPY und D3D12_COMMAND_LIST_TYPE_COMPUTE Befehlslistentypen. 

## <a name="cpugpu-synchronization"></a>CPU-/GPU-Synchronisierung

In Direct3D 11 war die CPU/GPU-Synchronisierung größtenteils automatisch, und es war nicht erforderlich, dass die App den Status des physischen Speichers aufrechtern.

In Direct3D 12 muss die App die beiden Zeitachsen (CPU und GPU) explizit verwalten. Dies erfordert, dass Informationen von der App verwaltet werden müssen, welche Ressourcen für die GPU erforderlich sind und wie lange sie benötigt werden. Dies bedeutet auch, dass die App dafür verantwortlich ist, sicherzustellen, dass sich der Inhalt von Ressourcen (z. B. Ressourcen, Heaps, Befehlszuweisungen) nicht ändert, bis die GPU sie nicht mehr verwendet.

Das Hauptobjekt zum Synchronisieren der Zeitachsen ist das [**ID3D12Fence-Objekt.**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) Der Betrieb von Fences ist recht einfach, und die GPU kann signalisieren, wenn sie eine Aufgabe abgeschlossen hat. Sowohl die GPU als auch die CPU können signalisieren, und beide können auf Fences warten.

In der Regel wird beim Übermitteln einer Befehlsliste zur Ausführung ein Fence-Signal von der GPU bei Abschluss (wenn das Lesen der Daten abgeschlossen ist) übertragen, sodass die CPU die Ressourcen wiederverwenden oder zerstören kann.

In Direct3D 11 behandelte das [**ID3D11DeviceContext::Map-Flag**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map) D3D11 MAP WRITE DISCARD im Wesentlichen jede Ressource als endlose Speicherquelle, in die die App schreiben kann (ein Prozess, der \_ \_ als \_ "Umbenennen" bezeichnet wird). In Direct3D 12 ist der Prozess explizit: Zusätzlicher Arbeitsspeicher muss zugewiesen werden, und fences sollten zum Synchronisieren der Vorgänge verwendet werden. Ringpuffer (bestehend aus großen Puffern) können dafür eine gute Methode sein. Weitere Informationen finden Sie im Ringpufferszenario unter [Fence-Based Resource Management](fence-based-resource-management.md).

![Verwenden eines Ringpuffers](images/ring-buffer-1.png)

## <a name="resource-binding"></a>Ressourcenbindung

Ansichten in Direct3D 11 (Shaderressourcenansichten, Renderzielansichten und so weiter) wurden in Direct3D 12 größtenteils durch das Konzept eines Deskriptors ersetzt. Die Erstellungsmethoden sind weiterhin in Direct3D 12 vorhanden (z. B. [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview) und [**CreateRenderTargetView),**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)die aufgerufen werden, nachdem der Deskriptorhap erstellt wurde, um die Daten in den Heap zu schreiben. Die Bindung in Direct3D 12 wird jetzt von Deskriptorhandles verarbeitet, die in einer Stammsignatur beschrieben sind, und mithilfe der [**Methoden SetGraphicsRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) oder [**SetComputeRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) übermittelt.

Stammsignaturen enthalten Zuordnungen zwischen der Nummer des Stammsignaturslots und den Deskriptortabellen, wobei die Deskriptortabelle Verweise auf Ressourcen enthalten kann, die für Vertex-Shader, Pixel-Shader und die anderen Shader verfügbar sind, z. B. konstante Puffer, Shaderressourcenansichten und Sampler. Diese Flexibilität trennt den HLSL-Registerbereich vom API-Bindungsraum in Direct3D 12, im Gegensatz zu Direct3D 11, bei dem eine 1:1-Zuordnung zwischen diesen besteht.

Eine der Auswirkungen dieses Systems ist, dass die App für das Umbenennen von Deskriptortabellen verantwortlich ist, wodurch Entwickler die Leistungskosten verstehen können, die sich durch das Ändern eines einzelnen Deskriptors pro Zeichnen-Aufruf ergeben.

Ein neues Feature von Direct3D 12 ist, dass eine App steuern kann, welche Deskriptoren von welchen Shaderstufen gemeinsam genutzt werden. In Direct3D 11 werden Ressourcen wie UAVs von allen Shaderstufen gemeinsam genutzt. Indem Deskriptoren für bestimmte Shaderstufen deaktiviert werden können, können die register, die von deaktivierten Deskriptoren verwendet werden, von Deskriptoren verwendet werden, die für eine bestimmte Shaderphase aktiviert sind.

Die folgende Tabelle zeigt eine Beispielstammsignatur.



| Stammparameterslot | Deskriptortabelleneintrag         |
|---------------------|--------------------------------|
| 0                   | VS-Deskriptorbereich b0-b13     |
| 1                   | VS-Deskriptorbereich t0-t127    |
| 2                   | VS-Deskriptorbereich s0-s16     |
| 3                   | PS-Deskriptorbereich b0-b13     |
| ...                 |                                |
| 14                  | DS-Deskriptorbereich s0-16      |
| 15                  | Freigegebener Deskriptorbereich u0-u63 |



 

## <a name="resource-state"></a>Ressourcenzustand

In Direct3D 11 wird der Ressourcenstatus nicht von der App, sondern vom Treiber verwaltet.

In Direct3D 12 liegt die Verwaltung des Ressourcenzustands in der Verantwortung der App, um vollständige Parallelität bei der Aufzeichnung von Befehlslisten zu ermöglichen: Die App muss die Aufzeichnungszeitachsen für Befehlslisten (die parallel erfolgen können) und die Ausführungszeitpläne verarbeiten, die sequenziell sein müssen.

Ein Ressourcenzustandsübergang wird von der [**ResourceBarrier-Methode**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) verarbeitet. In erster Linie muss die App den Treiber informieren, wenn sich die Ressourcennutzung ändert. Wenn beispielsweise eine Ressource als Renderziel verwendet wird und dann beim nächsten Zeichnen-Aufruf als Eingabe für einen Vertex-Shader verwendet werden soll, ist möglicherweise eine kurze Pause im GPU-Vorgang erforderlich, um den Renderzielvorgang vor dem Behandeln des Vertex-Shaders abschließen zu können.

Dieses System ermöglicht eine fein abgrenzende Synchronisierung (die GPU wird nicht mehr ausgeführt) der Grafikpipeline sowie Cache-Leerungen und möglicherweise einige Änderungen am Speicherlayout (z. B. Renderzielansicht bis Dekomprimierung der Tiefen-Schablonenansicht).

Dies wird als Übergangsbarriere bezeichnet. Es gibt andere Arten von Barrieren: In Direct3D 11 ermöglichte [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) die Verwendung desselben physischen Speichers durch zwei verschiedene gekachelte Ressourcen. In Direct3D 12 wird dies als "Aliasingbarriere" bezeichnet. Aliasingbarrieren können sowohl für gekachelte als auch für platzierte Ressourcen in Direct3D 12 verwendet werden. Darüber hinaus gibt es die UAV-Barriere. In Direct3D 11 müssen alle UAV-Dispatch- und Draw-Vorgänge serialisiert werden, obwohl diese Vorgänge parallel ausgeführt werden können. Für Direct3D 12 wird diese Einschränkung durch das Addition einer UAV-Barriere entfernt. Eine UAV-Barriere stellt sicher, dass UAV-Vorgänge sequenziell sind. Wenn also ein zweiter Vorgang erfordert, dass der erste abgeschlossen ist, wird der zweite durch das Addition der Barriere gezwungen, zu warten. Der Standardvorgang für UAVs ist einfach, dass die Vorgänge so schnell wie möglich fortgesetzt werden.

Es gibt natürlich Leistungssteigerungen, wenn eine Workload parallelisiert werden kann.

## <a name="swapchains"></a>Swapchains

Die DXGI-Swapkette ist die Grundlage für Austauschketten in Direct3D 11 und 12. Es gibt einige geringfügige Unterschiede: In Direct3D 11 sind die drei Typen der Swapkette SEQUENTIAL, DISCARD und FLIP \_ SEQUENTIAL. Für Direct3D 12 gibt es nur zwei Typen: FLIP \_ SEQUENTIAL und FLIP \_ DISCARD. Wie bereits erwähnt, sollten Sie Ihre Swapchain explizit über **IDXGIFactory4** oder höher erstellen und dieselbe Schnittstelle für jede Adapterenumeration verwenden.

In Direct3D 11 gibt es eine automatische Backbufferrotation: Für den Backpuffer 0 ist nur eine Renderzielansicht erforderlich. In Direct3D 12 ist die Pufferrotation explizit, es muss eine Renderzielansicht für jeden Backpuffer geben. Verwenden Sie [**die IDXGISwapChain3::GetCurrentBackBufferIndex-Methode, um auszuwählen, in welcher IdXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) gerendert werden soll. Auch hier ermöglicht diese zusätzliche Flexibilität eine größere Parallelisierung.

> [!NOTE]
> Es gibt zwar zahlreiche Möglichkeiten zum Einrichten Ihrer Anwendung, aber anwendungen verfügen in der Regel über einen **ID3D12CommandAllocator** pro Swap-Chain-Puffer. Dadurch kann die Anwendung mit dem Erstellen einer Reihe von Befehlen für den nächsten Frame fortfahren, während die GPU den vorherigen rendert.

## <a name="fixed-function-rendering"></a>Funktionsrendering korrigiert

In Direct3D 11 gab es einige Methoden, die verschiedene Vorgänge auf höherer Ebene vereinfachten, z. B. [**GenerateMips**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips) (Erstellen vollständiger MIP-Ketten) und [**DrawAuto**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto) (Verwendung der Streamausgabe als Shadereingabe ohne weitere Eingabe von der App). Diese Methoden sind in Direct3D 12 nicht verfügbar. Die App muss diese Vorgänge verarbeiten, indem shaders erstellt werden, um sie durchzuführen.

## <a name="odds-and-ends"></a>Wahrscheinlichkeit und Ende

Die folgende Tabelle zeigt eine Reihe von Features, die zwischen Direct3D 11 und 12 ähnlich sind, aber nicht identisch sind.



| Direct3D 11                                                                            | Direct3D 12                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Query**](/windows/win32/api/d3d11/nn-d3d11-id3d11query)                                              | [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) ermöglicht das Gruppen von Abfragen, wodurch die Kosten reduziert werden.                                                                                                                                                                                                                                                                                                                                     |
| [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate)                                      | Prädication wird jetzt aktiviert, indem Daten in einem vollständig transparenten Puffer gespeichert werden. Das Direct3D 11 [**ID3D11Predicate-Objekt**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate) wird durch [**ID3D12Resource::Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)ersetzt, das einem Aufruf von [**ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) und einem GPU-Synchronisierungsvorgang folgen muss, der einen Fence verwendet, um zu warten, bis die Daten bereit sind. Weitere Informationen finden [Sie unter Prädication](predication.md). |
| Ausgeblendeter UAV/SO-Indikator                                                                  | Die App ist für die Zuordnung und Verwaltung von SO/UAV-Leistungsindikatoren verantwortlich. Weitere Informationen finden [Sie unter Streamausgabeindikatoren](stream-output-counters.md) und [UAV-Leistungsindikatoren.](uav-counters.md)                                                                                                                                                                                                                                                             |
| Dynamische MinLOD-Ressourcen (Miniumebene der Details)                                       | Diese wurde in den statischen SRV-Deskriptor MinLOD verschoben.                                                                                                                                                                                                                                                                                                                                                                                 |
| Draw \* [**Indirect/DispatchIndirect**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-dispatchindirect) | Das Zeichnen indirekter Methoden wird alle mit der [**executeIndirect-Methode**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) zusammengeführt.                                                                                                                                                                                                                                                                                                        |
| Tiefenschnappungsformate sind übereinander gewebt.                                                   | DepthStencil-Formate sind planar. Beispielsweise würde ein Format von 24 Bits tiefe 8 Bits schablone im Format 24/8/24/8 gespeichert werden... etc in Direct3D 11, aber als 24/24/24... gefolgt von 8/8/8... in Direct3D 12. Beachten Sie, dass jede Ebene eine eigene Unterressource in D3D12 ist (siehe [Unterressourcen](subresources.md)).                                                                                                                    |
| [**ResizeTilePool**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)                   | Reservierte Ressourcen können mehreren Heaps zugeordnet werden. Wenn ein Kachelpool in D3D11 größer geworden wäre, kann stattdessen ein zusätzlicher Heap in D3D12 zugeordnet werden.                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videotutorials für erweitertes Lernen mit DirectX: Leitfaden zur Portierung von DirectX 11 zu DirectX 12](https://www.youtube.com/watch?v=BV64mdOCgZo)
</dt> <dt>

[Grundlegendes zu Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Arbeiten mit Direct3D 11, Direct3D 10 und Direct2D](direct3d-12-interop.md)
</dt> </dl>
