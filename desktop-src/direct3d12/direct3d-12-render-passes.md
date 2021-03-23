---
title: Direct3D 12-Rendering-Verläufen
description: Die Funktion "renderingüberläufen" hilft Ihrem Renderer, die GPU-Effizienz zu verbessern, indem der Speicher Datenverkehr auf den/aus dem Dies geschieht, indem es Ihrer Anwendung ermöglicht wird, Anforderungen an die Reihenfolge von Ressourcen Rendering und Daten Abhängigkeiten besser zu identifizieren.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: f776729f17ac0017d713c6f37bc71de7302a7c08
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2020
ms.locfileid: "104548635"
---
# <a name="direct3d-12-render-passes"></a>Direct3D 12-Rendering-Verläufen

Die Funktion "Rendering übergibt" ist neu für Windows 10, Version 1809 (10,0; Build 17763), und es wird das Konzept eines Direct3D 12-Renderpass eingeführt. Ein renderdurchlauf besteht aus einer Teilmenge der Befehle, die Sie in einer Befehlsliste aufzeichnen.

Um zu deklarieren, wo jeder renderdurchlauf beginnt und endet, Schachteln Sie die Befehle, die zu gehören und innerhalb von Aufrufen an [**ID3D12GraphicsCommandList4:: beginrenderpass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass) und [**endrenderpass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-endrenderpass)übergeben werden. Folglich enthält jede Befehlsliste 0 (null), ein oder mehrere Rendering-Durchläufen.

## <a name="scenarios"></a>Szenarien

Renderingerweiterungen können die Leistung Ihres Renderers verbessern, wenn er auf Tile-Based verzögertem Rendering (tbdr) basiert, und zwar neben anderen Techniken. Genauer gesagt unterstützt das Verfahren ihren Renderer, die GPU-Effizienz zu verbessern, indem der Speicher Datenverkehr auf den bzw. aus dem Off-Chip-Speicher reduziert wird, indem die Anwendung die Sortier Anforderungen und Daten Abhängigkeiten der Ressourcen Rendering besser identifiziert

Ein Anzeigetreiber, der ausdrücklich zur Nutzung der Rendering-Funktion geschrieben wurde, liefert die besten Ergebnisse. Renderpass-APIs können jedoch auch für bereits vorhandene Treiber ausgeführt werden (Dies ist jedoch nicht notwendigerweise bei Leistungsverbesserungen der gibt).

Dabei handelt es sich um Szenarios, in denen "Rendering Pass" einen Wert bereitstellt.

### <a name="allow-your-application-to-avoid-unnecessary-loadsstores-of-resources-fromto-main-memory-on-a-tile-based-deferred-rendering-tbdr-architecture"></a>Ermöglicht der Anwendung, unnötige Lade-und Speicherressourcen aus/in den Hauptspeicher einer Tile-Based verzögerten Rendering (tbdr)-Architektur zu vermeiden.

Einer der Wertbeiträge von Renderingvorgängen ist, dass Sie einen zentralen Speicherort bereitstellen, um die Daten Abhängigkeiten Ihrer Anwendung für eine Reihe von Renderingvorgängen anzugeben. Diese Daten Abhängigkeiten ermöglichen es dem Anzeigetreiber, diese Daten zur Bindungs-/Sperrzeit zu untersuchen und Anweisungen auszugeben, mit denen Ressourcen Belastungen/-Speicher aus/in den Hauptspeicher minimiert werden.

### <a name="allow-your-tbdr-architecture-to-opportunistically-persistent-resources-in-on-chip-cache-across-render-passes-even-in-separate-command-lists"></a>Ermöglichen Sie Ihrer tbdr-Architektur die opportunistische Persistenz von Ressourcen im on-Chip-Cache über Rendering-Pass (selbst in separaten Befehlslisten).

> [!NOTE]
> Insbesondere ist dieses Szenario auf die Fälle beschränkt, in denen Sie in die gleichen Renderziele in mehreren Befehlslisten schreiben.

