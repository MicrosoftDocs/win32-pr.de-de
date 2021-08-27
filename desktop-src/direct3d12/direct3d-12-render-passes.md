---
title: Direct3D 12-Renderdurchläufe
description: Das Renderdurchläufe-Feature hilft Ihrem Renderer, die GPU-Effizienz zu verbessern, indem der Arbeitsspeicherdatenverkehr zum/vom Off-Chip-Arbeitsspeicher reduziert wird. Dies geschieht, indem Ihre Anwendung die Anforderungen an die Sortierung von Ressourcenrendering und Datenabhängigkeiten besser identifizieren kann.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: 96ed14cecd518a3e03672f2667306ee0a4b8d64999aab01aa72aae04975f0a83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069690"
---
# <a name="direct3d-12-render-passes"></a>Direct3D 12-Renderdurchläufe

Das Renderdurchläufe-Feature ist neu für Windows 10, Version 1809 (10.0; Build 17763) und führt das Konzept eines Direct3D 12-Renderdurchlaufs ein. Ein Renderdurchlauf besteht aus einer Teilmenge der Befehle, die Sie in einer Befehlsliste aufzeichnen.

Um zu deklarieren, wo jeder Renderdurchlauf beginnt und endet, schachteln Sie die Befehle, die zu diesem gehören, in Aufrufen von [**ID3D12GraphicsCommandList4::BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass) und [**EndRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-endrenderpass). Folglich enthält jede Befehlsliste null, einen oder mehrere Renderdurchläufe.

## <a name="scenarios"></a>Szenarien

Renderdurchläufe können die Leistung Ihres Renderers verbessern, wenn er unter anderem auf Tile-Based Deferred Rendering (TBDR) basiert. Genauer gesagt hilft das Verfahren Ihrem Renderer, die GPU-Effizienz zu verbessern, indem der Arbeitsspeicherdatenverkehr zum bzw. vom Off-Chip-Speicher reduziert wird, indem es Ihrer Anwendung ermöglicht wird, Anforderungen an die Sortierung von Ressourcenrendering und Datenabhängigkeiten besser zu identifizieren.

Ein Anzeigetreiber, der ausdrücklich geschrieben wurde, um die Funktion "Renderdurchläufe" zu nutzen, liefert die besten Ergebnisse. Renderdurchlauf-APIs können jedoch auch auf bereits vorhandenen Treibern ausgeführt werden (jedoch nicht unbedingt mit Leistungsverbesserungen).

Dies sind die Szenarien, in denen Renderdurchläufe zum Bereitstellen von Werten entworfen wurden.

### <a name="allow-your-application-to-avoid-unnecessary-loadsstores-of-resources-fromto-main-memory-on-a-tile-based-deferred-rendering-tbdr-architecture"></a>Ermöglichen Sie es Ihrer Anwendung, unnötiges Laden/Speichern von Ressourcen aus dem/in den Hauptspeicher in einer tbdr-Architektur (Deferred Rendering) Tile-Based zu vermeiden.

Einer der Wertversprechen von Renderdurchläufen ist, dass sie ihnen einen zentralen Ort zur Verfügung stellt, um die Datenabhängigkeiten Ihrer Anwendung für eine Reihe von Renderingvorgängen anzugeben. Diese Datenabhängigkeiten ermöglichen es dem Anzeigetreiber, diese Daten zur Bindungs-/Barrierezeit zu überprüfen und Anweisungen zur Minimierung von Ressourcenladevorgängen/-speichern aus dem/in den Hauptspeicher auszugeben.

### <a name="allow-your-tbdr-architecture-to-opportunistically-persistent-resources-in-on-chip-cache-across-render-passes-even-in-separate-command-lists"></a>Ermöglichen Sie Es Ihrer TBDR-Architektur, ressourcen im On-Chip-Cache über Renderdurchläufe hinweg (auch in separaten Befehlslisten) zu speichern.

> [!NOTE]
> Insbesondere ist dieses Szenario auf die Fälle beschränkt, in denen Sie über mehrere Befehlslisten hinweg in dieselben Renderziele schreiben.

