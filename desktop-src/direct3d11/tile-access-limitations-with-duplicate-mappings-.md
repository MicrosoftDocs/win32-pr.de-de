---
title: Kachelzugriffseinschränkungen bei doppelten Zuordnungen
description: In diesem Abschnitt werden einschränkungen für den Zugriff auf Kacheln mit doppelten Zuordnungen beschrieben.
ms.assetid: 7A498E0D-9151-4A89-B7C3-C4F476457D17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ea4839b8115ccffe1993d767bc19d2d7c3db0c230aff65f8dd0fd9f74d3cad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124118"
---
# <a name="tile-access-limitations-with-duplicate-mappings"></a>Kachelzugriffseinschränkungen bei doppelten Zuordnungen

In diesem Abschnitt werden einschränkungen für den Zugriff auf Kacheln mit doppelten Zuordnungen beschrieben.

## <a name="copying-tiled-resources-with-overlapping-source-and-destination"></a>Kopieren von gekachelten Ressourcen mit überlappender Quelle und Ziel

Wenn Kacheln im Quell- und Zielbereich eines Kopiervorgang doppelte Zuordnungen im Kopierbereich haben, die sich auch dann überlappen würden, wenn beide Ressourcen keine gekachelten Ressourcen waren und der Kopiervorgang überlappende Kopien unterstützt, verhält sich der Kopiervorgang gut (als ob die Quelle vor dem Ziel an einen temporären Speicherort kopiert \* \* \* würde). Wenn die Überlappung jedoch nicht offensichtlich ist (z. B. die Quell- und Zielressourcen unterscheiden sich, aber Freigabezuordnungen oder Zuordnungen auf einer bestimmten Oberfläche dupliziert werden), sind die Ergebnisse des Kopiervorganges auf den freigegebenen Kacheln nicht definiert.

## <a name="copying-to-tiled-resource-with-duplicated-tiles-in-destination-area"></a>Kopieren in eine gekachelte Ressource mit duplizierten Kacheln im Zielbereich

Das Kopieren in eine kachelierte Ressource mit duplizierten Kacheln im Zielbereich führt zu nicht definierten Ergebnissen in diesen Kacheln, es sei denn, die Daten selbst sind identisch. Verschiedene Kacheln schreiben die Kacheln möglicherweise in unterschiedlichen Bestellungen.

## <a name="uav-accesses-to-duplicate-tiles-mappings"></a>UAV-Zugriffe auf zuordnungsduplizierte Kacheln

Angenommen, eine ungeordnete Zugriffsansicht (UAV) für eine gekachelte Ressource verfügt über doppelte Kachelzuordnungen in ihrem Bereich oder mit anderen Ressourcen, die an die Pipeline gebunden sind. Die Reihenfolge der Zugriffe auf diese duplizierten Kacheln ist nicht definiert, wenn sie von verschiedenen Threads ausgeführt wird, ebenso wie jede Reihenfolge des Speicherzugriffs auf UAVs im Allgemeinen ungeordnet ist.

## <a name="rendering-after-tile-mapping-changes-or-content-updates-from-outside-mappings"></a>Rendering nach Kachelzuordnungsänderungen oder Inhaltsaktualisierungen von externen Zuordnungen

Wenn sich die Kachelzuordnungen einer kachelgekachelten Ressource geändert haben oder der Inhalt in den Kacheln eines zugeordneten kachelgekachelten Pools über die Zuordnungen einer anderen kachelgekachelten Ressource geändert wurde und die gekachelte Ressource über die Renderzielansicht oder tiefen schablonenansicht gerendert wird, muss die Anwendung löschen (mithilfe der festen Funktion Clear-APIs) oder die Kacheln, die sich innerhalb des gerenderten Bereichs geändert haben (zugeordnet oder nicht), vollständig \* \* kopieren. Wenn eine Anwendung in diesen Fällen nicht löschen oder kopieren kann, führt dies dazu, dass Hardwareoptimierungsstrukturen für die gegebene Renderzielansicht oder Tiefen-Schablonenansicht veraltet sind. Dies führt zu Garbage Rendering-Ergebnissen auf hardware- und inkonsistenten Komponenten auf unterschiedlicher Hardware. Diese verborgenen Optimierungsdatenstrukturen, die von Hardware verwendet werden, sind möglicherweise lokal für einzelne Zuordnungen und für andere Zuordnungen zum gleichen Arbeitsspeicher nicht sichtbar.

