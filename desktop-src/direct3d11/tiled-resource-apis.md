---
title: APIs für gekachelte Ressourcen
description: Die in diesem Abschnitt beschriebenen APIs funktionieren mit gekachelten Ressourcen und Kachelpools.
ms.assetid: 02DCF9BA-F9EA-4176-AD6F-AA620CE968BA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f433b6c70d475d4da511b85fdcc2b1c273de1efa8e1186215b25ce6b9b95d0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894390"
---
# <a name="tiled-resource-apis"></a>APIs für gekachelte Ressourcen

Die in diesem Abschnitt beschriebenen APIs funktionieren mit gekachelten Ressourcen und Kachelpools.

-   [Zuweisen von Kacheln aus einem Kachelpool zu einer Ressource](#assigning-tiles-from-a-tile-pool-to-a-resource)
-   [Abfragen von Ressourcenkacheln und -unterstützung](#querying-resource-tiling-and-support)
-   [Kopieren von gekachelten Daten](#copying-tiled-data)
-   [Ändern der Größe des Kachelpools](#resizing-tile-pool)
-   [Gekachelte Ressourcenbarriere](#tiled-resource-barrier)
-   [Zugehörige Themen](#related-topics)

## <a name="assigning-tiles-from-a-tile-pool-to-a-resource"></a>Zuweisen von Kacheln aus einem Kachelpool zu einer Ressource

Die [**APIs ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) und [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) bearbeiten und fragen Kachelzuordnungen ab. Aktualisierungsaufrufe wirken sich nur auf die im Aufruf identifizierten Kacheln aus, und andere bleiben wie zuvor definiert erhalten.

Jede Kachel aus einem Kachelpool kann mehreren Speicherorten in einer Ressource und sogar mehreren Ressourcen zugeordnet werden. Diese Zuordnung umfasst Kacheln in einer Ressource, die über ein von der Implementierung ausgewähltes Layout (Mipmap-Packen ) verfügen, bei dem mehrere[Mipmaps](mipmap-packing.md)zu einer einzelnen Kachel gepackt werden. Der Catch ist, dass die Ergebnisse nicht definiert sind, wenn Daten über eine Zuordnung auf die Kachel geschrieben, aber über eine anders konfigurierte Zuordnung gelesen werden. Die sorgfältige Verwendung dieser Flexibilität kann jedoch für eine Anwendung dennoch nützlich sein, z. B. das Freigeben einer Kachel zwischen Ressourcen, die nicht gleichzeitig verwendet werden, wobei der Inhalt der Kachel immer über die gleiche Ressourcenzuordnung initialisiert wird, aus der sie anschließend gelesen werden. Auf ähnliche Weise funktioniert eine Kachel, die zugeordnet ist, um die gepackten Mipmaps mehrerer verschiedener Ressourcen mit den gleichen Oberflächendimensionen zu halten. Die Daten werden in beiden Zuordnungen gleich angezeigt.

Änderungen an Kachelzuweisungen für eine Ressource können jederzeit in einem unmittelbaren oder verzögerten Kontext vorgenommen werden.

## <a name="querying-resource-tiling-and-support"></a>Abfragen von Ressourcenkacheln und -unterstützung

Verwenden Sie zum Abfragen der Ressourcenkacheln [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling).

Verwenden Sie für andere Ressourcenkachelunterstützung [**ID3D11Device2::CheckMultisampleQualityLevels1**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-checkmultisamplequalitylevels1).

## <a name="copying-tiled-data"></a>Kopieren von gekachelten Daten

Alle Methoden in Direct3D zum Verschieben von Daten arbeiten mit gekachelten Ressourcen so, als würden sie nicht gekachelt, mit der Ausnahme, dass Schreibvorgänge in nicht zugeordnete Bereiche gelöscht werden und Lesevorgänge aus nicht zugeordneten Bereichen 0 erzeugen. Wenn ein Kopiervorgang das mehrmalige Schreiben an denselben Speicherort umfasst, da mehrere Speicherorte in der Zielressource demselben Kachelspeicher zugeordnet sind, sind die resultierenden Schreibvorgänge in Kacheln mit mehreren Zuordnungen nicht deterministisch und nicht wiederholbar. Das bedeutet, dass Zugriffe in der Reihenfolge ausgeführt werden, in der die Hardware die Kopie ausgeführt.

Direct3D 11.2 führt Methoden für diese zusätzlichen Möglichkeiten zum Kopieren ein:

-   Kopieren zwischen Kacheln in einer gekachelten Ressource (mit 64 KB Kachelgranularität) und (von/zu) einem Puffer im GPU-Arbeitsspeicher (Oder Stagingressource) – [ **ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   Kopieren aus dem von der Anwendung bereitgestellten Arbeitsspeicher in Kacheln in einer gekachelten Ressource – [ **ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)

Diese Methoden swizzle/deswizzle nach Bedarf und lassen ein D3D11 \_ TILE \_ COPY NO \_ OVERWRITE-Flag zu, wenn der Aufrufer verspricht, dass der Zielspeicher nicht von GPU-Arbeiten referenziert wird, die sich im Flugbetrieb \_ befindet.

Die an der Kopie beteiligten Kacheln dürfen keine Kacheln enthalten, die gepackte Mipmaps enthalten oder nicht definierte Ergebnisse enthalten. Um Daten in bzw. aus Mipmaps zu übertragen, die die Hardware in eine Kachel packt, müssen Sie die standardmäßigen (nicht kachelspezifischen) Kopier-/Aktualisierungs-APIs oder [**ID3D11DeviceContext::GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) für die gesamte MIP-Kette verwenden.

**Hinweis zu [**GenerateMips:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips)** Die Verwendung von [**ID3D11DeviceContext::GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) für eine Ressource mit teilweise zugeordneten Kacheln erzeugt Ergebnisse, die einfach den Regeln zum Lesen und Schreiben von **NULL** entsprechen, die auf den Algorithmus angewendet werden, den der Hardware- und Anzeigetreiber für **GenerateMips verwendet.** Daher ist es für eine Anwendung nicht besonders nützlich, dies  zu tun, es sei denn, in irgendeiner Weise haben die Bereiche mit NULL-Zuordnungen (und ihre Auswirkungen auf andere Mips während der Generierungsphase) keine Auswirkungen auf die Teile der Oberfläche, die für die Anwendung wichtig sind.

Das Kopieren von Kacheldaten von einer Stagingoberfläche oder aus dem Anwendungsspeicher wäre beispielsweise die Möglichkeit, Kacheln hochzuladen, die möglicherweise vom Datenträger gestreamt wurden. Eine Variation beim Streamen von Datenträgern ist das Hochladen von komprimierten Daten in den GPU-Arbeitsspeicher und das anschließende Decodieren auf der GPU. Das Decodierungsziel kann eine Pufferressource im GPU-Arbeitsspeicher sein, aus der [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) dann in die tatsächliche gekachelte Ressource kopiert wird. Mit diesem Kopierschritt kann die GPU schwanken, wenn das Swizzle-Muster nicht bekannt ist. Swizzling ist nicht erforderlich, wenn die gekachelte Ressource selbst eine Pufferressource ist (z. B. im Gegensatz zu einer Textur).

Das Speicherlayout der Kacheln auf der Nichtkacheln-Pufferressourcenseite der Kopie ist einfach linear im Arbeitsspeicher innerhalb von 64-KB-Kacheln, die der Hardware- und Anzeigetreiber bei der Übertragung zu bzw. von einer gekachelten Ressource je nach Kachel überschnaufen/deswizzle. Bei MsAA-Oberflächen (Multisample Antialiasing) werden die Stichproben der einzelnen Pixel in der Reihenfolge des Stichprobenindexes durchlaufen, bevor sie zum nächsten Pixel bewegt werden. Für Kacheln, die teilweise auf der rechten Seite ausgefüllt sind (für eine Oberfläche, die eine Breite hat, die nicht das Vielfache der Kachelbreite in Pixeln ist), entspricht die Tonhöhe/Stride, um eine Zeile nach unten zu bewegen, die vollständige Größe in Byte der Anzahl von Pixeln, die über die Kachel passen würden, wenn die Kachel voll wäre. Es kann also eine Lücke zwischen jeder Zeile mit Pixeln im Arbeitsspeicher geben. Der Einfachheit halber werden Mipmaps, die kleiner als eine Kachel sind, nicht im linearen Layout gepackt. Dies scheint eine Verschwendung von Speicherplatz zu sein, aber wie bereits erwähnt, ist das Kopieren auf Mips, dass die Hardwarepakete zusammen nicht über [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) oder [**UpdateTiles zulässig sind.**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) Die Anwendung kann einfach generische UpdateSubresource-APIs () oder CopySubresource () verwenden, um kleine Mips einzeln zu kopieren. Im Fall von CopySubresource () bedeutet dies jedoch, dass der lineare Speicher dieselbe Dimension wie die gekachelte Ressource sein muss. CopySubresource () kann z. B. nicht aus einer Pufferressource in \* \* eine \* \* Texture2D kopieren.

Wenn ein Hardwarestandard swizzle definiert ist, können Flags hinzugefügt werden, um anzugeben, dass die Daten im Puffer in diesem Format interpretiert werden sollen (kein Swizzle bei der Übertragung erforderlich), obwohl alternative Ansätze zum Hochladen von Daten auch in diesem Fall sinnvoll sein können, z. B. das Zulassen des direkten Zugriffs von Anwendungen auf den Kachelpoolspeicher.

Kopiervorgänge können in einem unmittelbaren oder verzögerten Kontext erfolgen.

## <a name="resizing-tile-pool"></a>Ändern der Größe des Kachelpools

Um die Größe eines Kachelpools zu ändern, verwenden Sie [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool).

## <a name="tiled-resource-barrier"></a>Gekachelte Ressourcenbarriere

Verwenden Sie [**ID3D11DeviceContext2::TiledResourceBarrier,**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)um eine Einschränkung für die Datenzugriffsbestellung zwischen mehreren gekachelten Ressourcen anzugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gekachelte Ressourcen](tiled-resources.md)
</dt> </dl>

 

 




