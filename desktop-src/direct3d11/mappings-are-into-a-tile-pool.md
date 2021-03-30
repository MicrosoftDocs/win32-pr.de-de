---
title: Zuordnungen in einen Kachelpool
description: Wenn eine Ressource mit dem D3D11 \_ ressourcenmisc-Kachel Kennzeichen erstellt wird \_ \_ , stammen die Kacheln, die die Ressource bilden, von den Positionen in einem Kachel Pool.
ms.assetid: 1DBE23B2-A1E6-4491-9B74-4E92508A68FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1537113d6685e39cab94445c8d3f16d406638820
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993367"
---
# <a name="mappings-are-into-a-tile-pool"></a>Zuordnungen in einen Kachelpool

Wenn eine Ressource mit dem [**D3D11 \_ \_ ressourcenmisc- \_ Kachel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Kennzeichen erstellt wird, stammen die Kacheln, die die Ressource bilden, von den Positionen in einem Kachel Pool. Ein Kachel Pool ist ein Arbeitsspeicher Pool (gestützt durch eine oder mehrere Zuordnungen im Hintergrund, die von der Anwendung nicht gesehen werden). Das Betriebssystem und der Anzeigetreiber verwalten diesen Speicherpool, und der Speicherbedarf wird von einer Anwendung leicht verstanden. Gekachelte Ressourcen ordnen Sie 64 KB-Regionen zu, indem Sie auf Positionen in einem Kachel Pool zeigen. Ein Fehler dieses Setups besteht darin, dass mehrere Ressourcen die gleichen Kacheln freigeben und wieder verwenden können und dass die gleichen Kacheln bei Bedarf an unterschiedlichen Positionen in einer Ressource wieder verwendet werden können.

Die Kosten für die Flexibilität beim Auffüllen der Kacheln für eine Ressource aus einem Kachel Pool besteht darin, dass die Ressource die Zuordnung und Verwaltung der Kacheln im Kachel Pool die für die Ressource benötigten Kacheln definieren und verwalten muss. Kachel Zuordnungen können geändert werden. Außerdem müssen nicht alle Kacheln in einer Ressource gleichzeitig zugeordnet werden. eine Ressource kann **null** -Zuordnungen aufweisen. Eine **null** -Zuordnung definiert eine Kachel als nicht verfügbar aus der Sicht der Ressource, auf die Sie zugreift.

Mehrere Kachel Pools können erstellt werden, und beliebig viele Kachel Ressourcen können einem bestimmten Kachel Pool gleichzeitig zugeordnet werden. Kachel Pools können auch vergrößert oder verkleinert werden. Weitere Informationen finden Sie unter [Ändern der Größe des Kachel Pools](tile-pool-resizing.md). Eine Einschränkung, die zur Vereinfachung der Anzeigetreiber-und Lauf Zeit Implementierung vorhanden ist, besteht darin, dass eine angegebene Kachel Ressource nur Zuordnungen zu höchstens einem Kachel Pool aufweisen kann (im Gegensatz zu gleichzeitiger Zuordnung zu mehreren Kachel Pools).

Die Größe des Speichers, der einer gekachelten Ressource selbst zugeordnet ist (d. h. unabhängiger Kachel Pool Speicher), ist ungefähr proportional zur Anzahl der Kacheln, die dem Pool tatsächlich zu einem bestimmten Zeitpunkt zugeordnet sind. In der Hardware wird dieser Fakt so skaliert, dass der Speicherbedarf für den Seitentabellen Speicher ungefähr mit der Menge der zugeordneten Kacheln skaliert wird (z. b. Wenn ein mehrstufiges Seitentabellen Schema nach Bedarf verwendet wird).

Der Kachel Pool ist eine vollständige Software Abstraktion, mit der Direct3D-Anwendungen die Seitentabellen auf der GPU (Graphics Processing Unit) effektiv programmieren können, ohne die Implementierungsdetails auf niedriger Ebene kennen zu müssen (oder direkt mit Zeiger Adressen umzugehen). Kachel Pools wenden keine weiteren Dereferenzierungsebenen auf Hardware an. Optimierungen einer Seiten Tabelle auf einer einzelnen Ebene, die Konstrukte wie Seiten Verzeichnisse verwenden, sind unabhängig vom Kachel Pool Konzept.

Wir untersuchen den Speicher, der für die Seiten Tabelle im ungünstigsten Fall erforderlich ist (in der Praxis ist es jedoch nur erforderlich, dass der Speicher ungefähr proportional zu den zugeordneten zugeordnet ist).

Angenommen, jeder Seitentabellen Eintrag ist 64 Bits.

Für die schlechteste Seitentabellen Größe, die für eine einzelne Oberfläche getroffen wurde, wenn die Ressourcen Grenzwerte in Direct3D 11 vorausgesetzt werden, wird angenommen, dass eine Kachel Ressource mit einem 128-Bit-pro-Element-Format (z. b. ein RGBA-float) erstellt wird, sodass eine 64-KB-Kachel nur 4096 Pixel enthält. Die maximal unterstützte [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) -Größe von 16384 \* 16384 \* 2048 (aber nur mit einer einzigen MipMap) erfordert ungefähr 1 GB Speicher in der Seiten Tabelle, wenn vollständig aufgefüllt (ohne Mipmaps) mithilfe von 64-Bit-Tabellen Einträgen. Durch das Hinzufügen von Mipmaps wird der vollständig zugeordnete Seitentabellen Speicher (ungünstigste Fall) um ungefähr eine dritte Größe von ungefähr 1,3 GB vergrößert.

Dieser Fall ermöglicht den Zugriff auf ungefähr 10,6 TB adressierbaren Arbeitsspeicher. Möglicherweise gibt es jedoch eine Beschränkung für die Menge des adressierbaren Speichers, wodurch diese Beträge reduziert werden, vielleicht um den Terabytebereich.

Ein weiterer Fall, der berücksichtigt werden muss, ist eine einzelne [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) -Ressource von 16384 \* 16384 mit einem 32-Bit-pro-Element-Format, einschließlich Mipmaps. Der Speicherplatz, der in einer vollständig aufgefüllten Seiten Tabelle benötigt wird, beträgt ungefähr 170 KB mit 64-Bit-Tabellen Einträgen.

Sehen Sie sich abschließend ein Beispiel mit einem BC-Format an, z. b. bzw bc7 mit 128 Bits pro Kachel mit 4 x 4 Pixeln. Das ist ein Byte pro Pixel. Ein [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) von 16384 \* 16384 \* 2048 einschließlich Mipmaps erfordert ungefähr 85 MB, um diesen Speicher vollständig in einer Seiten Tabelle aufzufüllen. Das ist nicht schlecht, wenn Sie dies in Erwägung ziehen, ist es möglich, dass eine Kachel Ressource 550 gigapixels (in diesem Fall 512 GB Arbeitsspeicher) umfasst.

In der Praxis würden diese vollständigen Zuordnungen nicht in naher Nähe definiert werden, da die Menge des verfügbaren physischen Speichers nicht zulässt, dass eine Menge an einem bestimmten Punkt zugeordnet wird. Bei einem Kachel Pool können sich Anwendungen jedoch für die Wiederverwendung von Kacheln entscheiden (als einfaches Beispiel für die Wiederverwendung einer "schwarzen" farbigen Kachel für große schwarze Bereiche in einem Bild), indem der Kachel Pool (d. h. Seitentabellen Zuordnungen) als Tool für die Speicher Komprimierung verwendet wird.

Der anfängliche Inhalt der Seiten Tabelle ist für alle Einträge **null** . Anwendungen können auch keine anfänglichen Daten für den Speicherinhalt der Oberfläche übergeben, da Sie ohne Arbeitsspeicher Unterstützung gestartet werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellung eines Kachelpools](tile-pool-creation.md)<br/>                                                 | Ein Kachel Pool wird über die [**ID3D11Device:: featebuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) -API erstellt, indem das Flag für den [**D3D11- \_ \_ ressourcenmisc- \_ Kachel \_ Pool**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) im **Fehlerflags** -Member der [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur, auf die der *PDE SC* -Parameter verweist, übergeben wird. <br/> |
| [Ändern der Größe des Kachelpools](tile-pool-resizing.md)<br/>                                                 | Verwenden Sie die [**ID3D11DeviceContext2:: resizetilepool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) -API, um einen Kachel Pool zu vergrößern, wenn für die Anwendung mehr Arbeits Sätze benötigt werden, damit die gekachelten Ressourcen darauf zuordnet werden. <br/>                                                                                                                    |
| [Gefahrennachverfolgung im Vergleich mit den Kachelpoolressourcen](hazard-tracking-versus-tile-pool-resources.md)<br/> | Bei nicht gekachelten Ressourcen kann Direct3D bestimmte Gefahren Bedingungen während des Renderings verhindern, aber da die gefährverfolgung auf Kachel Ebene für gekachelte Ressourcen erfolgen würde, kann das Nachverfolgen von Gefährdungs Zuständen beim Rendern von gekachelten Ressourcen zu teuer sein. <br/>                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Kachel Ressourcen](creating-tiled-resources.md)
</dt> </dl>

 