Ein gängiges renderingmuster besteht darin, dass Ihre Anwendung seriell in denselben Renderziel (en) über mehrere Befehlslisten gerendert wird, auch wenn die renderingbefehle parallel generiert werden. Die Verwendung von renderweiterungen in diesem Szenario ermöglicht es, dass diese weitergeleitet werden (da die Anwendung weiß, dass Sie das Rendering in der direkt nachfolgenden Befehlsliste fort setzt), dass der Anzeigetreiber eine Leerung in den Hauptspeicher der Befehlslisten Grenzen vermeiden kann.

## <a name="your-applications-responsibilities"></a>Zuständigkeiten ihrer Anwendung

Selbst bei der Funktion "Rendering übergibt" übernimmt weder die Direct3D 12-Laufzeit noch der Anzeigetreiber die Verantwortung für das Ableiten von Verkaufschancen zum erneuten Anordnen/vermeiden von Lade-und Speicher Vorgängen. Um die Funktion "Rendering-Pass" ordnungsgemäß nutzen zu können, hat ihre Anwendung diese Zuständigkeiten.

- Identifizieren Sie die Abhängigkeiten von Daten/Reihenfolge für Ihre Vorgänge ordnungsgemäß.
- Ordnen Sie die Übermittlungen so an, dass Leerungen minimiert werden (sodass Sie die Verwendung von **_PRESERVE** Flags minimieren).
- Verwenden Sie die Ressourcen Barrieren ordnungsgemäß, und verfolgen Sie den Ressourcen Status nach.
- Vermeiden Sie nicht benötigte Kopien/gelöschten Kopien. Um diese zu identifizieren, können Sie die automatisierten Leistungs Warnungen aus dem [pix on Windows-Tool](https://devblogs.microsoft.com/pix/)nutzen.

## <a name="using-the-render-pass-feature"></a>Verwenden der Funktion "Renderpass"

### <a name="what-is-a-render-pass"></a>Was ist ein *renderdurchlauf*?

Ein renderdurchlauf wird von diesen Elementen definiert.

- Ein Satz von Ausgabe Bindungen, die für die Dauer des Renderpass festgelegt sind. Diese Bindungen befinden sich in einer oder mehreren renderzielsichten (rtvs) und/oder in einer tiefen Schablonen Ansicht (DSV).
- Eine Liste von GPU-Vorgängen, die auf diesen Satz von Ausgabe Bindungen abzielen.
- Metadaten, die die Lade-/Speicherabhängigkeiten für alle Ausgabe Bindungen beschreiben, die auf den renderdurchlauf abzielen.

### <a name="declare-your-output-bindings"></a>Deklarieren der Ausgabe Bindungen

Am Anfang eines Renderpass deklarieren Sie Bindungen an die Renderziel (en) und/oder an ihren tiefen-/Stencil-Puffer. Es ist optional, eine Bindung an Renderziel (en) herzustellen, und es ist optional, eine Bindung an einen tiefen-oder Schablonen Puffer zu erstellen. Sie müssen jedoch mindestens eine Bindung an mindestens eine der beiden Bindungen herstellen, und im folgenden Codebeispiel binden wir an beides.

Sie deklarieren diese Bindungen in einem Aufrufen von [**ID3D12GraphicsCommandList4:: beginrenderpass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass).

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

Sie legen das erste Feld der [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) Struktur auf das CPU-Deskriptorhandle fest, das einer oder mehreren renderzielsichten (rtvs) entspricht. Entsprechend enthält [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) das CPU-Deskriptorhandle, das einer Sicht der tiefen Schablone (DSV) entspricht. Dabei handelt es sich um dieselben CPU-Deskriptorhandles, die Sie andernfalls an [**ID3D12GraphicsCommandList:: omantrendertargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)übergeben würden. Ebenso wie bei **omstrendertargets** werden die CPU-Deskriptoren zum Zeitpunkt des Aufrufens von **beginrenderpass** von ihren jeweiligen (CPU-Deskriptor-) Heaps abgedockt. 

Rtvs und DSV werden nicht in den renderdurchlauf geerbt. Stattdessen müssen Sie festgelegt werden. Ebenso wie die in **beginrenderpass** deklarierten rtvs und die DSV in der Befehlsliste weitergegeben wurden. Sie befinden sich vielmehr in einem nicht definierten Zustand nach dem Renderpass.

### <a name="render-passes-and-workloads"></a>Rendering-und Arbeits Auslastungen

Sie können renderpassungen nicht schachteln, und es ist nicht möglich, dass ein renderdurchlauf mehr als eine Befehlsliste überschreitet (Sie müssen beim Aufzeichnen in einer einzigen Befehlsliste beginnen und enden). Optimierungen, die für eine effiziente Generierung von Renderingvorgängen mit mehreren Threads entwickelt wurden, werden im Abschnitt weiter unten im Abschnitt [ renderingflags](#render-pass-flags)erläutert.

Ein Schreibvorgang, den Sie innerhalb eines Renderpass ausführen, ist für Sie bis zu einem nachfolgenden renderdurchlauf nicht *gültig* . Dies schließt einige Arten von Barrieren innerhalb des Renderings aus &mdash; , z. b. das verbarriering von **RENDER_TARGET** auf **SHADER_RESOURCE** auf dem momentan gebundenen Renderziel. Weitere Informationen finden Sie weiter unten im Abschnitt [Rendering-und Ressourcen Barrieren](#render-passes-and-resource-barriers).

Die einzige Ausnahme von der Schreib-Lese-Einschränkung, die gerade erwähnt wird, umfasst die impliziten Lesevorgänge, die als Teil des tiefen Tests und renderzielmischungen auftreten.
Diese APIs sind also innerhalb eines Renderpass nicht zulässig (die Core-Laufzeit entfernt die Befehlsliste, wenn Sie während der Aufzeichnung aufgerufen werden).

- [**ID3D12GraphicsCommandList1:: atomiccopybufferuint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)
- [**ID3D12GraphicsCommandList4:: beginrenderpass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass)
- [**ID3D12GraphicsCommandList:: cleardepthstencilview**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
- [**ID3D12GraphicsCommandList:: clearrendertargetview**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
- [**ID3D12GraphicsCommandList:: clearstate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
- [**ID3D12GraphicsCommandList:: clearunorderedaccessviewfloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
- [**ID3D12GraphicsCommandList:: clearunorderedaccessviewuint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
- [**ID3D12GraphicsCommandList:: copybufferregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
- [**ID3D12GraphicsCommandList:: copyresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
- [**ID3D12GraphicsCommandList:: copytextureregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
- [**ID3D12GraphicsCommandList:: copytiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
- [**ID3D12GraphicsCommandList::D iscardresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
- [**ID3D12GraphicsCommandList::D ispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
- [**ID3D12GraphicsCommandList:: omgtrendertargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
- [**ID3D12GraphicsCommandList:: resolvequerydata**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
- [**ID3D12GraphicsCommandList:: resolvesubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
- [**ID3D12GraphicsCommandList1:: resolvesubresourceregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion)
- [**ID3D12GraphicsCommandList3:: setprotectedresourcesession**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist3-setprotectedresourcesession)

### <a name="render-passes-and-resource-barriers"></a>Rendering und Ressourcen Barrieren

Ein Schreibvorgang, der innerhalb desselben Renderpass aufgetreten ist, kann nicht gelesen oder verwendet werden. Bestimmte Barrieren entsprechen nicht dieser Einschränkung, z. b. von **D3D12_RESOURCE_STATE_RENDER_TARGET** bis **\* _SHADER_RESOURCE** auf dem zurzeit gebundenen Renderziel (und die debugschicht führt zu diesem Effekt). Die gleiche Barriere für ein Renderziel, das *außerhalb* des aktuellen Renderpass geschrieben wurde, ist jedoch konform, da die Schreibvorgänge vor dem aktuellen renderdurchlauf abgeschlossen werden.
Sie können sich über bestimmte Optimierungen, die ein Anzeigetreiber in dieser Hinsicht treffen kann, in Kenntnis nehmen. Bei einer Übereinstimmung mit einer Übereinstimmung kann ein Anzeigetreiber eventuell alle in Ihrem renderdurchlauf gefundenen Barrieren an den Anfang des Renderpass verschieben. Dort können Sie zusammengefügt werden (und haben keine Auswirkungen auf das einarbeiten/klassifizieren). Dies ist eine gültige Optimierung, vorausgesetzt, dass alle Ihre Schreibvorgänge abgeschlossen sind, bevor der aktuelle renderdurchlauf gestartet wird.

Im folgenden finden Sie ein ausführeres Beispiel für die Treiber Optimierung, bei dem davon ausgegangen wird, dass Sie über ein Renderingmodul verfügen, das über einen Ressourcen Bindungs Entwurf vor dem Direct3D 12-Stil verfügt &mdash;  Beim Schreiben in eine ungeordnete Zugriffs Ansicht (UAV) bis zum Ende eines Frames (für die Verwendung im folgenden Frame) kann die Engine die Ressource möglicherweise im **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** Zustand am Ende des Frames belassen. Wenn die Engine im folgenden Frame die Ressource als Shader-Ressourcen Ansicht (SRV) bindet, wird feststellen, dass sich die Ressource nicht im richtigen Zustand befindet, und es wird eine Barriere von **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** auf **D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE** ausgegeben. Wenn diese Barriere im renderdurchlauf auftritt, wird der Anzeigetreiber so konfiguriert, dass er davon ausgeht, dass alle Schreibvorgänge bereits *außerhalb* dieses aktuellen renderlaufs stattgefunden haben. Folglich (und hier ist die Optimierung, in der die Optimierung erfolgt) kann der Anzeigetreiber die Barriere bis zum Anfang des renderdurchlaufs *verschieben* . Dies ist auch dann gültig, wenn der Code der in diesem Abschnitt und der letzten beschriebenen Schreib-/leseeinschränkung entspricht.


Dies sind Beispiele für konforme Barrieren.
- **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** **D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**.
- **D3D12_RESOURCE_STATE_COPY_DEST** **\* _SHADER_RESOURCE**.

Dies sind Beispiele für nicht konforme Barrieren.

- **D3D12_RESOURCE_STATE_RENDER_TARGET** in einen beliebigen Lese Zustand für aktuell gebundene rtvs/DSVs.
- **D3D12_RESOURCE_STATE_DEPTH_WRITE** in einen beliebigen Lese Zustand für aktuell gebundene rtvs/DSVs.
- Eine beliebige Aliasing Barriere.
- UAV-Barrieren (unsortierter Zugriffs Ansicht). 

### <a name="resource-access-declaration"></a>Deklaration des Ressourcen Zugriffs

Bei **beginrenderpass** und beim Deklarieren aller Ressourcen, die in diesem Durchlauf als rtvs und/oder DSV fungieren, müssen Sie auch deren Anfangs-und *endzugriffsmerkmale* angeben. Wie Sie im Codebeispiel im obigen Abschnitt [Deklarieren von Ausgabe Bindungen](#declare-your-output-bindings) sehen können, verwenden Sie die [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) -und [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) Strukturen.

Weitere Informationen finden Sie in den [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access) -und [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access) Strukturen und in den Enumerationen [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type) und [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type) .

### <a name="render-pass-flags"></a>Renderpassflags

Der letzte an **beginrenderpass** übergebene Parameter ist ein renderpassflag (ein Wert aus der [**D3D12_RENDER_PASS_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_flags) Enumeration).

```cppwinrt
enum D3D12_RENDER_PASS_FLAGS
{
    D3D12_RENDER_PASS_FLAG_NONE = 0,
    D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES = 0x1,
    D3D12_RENDER_PASS_FLAG_SUSPENDING_PASS = 0x2,
    D3D12_RENDER_PASS_FLAG_RESUMING_PASS = 0x4
};
```

#### <a name="uav-writes-within-a-render-pass"></a>UAV-Schreibvorgänge innerhalb eines Renderpass

UAV-Schreibvorgänge (unsortierter Zugriffs Ansicht) sind innerhalb eines Renderpass zulässig, aber Sie müssen explizit angeben, dass Sie UAV-Schreibvorgänge innerhalb des Renderpass ausgeben, indem Sie **D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES** angeben, sodass der Anzeigetreiber ggf. das Ticken deaktivieren kann.

UAV-Zugriffe müssen der oben beschriebenen Schreib-/leseeinschränkung folgen (Schreibvorgänge in einem renderdurchlauf können bis zu einem nachfolgenden renderdurchlauf nicht gelesen werden). UAV-Barrieren sind innerhalb eines Renderpass nicht zulässig.

UAV-Bindungen (über Stamm Tabellen oder Stamm Deskriptoren) werden in Rendering-Pässe geerbt und aus den Rendering-Durchläufen weitergegeben.

#### <a name="suspending-passes-and-resuming-passes"></a>Anhalten-übergibt und fortsetzen-übergibt

Sie können einen gesamten renderdurchlauf als einen anhaltedurchlauf und/oder einen fort Setz baren Durchlauf angeben. Ein "anhalten-gefolgt von a-fortsetzen"-paar muss über identische Sichten/Zugriffsflags zwischen den Durchläufen verfügen und möglicherweise keine zwischenzeitlichen GPU-Vorgänge (z. b. "zeichnet", "Dispatches", "verworfen", "löscht", "Kopien", "Update-Tile-Mappings", "Write-Buffer-unmittelates",

Der vorgesehene Anwendungsfall ist Multithread-Rendering, bei dem vier Befehlslisten (jeweils mit eigenen Renderingvorgängen) die gleichen Renderziele als Ziel haben können. Wenn die Rendering-Weitergabe über Befehlslisten hinweg angehalten/fortgesetzt wird, müssen die Befehlslisten in demselben Aufrufen von [**ID3D12CommandQueue:: executecommandlists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)ausgeführt werden.

Ein renderdurchlauf kann sowohl fortgesetzt als auch angehalten werden. Im soeben angegebenen Multithread-Beispiel werden die Befehlslisten 2 und 3 von 1 bis 2 fortgesetzt. 2 und 3 werden gleichzeitig auf 3 bzw. 4 ausgesetzt.

## <a name="query-for-render-passes-feature-support"></a>Abfrage für die Funktions Unterstützung von "Rendering"

Sie können " [**ID3D12Device:: checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) " anrufen, um das Ausmaß abzufragen, in dem ein Gerätetreiber und/oder die Hardware das Rendering von Vorgängen effizient unterstützt.

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

Aufgrund der Lauf Zeit-Mapping-Logik funktioniert Rendering immer. Abhängig von der Funktions Unterstützung bieten Sie jedoch nicht immer einen Vorteil. Sie können Code verwenden, der dem obigen Codebeispiel ähnelt, um zu bestimmen, ob es für Sie sinnvoll ist, Befehle als Renderpass auszugeben, und wenn es definitiv kein Vorteil ist (d. h., wenn die Laufzeit lediglich der vorhandenen API-Oberfläche entspricht). Die Durchführung dieser Überprüfung ist besonders wichtig, wenn Sie [D3D11On12](/windows/desktop/direct3d12/direct3d-11-on-12)verwenden).

Eine Beschreibung der drei Ebenen der Unterstützung finden Sie in der [**D3D12_RENDER_PASS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_tier) -Enumeration.
