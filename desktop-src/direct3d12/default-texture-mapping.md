---
title: UMA-Optimierungen CPU-zugängliche Texturen und Swizzle Standard
description: Universal Memory Architecture (UMA)-GPUs bieten einige Effizienzvorteile gegenüber diskreten GPUs, insbesondere bei der Optimierung für mobile Geräte.
ms.assetid: 26C41948-9625-4786-BBDF-552D1F8A2437
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2624a300811b4d4a1eef70873a31af89b0546224fd9b4f3ba06ecb1fbd2fac42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894670"
---
# <a name="uma-optimizations-cpu-accessible-textures-and-standard-swizzle"></a>UMA-Optimierungen: Barrierefreie CPU-Texturen und Swizzle-Standardtest

Universal Memory Architecture (UMA)-GPUs bieten einige Effizienzvorteile gegenüber diskreten GPUs, insbesondere bei der Optimierung für mobile Geräte. Wenn Ressourcen CPU-Zugriff erhalten, wenn die GPU UMA ist, kann der Kopieraufwand zwischen CPU und GPU reduziert werden. Es wird zwar nicht empfohlen, anwendungen blind CPU-Zugriff auf alle Ressourcen in UMA-Entwürfen zu geben, aber es gibt Möglichkeiten, die Effizienz zu verbessern, indem sie den richtigen RESSOURCEN CPU-Zugriff bieten. Im Gegensatz zu diskreten GPUs kann die CPU technisch gesehen einen Zeiger auf alle Ressourcen haben, auf die die GPU zugreifen kann.

