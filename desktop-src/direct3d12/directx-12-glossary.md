---
title: Direct3D 12-Glossar
description: Diese Begriffe gelten für Direct3D 12.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a7ad8d9c925d4bd3b82a3c7dd177a58afd7f50fb82836bed56fac6a20c8f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496880"
---
# <a name="direct3d-12-glossary"></a>Direct3D 12-Glossar

Diese Begriffe gelten für Direct3D 12.

<dl> <dt>

<span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**Bindung**
</dt> <dd>

Der Prozess des Anfügens von Arbeitsspeicher an die Grafikpipeline. Die Ressourcenbindung umfasst z. B. die Bindung einer Ressource, z. B. einer Textur, an die Pipeline, um sie zum Rendern eines Objekts zu verwenden.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**Puffer**
</dt> <dd>

Ein Typ von D3D-Ressource, der mit einer zusammenhängenden Speicherzuweisung synonym ist.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**Bündel**
</dt> <dd>

Ein Befehlspuffer, der von der Grafikprozessor (GRAPHICS Processing Unit, GPU) nur direkt über eine direkte *Befehlsliste ausgeführt werden kann.* Ein Bündel erbt den gpu-Zustand (mit Ausnahme des aktuell festgelegten *Pipelinezustandsobjekts* und der primitiven Topologie).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**Befehlszuweisung**
</dt> <dd>

Die zugrunde liegenden Speicherzuweisungen, in denen GPU-Befehle gespeichert werden. Das Befehlszuweisungsobjekt gilt sowohl für *direkte Befehlslisten als* auch *für Bundles.*

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**Befehlsliste**
</dt> <dd>

Eine Befehlsliste entspricht einem Satz von Befehlen, die die GPU ausführt. Dazu gehören Befehle wie zum Festlegen des Zustands, Zeichnen, Löschen und Kopieren. Die D3D12-Befehlslistenschnittstelle ist deutlich anders als die D3D11-Befehlslistenschnittstelle. Die D3D12-Befehlslistenschnittstelle enthält APIs, die den D3D11-Gerätekontextrendering-APIs ähneln.

Eine D3D12-Befehlsliste lässt weder Ressourcen zuordnen oder zuordnen, Kachelzuordnungen ändern, die Größe von Kachelpools ändern, Abfragedaten erhalten, noch übermittelt sie befehle zur Ausführung implizit an die GPU.

Im Gegensatz zu verzögerten D3D11-Kontexten unterstützen D3D12-Befehlslisten nur zwei Deskriptionsebenen. Eine *direkte Befehlsliste* entspricht einem Befehlspuffer, den die GPU ausführen kann. Ein *Paket* kann nur direkt über eine direkte Befehlsliste ausgeführt werden.

Eine direkte Befehlsliste erbt keinen GPU-Zustand. Ein Bündel erbt den gpu-Zustand (mit Ausnahme des aktuell festgelegten Pipelinezustandsobjekts und der primitiven Topologie).

Der Arbeitsspeicher für eine Befehlsliste wird durch die *Befehlszuweisung festgelegt.* Befehlslisten dienen dazu, dass sie als einzelne Renderinganforderung an eine GPU übermittelt werden können.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**Befehlswarteschlange**
</dt> <dd>

Eine *Befehlswarteschlange listet* auf, dass die GPU nacheinander ausgeführt wird. Anwendungen müssen Befehlslisten *explizit zur Ausführung* an eine Befehlswarteschlange übermitteln. In der Regel gibt es drei Befehlswarteschlangen: 3D-Grafiken, Compute- und Kopiermodule, die der 3D-Grafikpipeline, der Compute-Engine und mindestens einem Kopiermodul auf der GPU entspricht.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**konservative Rasterung**
</dt> <dd>

Die konservative Rasterung ist ein Betriebsmodus für die Rasterizerphase der Direct3D-Grafikpipeline. Sie deaktiviert die standardmäßige beispielbasierte Rasterung und rastert stattdessen ein Pixel, das durch eine beliebige Menge durch ein Primitiv abgedeckt wird. Ein wichtiger Unterschied ist, dass jede Abdeckung zwar überhaupt ein rasterisiertes Pixel erzeugt, diese Abdeckung jedoch nicht durch die Hardware gekennzeichnet werden kann, sodass die Abdeckung immer binär für einen Pixel-Shader angezeigt wird: entweder vollständig abgedeckt oder nicht abgedeckt. Es bleibt dem Pixelschattencode übrig, um die tatsächliche Abdeckung analytisch zu bestimmen.

