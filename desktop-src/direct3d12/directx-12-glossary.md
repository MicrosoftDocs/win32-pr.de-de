---
title: Direct3D 12 Glossar
description: Diese Begriffe sind von Direct3D 12 unterschiedlichen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a84b4b2e5a993b33b4c322b91682c8f9b5499bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548735"
---
# <a name="direct3d-12-glossary"></a>Direct3D 12 Glossar

Diese Begriffe sind von Direct3D 12 unterschiedlichen.

<dl> <dt>

<span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**lichere**
</dt> <dd>

Der Prozess des Anfügens von Speicher an die Grafik Pipeline. Die Ressourcen Bindung umfasst z. b. die Bindung einer Ressource, z. b. eine Textur an die Pipeline, die zum Rendern eines Objekts verwendet werden soll.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**ert**
</dt> <dd>

Ein D3D-Ressourcentyp, der mit einer zusammenhängenden Speicher Belegung Synonym ist.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**dels**
</dt> <dd>

Ein Befehls Puffer, der von der GPU (Graphics Processing Unit) nur direkt über eine *direkte Befehlsliste* ausgeführt werden kann. Ein Bundle erbt den gesamten GPU-Zustand (mit Ausnahme des aktuell festgelegten *Pipeline Zustands Objekts* und der primitiven Topologie).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**Befehls Zuweisung**
</dt> <dd>

Die zugrunde liegenden Speicher Belegungen, in denen GPU-Befehle gespeichert werden. Das Befehls zuordnerobjekt gilt sowohl für *direkte Befehlslisten* als auch für *Pakete*.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**Befehlsliste**
</dt> <dd>

Eine Befehlsliste entspricht einem Satz von Befehlen, die von der GPU ausgeführt werden. Dazu zählen Befehle wie z. b. das Festlegen von Status, zeichnen, löschen und kopieren. Die D3D12-Befehlslisten Schnittstelle unterscheidet sich deutlich von der-Schnittstelle der D3D11-Befehlsliste. Die D3D12-Befehlslisten Schnittstelle enthält ähnliche APIs wie die D3D11-Gerätekontext-Rendering-APIs.

In einer D3D12-Befehlsliste werden Ressourcen weder zugeordnet noch die Zuordnung aufgehoben, Kachel Zuordnungen geändert, die Größe der Kachel Pools geändert, Abfrage Daten erhalten oder es werden nie implizit Befehle zur Ausführung an die GPU übermittelt.

Anders als D3D11 verzögerte Kontexte unterstützen D3D12-Befehlslisten nur zwei Dereferenzierungsebenen. Eine *direkte Befehlsliste* entspricht einem Befehls Puffer, den die GPU ausführen kann. Ein *Bundle* kann nur direkt über eine direkte Befehlsliste ausgeführt werden.

Eine direkte Befehlsliste erbt keinen GPU-Zustand. Ein Bundle erbt den gesamten GPU-Zustand (mit Ausnahme des aktuell festgelegten Pipeline Zustands Objekts und der primitiven Topologie).

Der Arbeitsspeicher für eine Befehlsliste wird von der *Befehls Zuweisung* festgelegt. Der Zweck der Befehlslisten besteht darin, dass Sie als einzelne Renderinganforderung an eine GPU übermittelt werden können.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**Befehls Warteschlange**
</dt> <dd>

Eine *Befehls* Warteschlange, in der die GPU nacheinander ausgeführt wird. Anwendungen müssen *Befehlslisten* explizit zur Ausführung an eine Befehls Warteschlange übermitteln. In der Regel gibt es drei Befehls Warteschlangen: 3D-Grafiken, COMPUTE und Copy, die der 3D-Grafik Pipeline, der COMPUTE-Engine und einem oder mehreren Kopier Modulen auf der GPU entsprechen.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**konservative rasterisierung**
</dt> <dd>

Die konservative rasterisierung ist ein Betriebsmodus für die Raster-Phase der Direct3D-Grafik Pipeline. Dadurch wird die standardmäßige, auf Stichproben basierende rasterisierung deaktiviert, und stattdessen wird ein Pixel, das von einem beliebigen Betrag durch ein primitiv abgedeckt wird, rasteriert. Ein wichtiger Unterschied besteht darin, dass jede Abdeckung überhaupt ein rasterisiertes Pixel erzeugt, dass diese Abdeckung nicht durch die Hardware gekennzeichnet werden kann, sodass die Abdeckung immer Binär zu einem Pixelshader erscheint: entweder vollständig abgedeckt oder nicht abgedeckt. Es wird dem Pixelshader-Code überlassen, um die tatsächliche Abdeckung analytisch zu bestimmen.

