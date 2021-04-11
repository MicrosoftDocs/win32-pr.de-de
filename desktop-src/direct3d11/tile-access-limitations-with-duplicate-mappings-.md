---
title: Kachelzugriffseinschränkungen bei doppelten Zuordnungen
description: In diesem Abschnitt werden Kachel Zugriffs Einschränkungen mit doppelten Zuordnungen beschrieben.
ms.assetid: 7A498E0D-9151-4A89-B7C3-C4F476457D17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0909b0d10e286e5f774f6893b692abdeb19d3ef7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036484"
---
# <a name="tile-access-limitations-with-duplicate-mappings"></a>Kachelzugriffseinschränkungen bei doppelten Zuordnungen

In diesem Abschnitt werden Kachel Zugriffs Einschränkungen mit doppelten Zuordnungen beschrieben.

## <a name="copying-tiled-resources-with-overlapping-source-and-destination"></a>Kopieren von Kachel Ressourcen mit überlappenden Quellen und Zielen

Wenn Kacheln im Quell-und Zielbereich eines Kopier \* Vorgangs duplizierte Zuordnungen im Kopier Bereich aufweisen, die sich überlappen würden, auch wenn beide Ressourcen nicht gekachelte Ressourcen wären und der Kopier \* Vorgang überlappende Kopien unterstützt, verhält sich der Kopier \* Vorgang problemlos (als ob die Quelle vor dem Wechseln an einen temporären Speicherort kopiert wird). Wenn die Überschneidung jedoch nicht offensichtlich ist (weil die Quell-und Ziel Ressourcen unterschiedlich sind, aber Freigabe Zuordnungen oder Zuordnungen über eine bestimmte Oberfläche dupliziert werden), sind die Ergebnisse des Kopiervorgangs auf den freigegebenen Kacheln nicht definiert.

## <a name="copying-to-tiled-resource-with-duplicated-tiles-in-destination-area"></a>Kopieren in eine Kachel Ressource mit duplizierten Kacheln im Zielbereich

Beim Kopieren in eine Kachel Ressource mit doppelten Kacheln im Zielbereich werden in diesen Kacheln nicht definierte Ergebnisse erzeugt, es sei denn, die Daten selbst sind identisch. unterschiedliche Kacheln können die Kacheln in verschiedenen Reihen folgen schreiben.

## <a name="uav-accesses-to-duplicate-tiles-mappings"></a>UAV-Zugriffe auf doppelte Kacheln Zuordnungen

Angenommen, eine ungeordnete Zugriffs Ansicht (UAV) auf einer gekachelten Ressource verfügt über doppelte Kachel Zuordnungen in Ihrem Bereich oder mit anderen Ressourcen, die an die Pipeline gebunden sind. Die Reihenfolge der Zugriffe auf diese duplizierten Kacheln ist nicht definiert, wenn Sie von unterschiedlichen Threads durchgeführt wird, ebenso wie jede beliebige Reihenfolge des Speicherzugriffs auf die UAVs im Allgemeinen nicht

## <a name="rendering-after-tile-mapping-changes-or-content-updates-from-outside-mappings"></a>Rendering nach Änderungen der Kachel Zuordnung oder Inhalts Aktualisierungen von externen Zuordnungen