-   [Übersicht über CPU-zugängliche Texturen](#overview-of-cpu-accessible-textures)
-   [Übersicht über Swizzle Standard](#overview-of-standard-swizzle)
-   [APIs](#apis)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-cpu-accessible-textures"></a>Übersicht über CPU-zugängliche Texturen

CPU-zugängliche Texturen in der Grafikpipeline sind ein Feature der UMA-Architektur, das CPUs Lese- und Schreibzugriff auf Texturen ermöglicht. Bei gängigeren diskreten GPUs hat die CPU keinen Zugriff auf Texturen in der Grafikpipeline.

Der allgemeine Best Practice-Rat für Texturen ist die Aufnahme diskreter GPUs. Dies umfasst in der Regel das Folgen der Prozesse unter Hochladen von [Texturdaten](upload-and-readback-of-texture-data.md)über Puffer, zusammengefasst als:

-   Der Großteil der Texturen hat keinen CPU-Zugriff.
-   Festlegen des Texturlayouts auf D3D12 \_ TEXTURE \_ LAYOUT \_ UNKNOWN.
-   Hochladen der Texturen auf die GPU mit [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

In bestimmten Fällen können CPU und GPU jedoch so häufig mit denselben Daten interagieren, dass Zuordnungstexturen hilfreich sind, um Energie zu sparen oder ein bestimmtes Design auf bestimmten Adaptern oder Architekturen zu beschleunigen. Anwendungen sollten diese Fälle erkennen und die unnötigen Kopien optimieren. Berücksichtigen Sie in diesem Fall Folgendes, um eine optimale Leistung zu erzielen:

-   Beginnen Sie erst dann, wenn [**D3D12 \_ FEATURE \_ DATA \_ ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture)::UMA true ist, um die bessere Leistung von Zuordnungstexturen zu erzielen. Achten Sie dann auf *CacheCoherentUMA,* wenn Sie entscheiden, welche CPU-Cacheeigenschaften sie auf dem Heap auswählen möchten.

-   Die Nutzung des CPU-Zugriffs für Texturen ist komplizierter als bei Puffern. Die effizientesten Texturlayouts für GPUs sind selten \_ Zeilen-Hauptlayouts. Tatsächlich können einige GPUs beim Kopieren von Texturdaten nur \_ Zeilen-Haupttexturen unterstützen.

-   UMA-GPUs sollten universell von einer einfachen Optimierung profitieren, um Ladezeiten auf Ebene zu reduzieren. Nach der Erkennung von UMA kann die Anwendung die anfängliche [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) optimieren, um Texturen zu füllen, die die GPU nicht ändert. Anstatt die Textur in einem Heap mit D3D12 HEAP TYPE DEFAULT zu erstellen und die Texturdaten zu marshallen, kann die Anwendung \_ \_ \_ [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) verwenden, um ein Verständnis des tatsächlichen Texturlayouts zu vermeiden.

-   In D3D12 sind Texturen, die mit D3D12 TEXTURE LAYOUT UNKNOWN und ohne CPU-Zugriff erstellt wurden, am effizientesten für \_ \_ \_ häufiges GPU-Rendering und -Sampling. Bei Leistungstests sollten diese Texturen mit D3D12 TEXTURE LAYOUT UNKNOWN mit \_ \_ \_ CPU-Zugriff und D3D12 \_ TEXTURE LAYOUT STANDARD \_ \_ \_ SWIZZLE mit \_ \_ \_ CPU-Zugriff und D3D12 TEXTURE LAYOUT ROW \_ MAJOR für adapterübergreifende Unterstützung verglichen werden.

-   Die Verwendung von D3D12 TEXTURE LAYOUT UNKNOWN mit CPU-Zugriff ermöglicht die Methoden \_ \_ \_ [**WriteToSubresource,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) [**ReadFromSubresource,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (anwendungszugriff auf Zeiger wird einschließen) und [**Unmap.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)Dies kann jedoch die Effizienz des GPU-Zugriffs verfeinern.

-   Die Verwendung von D3D12 TEXTURE LAYOUT STANDARD SWIZZLE mit CPU-Zugriff ermöglicht \_ \_ \_ \_ [**WriteToSubresource,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) [**ReadFromSubresource,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (die [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)einen gültigen Zeiger auf die Anwendung zurückgibt) und Unmap . Es kann auch die Effizienz des GPU-Zugriffs mehr als D3D12 \_ TEXTURE LAYOUT UNKNOWN mit \_ \_ CPU-Zugriff einschleusen.

## <a name="overview-of-standard-swizzle"></a>Übersicht über Swizzle Standard

D3D12 (und D3D11.3) führen ein mehrdimensionales Standarddatenlayout ein. Dies wird durchgeführt, damit mehrere Verarbeitungseinheiten mit denselben Daten arbeiten können, ohne die Daten zu kopieren oder zwischen mehreren Layouts zu wischen. Ein standardisiertes Layout ermöglicht Effizienzsteigerungen durch Netzwerkeffekte und ermöglicht Es Algorithmen, unter Annahme eines bestimmten Musters Kurzeinschnitte zu treffen.

Eine ausführliche Beschreibung der Texturlayouts finden Sie unter [**D3D12 \_ TEXTURE \_ LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

Beachten Sie jedoch, dass es sich bei diesem Standard-Swizzle um ein Hardwarefeature handelt, das möglicherweise nicht von allen GPUs unterstützt wird.

Hintergrundinformationen zum Swizzling finden Sie unter [Z-Order Curve](https://en.wikipedia.org/wiki/Z-order_curve).

## <a name="apis"></a>APIs

Im Gegensatz zu D3D11.3 unterstützt D3D12 standardmäßig die Texturzuordnung, sodass [**D3D12 \_ FEATURE \_ DATA \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)nicht abfragen muss. D3D12 unterstützt jedoch nicht immer standard swizzle. Dieses Feature muss mit einem Aufruf von [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) abgefragt werden und das Feld *StandardSwizzle64KBSupported* von **D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS** überprüfen.

Die folgenden APIs verweisen auf textur mapping:

Enumerationen

-   [**D3D12 \_ \_TEXTURLAYOUT:**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) Steuert das Swizzle-Muster von Standardtexturen und aktiviert die Kartenunterstützung für CPU-zugängliche Texturen.

Strukturen

-   [**D3D12 \_ RESOURCE \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) Beschreibt eine Ressource, z. B. eine Textur. Dies ist eine häufig verwendete Struktur.
-   [**D3D12 \_ HEAP \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) Beschreibt einen Heap.

Methoden

-   [**ID3D12Device::CreateCommittedResource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) Erstellt eine einzelne Ressource und einen Hintergrundhap der richtigen Größe und Ausrichtung.
-   [**ID3D12Device::CreateHeap:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap) Erstellt einen Heap für einen Puffer oder eine Textur.
-   [**ID3D12Device::CreatePlacedResource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) Erstellt eine Ressource, die in einem bestimmten Heap platziert wird, in der Regel eine schnellere Methode zum Erstellen einer Ressource als [**CreateHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap).
-   [**ID3D12Device::CreateReservedResource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource) Erstellt eine Ressource, die reserviert ist, aber noch nicht gebunden oder in einem Heap platziert wurde.
-   [**ID3D12CommandQueue::UpdateTileMappings:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) Aktualisiert Zuordnungen von Kachelspeicherorten in gekachelten Ressourcen zu Speicherorten in einem Ressourcenhap.
-   [**ID3D12Resource::Map:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) Ruft einen Zeiger auf die angegebenen Daten in der Ressource ab und verweigert dem GPU-Zugriff auf die Unterressource.
-   [**ID3D12Resource::GetDesc:**](id3d12resource-getdesc.md) Ruft die Ressourceneigenschaften ab.
-   [**ID3D12Heap::GetDesc**](id3d12heap-getdesc.md) ruft die Heapeigenschaften ab.
-   [**ReadFromSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) Kopiert Daten aus einer Textur, die mit map zugeordnet [**wurde.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)
-   [**WriteToSubresource:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) Kopiert Daten in eine Textur, die mit map zugeordnet [**wurde.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)

Für Ressourcen und übergeordnete Heaps gelten Ausrichtungsanforderungen:

-   D3D12 \_ DEFAULT \_ MSAA RESOURCE PLACEMENT ALIGNMENT \_ \_ \_ (4MB) für Texturen mit mehreren Stichproben.
-   D3D12 \_ DEFAULT RESOURCE PLACEMENT ALIGNMENT \_ \_ (64 KB) für einzelne \_ Beispieltexturen und Puffer.
-   Das lineare Kopieren von Unterressourcen muss an D3D12 TEXTURE DATA PLACEMENT ALIGNMENT (512 Byte) ausgerichtet werden, bei dem die Zeilenhöhe an \_ \_ \_ \_ D3D12 \_ TEXTURE DATA PITCH ALIGNMENT \_ \_ \_ (256 Byte) ausgerichtet ist.
-   Konstante Pufferansichten müssen an D3D12 \_ CONSTANT BUFFER DATA PLACEMENT ALIGNMENT \_ \_ \_ \_ (256 Bytes) ausgerichtet werden.

Texturen, die kleiner als 64 KB sind, sollten über [**CreateCommittedResource verarbeitet werden.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)

Bei dynamischen Texturen (Texturen, die jeden Frame ändern) schreibt die CPU linear in den Upload-Heap, gefolgt von einem GPU-Kopiervorgang.

In der Regel erstellen Sie zum Erstellen dynamischer Ressourcen einen großen Puffer in einem Uploadhap (siehe [Unterzuordnung innerhalb von Puffern](large-buffers.md)). Erstellen Sie zum Erstellen von Stagingressourcen einen großen Puffer in einem Readback-Heap. Um statische Standardressourcen zu erstellen, erstellen Sie angrenzende Ressourcen in einem Standardhap. Um Standardmäßige Aliasressourcen zu erstellen, erstellen Sie überlappende Ressourcen in einem Standardhap.

[**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) und [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) ordnen Texturdaten zwischen einem Zeilen-Hauptlayout und einem nicht definierten Ressourcenlayout neu an. Der Vorgang ist synchron, daher sollte die Anwendung die CPU-Planung im Hinterkopf behalten. Die Anwendung kann das Kopieren immer in kleinere Regionen aufbrechen oder diesen Vorgang in einer anderen Aufgabe planen. MSAA-Ressourcen und Tiefen-Schablonenressourcen mit nicht transparenten Ressourcenlayouts werden von diesen CPU-Kopiervorgängen nicht unterstützt und verursachen einen Fehler. Formate, die keine Zwei-Elemente-Größe haben, werden ebenfalls nicht unterstützt und verursachen auch einen Fehler. Es können Nicht genügend Arbeitsspeicher-Rückgabecodes auftreten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Kernkonst constants**](constants.md)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Ressourcenbindung](resource-binding.md)
</dt> </dl>

 

 