Die konservative Rasterung kann bei Problemen wie Kollisionen und Treffererkennung, Binning und Okklusionsculling helfen, bei denen die Farbe eines Pixels genauer ist und Kantenfälle beseitigt werden können. Weitere Informationen [finden Sie unter Konservative Rasterung.](conservative-rasterization.md)

</dd> <dt>

<span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Konstante Pufferansicht (CONSTANT Buffer View, CBV)**
</dt> <dd>

Konstante Puffer enthalten Shaderkonstantdaten, z. B. eine Kameraansicht, Projektionsmatrizen und Weltmatrizen. Eine "konstante Pufferansicht" ist die formatspezifische Ansicht des Puffers, die von der Grafikpipeline angezeigt wird.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**Standard heap**
</dt> <dd>

Ein Benutzermodus-Heap, der sich auf die Unterstützung persistenter GPU-Ressourcentypen konzentriert, einschließlich GPU-geschriebener Ressourcen.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**Deskriptor**
</dt> <dd>

Deskriptoren sind die primäre Bindungseinheit für eine einzelne Ressource in D3D12. Ein Deskriptor ist ein relativ kleiner Datenblock, der ein Objekt für die GPU in einem GPU-spezifischen Format vollständig beschreibt. Es gibt viele verschiedene Arten von Deskriptoren: Shader-Ressourcenansichten (SRVs), ungeordnete Zugriffsansichten (Unordered Access Views, UAVs), Konstante Pufferansichten (CBVs) und Sampler sind einige Beispiele.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**Deskriptor-Heap**
</dt> <dd>

Ein Deskriptor-Heap ist eine Sammlung zusammenhängender Zuordnungen von Deskriptoren, eine Zuordnung für jeden Deskriptor. Der Hauptpunkt eines Deskriptorheaps besteht im Umfang der Speicherzuweisung, die zum Speichern der Deskriptorspezifikationen von Objekttypen erforderlich ist, auf die Shader so groß wie möglich in einem Renderingfenster verweisen (idealerweise ein gesamter Renderingrahmen oder mehr).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**Deskriptortabelle**
</dt> <dd>

Eine Deskriptortabelle ist logisch ein Array von Deskriptoren. Jede Deskriptortabelle speichert Deskriptoren eines oder mehrere Typen, einschließlich SRVs, UAVe, CBVs und Sampler. Eine Deskriptortabelle ist keine Speicherzuweisung, sondern lediglich ein Offset und eine Länge in einem Deskriptor-Heap.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**Direkte Befehlsliste**
</dt> <dd>

Ein Befehlspuffer, der von der GPU ausgeführt werden kann. Eine direkte Befehlsliste erbt keinen GPU-Zustand.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**Zaun**
</dt> <dd>

Ein Mechanismus zum Synchronisieren von GPU und CPU. Sowohl die GPU als auch die CPU können angewiesen werden, an einem Fence zu warten und auf den Aufholbedarf des anderen Prozessors zu warten. Weitere Informationen [finden Sie unter Multi-Engine-Synchronisierung.](./user-mode-heap-synchronization.md)

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**Gefahr, Gefahrverfolgung**
</dt> <dd>

Eine Gefährdung tritt auf, wenn eine Ressource für einen Zweck verwendet wurde und die App diese für einen anderen Zweck wiederverwenden möchte. Um die Ressource erneut zu verwenden, müssen Zwischencaches geleert oder für ungültig erklärt werden, die Komprimierungsanforderungen müssen mit der zweiten Verwendung konsistent sein, und die Ressource sollte sich im erforderlichen Zustand sein, um zu vermeiden, dass die Ressource gelesen wird, nachdem sie für den vorgesehenen Zweck geschrieben und für ungültig erklärt wurde.

Der Prozess der Verwaltung von Ressourcen und das Vermeiden dieser Synchronisierungsprobleme wird als Risikoverfolgung bezeichnet. Wenn es keine Risikoverfolgung durch den Fahrer gibt, ist die App dafür verantwortlich. In den meisten früheren Versionen von DirectX wurde die Gefahrverfolgung vom Treiber verarbeitet. Zur Verbesserung der Leistung sind Methoden ohne Risikoverfolgung in DirectX 12 verfügbar.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**High-Level Shader Language (HLSL)**
</dt> <dd>

Eine Computersprache, ähnlich, aber in vielerlei Hinsicht anders als C, die zum Schreiben von Shadercode verwendet wird. Vertex-, Pixel-, Geometry-, Compute-, Domänen- und Hüllen-Shader werden alle mit HLSL geschrieben. Ein Compiler konvertiert die HLSL-Quelle in ein Binärformat, das von der GPU genutzt werden kann.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**Multiengine**
</dt> <dd>