Wenn sich die Kachel Zuordnungen einer Kachel Ressource geändert haben oder sich der Inhalt in zugeordneten Kacheln im gekachelten Pool über die Zuordnungen einer anderen Kachel Ressource geändert hat, und die gekachelte Ressource wird über die renderzielsicht oder die Ansicht der tiefen Schablone gerendert. die Anwendung muss (mit der Funktion "Clear" der Fixed-Funktion) oder vollständig mit Copy/Update-APIs kopiert werden, um \* \* die Kacheln zu löschen, die sich innerhalb des gerenderten Bereichs geändert haben (zugeordnete Wenn eine Anwendung in diesen Fällen nicht gelöscht oder kopiert werden kann, führt dies dazu, dass die Hardware Optimierungs Strukturen für die angegebene renderzielsicht oder die Ansicht der tiefen Schablone veraltet sind und das Garbage Rendering zu Hardware und Inkonsistenz auf verschiedenen Hardware Ergebnissen führt. Diese ausgeblendeten Optimierungs Datenstrukturen, die von der Hardware verwendet werden, können für einzelne Zuordnungen lokal sein und sind für andere Zuordnungen im gleichen Speicher nicht sichtbar.

Der [**ID3D11DeviceContext1:: Clearview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview) -Vorgang unterstützt das Löschen von renderzielsichten mit Rechtecke. Für Hardware, die gekachelte Ressourcen unterstützt, muss **Clearview** auch das Löschen von tiefen Schablonen Ansichten mit Rechtecke unterstützen, für nur tiefe Oberflächen (ohne Schablone). Dieser Vorgang ermöglicht es Anwendungen, nur den erforderlichen Bereich einer Oberfläche zu löschen.

Wenn eine Anwendung vorhandenen Speicherinhalt von Bereichen in einer gekachelten Ressource beibehalten muss, in der sich die Zuordnungen geändert haben, muss diese Anwendung die klare Anforderung umgehen. Die Anwendung kann diese Problem Umgehung erreichen, indem zuerst der Inhalt gespeichert wird, in dem sich die Kachel Zuordnungen geändert haben (indem Sie auf eine temporäre Oberfläche kopiert werden, z. b. mithilfe von [**ID3D11DeviceContext2:: copytiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)), indem der erforderliche Clear-Befehl ausgegeben und der Inhalt anschließend wieder kopiert wird. Dies würde dazu führen, dass der Inhalt für das inkrementelle Rendering vollständig beibehalten wird. der Nachteil ist jedoch, dass die nachfolgende Renderingleistung auf der Oberfläche beeinträchtigt werden kann, da renderoptimierungen

Wenn eine Kachel gleichzeitig mehreren gekachelten Ressourcen zugeordnet ist und der Inhalt der Kachel auf irgendeine Weise (Rendern, kopieren usw.) über eine der gekachelten Ressourcen manipuliert wird, muss die Kachel zunächst wie zuvor beschrieben gelöscht werden, wenn die Kachel über eine beliebige andere Kachel Ressource gerendert werden soll.

## <a name="rendering-to-tiles-shared-outside-render-area"></a>Rendern von Kacheln, die außerhalb des renderbereichs

Angenommen, ein Bereich in einer gekachelten Ressource wird in gerendert, und die Kacheln des Kachel Pools, auf die durch den Renderbereich verwiesen wird, werden auch außerhalb des renderbereichs (einschließlich der gleichzeitig über andere gekachelten Ressourcen) zugeordnet. Daten, die auf diesen Kacheln gerendert werden, werden bei der Anzeige durch die anderen Zuordnungen nicht garantiert ordnungsgemäß angezeigt, auch wenn das zugrunde liegende Speicher Layout kompatibel ist Dies liegt an Optimierungs Datenstrukturen, bei denen es sich um Hardware Anwendungen handelt, die für einzelne Zuordnungen für renderbare Oberflächen lokal sein können und für andere Zuordnungen nicht an derselben Speicheradresse sichtbar sind. Sie können diese Einschränkung umgehen, indem Sie aus der gerenderten Zuordnung zu allen anderen Zuordnungen in denselben Speicher kopieren, auf den möglicherweise zugegriffen wird (oder den Speicher löschen oder andere Daten kopieren, wenn der alte Inhalt nicht mehr benötigt wird). Obwohl diese Problem Umgehung redundant erscheint, werden alle anderen Zuordnungen in denselben Speicher ordnungsgemäß verstanden, wie auf Ihre Inhalte zugegriffen werden kann, und zumindest die Arbeitsspeicher Einsparung, bei der nur eine einzige physische Arbeitsspeicher Unterstützung vorhanden ist. Außerdem müssen Sie die [**ID3D11DeviceContext2:: tiledresourcebarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) -API zwischen den Switches aufrufen, wenn Sie zwischen der Verwendung verschiedener Kachel Ressourcen wechseln, die Zuordnungen gemeinsam verwenden (es sei denn, es wird nur gelesen).

## <a name="rendering-to-tiles-shared-within-render-area"></a>Rendering in Kacheln, die im Renderbereich verwendet werden

Wenn ein Bereich in einer gekachelten Ressource in gerendert wird und innerhalb des renderbereichs mehrere Kacheln demselben Kachel Pool Speicherort zugeordnet sind, werden renderingergebnisse auf diesen Kacheln nicht definiert.

## <a name="data-compatibility-across-tiled-resources-sharing-tiles"></a>Daten Kompatibilität zwischen gekachelten Ressourcen gemeinsam mit Kacheln

Angenommen, mehrere Kachel Ressourcen haben Zuordnungen zu denselben Kachel Pool Standorten, und jede Ressource wird für den Zugriff auf dieselben Daten verwendet. Dieses Szenario ist nur gültig, wenn die anderen Regeln zur Vermeidung von Problemen mit Hardware Optimierungs Strukturen vermieden werden, die entsprechenden Aufrufe von [**ID3D11DeviceContext2:: tiledresourcebarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) vorgenommen werden und die gekachelten Ressourcen miteinander kompatibel sind. Letzteres wird hier in Bezug auf die Bedeutung der Kachel Ressourcen beschrieben, die Kacheln gemeinsam nutzen, damit Sie nicht kompatibel sind. Die Inkompatibilitäts Bedingungen für den Zugriff auf die gleichen Daten über doppelte Kachel Zuordnungen sind die Verwendung unterschiedlicher Oberflächen Dimensionen oder des Formats oder Unterschiede bei der Verwendung von Renderziel-oder tiefen Schablone-Bindungs Flags für die Ressourcen. Das Schreiben in den Arbeitsspeicher mit einer Art von Zuordnung erzeugt nicht definierte Ergebnisse, wenn Sie anschließend über eine Zuordnung von einer nicht kompatiblen Ressource lesen oder Rendering. Wenn die anderen Zuordnungen für die gemeinsame Nutzung von Ressourcen zuerst mit neuen Daten initialisiert werden (der Arbeitsspeicher wird für einen anderen Zweck wieder verwendet), ist der nachfolgende Lese-oder Rendering Vorgang in Ordnung, da Daten nicht über inkompatible Interpretationen hinweg Sie müssen jedoch die **tiledresourcebarrier** -API aufrufen, wenn Sie zwischen dem Zugriff auf inkompatible Zuordnungen wie diesem wechseln.

Wenn das Flag Renderziel oder tiefen Schablone für eine der Ressourcen, die Zuordnungen gemeinsam nutzen, nicht festgelegt ist, gibt es weitaus weniger Einschränkungen. Solange die Format-und Oberflächentypen (z. b. Texture2D) identisch sind, können Kacheln gemeinsam genutzt werden. Verschiedene Formate, die kompatibel sind, sind Fälle wie z. b. BC \* -Oberflächen und die äquivalente nicht komprimierte 32-Bit-oder 16-Bit-Format-Format, wie BC6H Viele 32-Bit-pro-Element-Formate können auch mit "R32" \_ \* (R10G10B10A2 \_ \* , R8G8B8A8 \_ \* , B8G8R8A8 \_ \* , B8G8R8X8 \_ \* , R16G16) versehen werden \_ \* . dieser Vorgang ist für nicht-Kachel Ressourcen immer zulässig.

Die gemeinsame Nutzung von gepackten und nicht verpackten Kacheln ist in Ordnung, wenn die Formate kompatibel sind und die Kacheln mit voll Tonfarbe gefüllt sind.

Wenn die Ressourcen gemeinsame Kachel Zuordnungen nicht gemeinsam sind, mit dem Unterschied, dass keine Flags für Renderziel oder tiefen Schablone verwendet werden, kann nur der mit 0 gefüllte Speicher sicher freigegeben werden. die Zuordnung wird für die Definition des angegebenen Ressourcen Formats (in der Regel nur 0) als "0" decodiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pipeline Zugriff auf gekachelte Ressourcen](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




