---
title: Verwenden von Ressourcen Barrieren zum Synchronisieren von Ressourcen Zuständen in Direct3D 12
description: Um die CPU-Gesamtauslastung zu reduzieren und das Multithreading und die Vorverarbeitung von Treibern zu ermöglichen, verschiebt Direct3D 12 die Verantwortung für die Ressourcen übergreifende Zustands Verwaltung vom Grafiktreiber zur Anwendung.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c766f18e85ab8acc2ed0afad8e680d566a723a68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104548741"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a>Verwenden von Ressourcen Barrieren zum Synchronisieren von Ressourcen Zuständen in Direct3D 12

Um die CPU-Gesamtauslastung zu reduzieren und das Multithreading und die Vorverarbeitung von Treibern zu ermöglichen, verschiebt Direct3D 12 die Verantwortung für die Ressourcen übergreifende Zustands Verwaltung vom Grafiktreiber zur Anwendung. Ein Beispiel für den ressourcenbezogenen Status ist, ob auf eine Textur Ressource zurzeit als über einen Shader Ressourcenansicht oder als renderzielansicht zugegriffen wird. In Direct3D 11 waren Treiber erforderlich, um diesen Zustand im Hintergrund zu verfolgen. Dies ist aus der CPU-Sicht aufwendig und erschwert jede Art von Multithreaded-Design erheblich. In Microsoft Direct3D 12 werden die meisten Ressourcen pro Ressourcen von der Anwendung mit einer einzigen API, [**ID3D12GraphicsCommandList:: resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier), verwaltet.