Die konservative rasterisierung kann bei solchen Problemen hilfreich sein, z. b. bei der Kollision und Treffer Erkennung, bei der Klassifizierung und bei der Verschleierung, bei der die Farbe eines Pixels genauer ist, und die Kanten Fälle entfernt werden können. Siehe [konservative rasterization](conservative-rasterization.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Konstante Puffer Ansicht (CBV)**
</dt> <dd>

Konstante Puffer enthalten Shader-Konstante Daten, z. b. eine Kameraansicht, Projektions Matrizen und Welt Matrizen. Eine "Konstante Puffer Ansicht" ist die Format spezifische Ansicht des Puffers, wie von der Grafik Pipeline ersichtlich.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**Standard Heap**
</dt> <dd>

Ein Heap im Benutzermodus, der sich auf die Unterstützung von permanenten GPU-Ressourcentypen konzentriert, einschließlich von GPU-geschriebenen Ressourcen.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**Deskriptor**
</dt> <dd>

Deskriptoren sind die primäre Bindungs Einheit für eine einzelne Ressource in D3D12. Ein Deskriptor ist ein relativ kleiner Datenblock, in dem ein Objekt für die GPU vollständig in einem GPU-spezifischen Format beschrieben wird. Es gibt viele verschiedene Arten von Deskriptoren: Shader-Ressourcen Sichten (Srvs), unsorderte Zugriffs Sichten (UAVs), Konstante Puffer Ansichten (cbvs) und Samplers sind einige Beispiele.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**deskriptorheap**
</dt> <dd>

Ein deskriptorheap ist eine Auflistung zusammenhängender Belegungen von Deskriptoren, eine Zuordnung für jeden Deskriptor. Der primäre Punkt eines deskriptorheaps besteht darin, den größten Teil der Arbeitsspeicher Belegung zu umfassen, der zum Speichern der deskriptorspezifikationen von Objekttypen erforderlich ist, auf die sich Shader für einen großen Teil des Renderings als möglich (idealerweise ein ganzer Renderingbereich) beziehen.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**Deskriptortabelle**
</dt> <dd>

Eine Deskriptortabelle ist logisch ein Array von Deskriptoren. Jede Deskriptortabelle speichert Deskriptoren von einem oder mehreren Typen, einschließlich Srvs, uave, cbvs und Samplers. Eine Deskriptortabelle ist keine Speicher Belegung, sondern lediglich ein Offset und eine Länge in einem deskriptorheap.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**direkte Befehlsliste**
</dt> <dd>

Ein Befehls Puffer, der von der GPU ausgeführt werden kann. Eine direkte Befehlsliste erbt keinen GPU-Zustand.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**einzu**
</dt> <dd>

Ein Mechanismus zum Synchronisieren von GPU und CPU. Sowohl die GPU als auch die CPU können angewiesen werden, auf einen Fence zu warten, und es wird darauf gewartet, dass der andere Prozessor in Kraft ist. Siehe [Synchronisierung mit mehreren](./user-mode-heap-synchronization.md)Modulen.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**Gefährdung, Gefahren Verfolgung**
</dt> <dd>

Eine Gefahr tritt auf, wenn eine Ressource für einen Zweck verwendet wurde, und die APP beabsichtigt, Sie für einen anderen Zweck wiederzuverwenden. Um die Ressource erneut zu verwenden, müssen zwischengespeicherte Caches geleert oder ungültig gemacht werden. die Komprimierungs Anforderungen müssen mit der zweiten Verwendung konsistent sein, und die Ressource sollte sich im erforderlichen Zustand befinden, um das Lesen der Ressource zu vermeiden, nachdem Sie für den beabsichtigten Zweck geschrieben und für ungültig erklärt wurde.

Der Prozess der Wartung von Ressourcen und die Vermeidung dieser Synchronisierungs Probleme wird als Risiko Verfolgung bezeichnet. Wenn keine Gefahren Nachverfolgung durch den Treiber vorhanden ist, ist die App dafür verantwortlich. In den meisten früheren Versionen von DirectX wurde die Gefahren Nachverfolgung durch den Treiber behandelt. Um die Leistung zu verbessern, sind Methoden ohne Risiko Verfolgung in DirectX 12 verfügbar.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**High-Level-Shader-Sprache (HLSL)**
</dt> <dd>

Eine Computersprache, die sich in vielerlei Hinsicht von C unterscheidet, die zum Schreiben von Shader-Code verwendet wird. Vertex-, Pixel-, Geometrie-, COMPUTE-, Domänen-und Hull-Shader werden mithilfe von HLSL geschrieben. Ein Compiler konvertiert die HLSL-Quelle in ein binäres Format, das von der GPU verwendet werden soll.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**
</dt> <dd>

Die verschiedenen Instanzen und Typen von Engines in einer einzelnen GPU. Die Arten von Engines umfassen: Grafiken, COMPUTE und Copy.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**Multigpu**
</dt> <dd>

Eine Hardwarekonfiguration, bei der mehr als ein Grafikadapter vorhanden ist. Die separaten Adapter werden manchmal als Knoten bezeichnet. Wenn Sie über mehrere GPUs verfügen, können Sie die Synchronisierung mit der CPU und einander erheblich komplexer machen als mit einer einzelnen GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Pipeline Zustands Objekt (PSO)**
</dt> <dd>

Ein erheblicher Teil des Status der GPU. Dieser Status umfasst alle aktuell festgelegten Shader und bestimmte Zustands Objekte mit fester Funktions Zeit. Die einzige Möglichkeit zum Ändern von Zuständen, die im Pipeline Objekt enthalten sind, besteht darin, das zurzeit gebundene Pipeline Objekt zu ändern.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**Prädikation übersprungen**
</dt> <dd>

Das-Prädikat ist ein Feature, mit dem die GPU anstelle der CPU feststellen kann, ob ein Objekt nicht gezeichnet, kopiert oder versendet werden soll. Wenn z. b. ein Begrenzungsfeld eines Objekts vollständig von einem anderen Objekt oder einer Perspektive vollständig auf eine geringere Größe als die Pixelgröße reduziert wurde, ist es möglicherweise nicht sinnvoll, das verborgene Objekt zu zeichnen. Siehe [prediation](predication.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Reihen folgen Ansicht des Rasterizers (Row)**
</dt> <dd>

Standard Grafik Pipelines haben möglicherweise Probleme mit der ordnungsgemäßen Zusammensetzung mehrerer Texturen, die Transparenz enthalten. Objekte wie z. b. Drahtzäune, Rauch, Feuer, Vegetation und farbige Glas verwenden Transparenz, um den gewünschten Effekt zu erzielen. Es treten Probleme auf, wenn mehrere Texturen, die Transparenz enthalten, aufeinander zueinander stehen (Feuer vor einem Fence vor einem Glasgebäude, das eine Vegetations enthält). Mithilfe von "Rasterizer-Ansichten" (ROVs) können die zugrunde liegenden OIT-Algorithmen (Order Independent Transparenz) die Features der Hardware zum ordnungsgemäßen Auflösen der Transparenz Reihenfolge verwenden. Transparenz wird vom Pixelshader behandelt.

Mithilfe geordneter Ansichten von Rasterizer (ROVs) können Pixel-Shader-Code ungeordnete zugriffsansichts-Bindungen (UAV) mit einer Deklaration markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**Read-Back-Heap**
</dt> <dd>

Ein Heap im Benutzermodus, der sich auf die Datenübertragung von der GPU zurück zur CPU konzentriert.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**Ressource**
</dt> <dd>

Eine Entität, die Daten für die Pipeline bereitstellt und definiert, was während der Szene gerendert wird. Ressourcen können von ihren Spiel Medien geladen oder dynamisch zur Laufzeit erstellt werden. In der Regel enthalten Ressourcen Textur Daten, Scheitelpunkt Daten und shaderdaten. Die meisten Direct3D-Anwendungen erstellen und zerstören Ressourcen in der gesamten Lebensdauer.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**Ressourcen Barriere**
</dt> <dd>

Eine Ressourcengrenze benachrichtigt den Treiber, dass möglicherweise eine Synchronisierung mehrerer Zugriffe auf eine einzelne Ressource erforderlich ist, z. b. das Lesen und Schreiben in dieselbe Textur.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**Ressourcen Bindung**
</dt> <dd>

Bei der Ressourcen Bindung werden Ressourcen (Texturen, Vertex-Puffer, Index Puffer usw.) mit der Grafik Pipeline verknüpft, sodass die Shader der Pipeline die richtige Ressource verarbeiten können.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**Ressourcen Heaps**
</dt> <dd>

Ressourcen Heaps sind ein allgemeiner Begriff für die Heaps, bei denen es sich um Speicherpuffer handelt, die bei der Übertragung an und von der GPU reserviert werden. Eine Übertragung an die GPU erfordert einen uploadheap, von der GPU bis zur CPU erfordert einen abzurufenden Heap, und ein persistenter Heap für die GPU, der über mehrere renderingframes gewartet werden soll, wird als Standard Heap bezeichnet.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**Stamm Signatur**
</dt> <dd>

Stamm Signaturen definieren alle Ressourcen, die an die Grafiken oder COMPUTE-Pipelines gebunden werden sollen. Eine Stamm Signatur wird von der APP und Verknüpfungen Befehlslisten mit den Ressourcen konfiguriert, die für die Shader normalerweise erforderlich sind. es gibt jeweils eine Grafik und eine computestammsignatur pro app.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**Sammel**
</dt> <dd>

Ein Sampler ist Code, der aus einer Textur liest.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Shader-Ressourcenansicht (SRV)**
</dt> <dd>

Eine Format spezifische Methode zum Überprüfen der Daten in einer Shader-Ressource, z. b. eine Textur.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**statischer Heap**
</dt> <dd>

Ein Heap im Benutzermodus, der sich auf mehrere GPU-schreibgeschützte Ressourcen konzentriert, die normalerweise gleichzeitig verwendet werden und nicht häufig geändert werden.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**Austausch Kette**
</dt> <dd>

Austausch Ketten steuern die Hintergrund Puffer Drehung und bilden die Grundlage der Grafik Animation. Swapketten werden vom Low-Level-API-Satz DXGI behandelt (Weitere Informationen finden Sie unter [DXGI Overview](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**Swizzle**
</dt> <dd>

Eine Technik, mit der Mehrdimensionale Daten im Arbeitsspeicher gesucht werden, sodass Daten aus der nahen Dimensionalität in der Regel nahe gelegene Adressen aufweisen. Vor allem werden alle Daten für eine Zeile vor den Daten für die nächste Zeile nicht zusammenhängend gefunden. Ein "parametrisiertes schwenken" beschreibt eine standardisierte Methode zum Beschreiben von swidingmustern.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**Konsistenz**
</dt> <dd>

Ein D3D-Ressourcentyp, der mehrdimensional ist und über ein Speicher Layout verfügt, das für den mehrdimensionalen Zugriff von der GPU optimiert ist. Texturen enthalten häufig das Rohbild, das zum Renderingvorgang auf einer Oberfläche erforderlich ist, bevor Beleuchtung und Vermischung stattfinden, aber auch andere Formen von Daten enthalten können, z. b. Farbverläufe und Bezugs Farben. Direct3D 12 unterstützt eine, zwei und dreidimensionale Texturen.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**Stein**
</dt> <dd>

Eine Seite mit Video Arbeitsspeicher, ähnlich einer CPU/System-Seite des Speichers. Mithilfe der Kachel Notation kann das subsubsystem des virtuellen GPU-Speichers vom virtuellen CPU-Speichersubsystem unterschieden werden. GPUs bieten ähnliche Funktionen für den virtuellen Arbeitsspeicher wie der virtuelle Systemspeicher. Einige GPUs verfügen über freigegebene Funktionen für den virtuellen Arbeitsspeicher, die die Freigabe einiger Seiten des virtuellen Speicher Subsystems sowohl mit der CPU als auch mit der GPU ermöglichen.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**Gekachelte Ressourcen**
</dt> <dd>

Gekachelte Ressourcen werden benötigt, sodass weniger GPU-Speicherplatz für das Speichern von Bereichen von Oberflächen verschwendet wird, auf die die Anwendung keinen Zugriff hat, und die Hardware weiß, wie Sie über angrenzende Kacheln filtern kann. Bei gekachelten Ressourcen handelt es sich um große logische Ressourcen, die jedoch nur wenige physische Speichermengen erfordern.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Unsortierter Zugriffs Ansicht (UAV)**
</dt> <dd>

Eine ungeordnete Zugriffs Ansicht in eine Ressource (die Puffer, Texturen und Textur Arrays enthält, ohne Multisampling), ermöglicht temporalen ungeordneten Lese-/Schreibzugriff von mehreren Threads. Dies bedeutet, dass dieser Ressourcentyp gleichzeitig von mehreren Threads gelesen/geschrieben werden kann, ohne dass Speicher Konflikte entstehen.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**Heap hochladen**
</dt> <dd>

Ein Heap im Benutzermodus, der sich auf die Datenübertragung von der CPU an die GPU konzentriert.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**benutzermodusheap**
</dt> <dd>

Eine Auflistung großer, zusammenhängender Speicher Belegungen, die ohne das Wissen der Kernel Komponente wieder verwendet werden: die Zuordnungs-und Zerstörungs Methoden werden während des stabilen Zustands nicht als Kernel Zuordnungs-und Zerstörungs Methoden bezeichnet. Upload-, leseback-und Standard-Heaps sind Varianten von Heaps im Benutzermodus.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**Menge an Kacheln**
</dt> <dd>

Dreidimensionale [gekachelte Ressourcen](/windows).

</dd> </dl>

 

 