Der [**Vorgang ID3D11DeviceContext1::ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview) unterstützt das Löschen von Renderzielansichten mit Rechtecke. Für Hardware, die gekachelte Ressourcen unterstützt, muss **ClearView** auch das Löschen von Tiefen-Schablonenansichten mit Rechtecke unterstützen, nur für Tiefenoberflächen (ohne Schablone). Mit diesem Vorgang können Anwendungen nur den erforderlichen Bereich einer Oberfläche löschen.

Wenn eine Anwendung vorhandene Speicherinhalte von Bereichen in einer gekachelten Ressource beibehalten muss, in denen sich Zuordnungen geändert haben, muss diese Anwendung die klare Anforderung umarbeiten. Die Anwendung kann diese Aufgabe ausführen, indem sie zuerst den Inhalt dort speichern, wo sich Kachelzuordnungen geändert haben (indem sie sie z. B. mithilfe von [**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)auf eine temporäre Oberfläche kopiert) und dann den erforderlichen clear-Befehl ausstellen und dann den Inhalt zurückkopieren. Dies würde zwar die Aufgabe erfüllen, Oberflächeninhalte für inkrementelles Rendering zu erhalten, der Nachteil ist jedoch, dass die nachfolgende Renderingleistung auf der Oberfläche möglicherweise darunter liegt, dass Renderingoptimierungen verloren gehen könnten.

Wenn eine Kachel gleichzeitig mehreren gekachelten Ressourcen zugeordnet wird und kachelinhalt auf beliebige Weise (Rendern, Kopieren und so weiter) über eine der gekachelten Ressourcen bearbeitet wird. Wenn dieselbe Kachel über eine andere gekachelte Ressource gerendert werden soll, muss die Kachel wie zuvor beschrieben zuerst wiederge löschen werden.

## <a name="rendering-to-tiles-shared-outside-render-area"></a>Rendern auf Kacheln, die außerhalb des Renderbereichs freigegeben sind

Angenommen, ein Bereich in einer gekachelten Ressource wird gerendert, und die Kachelpoolkacheln, auf die der Renderbereich verweist, werden auch von außerhalb des Renderbereichs zugeordnet (auch über andere gekachelte Ressourcen, zur gleichen Zeit oder nicht). Auf diesen Kacheln gerenderte Daten werden nicht ordnungsgemäß angezeigt, wenn sie über die anderen Zuordnungen angezeigt werden, obwohl das zugrunde liegende Speicherlayout kompatibel ist. Dies liegt an der Optimierung von Datenstrukturen, die von einigen Hardwarekomponenten verwendet werden, die lokal für einzelne Zuordnungen für renderbare Oberflächen sein können und für andere Zuordnungen zur gleichen Speicherposition nicht sichtbar sind. Sie können diese Einschränkung umgehen, indem Sie aus der gerenderten Zuordnung in alle anderen Zuordnungen in denselben Speicher kopieren, auf den zugegriffen werden kann (oder indem Sie diesen Arbeitsspeicher löschen oder andere Daten in ihn kopieren, wenn der alte Inhalt nicht mehr benötigt wird). Diese Arbeitsumgehung scheint zwar redundant zu sein, aber alle anderen Zuordnungen zum gleichen Speicher machen richtig verstehen, wie auf den Inhalt des Speichers zu zugreifen, und zumindest die Speichereinsparungen, die durch die Verwendung einer einzigen physischen Speicherbewegung erzielt werden, bleiben intakt. Wenn Sie zwischen verschiedenen kachelierten Ressourcen wechseln, die Zuordnungen gemeinsam nutzen (es sei denn, sie lesen nur), müssen Sie die [**ID3D11DeviceContext2::TiledResourceBarrier-API**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) zwischen den Switches aufrufen.