-   [Verwenden der resourcebarrier-API zum Verwalten des ressourcenbezogenen Zustands](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [Ressourcen Zustände](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [Anfängliche Zustände für Ressourcen](#initial-states-for-resources)
    -   [Ressourcen Zustands Einschränkungen für Lese-/Schreibzugriff](#readwrite-resource-state-restrictions)
    -   [Ressourcen Zustände für das darstellen von backpuffern](#resource-states-for-presenting-back-buffers)
    -   [Verwerfen von Ressourcen](#discarding-resources)
-   [Implizite Zustandsübergänge](#implicit-state-transitions)
    -   [Allgemeine Zustands herauf Stufung](#common-state-promotion)
    -   [Status Verfall in "Allgemein"](#state-decay-to-common)
    -   [Folgen für die Leistung](#performance-implications)
-   [Grenzen aufteilen](#split-barriers)
-   [Beispielszenario für Ressourcen Barriere](#resource-barrier-example-scenario)
-   [Beispiel für allgemeine Zustands herauf Stufung und-Verfall](#common-state-promotion-and-decay-sample)
-   [Beispiel für geteilte Barrieren](#example-of-split-barriers)
-   [Verwandte Themen](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a>Verwenden der resourcebarrier-API zum Verwalten des ressourcenbezogenen Zustands

[**Resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) benachrichtigt den Grafiktreiber über Situationen, in denen der Treiber möglicherweise mehrere Zugriffe auf den Speicher synchronisieren muss, in dem eine Ressource gespeichert wird. Die-Methode wird mit mindestens einer Ressourcen Barriere-Beschreibungs Struktur aufgerufen, die den Typ der zu deklarierten Ressourcen Barriere angibt.

Es gibt drei Arten von Ressourcen Barrieren:

-   **Übergangs Barriere** : eine Übergangs Barriere gibt an, dass ein Satz von untergeordneten Quellen zwischen unterschiedlichen Verwendungen übergeht. Eine [**D3D12- \_ Ressourcen \_ Übergangs \_ Barriere**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) -Struktur wird verwendet, um die unter Berichts Quelle sowie den Zustand *vor* und *nach* der untergeordneten Quelle anzugeben.

    Das System überprüft, ob die Übergängen von untergeordneten Quellen in einer Befehlsliste mit vorherigen Übergängen in derselben Befehlsliste konsistent sind. Die debugschicht verfolgt den Status der untergeordneten Quelle weiter, um andere Fehler zu finden. diese Überprüfung ist jedoch konservativ und nicht vollständig.

    Beachten Sie, dass Sie das Flag "D3D12 \_ Resource \_ Barrier \_ all unter Ressourcen" verwenden können, \_ um anzugeben, dass alle unter Ressourcen innerhalb einer Ressource übertragen werden.

-   **Aliasing-Barriere** : eine Aliasing-Barriere gibt einen Übergang zwischen der Verwendung von zwei verschiedenen Ressourcen an, die überlappende Zuordnungen in denselben Heap haben. Dies gilt für reservierte und Angestellte Ressourcen. Eine [**D3D12 \_ \_ ressourcenaliasing- \_ Barriere**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) wird verwendet, um die *vorher* -Ressource und die *after* -Ressource anzugeben.

    Beachten Sie, dass eine oder beide Ressourcen NULL sein können, was bedeutet, dass jede gekachelte Ressource Aliasing verursachen könnte. Weitere Informationen zum Verwenden von gekachelten Ressourcen finden Sie unter [gekachelte](../direct3d11/tiled-resources.md) Ressourcen und [Volumen Kachel Ressourcen](volume-tiled-resources.md).

-   **Ungeordnete Zugriffsansicht (UAV) Barriere** -eine UAV-Barriere gibt an, dass alle UAV-Zugriffe, sowohl Lese-als auch Schreibzugriff auf eine bestimmte Ressource, zwischen allen zukünftigen UAV-Zugriffen, sowohl Lese-als auch Schreibzugriff Es ist nicht erforderlich, dass eine APP eine UAV-Barriere zwischen zwei Draw-oder Dispatch-aufrufen platziert, die nur aus einer UAV gelesen werden. Außerdem ist es nicht erforderlich, eine UAV-Barriere zwischen zwei Draw-oder Dispatch-aufrufen zu platzieren, die in dieselbe UAV schreiben, wenn die Anwendung weiß, dass es sicher ist, dass der UAV-Zugriff in beliebiger Reihenfolge ausgeführt werden kann. Eine [**D3D12 \_ Resource \_ UAV- \_ Sperrungs**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) Struktur wird verwendet, um die UAV-Ressource anzugeben, für die die Barriere gilt. Die Anwendung kann für die UAV der Barriere NULL angeben. Dies bedeutet, dass jeder UAV-Zugriff die Barriere erfordern könnte.

Wenn [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) mit einem Array von Ressourcen Sperr Beschreibungen aufgerufen wird, verhält sich die API so, als ob Sie einmal für jedes Element in der Reihenfolge aufgerufen wurde, in der Sie bereitgestellt wurden.

Ein unter Bericht befindet sich zu einem beliebigen Zeitpunkt in genau einem Zustand, der durch den Satz von [**D3D12- \_ ressourcenstatusflags \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) festgelegt wird, die für [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)bereitgestellt werden. Die Anwendung muss sicherstellen, dass der Zustand *vor* und *nach* aufeinander folgender Aufrufe von **resourcebarrier** zustimmt.

> [!TIP]
>
> Anwendungen sollten nach Möglichkeit mehrere Übergänge in einen API-Befehl stapeln.

 

### <a name="resource-states"></a>Ressourcen Zustände

Eine umfassende Liste mit Ressourcen Zuständen, zwischen denen eine Ressource wechseln kann, finden Sie im Referenz Thema für die [**D3D12 \_ Resource \_ States**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) -Enumeration.

Informationen zu Teilen von Ressourcen Barrieren finden Sie auch unter [**D3D12 \_ \_ ressourcensperrenflags \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).

### <a name="initial-states-for-resources"></a>Anfängliche Zustände für Ressourcen

Ressourcen können mit einem beliebigen benutzerdefinierten Anfangszustand (gültig für die Ressourcen Beschreibung) mit den folgenden Ausnahmen erstellt werden:

-   Das Hochladen von Heaps muss im Zustand "State D3D12 \_ Resource \_ State Generic Read" beginnen. \_ \_ Dies ist eine bitweise OR-Kombination aus:
    -   D3D12 \_ Resource \_ State \_ -Scheitelpunkt \_ und \_ \_ Konstantenpuffer
    -   D3D12 \_ Resource \_ State \_ Index- \_ Puffer
    -   D3D12 \_ ressourcenstatuskopie- \_ \_ \_ Quelle
    -   D3D12 \_ Resource \_ State- \_ nicht-Pixel- \_ \_ Shader- \_ Ressource
    -   D3D12 \_ Resource \_ State- \_ Pixel- \_ Shader- \_ Ressource
    -   D3D12 \_ \_ \_ indirektes Argument des Ressourcen Zustands \_
-   Das Lesen von Heaps muss mit dem Status "D3D12 \_ Resource \_ State \_ Copy \_ dest" beginnen.
-   Austausch Ketten-Back-Puffer beginnen automatisch mit dem \_ allgemeinen Status des D3D12-Ressourcen \_ Zustands \_ .

Bevor ein Heap das Ziel eines GPU-Kopiervorgangs sein kann, muss der Heap normalerweise zuerst in den Zustand "D3D12 \_ Resource \_ State \_ Copy \_ dest" übergeht. Beim Hochladen von Heaps erstellte Ressourcen müssen jedoch in gestartet werden und können sich nicht vom generischen \_ Lese Zustand ändern, da nur die CPU Schreibvorgänge durchführt. Umgekehrt müssen in den Rückmeldungen erstellte Ressourcen mit zugesichertem Commit in gestartet werden und können sich nicht im Zustand "Kopie dest" ändern \_ .

### <a name="readwrite-resource-state-restrictions"></a>Ressourcen Zustands Einschränkungen für Lese-/Schreibzugriff

Die Verwendungs Bits des Ressourcen Zustands, die zur Beschreibung eines Ressourcen Status verwendet werden, sind in schreibgeschützte und Lese-/schreibzustände unterteilt. Das Referenz Thema für den [**D3D12 \_ - \_ Ressourcen**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) Status gibt die Lese-/Schreib-Zugriffsebene für jedes Bit in der-Enumeration an.

Höchstens ein Lese-/schreibbit kann für jede Ressource festgelegt werden. Wenn ein Schreib Bit festgelegt ist, kann für diese Ressource kein Schreib geschütztes Bit festgelegt werden. Wenn kein Schreib Bit festgelegt ist, kann eine beliebige Anzahl von gelesenen Bits festgelegt werden.

### <a name="resource-states-for-presenting-back-buffers"></a>Ressourcen Zustände für das darstellen von backpuffern

Bevor ein Hintergrund Puffer angezeigt wird, muss er sich im Status "D3D12 \_ Resource \_ State Common" befinden \_ . Beachten Sie, dass der Ressourcen Status D3D12 der \_ Ressourcen Status \_ \_ ist ein Synonym für den \_ allgemeinen D3D12 \_ -Ressourcen Status \_ und beide den Wert 0 aufweisen. Wenn [**idxgiswapchain::P Resent**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (oder [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) für eine Ressource aufgerufen wird, die sich zurzeit nicht in diesem Zustand befindet, wird eine debugebenenwarnung ausgegeben.

### <a name="discarding-resources"></a>Verwerfen von Ressourcen

Alle unter Ressourcen in einer Ressource müssen den \_ renderzielstatus oder den tiefen \_ Schreib Zustand für Renderziele/tiefen Schablone-Ressourcen aufweisen, wenn [**ID3D12GraphicsCommandList::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) aufgerufen wird.

## <a name="implicit-state-transitions"></a>Implizite Zustandsübergänge

Ressourcen können nur "höher gestuft" aus dem allgemeinen D3D12- \_ Ressourcen \_ Status werden \_ . Ebenso werden Ressourcen nur für den gemeinsamen D3D12- \_ Ressourcen \_ Status verwendet \_ .

### <a name="common-state-promotion"></a>Allgemeine Zustands herauf Stufung

Alle Puffer Ressourcen und Texturen mit dem D3D12- \_ \_ ressourcenflag \_ Allow \_ gleichzeitige \_ Zugriffs Kennzeichen werden implizit von dem D3D12- \_ Ressourcen Status herauf gestuft \_ \_ , der für den ersten GPU-Zugriff auf den entsprechenden Status festgelegt ist, einschließlich des generischen Lese Zugriffs, \_ um alle Lese Szenarien abzudecken. Auf jede Ressource im gemeinsamen Zustand kann zugegriffen werden, während Sie sich in einem einzelnen Zustand mit

<dl> 1 Schreibflag oder  
mindestens 1 leseflags  
</dl>

Ressourcen können basierend auf der folgenden Tabelle aus dem allgemeinen Status herauf gestuft werden:



| Statusflag                    | Erweiterbarer Zustand                             |                                      |
|-------------------------------|----------------------------------------------|--------------------------------------|
|                               | **Puffer-und Simultaneous-Access Texturen** | **Nicht gleichzeitige Zugriffs Texturen** |
| Vertex \_ und \_ konstanter \_ Puffer | Ja                                          | Nein                                   |
| Index \_ Puffer                 | Ja                                          | Nein                                   |
| \_Renderziel                | Ja                                          | Nein                                   |
| unsortierter \_ Zugriff             | Ja                                          | Nein                                   |
| Ausführlichere \_ Schreibvorgänge                  | Nein<sup>\*</sup>                              | No                                   |
| \_Lesetiefe                   | Nein<sup>\*</sup>                              | No                                   |
| nicht \_ Pixel- \_ Shader- \_ Ressource  | Ja                                          | Ja                                  |
| Pixel- \_ Shader- \_ Ressource       | Ja                                          | Ja                                  |
| Stream \_ ausgehend                   | Ja                                          | Nein                                   |
| indirektes \_ Argument            | Ja                                          | Nein                                   |
| Kopie \_ dest                    | Ja                                          | Ja                                  |
| \_Quelle kopieren                  | Ja                                          | Ja                                  |
| \_dest auflösen                 | Ja                                          | Nein                                   |
| \_Quelle auflösen               | Ja                                          | Nein                                   |
| Prädikation übersprungen                   | Ja                                          | Nein                                   |



 

<sup>\*</sup>Tiefen Schablonen Ressourcen müssen nicht gleichzeitig auf Texturen zugreifen und können daher nie implizit herauf gestuft werden.

Wenn dieser Zugriff auftritt, verhält sich die herauf Stufung wie eine implizite Ressourcen Barriere. Bei nachfolgenden Zugriffen werden Ressourcen Sperren benötigt, um den Ressourcen Status bei Bedarf zu ändern. Beachten Sie, dass die herauf Stufung von einem höher gestuften Lese Zustand in den Zustand "mehrere Lesevorgänge" gültig ist, dies jedoch nicht für Schreib Zustände gilt.  
Wenn z. b. eine Ressource im gemeinsamen Zustand in einem zeichnen-Befehl zu einer Pixel-Shader-Ressource herauf gestuft wird \_ \_ , kann Sie weiterhin zu NON_PIXEL \_ Shader- \_ Ressource herauf gestuft werden. Pixel- \_ Shader- \_ Ressource in einem anderen Draw-Befehl. Wenn Sie jedoch in einem Schreibvorgang, z. b. einem Kopier Ziel, verwendet wird, wird eine Ressourcen Zustands Übergangs Barriere von den kombinierten höher gestuften Lese Zuständen hier NON_PIXEL \_ Shader- \_ Ressource | Die Pixel- \_ Shader- \_ Ressource zum Kopieren der dest-Ressource \_ ist erforderlich.  
Ebenso muss bei herauf Stufung von Common zum Kopieren \_ dest noch eine Barriere von der Kopie \_ dest zum Renderziel gewechselt werden \_ .

Beachten Sie, dass die gemeinsame Zustands herauf Stufung "kostenlos" ist, da die GPU keine Synchronisierungs Wartezeiten ausführen muss. Die herauf Stufung stellt die Tatsache dar, dass Ressourcen im gemeinsamen Zustand keine zusätzliche GPU-Arbeit oder Treiber Nachverfolgung benötigen, um bestimmte Zugriffe zu unterstützen.

### <a name="state-decay-to-common"></a>Status Verfall in "Allgemein"

Die Kehrseite der allgemeinen herauf Stufung des Zustands wird wieder in den allgemeinen D3D12- \_ Ressourcen Status zurückversetzt \_ \_ . Ressourcen, die bestimmte Anforderungen erfüllen, werden als zustandslos angesehen und werden effektiv in den gemeinsamen Zustand zurückversetzt, wenn die GPU die Ausführung eines [**executecommandlists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) -Vorgangs beendet. Der Zerfall tritt nicht zwischen Befehlslisten auf, die gemeinsam im selben **executecommandlists** -Befehl ausgeführt werden.

Die folgenden Ressourcen verfallen, wenn ein [**executecommandlists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) -Vorgang auf der GPU abgeschlossen ist:

-   Ressourcen, auf die in einer Kopier Warteschlange zugegriffen wird, *oder*
-   Puffer Ressourcen für beliebige Warteschlangen Typen *oder*
-   Textur Ressourcen für beliebige Warteschlangen Typen, für die das D3D12- \_ \_ ressourcenflag das \_ \_ gleichzeitige \_ Zugriffsflag zulässt, *oder*
-   Alle Ressourcen, die implizit in einen schreibgeschützten Zustand herauf gestuft wurden.

Wie bei der allgemeinen herauf Stufung ist der Verfall in kostenlos, da keine zusätzliche Synchronisierung erforderlich ist. Durch die Kombination von Common State Promotion und Decay können viele unnötige [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) -Übergänge vermieden werden. In einigen Fällen kann dies erhebliche Leistungsverbesserungen bieten.

Puffer und Simultaneous-Access Ressourcen werden in den gemeinsamen Zustand übergehen, unabhängig davon, ob Sie explizit mithilfe von Ressourcen Barrieren oder implizit höher gestuft wurden.

### <a name="performance-implications"></a>Folgen für die Leistung

Beim Aufzeichnen expliziter [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) -Übergänge für Ressourcen im gemeinsamen Zustand ist es richtig, entweder "D3D12 \_ Resource \_ State \_ Common" oder einen beliebigen heraufstufbaren Zustand als " *beforestate* "-Wert in der D3D12- \_ Ressourcen \_ Übergangs \_ Barriere-Struktur zu verwenden. Dies ermöglicht eine herkömmliche Zustands Verwaltung, bei der der automatische Zerfall von Puffern und Texturen mit gleichzeitigem Zugriff ignoriert wird Dies ist jedoch möglicherweise nicht wünschenswert, da der Übergang von **resourcebarrier** -aufrufen mit Ressourcen, die bekanntermaßen den gemeinsamen Zustand aufweisen, die Leistung erheblich verbessern kann. Ressourcen Barrieren können teuer sein. Sie sind darauf ausgelegt, Cache Leerungen, Änderungen am Arbeitsspeicher Layout und andere Synchronisierungen zu erzwingen, die für Ressourcen, die sich bereits im gemeinsamen Zustand befinden, nicht erforderlich sind. Eine Befehlsliste, in der eine Ressourcen Barriere von einem nicht gemeinsamen Zustand zu einem anderen nicht allgemeinen Zustand für eine Ressource verwendet wird, die sich derzeit im gemeinsamen Status befindet, kann zu einem viel unbenötigten Aufwand führen.

Vermeiden Sie außerdem explizite [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) -Übergänge in \_ den D3D12-Ressourcen \_ Status, \_ sofern dies nicht unbedingt erforderlich ist (z. b. der nächste Zugriff auf eine Kopier Befehls Warteschlange, die erfordert, dass Ressourcen mit einem gemeinsamen Zustand beginnen). Übermäßige Übergänge in den gemeinsamen Status können die GPU-Leistung erheblich verlangsamen.

Versuchen Sie sich zusammenfassend, sich auf allgemeine Zustands herauf Stufung und-Verfall zu verlassen, wenn die Semantik Ihnen ermöglicht, keine [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) -Aufrufe auszugeben.

## <a name="split-barriers"></a>Grenzen aufteilen

Eine Ressourcen Übergangs Barriere mit dem Flag "D3D12 \_ Resource \_ Barrier \_ Flag \_ Begin \_ only" beginnt eine geteilte Barriere, und die Übergangs Barriere wird als ausstehend bezeichnet. Während der Barriere steht, kann die (Sub)-Ressource nicht von der GPU gelesen oder geschrieben werden. Die einzige zulässige Übergangs Barriere, die auf eine (Sub)-Ressource mit einer ausstehenden Barriere angewendet werden kann, ist eine, die *vor* und *nach* den Zuständen gleich ist, und das \_ Flag D3D12 Resource \_ Barrier \_ Flag \_ End \_ only, das die Grenze für den ausstehenden Übergang abschließt.

Geteilte Barrieren stellen Hinweise für die GPU bereit, dass eine Ressource in Bundesland *a* später später in Bundesland *B* verwendet wird. Dadurch kann die GPU die Übergangs Arbeitsauslastung optimieren und Ausführungs Staus möglicherweise verringern oder eliminieren. Das Ausstellen der reinen Sperre gewährleistet, dass alle GPU-Übergangs Aufgaben abgeschlossen sind, bevor Sie mit dem nächsten Befehl fortfahren.

Die Verwendung von Teilungs Barrieren kann zur Verbesserung der Leistung beitragen, insbesondere in Szenarios mit mehreren Engines oder bei der Umstellung von Ressourcen mit Lese-/Schreibzugriff in einer oder mehreren Befehlslisten.

## <a name="resource-barrier-example-scenario"></a>Beispielszenario für Ressourcen Barriere

Die folgenden Code Ausschnitte zeigen die Verwendung der [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) -Methode in einem Multithreading-Beispiel.

Erstellen der Ansicht "tiefen Schablone", die in einen beschreibbaren Zustand übergeht.


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



Erstellen der vertexpufferansicht, ändern Sie Sie zuerst von einem gemeinsamen Zustand in ein Ziel und dann von einem Ziel in einen generischen lesbaren Zustand.


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



Erstellen der Index Puffer Ansicht, ändern Sie Sie zuerst von einem gemeinsamen Zustand in ein Ziel und dann von einem Ziel in einen allgemeinen lesbaren Zustand.


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



Erstellen von Texturen und Shader-Ressourcen Ansichten. Die Textur wird von einem gemeinsamen Zustand in ein Ziel und dann von einem Ziel zu einer Pixel-Shader-Ressource geändert.


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



Beginnen eines Frames Dadurch wird nicht nur [**resourcebarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) verwendet, um anzugeben, dass der Swapkette als Renderziel verwendet werden soll, sondern auch die Frame-Ressource initialisiert (die **resourcebarrier** für den tiefen Schablone-Puffer aufruft).


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



Das Beenden eines Frames, der angibt, dass der Hintergrund Puffer jetzt verwendet wird.


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



Beim Initialisieren einer Frame Ressource, die beim Starten eines Frames aufgerufen wird, wird der tiefen Schablone-Puffer in einen beschreibbaren Puffer übergegangen.


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



Barrieren werden Mid-Frame ausgetauscht, wobei die Schatten Zuordnung vom beschreibbaren in lesbar ist.


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



"Finish" wird aufgerufen, wenn ein Frame beendet wird, wobei die Schatten Zuordnung in einen gemeinsamen Zustand übergeht.


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a>Beispiel für allgemeine Zustands herauf Stufung und-Verfall

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a>Beispiel für geteilte Barrieren

Im folgenden Beispiel wird gezeigt, wie Sie eine geteilte Barriere zum Reduzieren von Pipeline Ständen verwenden können. Der folgende Code verwendet keine Splitter Barrieren:

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

Der folgende Code verwendet geteilte Barrieren:

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a>Verwandte Themen

[Video-Tutorials zu DirectX Advanced Learning: Ressourcen Barrieren und Zustandsüberwachung](https://www.youtube.com/watch?v=nmB2XMasz2o)

[Multi-Engine-Synchronisierung](./user-mode-heap-synchronization.md)

[Arbeits Übermittlung in Direct3D 12](command-queues-and-command-lists.md)

[Ein Einblick in D3D12 Ressourcen Zustands Barrieren](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

