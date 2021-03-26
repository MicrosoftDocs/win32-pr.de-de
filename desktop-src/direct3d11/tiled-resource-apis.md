---
title: Ressourcen-APIs mit Kachel
description: Die in diesem Abschnitt beschriebenen APIs funktionieren mit gekachelten Ressourcen und einem Kachel Pool.
ms.assetid: 02DCF9BA-F9EA-4176-AD6F-AA620CE968BA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0d97f5272f4f96db56e6e89b871951de035105
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388031"
---
# <a name="tiled-resource-apis"></a>Ressourcen-APIs mit Kachel

Die in diesem Abschnitt beschriebenen APIs funktionieren mit gekachelten Ressourcen und einem Kachel Pool.

-   [Zuweisen von Kacheln aus einem Kachel Pool zu einer Ressource](#assigning-tiles-from-a-tile-pool-to-a-resource)
-   [Abfragen von Ressourcen-und Support](#querying-resource-tiling-and-support)
-   [Kopieren von Kachel Daten](#copying-tiled-data)
-   [Ändern der Größe des Kachel Pools](#resizing-tile-pool)
-   [Gekachelte Ressourcen Barriere](#tiled-resource-barrier)
-   [Zugehörige Themen](#related-topics)

## <a name="assigning-tiles-from-a-tile-pool-to-a-resource"></a>Zuweisen von Kacheln aus einem Kachel Pool zu einer Ressource

Die [**ID3D11DeviceContext2:: updatetilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) -und [**ID3D11DeviceContext2:: copytilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) -APIs bearbeiten und Abfragen Kachel Zuordnungen. Update-Aufrufe wirken sich nur auf die im Aufruf identifizierten Kacheln aus, und andere bleiben wie zuvor definiert.

Eine beliebige Kachel aus einem Kachel Pool kann mehreren Speicherorten in einer Ressource und sogar mehreren Ressourcen zugeordnet werden. Diese Zuordnung umfasst Kacheln in einer Ressource, die über ein von der Implementierung ausgewähltes Layout ([MipMap-Verpackung](mipmap-packing.md)) verfügen, in dem mehrere Mipmaps in einer einzelnen Kachel verpackt werden. Der catch besteht darin, dass die Ergebnisse nicht definiert sind, wenn Daten über eine Zuordnung in die Kachel geschrieben werden, aber über eine anders konfigurierte Zuordnung gelesen werden. Die sorgfältige Verwendung dieser Flexibilität kann für eine Anwendung dennoch nützlich sein, wie z. b. das Freigeben einer Kachel zwischen Ressourcen, die nicht gleichzeitig verwendet werden, wobei der Inhalt der Kachel immer durch dieselbe Ressourcen Zuordnung initialisiert wird, wie Sie später aus dem gelesen werden. Ebenso funktioniert eine Kachel, die die gepackten Mipmaps mehrerer verschiedener Ressourcen mit denselben Oberflächen Dimensionen enthält, einwandfrei. die Daten werden in beiden Zuordnungen gleich angezeigt.

Änderungen an den Kachel Zuweisungen für eine Ressource können jederzeit in einem unmittelbaren oder verzögerten Kontext vorgenommen werden.

## <a name="querying-resource-tiling-and-support"></a>Abfragen von Ressourcen-und Support

Verwenden Sie [**ID3D11Device2:: getresourcetick**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling), um die Ressourcen-tiult abzufragen.

Verwenden Sie [**ID3D11Device2:: CheckMultisampleQualityLevels1**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-checkmultisamplequalitylevels1), um weitere Unterstützung für Ressourcen Unterstützung zu erhalten.

## <a name="copying-tiled-data"></a>Kopieren von Kachel Daten

Alle Methoden in Direct3D zum Verschieben von Daten um die Arbeit mit gekachelten Ressourcen so, als wären Sie nicht gekachelt, mit der Ausnahme, dass Schreibvorgänge in nicht zugeordnete Bereiche gelöscht und Lesevorgänge aus nicht zugeordneten Bereichen 0 ergeben. Wenn bei einem Kopiervorgang mehrere Male an denselben Speicherort geschrieben werden müssen, weil mehrere Speicherorte in der Ziel Ressource demselben Kachel Speicher zugeordnet sind, sind die resultierenden Schreibvorgänge auf mehrfach zugeordnete Kacheln nicht deterministisch und nicht wiederholbar. Das heißt, dass Zugriffe in jeder Reihenfolge erfolgen, in der sich die Hardware für die Ausführung der Kopie verhält.

In Direct3D 11,2 werden Methoden für diese zusätzlichen Methoden zum Kopieren eingeführt:

-   Kopieren zwischen Kacheln in einer gekachelten Ressource (mit einer Kachel Genauigkeit von 64 KB) und (in/aus) einem Puffer im GPU-Speicher (Graphics Processing Unit) (oder in der stagingressource)- [ **ID3D11DeviceContext2:: copytiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   Von der Anwendung bereitgestellten Arbeitsspeicher auf Kacheln in einer gekachelten Ressource kopieren- [ **ID3D11DeviceContext2:: updatetiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)

Diese Methoden wischen bei Bedarf, und lassen das Flag "D3D11 \_ Tile \_ Copy No Überschreibung" zu, wenn der Aufrufer \_ \_ auf den Zielspeicher zuweist, dass GPU-Arbeit, die aktiv ist, nicht referenziert wird.

Die Kacheln, die an der Kopie beteiligt sind, dürfen keine Kacheln enthalten, die gepackte Mipmaps enthalten oder die nicht definierte Ergebnisse aufweisen. Zum Übertragen von Daten in/aus Mipmaps, die von den Hardware Paketen in eine Kachel kopiert werden, müssen Sie für die gesamte MIP-Kette die standardmäßigen (nicht Kachel spezifischen) Kopier-/Update-APIs oder [**Verknüpfung id3d11devicecontext aus:: generatemips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) verwenden.

**Hinweis bei [**generatemips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips):** bei Verwendung von [**Verknüpfung id3d11devicecontext aus:: generatemips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) für eine Ressource mit teilweise zugeordneten Kacheln werden Ergebnisse erzeugt, die einfach den Regeln für das Lesen und Schreiben von **null** folgen, die auf den Algorithmus angewendet werden, der von Hardware und Anzeigetreiber für **generatemips** verwendet wird. Daher ist es für eine Anwendung nicht besonders nützlich, dies zu tun, es sei denn, die Bereiche mit **null** -Zuordnungen (und ihre Auswirkung auf andere MIPS während der Generierungs Phase) haben keine Auswirkungen auf die Teile der Oberfläche, die für die Anwendung wichtig sind.

Wenn Sie Kachel Daten aus einer stagingoberfläche oder aus dem Anwendungs Speicher kopieren, können Sie beispielsweise Kacheln hochladen, die möglicherweise von einem Datenträger gestreamt wurden. Eine Variation beim Streaming von einem Datenträger lädt eine Komprimierung von komprimierten Daten in den GPU-Speicher hoch und dann die Decodierung auf der GPU. Beim decodierungsziel kann es sich um eine Puffer Ressource im GPU-Speicher handeln, von der [**copytiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) dann in die tatsächlich gekachelte Ressource kopiert werden. Dieser Kopier Schritt ermöglicht die GPU, wenn das Swizzle-Muster nicht bekannt ist. Das Schwenken ist nicht erforderlich, wenn die gekachelte Ressource selbst eine Puffer Ressource ist (z. b. im Gegensatz zu einer Textur).

Das Speicher Layout der Kacheln auf der Ressourcenseite des nicht gekachelten Puffers der Kopie ist einfach linear im Arbeitsspeicher innerhalb von 64 KB-Kacheln, die der Hardware-und Anzeigetreiber bei der Übertragung in eine oder aus einer gekachelten Ressource nach Bedarf durchläuft. Bei Multisampling-Antialiasing (MSAA)-Oberflächen werden die Stichproben der einzelnen Pixel vor dem Wechsel zum nächsten Pixel in der Beispiel Index Reihenfolge durchlaufen. Bei Kacheln, die teilweise auf der rechten Seite aufgefüllt sind (für eine Oberfläche mit einer Breite, die kein Vielfaches der Kachel Breite in Pixel ist), ist die Menge bzw. der Schritt zum nach unten einer Zeile die vollständige Größe in Byte der Anzahl von Pixeln, die auf die Kachel passen, wenn die Kachel voll ist. Daher kann eine Lücke zwischen den einzelnen Zeilen der Pixel im Speicher bestehen. Aus Gründen der Einfachheit werden Mipmaps, die kleiner sind als eine Kachel, nicht im linearen Layout verpackt. Dies scheint eine Verschwendung von Speicherplatz zu sein, aber wie bereits erwähnt, dass die Hardware Pakete über [**copytiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) oder [**updatetiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)zusammen kopiert werden. Die Anwendung kann nur generische updatesubresource \* ()-oder copysubresource \* ()-APIs verwenden, um Small MIPS einzeln zu kopieren, jedoch im Fall von copysubresource \* (). Dies bedeutet, dass der lineare Speicher dieselbe Dimension wie die gekachelte Ressource sein muss. copysubresource \* () kann nicht aus einer Puffer Ressource in eine Texture2D-Instanz kopieren.

Wenn ein Hardware Standard-swidwert definiert ist, können Flags hinzugefügt werden, um anzugeben, dass die Daten im Puffer in diesem Format interpretiert werden sollen (kein swilen erforderlich), obwohl alternative Vorgehensweisen zum Hochladen von Daten in diesem Fall sinnvoll sein können, z. b. Wenn Anwendungen den direkten Zugriff auf den Kachel Pool Speicher erlauben.

Kopiervorgänge können in einem unmittelbaren oder verzögerten Kontext durchgeführt werden.

## <a name="resizing-tile-pool"></a>Ändern der Größe des Kachel Pools

Verwenden Sie [**ID3D11DeviceContext2:: resizetilepool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool), um die Größe eines Kachel Pools zu ändern.

## <a name="tiled-resource-barrier"></a>Gekachelte Ressourcen Barriere

Verwenden Sie [**ID3D11DeviceContext2:: tiledresourcebarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier), um eine Einschränkung der Datenzugriffs Anordnung zwischen mehreren gekachelten Ressourcen anzugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gekachelte Ressourcen](tiled-resources.md)
</dt> </dl>

 

 