## <a name="rendering-to-tiles-shared-within-render-area"></a>Rendern auf Kacheln, die im Renderbereich freigegeben sind

Wenn ein Bereich in einer gekachelten Ressource gerendert wird und innerhalb des Renderbereichs mehrere Kacheln derselben Kachelpoolposition zugeordnet werden, sind die Renderingergebnisse auf diesen Kacheln nicht definiert.

## <a name="data-compatibility-across-tiled-resources-sharing-tiles"></a>Datenkompatibilität zwischen kachelierten Ressourcen, die Kacheln gemeinsam nutzen

Angenommen, mehrere gekachelte Ressourcen verfügen über Zuordnungen zu denselben Kachelpoolstandorten, und jede Ressource wird für den Zugriff auf dieselben Daten verwendet. Dieses Szenario ist nur gültig, wenn die anderen Regeln zum Vermeiden von Problemen mit Hardwareoptimierungsstrukturen vermieden werden, entsprechende Aufrufe von [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) vorgenommen werden und die gekachelten Ressourcen miteinander kompatibel sind. Letzteres wird hier in Bezug darauf beschrieben, was es bedeutet, dass kachelverkachelte Ressourcen, die Kacheln gemeinsam nutzen, inkompatibel sind. Die Inkompatibilitätsbedingungen für den Zugriff auf dieselben Daten über doppelte Kachelzuordnungen hinweg sind die Verwendung verschiedener Oberflächendimensionen oder -formate oder Unterschiede beim Vorhandensein von Renderziel- oder Tiefen-Schablonenbindungsflags für die Ressourcen. Das Schreiben in den Arbeitsspeicher mit einem Zuordnungstyp führt zu nicht definierten Ergebnissen, wenn Sie anschließend über eine Zuordnung aus einer inkompatiblen Ressource lesen oder rendern. Wenn die anderen Ressourcenfreigabezuordnungen zuerst mit neuen Daten initialisiert werden (Wiederverwendung des Arbeitsspeichers für einen anderen Zweck), ist der nachfolgende Lese- oder Rendervorgang in Ordnung, da die Daten nicht über inkompatible Interpretationen hinweg unkompatibel sind. Sie müssen jedoch die **TiledResourceBarrier-API** aufrufen, wenn Sie zwischen dem Zugriff auf inkompatible Zuordnungen wie diese wechseln.

Wenn das Bindungsflag für das Renderziel oder die Tiefen-Schablone für keine der Ressourcen festgelegt ist, die Zuordnungen miteinander teilen, gibt es deutlich weniger Einschränkungen. Solange das Format und die Oberflächentypen (z. B. Texture2D) identisch sind, können Kacheln freigegeben werden. Verschiedene Formate, die kompatibel sind, sind z. B. BC-Oberflächen und das entsprechende unkomprimierte 32-Bit- oder 16-Bit-Format pro Komponente, z. B. \* BC6H und R32G32B32A32. Viele 32-Bit-Formate pro Element können auch mit R32 aliasiert werden \_ \* (R10G10B10A2, \_ \* R8G8B8A8, \_ \* B8G8R8A8 \_ \* , B8G8R8X8 \_ \* ,R16G16); \_ \* dieser Vorgang war für nicht gekachelte Ressourcen immer zulässig.

Die Freigabe zwischen gepackten und nicht gepackten Kacheln ist in Ordnung, wenn die Formate kompatibel sind und die Kacheln mit Volltonfarbe gefüllt sind.

Wenn die Ressourcen, die Kachelzuordnungen gemeinsam nutzen, nicht gemeinsam genutzt werden, außer dass keine über Renderziel- oder Tiefen-Schablonenbindungsflags verfügen, kann nur mit 0 gefüllter Speicher sicher freigegeben werden. Die Zuordnung wird für die Definition des angegebenen Ressourcenformats als 0 decodiert angezeigt (in der Regel nur 0).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pipelinezugriff auf gekachelte Ressourcen](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