Ein gängiges Renderingmuster besteht darin, dass Ihre Anwendung in mehreren Befehlslisten seriell auf denselben Renderzielen gerendert wird, obwohl die Renderingbefehle parallel generiert werden. Durch die Verwendung von Renderdurchläufen in diesem Szenario können diese Durchläufe so kombiniert werden (da die Anwendung weiß, dass das Rendering in der unmittelbar nachfolgenden Befehlsliste fortgesetzt wird), sodass der Anzeigetreiber eine Leerung in den Hauptspeicher an Befehlslistengrenzen vermeiden kann.

## <a name="your-applications-responsibilities"></a>Zuständigkeiten Ihrer Anwendung

Selbst mit dem Renderdurchlauf-Feature übernehmen weder die Direct3D 12-Runtime noch der Anzeigetreiber die Verantwortung dafür, Möglichkeiten zur Neuordnung/Vermeidung von Auslastungen und Speichern zu ableiten. Um das Renderdurchläufe-Feature ordnungsgemäß nutzen zu können, hat Ihre Anwendung diese Zuständigkeiten.

- Identifizieren Sie die Daten-/Sortierabhängigkeiten für ihre Vorgänge ordnungsgemäß.
- Ordnen Sie die Übermittlungen so an, dass Leerungen minimiert werden (also minimieren Sie die Verwendung von **_PRESERVE** Flags).
- Verwenden Sie ressourcenbarrieren ordnungsgemäß, und verfolgen Sie den Ressourcenstatus.
- Vermeiden Sie nicht benötigte Kopien/Löschen. Um diese zu identifizieren, können Sie die automatisierten Leistungswarnungen aus dem [PIX auf Windows Tool](https://devblogs.microsoft.com/pix/)verwenden.

## <a name="using-the-render-pass-feature"></a>Verwenden der Renderdurchlauffunktion

### <a name="what-is-a-render-pass"></a>Was ist ein *Renderdurchlauf?*

Ein Renderdurchlauf wird von diesen Elementen definiert.

- Eine Reihe von Ausgabebindungen, die für die Dauer des Renderdurchlaufs festgelegt sind. Diese Bindungen gelten für eine oder mehrere Renderzielsichten (RTVs) und/oder für eine Tiefenschablonenansicht (DSV).
- Eine Liste von GPU-Vorgängen, die auf diesen Satz von Ausgabebindungen ausgerichtet sind.
- Metadaten, die die Last-/Speicherabhängigkeiten für alle Ausgabebindungen beschreiben, auf die der Renderdurchlauf abzielt.

### <a name="declare-your-output-bindings"></a>Deklarieren Der Ausgabebindungen

Zu Beginn eines Renderdurchlaufs deklarieren Sie Bindungen an Ihre Renderziele und/oder an Ihren Tiefen-/Schablonenpuffer. Es ist optional, an Renderziele zu binden, und es ist optional, an einen Tiefen-/Schablonenpuffer zu binden. Sie müssen jedoch an mindestens eine der beiden Bindungen binden, und im folgenden Codebeispiel binden wir an beide.

Sie deklarieren diese Bindungen in einem Aufruf von [**ID3D12GraphicsCommandList4::BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass).

```cppwinrt
void render_passes(::ID3D12GraphicsCommandList4 * pIGCL4,
    D3D12_CPU_DESCRIPTOR_HANDLE const& rtvCPUDescriptorHandle,
    D3D12_CPU_DESCRIPTOR_HANDLE const& dsvCPUDescriptorHandle)
{
    const float clearColor4[]{ 0.f, 0.f, 0.f, 0.f };
    CD3DX12_CLEAR_VALUE clearValue{ DXGI_FORMAT_R32G32B32_FLOAT, clearColor4 };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessClear{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_CLEAR, { clearValue } };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessPreserve{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_PRESERVE, {} };
    D3D12_RENDER_PASS_RENDER_TARGET_DESC renderPassRenderTargetDesc{ rtvCPUDescriptorHandle, renderPassBeginningAccessClear, renderPassEndingAccessPreserve };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessNoAccess{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessNoAccess{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_DEPTH_STENCIL_DESC renderPassDepthStencilDesc{ dsvCPUDescriptorHandle, renderPassBeginningAccessNoAccess, renderPassBeginningAccessNoAccess, renderPassEndingAccessNoAccess, renderPassEndingAccessNoAccess };

    pIGCL4->BeginRenderPass(1, &renderPassRenderTargetDesc, &renderPassDepthStencilDesc, D3D12_RENDER_PASS_FLAG_NONE);
    // Record command list.
    pIGCL4->EndRenderPass();
    // Begin/End further render passes and then execute the command list(s).
}
```

Sie legen das erste Feld der [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) Struktur auf das CPU-Deskriptorhandle fest, das mindestens einer Renderzielansicht (RTVs) entspricht. Ebenso enthält [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) das CPU-Deskriptorhandle, das einer Tiefenschablonenansicht (DSV) entspricht. Diese CPU-Deskriptorhandles sind die gleichen, die Sie andernfalls an [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)übergeben würden. Und wie bei **OMSetRenderTargets** werden die CPU-Deskriptoren zum Zeitpunkt des Aufrufs von **BeginRenderPass** von ihren jeweiligen Heaps (CPU-Deskriptor) *angedockt.*

RtVs und DSV werden nicht an den Renderdurchlauf geerbt. Stattdessen müssen sie festgelegt werden. RtVs und DSV werden auch nicht in **BeginRenderPass** deklariert und an die Befehlsliste weitergegeben. Stattdessen befinden sie sich nach dem Renderdurchlauf in einem nicht definierten Zustand.

### <a name="render-passes-and-workloads"></a>Rendern von Durchläufen und Workloads

Renderdurchläufe können nicht geschachtelt werden, und Sie können keinen Renderdurchlauf mit mehreren Befehlslisten verwenden (sie müssen beginnen und enden, während sie in einer einzigen Befehlsliste aufgezeichnet werden). Optimierungen, die die effiziente Generierung von Renderdurchläufen mit mehreren Threads ermöglichen sollen, werden im Abschnitt [ Renderdurchlaufflags](#render-pass-flags)weiter unten erläutert.

Ein Schreibvorgang, den Sie innerhalb eines Renderdurchlaufs durchführen, ist für Das Lesen aus bis zu einem nachfolgenden Renderdurchlauf nicht *gültig.* Dies schließt einige Arten von Barrieren innerhalb des Renderdurchlaufs &mdash; aus, z. B. das Barriering von **RENDER_TARGET** zu **SHADER_RESOURCE** auf dem derzeit gebundenen Renderziel. Weitere Informationen finden Sie weiter unten im Abschnitt [Rendern von Durchläufen und Ressourcenbarrieren.](#render-passes-and-resource-barriers)

Die einzige Ausnahme der gerade erwähnten Schreib-/Leseeinschränkung umfasst die impliziten Lesezugriffe, die im Rahmen von Tiefentests und Renderzielblending erfolgen.
Daher sind diese APIs innerhalb eines Renderdurchlaufs nicht zulässig (die Kernlaufzeit entfernt die Befehlsliste, wenn einer von ihnen während der Aufzeichnung aufgerufen wird).

- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)
- [**ID3D12GraphicsCommandList4::BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass)
- [**ID3D12GraphicsCommandList::ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
- [**ID3D12GraphicsCommandList::ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
- [**ID3D12GraphicsCommandList::ClearState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
- [**ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
- [**ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
- [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
- [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
- [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
- [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
- [**ID3D12GraphicsCommandList::D iscardResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
- [**ID3D12GraphicsCommandList::D ispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
- [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
- [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
- [**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
- [**ID3D12GraphicsCommandList1::ResolveSubresourceRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion)
- [**ID3D12GraphicsCommandList3::SetProtectedResourceSession**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist3-setprotectedresourcesession)

### <a name="render-passes-and-resource-barriers"></a>Rendern von Durchläufen und Ressourcenbarrieren

Sie dürfen einen Schreibvorgang, der innerhalb desselben Renderdurchlaufs aufgetreten ist, nicht lesen oder nutzen. Bestimmte Barrieren entsprechen dieser Einschränkung nicht, z. B. von **D3D12_RESOURCE_STATE_RENDER_TARGET** **bis \*** _SHADER_RESOURCE auf dem derzeit gebundenen Renderziel (und die Debugebene führt zu einem Fehler in diesem Effekt). Dieselbe Barriere auf einem Renderziel, das *außerhalb* des aktuellen Renderdurchlaufs geschrieben wurde, ist jedoch konform, da die Schreibvorgänge vor dem Start des aktuellen Renderdurchlaufs abgeschlossen werden.
Sie können davon profitieren, dass Sie bestimmte Optimierungen kennen, die ein Anzeigetreiber in dieser Hinsicht vornehmen kann. Bei einer konformen Arbeitsauslastung kann ein Anzeigetreiber alle Barrieren, die in Ihrem Renderdurchlauf auftreten, an den Anfang des Renderdurchlaufs verschieben. Dort können sie zusammengeknüpft werden (und beeinträchtigen keine Tiling-/Binningvorgänge). Dies ist eine gültige Optimierung, vorausgesetzt, dass alle Schreibvorgänge abgeschlossen sind, bevor der aktuelle Renderdurchlauf gestartet wird.

Hier sehen Sie ein vollständigeres Beispiel für die Treiberoptimierung, bei dem davon ausgegangen wird, dass Sie über eine Rendering-Engine verfügen, die über einen Ressourcenbindungsentwurf vor Direct3D im 12-Stil verfügt, der bei &mdash; *Bedarf* Barrieren basierend auf der Bindung von Ressourcen erzeugt. Beim Schreiben in eine ungeordnete Zugriffsansicht (UAV) gegen Ende eines Frames (für die Nutzung im folgenden Frame) kann es vorkommen, dass die Engine die Ressource am Ende des Frames im **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** Zustand belässt. Wenn die Engine die Ressource als Shaderressourcenansicht (Shader Resource View, SRV) bindet, wird im folgenden Frame festgestellt, dass sich die Ressource nicht im richtigen Zustand befindet, und es wird eine Barriere von **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** zu **D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE** ausgegeben. Wenn diese Barriere innerhalb des Renderdurchlaufs auftritt, ist der Anzeigetreiber berechtigt, davon auszugehen, dass alle Schreibvorgänge bereits *außerhalb* dieses aktuellen Renderdurchlaufs erfolgt sind. Daher kann der Anzeigetreiber die Barriere bis zum Anfang des Renderdurchlaufs *verschieben* (und hier an der Stelle, an der die Optimierung eingeht). Auch hier ist dies gültig, solange Ihr Code der in diesem Abschnitt und der letzten beschriebenen Schreib-/Leseeinschränkung entspricht.


Dies sind Beispiele für konforme Barrieren.
- **D3D12_RESOURCE_STATE_UNORDERED_ACCESS,** um zu **D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT.**
- **D3D12_RESOURCE_STATE_COPY_DEST,** um zu **\* _SHADER_RESOURCE.**

Dies sind Beispiele für nicht konforme Barrieren.

- **D3D12_RESOURCE_STATE_RENDER_TARGET** zu einem beliebigen Lesezustand auf derzeit gebundenen RTVs/DSVs.
- **D3D12_RESOURCE_STATE_DEPTH_WRITE** zu einem beliebigen Lesezustand auf derzeit gebundenen RTVs/DSVs.
- Alle Aliasingbarrieren.
- UAV-Barrieren (Unordered Access View). 

### <a name="resource-access-declaration"></a>Ressourcenzugriffsdeklaration

Zur **BeginRenderPass-Zeit** sowie zum Deklarieren aller Ressourcen, die als RTVs und/oder DSV innerhalb dieses Durchlaufs dienen, müssen Sie auch deren Start- und *Endzugriffsmerkmale* angeben. Wie Sie im Codebeispiel oben im Abschnitt [Deklarieren ihrer Ausgabebindungen](#declare-your-output-bindings) sehen können, geschieht dies mit den [**D3D12_RENDER_PASS_RENDER_TARGET_DESC-**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) und [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC-Strukturen.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc)

Weitere Informationen finden Sie in den [**D3D12_RENDER_PASS_BEGINNING_ACCESS-**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access) und [**D3D12_RENDER_PASS_ENDING_ACCESS-Strukturen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access) sowie in den [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE-**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type) und D3D12_RENDER_PASS_ENDING_ACCESS_TYPE-Enumerationen. [](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type)

### <a name="render-pass-flags"></a>Rendern von Passflags

Der letzte parameter, der an **BeginRenderPass übergeben** wird, ist ein Renderpassflag (ein Wert aus der [**D3D12_RENDER_PASS_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_flags) Enumeration).

```cppwinrt
enum D3D12_RENDER_PASS_FLAGS
{
    D3D12_RENDER_PASS_FLAG_NONE = 0,
    D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES = 0x1,
    D3D12_RENDER_PASS_FLAG_SUSPENDING_PASS = 0x2,
    D3D12_RENDER_PASS_FLAG_RESUMING_PASS = 0x4
};
```

#### <a name="uav-writes-within-a-render-pass"></a>UAV-Schreibvorgänge innerhalb eines Renderpasses

Ungeordnete Zugriffsansichts-Schreibvorgänge (UAV) sind innerhalb eines Renderpasses zulässig. Sie müssen jedoch ausdrücklich angeben, dass Sie UAV-Schreibvorgänge innerhalb des Renderpasses ausstellen, indem Sie **D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES** angeben, damit der Anzeigetreiber das Kacheln bei Bedarf deaktivieren kann.

UAV-Zugriffe müssen der oben beschriebenen Schreib-/Leseeinschränkung folgen (Schreibvorgänge in einem Renderpass sind bis zu einem nachfolgenden Renderpass nicht zum Lesen gültig). UAV-Barrieren sind innerhalb eines Renderpasses nicht zulässig.

UAV-Bindungen (über Stammtabellen oder Stammdeskriptoren) werden in Renderüberläufe geerbt und aus Renderüberläufen propagiert.

#### <a name="suspending-passes-and-resuming-passes"></a>Aussetzen von Durchläufen und Fortsetzen von Durchläufen

Sie können einen gesamten Renderpass als "Suspending Pass" und/oder "resuming-pass" angeben. Ein suspending-followed-by-a-resuming-Paar muss über identische Ansichten/Zugriffsflags zwischen den Durchläufen verfügen und darf keine dazwischen folgenden GPU-Vorgänge (z. B. Zeichnet, Dispatchs, Verwerfen, Löschen, Kopieren, Updatekachelzuordnungen, Schreibpuffer-Direktaufnahmen, Abfragen, Abfrage-Auflösungen) zwischen dem angehaltenen Renderdurchlauf und dem fortsetzenden Renderdurchlauf haben.

Der beabsichtigte Verwendungsfall ist das Multithreadrendering, bei dem beispielsweise vier Befehlslisten (jeweils mit eigenen Renderüberläufen) auf dieselben Renderziele zielen können. Wenn Renderdurchläufe über Befehlslisten hinweg angehalten/fortgesetzt werden, müssen die Befehlslisten im gleichen Aufruf von [**ID3D12CommandQueue::ExecuteCommandLists ausgeführt werden.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)

Ein Renderpass kann sowohl fortsetzen als auch angehalten werden. Im soeben angegebenen Multithread-Beispiel würden die Befehlslisten 2 und 3 von 1 bzw. 2 fortsetzen. Gleichzeitig würden 2 und 3 jeweils auf 3 bzw. 4 angehalten.

## <a name="query-for-render-passes-feature-support"></a>Abfrage der Featureunterstützung für Renderüberläufe

Sie können [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) aufrufen, um das Ausmaß zu abfragen, in dem ein Gerätetreiber und/oder die Hardware Renderüberläufe effizient unterstützt.

```cppwinrt
D3D12_RENDER_PASS_TIER get_render_passes_tier(::ID3D12Device * pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS5 featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS5, &featureSupport, sizeof(featureSupport))
    );
    return featureSupport.RenderPassesTier;
}
...
    D3D12_RENDER_PASS_TIER renderPassesTier{ get_render_passes_tier(pIDevice) };
```

Aufgrund der Zuordnungslogik der Laufzeit übergibt das Rendern immer die -Funktion. Je nach Featureunterstützung bieten sie jedoch nicht immer einen Vorteil. Sie können code ähnlich wie im obigen Codebeispiel verwenden, um zu bestimmen, ob/wann es sich lohnt, Befehle als Renderüberläufe ausgibt, und wenn dies definitiv kein Vorteil ist (d. h., wenn die Laufzeit nur der vorhandenen API-Oberfläche zugibt). Diese Überprüfung ist besonders wichtig, wenn Sie [D3D11On12 verwenden.](/windows/desktop/direct3d12/direct3d-11-on-12)

Eine Beschreibung der drei Supportebenen finden Sie in der [**D3D12_RENDER_PASS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_tier) Enumeration.
