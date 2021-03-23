---
title: Umdrehungen-Optimierungen der CPU-Barrierefreiheit und Standard-Swizzle
description: Die GPUs der Universal Memory Architecture (UMA) bieten einige Effizienzvorteile gegenüber diskreten GPUs, insbesondere bei der Optimierung mobiler Geräte.
ms.assetid: 26C41948-9625-4786-BBDF-552D1F8A2437
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47725702676d385d607fa87533680b9ffe0fc0df
ms.sourcegitcommit: 294c5ab750c46b5100bb2c84ef6c33ef7266c54b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "104548705"
---
# <a name="uma-optimizations-cpu-accessible-textures-and-standard-swizzle"></a>Umdrehungen-Optimierungen: auf die CPU zugreif Bare Texturen und standardend

Die GPUs der Universal Memory Architecture (UMA) bieten einige Effizienzvorteile gegenüber diskreten GPUs, insbesondere bei der Optimierung mobiler Geräte. Wenn Ressourcen CPU-Zugriff erhalten, wenn die GPU "Uma" ist, kann das Kopieren zwischen CPU und GPU reduziert werden. Obwohl es nicht empfehlenswert ist, dass Anwendungen den CPU-Zugriff auf alle Ressourcen in den UMA-Entwürfen Blind gewähren, können Sie die Effizienz verbessern, indem Sie die richtigen Ressourcen für den CPU-Zugriff Im Gegensatz zu diskreten GPUs kann die CPU technisch einen Zeiger auf alle Ressourcen aufweisen, auf die die GPU zugreifen kann.

