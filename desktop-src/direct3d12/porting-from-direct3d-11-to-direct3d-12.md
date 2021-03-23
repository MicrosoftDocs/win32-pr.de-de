---
title: Portieren von Direct3D 11 zu Direct3D 12
description: Dieser Abschnitt enthält eine Anleitung zum Portieren von einer benutzerdefinierten Direct3D 11-Grafik-Engine zu Direct3D 12.
ms.assetid: 9EB4AC6B-AFDD-4673-8EB3-54272C151784
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b5bc6784d6f96c3c1599a601a57bf68b0d612d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548726"
---
# <a name="porting-from-direct3d-11-to-direct3d-12"></a>Portieren von Direct3D 11 zu Direct3D 12

Dieser Abschnitt enthält eine Anleitung zum Portieren von einer benutzerdefinierten Direct3D 11-Grafik-Engine zu Direct3D 12.

-   [Geräte Erstellung](#device-creation)
-   [Zugesicherte Ressourcen](#committed-resources)
-   [Reservierte Ressourcen](#reserved-resources)
-   [Hochladen von Daten](#uploading-data)
-   [Shaders und Shader-Objekte](#shaders-and-shader-objects)
-   [Übermitteln von Arbeit an die GPU](#submitting-work-to-the-gpu)
-   [CPU/GPU-Synchronisierung](#cpugpu-synchronization)
-   [Ressourcen Bindung](#resource-binding)
-   [Ressourcenzustand](#resource-state)
-   [SwapChain](#swapchains)
-   [Festes Funktions Rendering](#fixed-function-rendering)
-   [Quoten und Ende](#odds-and-ends)
-   [Verwandte Themen](#related-topics)

## <a name="device-creation"></a>Geräte Erstellung

Sowohl Direct3D 11 als auch Direct3D 12 nutzen ein ähnlich-Geräte Erstellungs Muster gemeinsam. Vorhandene Direct3D 12-Treiber sind alle **D3D_FEATURE_LEVEL_11_0** oder besser, sodass Sie die älteren featureebenen und zugeordneten lmittierungen ignorieren können.

Beachten Sie auch, dass Sie mit Direct3D 12 Geräteinformationen mithilfe von DXGI-Schnittstellen explizit auflisten sollten. In Direct3D 11 konnten Sie vom Direct3D-Gerät zurück zum DXGI-Gerät *zurück verketten* , und dies wird für Direct3D 12 nicht unterstützt.

Das Erstellen eines Warp-Software Geräts auf Direct3D 12 erfolgt durch Bereitstellen eines expliziten Adapters, der von **IDXGIFcatory4:: enumwarpadapter** abgerufen wird. Das Warp-Gerät für Direct3D 12 ist nur auf Systemen verfügbar, für die das optionale Feature " **Graphics Tools** " aktiviert ist.

> [!NOTE]
> Es gibt keine Entsprechung zu **D3D11CreateDeviceAndSwapChain**. Selbst bei Direct3D 11 wird die Verwendung dieser Funktion davon abgeraten, da es häufig besser ist, das Gerät und vorhandenes SwapChain in verschiedenen Schritten zu erstellen.

## <a name="committed-resources"></a>Zugesicherte Ressourcen

Objekte, die mit den folgenden Schnittstellen in Direct3D 11 erstellt werden, werden in Direct3D 12 in den Namen "zugesicherte Ressourcen" übersetzt. Eine zugeordnete Ressource ist eine Ressource, der sowohl ein virtueller Adressraum als auch physische Seiten zugeordnet sind. Dabei handelt es sich um ein Konzept des Microsoft Windows-Gerätetreibers 2 (WDD2)-Speicher Modells, auf dem Direct3D 12 basiert.

Direct3D 11 Ressourcen:

-   [**ID3D11Resource**](/windows/win32/api/d3d11/nn-d3d11-id3d11resource)
-   [**ID3D11Buffer**](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) und [ **ID3D11Device:: up Buffer**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createbuffer)
-   [**ID3D11Texture1D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture1d) und [ **ID3D11Device: CreateTexture1D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture1d)
-   [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) und [ **ID3D11Device:: CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d)
-   [**ID3D11Texture3D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture3d) und [ **ID3D11Device:: CreateTexture3D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture3d)

In Direct3D 12 werden diese alle durch [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) und [**ID3D12Device:: kreatecommittedresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)dargestellt.

## <a name="reserved-resources"></a>Reservierte Ressourcen

Reservierte Ressourcen sind Ressourcen, bei denen nur virtueller Adressraum zugewiesen wurde. der physische Arbeitsspeicher wird erst zugewiesen, wenn [**ID3D12Device:: createheap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)aufgerufen wird. Dabei handelt es sich im Wesentlichen um das gleiche Konzept wie die Kachel Ressourcen in Direct3D 11.

Die Flags ([**D3D11 \_ Resource \_ misc- \_ Flag**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)), die in Direct3D 11 zum Einrichten von gekachelten Ressourcen verwendet werden, und ordnen Sie Sie dann dem physischen Speicher zu.

-   D3D11 \_ \_ ressourcenmisc \_ gekachelt
-   D3D11 \_ \_ ressourcenmisc- \_ Kachel \_ Pool

## <a name="uploading-data"></a>Hochladen von Daten

In Direct3D 11 gibt es die Darstellung einer einzelnen Zeitachse (Aufrufe nach einer Sequenz, z. b. Daten, die mit [**D3D11 \_ subresource- \_ Daten**](/windows/win32/api/d3d11/ns-d3d11-d3d11_subresource_data)initialisiert werden. Anschließend wird ein Aufruf an [**Verknüpfung id3d11devicecontext aus:: updatesubresource**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource)und dann an [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)) durchgeführt. Die Anzahl der Kopien, die von den Daten erstellt werden, ist für einen Direct3D 11-Entwickler nicht offensichtlich.

In Direct3D 12 gibt es zwei Zeitachsen: die GPU-Zeitachse (durch Aufrufe an [**copytextureregion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)und [**copybufferregion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) aus dem mappable-Speicher eingerichtet) und die CPU-Zeitachse (durch Aufrufe von [**map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)festgelegt). Hilfsfunktionen werden (in der Datei d3dx12. h) als [**updatesubresources**](updatesubresources1.md) bereitgestellt, die eine freigegebene Zeitachse verwenden. Es gibt mehrere Variationen dieser Hilfsfunktion, die einen verwendet, der [**ID3D12Device:: getcopyablefootprints**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)verwendet, einen weiteren, der einen Heap Zuweisungs Mechanismus verwendet, und einen weiteren, der einen Mechanismus zur Stapel Zuweisung verwendet. Diese Hilfsfunktionen kopieren Ressourcen über einen Stagingbereich des Arbeitsspeichers sowohl auf GPU als auch auf CPU.

In der Regel verfügen die GPU und die CPU jeweils über eine eigene Kopie einer Ressource, die mit ihrer eigenen Zeitachse verknüpft ist. Der Ansatz der freigegebenen Zeitachse verwaltet auf ähnliche Weise zwei Kopien

## <a name="shaders-and-shader-objects"></a>Shaders und Shader-Objekte

In Direct3D 11 gibt es eine große Anzahl von Shader-und State-Objekten sowie das Festlegen des Status dieser Objekte mithilfe der [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) -Erstellungs Methoden und der [**Verknüpfung id3d11devicecontext aus**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) Set-Methoden. In der Regel wird eine große Anzahl von Aufrufen an diese Methoden durchgeführt, die dann zur zeichnungszeit vom Treiber kombiniert werden, um den korrekten Pipeline Status festzulegen.

In Direct3D 12 wurde diese Einstellung des Pipeline Status zu einem einzelnen Objekt ("" erstellt "" " [**" für eine COMPUTE-Engine**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) "" und "[**" für eine**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) Grafik-Engine "" mit einer Befehlsliste verknüpft), das dann vor dem Zeichnen-Befehl mit einem Aufrufen von " [**setpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)" an eine Befehlsliste angehängt wird.

Diese Aufrufe ersetzen alle einzelnen Aufrufe von "Set Shaders", "Input Layout", "Blend State", "Raster State", "tiefen Schablone State" usw. in Direct3D 11.

- Device 11-Methoden: ``CreateInputLayout`` , ``CreateXShader`` , ``CreateDepthStencilState`` , andd ``CreateRasterizerState`` .
- Gerätekontext 11-Methoden:  ``IASetInputLayout`` , ``xxSetShader`` , ``OMSetBlendState`` , ``OMSetDepthStencilState`` und ``RSSetState`` .

Obwohl Direct3D 12 ältere kompilierte Shader-BLOB unterstützen kann, sollten Shader entweder mit dem Shader-Modell 5,1 mit den FXC/D3DCompile-APIs oder mit dem dxil DXC-Compiler mithilfe von Shader Model 6 erstellt werden. Sie sollten die Unterstützung von Shadermodell 6 mit [**checkfeaturesupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) und **D3D12_FEATURE_SHADER_MODEL** überprüfen.

## <a name="submitting-work-to-the-gpu"></a>Übermitteln von Arbeit an die GPU

in Direct3D 11 gibt es nur wenig Kontrolle darüber, wie die Arbeit übermittelt wird, Sie wird größtenteils vom Treiber verarbeitet, obwohl ein Steuerelement über die [**Verknüpfung id3d11devicecontext aus:: Flush**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-flush) -und [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) -Aufrufe aktiviert wird.

In Direct3D 12 ist die Arbeits Übermittlung sehr explizit und wird von der APP gesteuert. Das primäre Konstrukt für das Übermitteln von Arbeit ist [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist), das verwendet wird, um alle App-Befehle aufzuzeichnen (und ist dem Konzept des ID3D11 verzögerten Kontexts recht ähnlich). Der Sicherungs Speicher für eine Befehlsliste wird von [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)bereitgestellt, wodurch die APP die Arbeitsspeicher Nutzung der Befehlsliste verwalten kann, indem Sie tatsächlich den Arbeitsspeicher verfügbar macht, der vom Direct3D 12-Treiber zum Speichern der Befehlsliste verwendet wird.

Schließlich ist [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) eine First-in-First-Out-Warteschlange, in der die richtige Reihenfolge der Befehlslisten für die Übermittlung an die GPU gespeichert wird. Nur wenn die Ausführung einer Befehlsliste auf der GPU abgeschlossen ist, wird die nächste Befehlsliste aus der Warteschlange vom Treiber gesendet.

In Direct3D 11 gibt es kein explizites Konzept einer Befehls Warteschlange. Bei der allgemeinen Einrichtung für Direct3D 12 kann die aktuell geöffnete **D3D12_COMMAND_LIST_TYPE_DIRECT** Befehlsliste für den aktuellen Frame als analog zum unmittelbaren Kontext Direct3D 11 betrachtet werden. Dies stellt viele der gleichen Funktionen bereit.


| D3D11DeviceContext                  | ID3D12GraphicsCommand-Liste     |
|-------------------------------------|--------------------------------|
| ClearDepthStencilView               | ClearDepthStencilView          |
| ClearRenderTargetView               | ClearRenderTargetView          |
| Clearunorderedaccess *               | Clearunorderedaccess *          |
| Zeichnen, drawinstanzierte                 | Drawinstanzierte                  |
| Drawindebug, drawindexedinstanzierte   | Drawindexedinstangeleitet           |
| Dispatch                            | Dispatch                       |
| Iasetinputlayout, xxsetshader usw. | Setpipelinestate               |
| Omsetblendstate                     | Omsetblendfactor               |
| Omsetdepthstencilstate              | Omsetstencilref                |
| Omantrendertargets                  | Omantrendertargets             |
| Rssetviewports                      | Rssetviewports                 |
| Rssezcissorrects                   | Rssezcissorrects              |
| Iasetprimitivetopology              | Iasetprimitivetopology         |
| Iasetvertexbuffers                  | Iasetvertexbuffers             |
| Iasetindexbuffer                    | Iasetindexbuffer               |
| Resolvesubresource                  | Resolvesubresource             |
| Copysubresourceregion               | Copybufferregion               |
| Updatesubresource                   | Copytextureregion              |
| Copyresource                        | Copyresource                   |

> [!NOTE]
> Eine Befehlsliste, die mit **D3D12_COMMAND_LIST_TYPE_BUNDLE** erstellt wurde, ist für einen verzögerten Kontext ähnlich. Direct3D 12 unterstützt auch die Unterstützung für den Zugriff auf einige Features eines *unmittelbaren Kontexts* , gleichzeitig über **D3D12_COMMAND_LIST_TYPE_COPY** und **D3D12_COMMAND_LIST_TYPE_COMPUTE** Befehlslisten Typen.

## <a name="cpugpu-synchronization"></a>CPU/GPU-Synchronisierung

In Direct3D 11 war die CPU/GPU-Synchronisierung größtenteils automatisch, und es war nicht erforderlich, dass die APP den Status des physischen Speichers beibehält.

in Direct3D 12 muss die APP die beiden Zeitachsen (CPU und GPU) explizit verwalten. Dies erfordert, dass Informationen von der APP verwaltet werden müssen, welche Ressourcen von der GPU benötigt werden und wie lange es dauert. Dies bedeutet auch, dass die App dafür verantwortlich ist, den Inhalt von Ressourcen (z. b. zugesicherte Ressourcen, Heaps, Befehls Zuweisungen) nicht zu ändern, bis Sie von der GPU nicht mehr verwendet werden.

Das Hauptobjekt für die Synchronisierung der Zeitachsen ist das [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) -Objekt. Der Vorgang von Zäunen ist failry Simple und ermöglicht der GPU das Signal, wenn eine Aufgabe abgeschlossen wurde. Die GPU und CPU können beide signalisieren und können auf Zäune warten.

In der Regel besteht der Ansatz darin, dass beim Übermitteln einer Befehlsliste für die Ausführung ein Fence Signal bei Abschluss (wenn das Lesen der Daten abgeschlossen ist) von der GPU übertragen wird, sodass die CPU die Ressourcen wieder verwenden oder zerstören kann.

In Direct3D 11 hat das [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map) -Flag D3D11 \_ map \_ Write \_ verwerfen jede Ressource als unendliche Speichermenge behandelt, in die die app schreiben konnte (ein Prozess, der als "umbenennen" bezeichnet wird). In Direct3D 12 ist der Prozess explizit: zusätzlicher Arbeitsspeicher muss zugewiesen werden, und die Verwendung von Zäunen sollte zum Synchronisieren der Vorgänge verwendet werden. Ringpuffer (bestehend aus großen Puffern) können hierfür eine gute Methode sein. Weitere Informationen finden Sie im Ringpuffer Szenario in der [Fence-basierten Ressourcenverwaltung](fence-based-resource-management.md).

![Verwenden eines Ring Puffers](images/ring-buffer-1.png)

## <a name="resource-binding"></a>Ressourcen Bindung

Sichten in Direct3D 11 (Shader-Ressourcen Sichten, renderzielsichten usw.) wurden größtenteils in Direct3D 12 durch das Konzept eines Deskriptors ersetzt. Die Erstellungs Methoden sind immer noch in Direct3D 12 vorhanden (z. b. " [**kreateshaderresourceview**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview) " und " [**kreaterendertargetview**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)"), die nach der Erstellung des deskriptorheaps aufgerufen werden, um die Daten in den Heap zu schreiben. Die Bindung in Direct3D 12 wird jetzt von Deskriptorhandles behandelt, die in einer Stamm Signatur beschrieben und mithilfe der [**setgraphicsrootdescriptortable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) -Methode oder der [**setcomputerootdescriptortable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) -Methode gesendet werden.

Stamm Signaturen enthalten Details zu den Zuordnungen zwischen der Stamm Signatur Slot-Nummer und den deskriptortabellen, wobei die Deskriptortabelle Verweise auf Ressourcen enthalten kann, die für Vertex-Shader, Pixel-Shader und andere Shader verfügbar sind, wie z. b. Konstante Puffer, shaderressourcensichten und Samplers. Durch diese Flexibilität wird der HLSL-Register Bereich vom API-Bindungs Bereich in Direct3D 12 getrennt, anders als bei Direct3D 11, bei dem zwischen diesen eine Zuordnung besteht.

Eine der Implikationen dieses Systems besteht darin, dass die APP für das Umbenennen von deskriptortabellen zuständig ist. Dadurch können Entwickler die Leistungseinbußen bei der Änderung eines einzelnen Deskriptors pro zeichnen-Befehl verstehen.

Ein neues Feature von Direct3D 12 ist, dass eine App steuern kann, welche Deskriptoren zwischen den Shader-Stufen gemeinsam verwendet werden. In Direct3D 11 werden Ressourcen wie UAVs von allen Shader-Stufen gemeinsam genutzt. Wenn die Deskriptoren für bestimmte Shader-Stufen deaktiviert werden, können die von Deskriptoren verwendeten Register von Deskriptoren verwendet werden, die für eine bestimmte Shader-Stufe aktiviert sind.

In der folgenden Tabelle wird ein Beispiel für eine Stamm Signatur angezeigt.



| Stammparameterslot | Deskriptortabelleneintrag         |
|---------------------|--------------------------------|
| 0                   | VS-Deskriptorbereich B0-B13     |
| 1                   | VS-Deskriptorbereich T0-T127    |
| 2                   | VS-Deskriptorbereich S0-S16     |
| 3                   | PS-Deskriptorbereich B0-B13     |
| ...                 |                                |
| 14                  | DS-Deskriptorbereich S0-16      |
| 15                  | Frei gegebener Deskriptorbereich U0-u63 |



 

## <a name="resource-state"></a>Ressourcenzustand

In Direct3D 11 wird der Ressourcen Status nicht von der APP, sondern vom Treiber verwaltet.

In Direct3D 12 wird die Verwaltung des Ressourcen Zustands in die Zuständigkeit der APP versetzt, um die vollständige Parallelität bei der Aufzeichnung von Befehlslisten zu aktivieren: die APP muss die Aufzeichnungs Zeilenlinien für Befehlslisten verarbeiten (was parallel erfolgen kann) und die Ausführungszeit Achsen, die sequenziell sein müssen.

Ein Ressourcen Zustandsübergang wird von der [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) -Methode behandelt. Hauptsächlich muss die APP den Treiber informieren, wenn sich die Ressourcennutzung ändert. Wenn z. b. eine Ressource als Renderziel verwendet wird und Sie als Eingabe für einen Vertex-Shader beim nächsten zeichnen-Befehl verwendet werden soll, erfordert dies möglicherweise einen kurzen Stall beim GPU-Vorgang, um den Renderziel-Vorgang abzuschließen, bevor der Vertex-Shader verarbeitet wird.

Dieses System ermöglicht eine fein Komprimierung (die GPU-Ställe) der Grafik Pipeline sowie Cache Leerungen und möglicherweise einige Änderungen am Speicher Layout (z. b. renderzielansicht zur Dekomprimierung der tiefen Schablone).

Dies wird als Übergangs Barriere bezeichnet. Es gibt andere Arten von Barrieren Direct3D 11 [**ID3D11DeviceContext2:: tiledresourcebarrier**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) aktivierte den gleichen physischen Speicher, der von zwei verschiedenen gekachelten Ressourcen verwendet werden kann. In Direct3D 12 wird dies als "Aliasing Barriere" bezeichnet. Aliasing-Barrieren können für gekachelte und platzierte Ressourcen in Direct3D 12 verwendet werden. Außerdem gibt es die UAV-Barriere. In Direct3D 11 müssen alle UAV-dispatchvorgänge und Draw-Vorgänge serialisiert werden, auch wenn diese Vorgänge Pipelines oder parallel funktionieren können. Für Direct3D 12 wird diese Einschränkung durch das Hinzufügen einer UAV-Barriere entfernt. Eine UAV-Barriere stellt sicher, dass UAV-Vorgänge sequenziell sind. Wenn also für einen zweiten Vorgang der erste Vorgang erforderlich ist, wird der zweite Vorgang gezwungen, beim Hinzufügen der Barriere zu warten. Der Standard Vorgang für UAVs ist, dass die Vorgänge so schnell wie möglich fortgesetzt werden.

Wenn eine Arbeitsauslastung parallelisiert werden kann, gibt es eindeutig Leistungssteigerungen.

## <a name="swapchains"></a>SwapChain

Die DXGI-Swapkette ist die Grundlage für Swapketten in Direct3D 11 und 12. Es gibt einige geringfügige Unterschiede. in Direct3D 11 sind die drei Arten der SwapChain sequenziell, verwerfen und \_ sequenziell. Für Direct3D 12 gibt es nur zwei Typen: " \_ sequenziell" und "kippen \_ verwerfen". Wie bereits erwähnt, sollten Sie die vorhandenes SwapChain explizit über **IDXGIFactory4** oder höher erstellen und die gleiche Schnittstelle für jede adapterenumeration verwenden.

In Direct3D 11 gibt es eine automatische Swapkette-Rotation: nur eine renderzielansicht wird für den Hintergrund Puffer 0 benötigt. In Direct3D 12 ist die Puffer Drehung explizit, es muss für jeden Hintergrund Puffer eine renderzielansicht vorhanden sein. Verwenden Sie die [**IDXGISwapChain3:: getcurrentbackbufferindex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) -Methode, um auszuwählen, in welcher Sie dargestellt werden soll. Diese zusätzliche Flexibilität ermöglicht wiederum eine größere Parallelisierung.

> [!NOTE]
> Es gibt zwar viele Möglichkeiten zum Einrichten Ihrer Anwendung, aber in der Regel verfügen Anwendungen über einen **ID3D12CommandAllocator** pro SwapChain-Puffer. Dadurch kann die Anwendung mit dem Aufbau eines Satzes von Befehlen für den nächsten Frame fortfahren, während die GPU die vorherige rendert.

## <a name="fixed-function-rendering"></a>Festes Funktions Rendering

In Direct3D 11 gab es einige Methoden, die verschiedene Vorgänge auf höherer Ebene vereinfachen, wie z. b. [**generatemips**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips) (Erstellen vollständiger MIP-Ketten) und [**drawauto**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto) (unter Verwendung der Streamausgabe als Shadereingabe ohne weitere Eingabe aus der APP). Diese Methoden sind in Direct3D 12 nicht verfügbar. die APP muss diese Vorgänge durch Erstellen von Shadern durchführen, um Sie auszuführen.

## <a name="odds-and-ends"></a>Quoten und Ende

Die folgende Tabelle zeigt eine Reihe von Features, die in Direct3D 11 und 12 ähnlich sind, aber nicht identisch sind.



| Direct3D 11                                                                            | Direct3D 12                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Query**](/windows/win32/api/d3d11/nn-d3d11-id3d11query)                                              | [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) ermöglicht das Gruppieren von Abfragen, wodurch die Kosten gesenkt werden.                                                                                                                                                                                                                                                                                                                                     |
| [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate)                                      | Das Prädikat wird jetzt aktiviert, indem Daten in einem voll transparenten Puffer vorhanden sind. Das Direct3D 11 [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate) -Objekt wird durch [**ID3D12Resource:: Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)ersetzt, das einen aufzurufenden [**resolvequerydata**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) -Vorgang und einen GPU-Synchronisierungs Vorgang mit einem Fence ausführen muss, um darauf zu warten, dass die Daten bereit sind. Verweisen Sie auf das [Prädikat](predication.md). |
| UAV/so ausgeblendeter Counter                                                                  | Die APP ist für die Zuordnung und Verwaltung von sogenannten/UAV-Leistungsindikatoren verantwortlich. Weitere Informationen finden Sie unter Daten [Strom-ausgabezähler](stream-output-counters.md) und [UAV](uav-counters.md)-Indikatoren                                                                                                                                                                                                                                                             |
| Ressource Dynamic minlod (MINIUM Detailstufe)                                       | Diese wurde in die statische minlod für den SRV-Deskriptor verschoben.                                                                                                                                                                                                                                                                                                                                                                                 |
| \*Indirekt/[**dispatchindirekt** zeichnen](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-dispatchindirect) | Das Zeichnen indirekter Methoden wird alle in der einzelnen [**executeindirect**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) -Methode zusammengeführt.                                                                                                                                                                                                                                                                                                        |
| Die depthstencil-Formate sind verschachtelt.                                                   | Die depthstencil-Formate sind Planar. Beispielsweise wird ein Format von 24 Bits der Tiefe von 8 Bits der Schablone im Format 24/8/24/8... usw. in Direct3D 11, aber als 24/24/24... gefolgt von 8/8/8... in Direct3D 12. Beachten Sie, dass jede Ebene eine eigene untergeordnete Quelle in D3D12 ist (siehe unter [geordnete Quellen](subresources.md)).                                                                                                                    |
| [**Resizetilepool**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)                   | Reservierte Ressourcen können mehreren Heaps zugeordnet werden. Wenn ein Kachel Pool in D3D11 vergrößert wurde, kann in D3D12 stattdessen ein zusätzlicher Heap zugeordnet werden.                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Video Lernprogramme für DirectX 11 bis DirectX 12](https://www.youtube.com/watch?v=BV64mdOCgZo)
</dt> <dt>

[Grundlegendes zu Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Arbeiten mit Direct3D 11, Direct3D 10 und Direct2D](direct3d-12-interop.md)
</dt> </dl>