Die verschiedenen Instanzen und Typen von Engines in einer einzelnen GPU. Zu den Arten von Engines gehören: Grafiken, Compute und Kopier.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**
</dt> <dd>

Eine Hardwarekonfiguration, bei der mehrere Grafikkarten enthalten sind. Die separaten Adapter werden manchmal als Knoten bezeichnet. Die Verwendung mehrerer GPUs kann die Aufgabe der Synchronisierung mit der CPU und untereinander erheblich komplexer als bei einer einzelnen GPU machen.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Pipelinezustandsobjekt (PSO)**
</dt> <dd>

Ein wesentlicher Teil des GPU-Zustands. Dieser Zustand schließt alle derzeit festgelegten Shader und bestimmte Objekte mit festem Funktionszustand ein. Die einzige Möglichkeit, die im Pipelineobjekt enthaltenen Zustände zu ändern, besteht darin, das aktuell gebundene Pipelineobjekt zu ändern.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**Prädication**
</dt> <dd>

Prädication ist ein Feature, mit dem die GPU und nicht die CPU bestimmen kann, ob ein Objekt nicht ge zeichnen, kopiert oder gesendet werden soll. Wenn z. B. ein Begrenzungsfeld eines Objekts vollständig von einem anderen Objekt oder einer anderen Perspektive verdeckt wird, das Objekt auf einen kleineren Bereich als ein Pixel reduziert hat, kann es keinen Sinn machen, das ausgeblendete Objekt zu zeichnen. Weitere Informationen [finden Sie unter Prädication](predication.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Rasterizer Order View (ROV)**
</dt> <dd>

Bei Standardgrafikpipelines können Probleme beim richtigen Zusammenordnen mehrerer Texturen mit Transparenz auftkommen. Objekte wie Wire Fences, Feuer, Feuer, Brand und farbiges Wasser verwenden Transparenz, um die gewünschte Wirkung zu erzielen. Probleme treten auf, wenn mehrere Texturen, die Transparenz enthalten, miteinander in Einklang stehen (z. B. Qualm vor einem Zäun vor einem glasigen Gebäude, das Dieben enthält). Rasterizer ordered views (ROVs) ermöglichen es den zugrunde liegenden OIT-Algorithmen (Order Independent Transparency), Features der Hardware zu verwenden, um zu versuchen, die Transparenz reihenfolge richtig aufzulösen. Transparenz wird vom Pixel-Shader verarbeitet.

RoVs (Rasterizer Ordered Views) ermöglichen es Pixel-Shadercode, UAV-Bindungen (Unordered Access View) mit einer Deklaration zu markieren, die die normalen Anforderungen für die Reihenfolge der Grafikpipelineergebnisse für UAVs ändert.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**Readback-Heap**
</dt> <dd>

Ein Benutzermodus-Heap, der sich auf die Datenübertragung von der GPU zurück zur CPU konzentriert.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**Ressource**
</dt> <dd>

Eine Entität, die Daten für die Pipeline liefert und definiert, was während Ihrer Szene gerendert wird. Ressourcen können von Ihren Spielmedien geladen oder dynamisch zur Laufzeit erstellt werden. Zu den Ressourcen gehören in der Regel Texturdaten, Scheitelpunktdaten und Shaderdaten. Die meisten Direct3D-Anwendungen erstellen und zerstören Ressourcen während ihrer gesamten Lebensdauer umfassend.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**Ressourcenbarriere**
</dt> <dd>

Eine Ressourcenbarriere benachrichtigt den Treiber, dass die Synchronisierung mehrerer Zugriffe auf eine einzelne Ressource erforderlich sein kann, z. B. lesen und in dieselbe Textur schreiben.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**Ressourcenbindung**
</dt> <dd>

Bei der Ressourcenbindung werden Ressourcen (Texturen, Scheitelpunktpuffer, Indexpuffer usw.) mit der Grafikpipeline verknüpft, sodass die Shader der Pipeline die richtige Ressource verarbeiten können.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**Ressourcenheaps**
</dt> <dd>

Ressourcenheaps sind ein allgemeiner Begriff für die Heaps, bei denen es sich um Speicherpuffer handelt, die für die Speicherung von Ressourcen bei der Übertragung auf und von der GPU vorgesehen sind. Eine Übertragung an die GPU erfordert einen Hochladen Heap, von der GPU zur CPU erfordert einen Rückleseheap, und ein persistenter Heap, den die GPU über mehrere Renderingframes verwalten kann, wird als Standardheap bezeichnet.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**Stammsignatur**
</dt> <dd>

Stammsignaturen definieren alle Ressourcen, die an die Grafik- oder Computepipelines gebunden werden sollen. Eine Stammsignatur wird von der App konfiguriert und verknüpft Befehlslisten mit den Ressourcen, die die Shader benötigen. In der Regel gibt es eine Grafik und eine Computestammsignatur pro App.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**Sampler**
</dt> <dd>

Ein Sampler ist Code, der aus einer Textur liest.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Shader Ressourcenansicht (SRV)**
</dt> <dd>

Eine formatspezifische Möglichkeit zum Anzeigen der Daten in einer Shaderressource, z. B. einer Textur.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**Statischer Heap**
</dt> <dd>

Ein Benutzermodusheap, der sich auf mehrere lesegeschützte GPU-Ressourcen konzentriert, die in der Regel gleichzeitig verwendet werden und nicht häufig geändert werden.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**Swapkette**
</dt> <dd>

Swapketten steuern die Hintergrundpufferrotation und bilden die Grundlage der Grafikanimation. Austauschketten werden vom LOW-API-Satz DXGI verarbeitet (siehe [DXGI-Übersicht](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**
</dt> <dd>

Eine Technik der Suche nach mehrdimensionalen Daten im Arbeitsspeicher, sodass Daten von in der Nähe befindlichen Dimensionen tendenziell Adressen in der Nähe haben. Insbesondere befinden sich nicht alle Daten für eine Zeile zusammenhängend vor den Daten für die nächste Zeile. Eine "parametrisierte Swizzle" beschreibt eine standardisierte Methode zum Beschreiben von Swizzlemustern.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**Textur**
</dt> <dd>

Ein D3D-Ressourcentyp, der mehrdimensional ist und über ein Speicherlayout verfügt, das für den mehrdimensionalen Zugriff über die GPU optimiert ist. Texturen enthalten häufig das rohe Bild, das zum Rendern auf einer Oberfläche erforderlich ist, bevor Beleuchtung und Mischung stattfinden, können aber andere Formen von Daten enthalten, z. B. Farbverläufe und Referenzfarben. Direct3D 12 unterstützt ein-, zwei- und dreidimensionale Texturen.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**Fliese**
</dt> <dd>

Eine Seite mit Videospeicher, ähnlich einer CPU-/Systemseite des Arbeitsspeichers. Die Kachel notation hilft dabei, das VIRTUELLE GPU-Speichersubsystem von dem VIRTUELLEN CPU-Speichersubsystem zu unterscheiden. GPUs bieten ähnliche virtuelle Arbeitsspeicherfunktionen wie virtueller Systemspeicher. Einige GPUs verfügen über funktionen für gemeinsam genutzten virtuellen Arbeitsspeicher, die die Freigabe einiger Seiten des Subsystems für virtuellen Speicher sowohl mit der CPU als auch mit der GPU ermöglichen.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**Gekachelte Ressourcen**
</dt> <dd>

Kachelressourcen werden benötigt, sodass weniger GPU-Arbeitsspeicher für die Speicherung von Oberflächenbereichen verschwendet wird, von denen die Anwendung weiß, dass nicht zugegriffen werden kann, und die Hardware kann verstehen, wie über angrenzende Kacheln gefiltert wird. Gekachelte Ressourcen sind große logische Ressourcen, erfordern jedoch kleine Mengen an physischem Arbeitsspeicher.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Ungeordnete Zugriffsansicht (UAV)**
</dt> <dd>

Eine unsortierte Zugriffsansicht auf eine Ressource (die Puffer, Texturen und Texturarrays ohne Mehrfachsampling umfasst) ermöglicht den zeitlich ungeordneten Lese-/Schreibzugriff von mehreren Threads. Dies bedeutet, dass dieser Ressourcentyp von mehreren Threads gleichzeitig gelesen/geschrieben werden kann, ohne Speicherkonflikte zu generieren.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**Uploadheap**
</dt> <dd>

Ein Benutzermodusheap, der sich auf die Datenübertragung von der CPU zur GPU konzentriert.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**Benutzermodusheap**
</dt> <dd>

Eine Sammlung von großen, zusammenhängenden Speicherbelegungen, die ohne das Bewusstsein einer Kernelkomponente wiederverwendet werden: Die Zuordnungs- und Zerstörungsmethoden rufen keine Kernelzuordnungs- und -zerstörungsmethoden im stabilen Zustand auf. Hochladen, Readback und Standardheaps sind Varianten von Heaps im Benutzermodus.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**Volumekachelressourcen**
</dt> <dd>

Dreidimensionale [gekachelte Ressourcen.](/windows)

</dd> </dl>

 

 