-   [Übersicht über die verfügbaren CPU-Texturen](#overview-of-cpu-accessible-textures)
-   [Übersicht über Standard-Swizzle](#overview-of-standard-swizzle)
-   [APIs](#apis)
-   [Verwandte Themen](#related-topics)

## <a name="overview-of-cpu-accessible-textures"></a>Übersicht über die verfügbaren CPU-Texturen

Auf die CPU zugreif Bare Texturen in der Grafik Pipeline sind eine Funktion der UMA-Architektur, die CPUs Lese-und Schreibzugriff auf Texturen ermöglicht. Bei den gängigeren diskreten GPUs hat die CPU keinen Zugriff auf Texturen in der Grafik Pipeline.

Die allgemeine Empfehlung für Texturen besteht darin, diskrete GPUs zu integrieren. Dies umfasst in der Regel das Befolgen der Prozesse beim [Hochladen von Textur Daten über Puffer](upload-and-readback-of-texture-data.md), zusammengefasst als:

-   Kein CPU-Zugriff für die Mehrzahl der Texturen.
-   Das Textur Layout wird auf das D3D12 \_ Textur \_ Layout Unknown festgelegt \_ .
-   Hochladen der Texturen in die GPU mit [**copytextureregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

Allerdings können die CPU und GPU in bestimmten Fällen so häufig auf denselben Daten interagieren, dass die Zuordnung von Texturen hilfreich ist, um Energie zu sparen oder einen bestimmten Entwurf für bestimmte Adapter oder Architekturen zu beschleunigen. Anwendungen sollten diese Fälle erkennen und die unnötigen Kopien optimieren. Beachten Sie in diesem Fall die folgenden Punkte, um eine optimale Leistung zu erzielen:

-   Beginnen Sie nur mit der Unterhaltung einer besseren Leistung bei der Zuordnung von Texturen, wenn [**D3D12 \_ Feature \_ Data \_ Architecture**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture):: Uma true ist. Achten Sie dann auf *cachecoherentuma* , wenn Sie entscheiden, welche CPU-Cache Eigenschaften auf dem Heap ausgewählt werden sollen.

-   Die Nutzung des CPU-Zugriffs für Texturen ist komplizierter als für Puffer. Die effizientesten Textur Layouts für GPUs sind selten Zeilen \_ Haupt-. Tatsächlich können einige GPUs nur Zeilen haupttexturen unterstützen, \_ Wenn Textur Daten kopiert werden.

-   Die UMA-GPUs sollten universell von einer einfachen Optimierung profitieren, um die Ladezeiten der Ebene zu verringern. Nach dem Erkennen von Uma kann die Anwendung die ursprüngliche [**copytextureregion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) optimieren, um Texturen aufzufüllen, die von der GPU nicht geändert werden. Anstatt die Textur in einem Heap mit dem D3D12 \_ \_ -heaptyp \_ Default zu erstellen und die Textur Daten durch zu Marshalling, kann die Anwendung mithilfe von "Write Team Report [**Source**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) " das tatsächliche Textur Layout nicht verstehen.

-   In D3D12 sind Texturen, die mit D3D12 \_ Texture \_ Layout \_ Unknown und kein CPU-Zugriff erstellt wurden, für häufiges GPU-Rendering und Sampling am effizientesten. Beim Testen der Leistung sollten diese Texturen mit dem D3D12- \_ Textur \_ Layout \_ , das mit dem CPU-Zugriff unbekannt ist, und dem D3D12 \_ Texture \_ Layout \_ Standard- \_ Swizzle mit dem CPU-Zugriff verglichen werden, und D3D12 \_ Textur \_ Layout \_ Row \_ Major für Adapter übergreifende Unterstützung.

-   Die Verwendung \_ \_ des D3D12-Textur Layouts \_ Unknown mit dem CPU-Zugriff ermöglicht die Methoden " [**Beschreib tedesubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)", "read [**fromsubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)", " [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) " (Ausschluss des Anwendungs Zugriffs auf Zeiger) und "Aufheben der Zuordnung", kann jedoch die Effizienz des GPU-Zugriffs [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)

-   Die Verwendung des D3D12 \_ Texture \_ Layout \_ Standard- \_ swidels mit dem CPU-Zugriff ermöglicht das Schreiben von "Write- [**desubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)", "read [**fromsubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)" [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap), " [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) " (das einen gültigen Zeiger auf die Anwendung zurückgibt) Außerdem kann die Effizienz des GPU-Zugriffs mehr als D3D12 \_ Textur \_ Layout \_ Unknown durch den CPU-Zugriff geopfert werden.

## <a name="overview-of-standard-swizzle"></a>Übersicht über Standard-Swizzle

D3D12 (und D3D 11.3) stellen ein Standardmäßiges mehrdimensionales Datenlayout dar. Dies erfolgt, damit mehrere Verarbeitungseinheiten mit denselben Daten arbeiten können, ohne die Daten zu kopieren oder die Daten zwischen mehreren Layouts zu schwenken. Ein standardisiertes Layout ermöglicht Effizienzsteigerungen durch Netzwerkeffekte und ermöglicht es Algorithmen, kurze Einschnitte bei einem bestimmten Muster zu ermöglichen.

Eine ausführliche Beschreibung der Textur Layouts finden Sie unter [**D3D12 \_ Texture \_ Layout**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

Beachten Sie, dass es sich bei diesem Standard-Swizzle um eine Hardware Funktion handelt, die möglicherweise nicht von allen GPUs unterstützt wird.

Hintergrundinformationen zum Schwenken finden Sie in der [Z-Reihenfolge Kurve](https://en.wikipedia.org/wiki/Z-order_curve).

## <a name="apis"></a>APIs

Im Gegensatz zu D3D 11.3 unterstützt D3D12 standardmäßig die Textur Zuordnung, sodass es nicht erforderlich ist, [**D3D12 \_ Feature \_ Data \_ D3D12- \_ Optionen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)abzufragen. "D3D12" unterstützt jedoch nicht immer "Standard-Swizzle". diese Funktion muss mithilfe eines Aufrufens von [**checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) abgefragt und das *StandardSwizzle64KBSupported* -Feld der **D3D12 \_ Feature \_ Data D3D12- \_ \_ Optionen** überprüft werden.

Die folgenden APIs verweisen auf die Textur Zuordnung:

Enumerationen

-   [**D3D12 \_ Textur \_ Layout**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) : steuert das Schraffurmuster von Standard Texturen und ermöglicht die Unterstützung von Zuordnungen auf durch die CPU erreichbare Texturen.

Strukturen

-   [**D3D12 \_ Resource \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) Debug: Beschreibt eine Ressource, z. b. eine Textur, dies ist eine stark verwendete Struktur.
-   [**D3D12 \_ Heap \_ -Debugheap**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) : Beschreibt einen Heap.

Methoden

-   [**ID3D12Device:: kreatecommittedresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) : erstellt eine einzelne Ressource und einen Sicherungs Heap der richtigen Größe und Ausrichtung.
-   [**ID3D12Device:: kreateheap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap) : erstellt einen Heap für einen Puffer oder eine Textur.
-   [**ID3D12Device:: deateplacedresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) : erstellt eine Ressource, die sich in einem bestimmten Heap befindet, normalerweise eine schnellere Methode zum Erstellen einer Ressource als " [**samateheap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)".
-   [**ID3D12Device:: anatereservedresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource) : erstellt eine Ressource, die reserviert ist, aber noch nicht committet oder in einem Heap abgelegt wurde.
-   [**ID3D12CommandQueue:: updatetilemappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : aktualisiert Zuordnungen von Kachel Positionen in gekachelten Ressourcen zu Speicherorten in einem Ressourcenheap.
-   [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : Ruft einen Zeiger auf die angegebenen Daten in der Ressource ab und verweigert den GPU-Zugriff auf die untergeordnete Quelle.
-   [**ID3D12Resource:: getdebug**](id3d12resource-getdesc.md) : Ruft die Ressourcen Eigenschaften ab.
-   [**ID3D12Heap:: getdebug**](id3d12heap-getdesc.md) Ruft die Heap Eigenschaften ab.
-   Read [**fromsubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : kopiert Daten aus einer Textur, die mithilfe von [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)zugeordnet wurde.
-   [**Write-to-subresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : kopiert Daten in eine Textur, die mithilfe von [**map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)zugeordnet wurde.

Ressourcen und übergeordnete Heaps weisen Ausrichtungs Anforderungen auf:

-   D3D12 \_ standardmäßige \_ MSAA- \_ Ressourcen \_ Platzierungs \_ Ausrichtung (4 MB) für Multisample-Texturen.
-   D3D12 \_ standardmäßige \_ Ausrichtung der Ressourcen \_ Platzierung \_ (64 KB) für einzelne Beispiel Texturen und Puffer.
-   Das Kopieren von linearen unter Quellen muss an die Ausrichtung der D3D12- \_ Textur \_ Daten \_ \_ (512 Byte) ausgerichtet werden, wobei die Zeilengröße an der D3D12- \_ Textur \_ Daten- \_ einstellungsausrichtung \_ (256 Bytes) ausgerichtet wird.
-   Konstantenpuffersichten müssen an der Ausrichtung der D3D12- \_ Konstante \_ Puffer \_ Daten \_ \_ (256 Bytes) ausgerichtet werden.

Texturen, die kleiner als 64 KB sind, [**sollten über die**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)Datei "" von "" "" "".

Bei dynamischen Texturen (Texturen, die jeden Frame ändern) schreibt die CPU linear in den uploadheap, gefolgt von einem GPU-Kopiervorgang.

Zum Erstellen dynamischer Ressourcen erstellen Sie in der Regel einen großen Puffer in einem uploadheap (siehe [unter Zuordnung in Puffern](large-buffers.md)). Um Staging-Ressourcen zu erstellen, erstellen Sie einen großen Puffer in einem Read-Back-Heap. Um statische Standard Ressourcen zu erstellen, erstellen Sie angrenzende Ressourcen in einem Standard Heap. Erstellen Sie überlappende Ressourcen in einem Standard Heap, um standardmäßige Aliasing-Ressourcen zu erstellen.

" [**Write-desubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) " und "read [**fromsubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) " ordnen Textur Daten zwischen einem Zeilen Hauptlayout und einem nicht definierten Ressourcen Layout neu an. Der Vorgang ist synchron, sodass die Anwendung die CPU-Planung berücksichtigen muss. Die Anwendung kann den Kopiervorgang immer in kleinere Bereiche unterbrechen oder diesen Vorgang in einer anderen Aufgabe planen. MSAA-Ressourcen und tiefen Schablonen Ressourcen mit nicht transparenten Ressourcen Layouts werden von diesen CPU-Kopier Vorgängen nicht unterstützt. Dies führt zu einem Fehler. Formate, die keine Potenz von zwei Elementen aufweisen, werden ebenfalls nicht unterstützt, und es wird auch ein Fehler verursacht. Es können nicht genügend Arbeitsspeicher zurückgegeben werden.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[**Kern Konstanten**](constants.md)
</dt> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Ressourcen Bindung](resource-binding.md)
</dt> </dl>

 

 




