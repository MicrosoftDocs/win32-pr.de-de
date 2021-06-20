---
description: Erfahren Sie mehr über die Gitternetzunterstützung in D3DX. D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bietet. Es handelt sich um eine Ebene über der Direct3D-Komponente.
ms.assetid: 7892370f-0807-4ab7-b7cd-a7e1182e3f9c
title: Mesh-Unterstützung in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1600b372432d59357a7431c70ce70ce2958002c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408133"
---
# <a name="mesh-support-in-d3dx-direct3d-9"></a>Mesh-Unterstützung in D3DX (Direct3D 9)

D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bietet. Es handelt sich um eine Ebene über der Direct3D-Komponente.

## <a name="meshes"></a>Gittermodelle

D3DX implementiert das Gitternetzkonstrukt zum Laden, Bearbeiten und Rendern von X-Dateiinhalten. Ein Gitternetz ist im Grunde eine Sammlung von Scheitelungen, die eine Geometrie definieren, und eine Reihe von Indizes, die die Gesichter definieren. Es gibt mehrere Gitternetztypen.

[**ID3DXBaseMesh**](id3dxbasemesh.md) bietet die Grundlagen. [**ID3DXMesh**](id3dxmesh.md) erbt von ID3DXBaseMesh und fügt die Gitternetzoptimierung mithilfe des Scheitelpunktcaches pro Chip hinzu. [**ID3DXSkinInfo bietet**](id3dxskininfo.md) Skinned Mesh-Unterstützung.

[**ID3DXBaseMesh bietet**](id3dxbasemesh.md) Methoden zum Bearbeiten und Abfragen von [**ID3DXMesh-Gitterobjekten,**](id3dxmesh.md) die vom Basisgitternetz erben. Dies schließt Adjacency-Vorgänge, geometry buffer retrieval, lock/unlock operations (vertex and index) und copying, rendering, face, and vertex information (Kopieren, Rendern, Gesichtserkennung und Scheitelpunktinformationen) ein.

> [!Note]  
> Die Schnittstellen ID3DXPMesh und ID3DXSPMesh (zur Unterstützung progressiver bzw. vereinfachter Gitternetze), die in früheren Versionen von Direct3D 9 verfügbar waren, wurden gelöscht.

 

## <a name="mesh-architecture"></a>Mesh-Architektur

Ein Gittermodell enthält die Daten für ein komplexes Modell. Es handelt sich um einen abstrakten Datencontainer, der Ressourcen wie Texturen und Materialien sowie Attribute wie Positionsdaten und Adjakencydaten enthält. Es gibt mehrere Gitternetzoperationen, die die Zeichnungsleistung und die Darstellung einer Oberfläche verbessern. Darüber hinaus gibt es eine Reihe anderer Gitternetzkonzepte, die sich auf die Funktionalität von Gitternetzvorgängen wirken. Wenn Sie diese Meshkonzepte so verstehen, dass Sie sie anwenden können, wird die Gitternetzleistung verbessert.

## <a name="mesh-object-data"></a>Mesh-Objektdaten

Ein Gitternetz enthält einen Scheitelpunktpuffer, einen Indexpuffer und einen Attributpuffer.

-   Der Scheitelpunktpuffer enthält die Scheitelpunktdaten, die die Gitternetzvertices sind.
-   Der Indexpuffer enthält Scheitelpunktindizes für den Zugriff auf den Scheitelpunktpuffer. Dies kann die Größe des Scheitelpunktpuffers verringern, indem doppelte Scheitelpunkte reduziert werden. Nur ein indiziertes Gitternetz verwendet den Indexpuffer. Wenn ein Gitternetz beispielsweise aus einer Dreiecksliste besteht, wird der Indexpuffer nicht verwendet.
-   Der Attributpuffer enthält Attributdaten. Attribute sind Eigenschaften der Gitternetzvertices in keiner bestimmten Reihenfolge. Ein D3DX-Gitternetz speichert Attribute in einer Gruppe von DWORDS für jedes Gesicht.

### <a name="attribute-tables"></a>Attributtabellen

Eine Attributtabelle ist eine präzise Darstellung des Inhalts eines Attributpuffers. Attributtabellen können durch Aufrufen einer der Optimize-Methoden mit D3DXMESHOPT ATTRSORT, durch Sperren des Attributpuffers und Auffüllen mit Daten oder durch Aufrufen von \_ SetAttributeTable erstellt werden. Ein Gitternetz enthält eine Attributtabelle, wenn das Gitternetz in Gruppen neu angeordnet wird. Dies geschieht, wenn Optimize aufgerufen wird, vorausgesetzt, eine Attributsortierungsoption (D3DXMESHOPT \_ ATTRSORT oder höher) wird bereitgestellt. D3DX-Gitternetze verwenden indizierte Dreieckslisten und werden daher mit [**IDirect3DDevice9::D rawIndexedPrimitive gezeichnet.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)

Attributtabellen werden als Ergebnis des Aufrufs von Optimize erstellt. Die Gesichter müssen nicht nebeneinander angeordnet werden, da Optimize sie so neu anordnt, dass sie nebeneinander angeordnet werden. Beispielsweise könnten die Hände eines menschlichen Gitters das gleiche Attribut verwenden. Die ID hilft, die Gesichter in Gruppen zu sortieren. Gitternetze aus X-Dateien haben automatisch Attribute für Material- und Textureigenschaften generiert. Sie müssen Optimize(ATTRSORT) oder die effektivere Optimize(VERTEXCACHE) aufrufen, um eine gute Leistung zu erzielen. Die Ladefunktionen versuchen, die Daten genau in der Form zu präsentieren, in der sie gespeichert wurden. Wenn Sie ein vertexpuffer-/indexpufferbasiertes Gitternetz verwenden, bietet die Mesh-API Optimierungsfunktionen und Skinningtransformationen mit wenig Aufwand.

Die Optimierungstypen sind kumulativ, beginnend mit dem am wenigsten optimalen (D3DXMESHOPT COMPACT) bis zum optimalen \_ (D3DXMESHOPT \_ IGNOREVERTS). D3DXMESHOPT \_ STRIPREORDER führt eine Nachrichten- und Attributsortierung durch. D3DXMESHOPT VERTEXCACHE wird immer empfohlen, auch auf Geräten ohne echten \_ Scheitelpunktcache.

## <a name="application-data"></a>Anwendungsdaten

Anwendungsdaten sind Meshdaten, die von einer Anwendung verwaltet werden. Zwischen den Vertexdaten des Gitters und den von diesen Puffern verwalteten Daten besteht eine enge Kopplung.

Der Materialpuffer enthält n Materialien. Die Materialien werden von der Load-Funktion zurückgegeben, wenn die X-Datei geladen wird. Jede Teilmenge kann eigene Materialien und Texturen aufweisen. Der Materialpuffer ist statisch.

Der Adjacency-Puffer enthält Informationen zu Kanten, Gesichtern und angrenzenden Gesichtern. Einige Gitternetzvorgänge hängen davon ab, dass sie wissen, welche Gesichter nebeneinander liegen. Diese Informationen, die als Adjacency-Daten bezeichnet werden, werden in einem Adjacency-Puffer gespeichert. Es ist nicht Teil des Gitters, wird jedoch von der Anwendung verwaltet und muss bei Bedarf für die Meshmethoden bereitgestellt werden.

Der Effektinstanzpuffer enthält eine Liste von Effektinstanzen. Eine Effektinstanz speichert den Zustand. Diese Zustandsinformationen werden verwendet, um die Pipeline zu initialisieren. Eine Effect-Instanz enthält Name-Wert-Paare in einem Effekt.

## <a name="advanced-mesh-topics"></a>Advanced Mesh-Themen

Optimierte Gitternetze bauen auf der Basisnetzfunktionalität auf und fügen Vertexcache-Optimierungsfunktionen mit zwei Methoden hinzu: Optimize, wodurch ein neues Gitternetz erstellt wird, und OptimizeInPlace, das das ursprüngliche Gitternetz ändert.

D3DXGeneratePMesh verwendet den D3DX-Vereinfachungsalgorithmus, um ein progressives Gitter aus dem Eingabegitter zu generieren. D3DXSimplifyMesh generiert mit dem gleichen Vereinfachungsalgorithmus ein Standardgitternetz mit der angegebenen Detailebene aus einem Eingabegitter. Der Benutzer hat die Kontrolle über die Fehlermetrik, die über die pro Scheitelpunktkomponente angegebenen Gewichtungen und die pro Scheitelpunkt angegebenen Gewichtungen verwendet wird. Komponentenspezifische Gewichtungen werden mit dem Komponententeil des Fehlers multipliziert, der pro Edge-Reduzieren berechnet wird. Die Gewichtungen pro Scheitelpunkt werden mit dem Fehlermetrikwert multipliziert, der zum Entfernen dieses Scheitelpunkts bestimmt wurde. Wenn Sie beispielsweise nie möchten, dass ein Scheitelpunkt entfernt wird, legen Sie die Gewichtung dieses bestimmten Scheitelpunkts auf einen großen Wert fest. Wenn Sie hingegen möchten, dass es zuvor entfernt wird, legen Sie ihn auf einen kleinen Wert (kleiner als 1) fest.

[**ID3DXSkinInfo unterstützt**](id3dxskininfo.md) Skinnzeichen. Ein skinniertes Zeichen wird durch einen Satz von Gittern und eine Reihe von Gittern definiert, die sich auf die Scheitelungen der Gitternetze auswirken. Die Brüche werden als Transformationshierarchie dargestellt. Für jedes Gitternetz gibt es eine Matrix für jedes Gitter, die sich darauf auswirken, wodurch das Gitternetz in den lokalen Koordinatenraum des Gitters transformiert wird. Diese Matrix ist die Kastenraumtransformation des Gitters. Dies wird zu dem Zeitpunkt definiert, zu dem das Gerüst dem Gittermodell im Erstellungsprozess zugeordnet ist.

### <a name="skinning"></a>Skinning

Skinning ist ein Verfahren zum Transformieren von Gitternetzvertices mithilfe von Gittern. Die Körper sind in der Regel in einem hierarchischen Gerüst angeordnet, ähnlich wie die Menschlichen in einem menschlichen Körper. Objektvertices werden dann dem Gittermodell zugeordnet, z. B. das Anfügen von Skin an die Zieel. Wenn die Gebilde transformiert werden, wird auch die Skin transformiert.

Skinnierte Gitternetze verwenden Gitter, um eine Reihe von Scheitelungen zu beeinflussen. Vom Benutzer bereitgestellte Transformationsdaten zur Transformation von Transformationen, um zu beeinflussen, wie die Benutzeroberfläche mit SRT umgewandelt werden kann. Das Gitternetz verwendet die transformierten Gitter, um die Scheitelungen zu beeinflussen, die der Ziege zugeordnet sind. Paletten sind Arrays von SRT-Transformationen. Paletten werden häufig als Matrizen implementiert, können jedoch SRT-Werte enthalten.

### <a name="progressive-mesh-trimming"></a>Progressive Mesh-Kürzung

Niedrige Detailbereiche können es sich leisten, Scheitelungen zu verlieren, die die gerenderte Darstellung der Oberfläche nicht ändern. Dies gilt insbesondere für Objekte, wenn sie sich weiter von der Kamera bewegen. Dies wird als Detailebene bezeichnet. Benutzer verfügen über Rendersteuerelemente auf API-Ebene zum Festlegen der Detailebene, um die Renderingeffizienz zu maximieren.

Progressive Mesh-Objekte beginnen mit einer hohen Anzahl von Gesichtern und verwenden Vereinfachung, um die Anzahl von Gesichtern zu reduzieren. Ein progressives Gitternetz, das unabhängig von der Ansicht ist, wird als ansichtsunabhängiges progressives Gitternetz (VIPM) bezeichnet.

Eine weitere Möglichkeit, die Anzahl von Gesichtern zu reduzieren, ist das Kürzen. Dadurch werden tatsächlich Scheitelungen und Gesichter aus dem Gitternetz entfernt. Das Kürzen kann am hohen Ende (um die maximale Anzahl von Gesichtern zu begrenzen) oder am unteren Ende (um die Mindestanzahl von Gesichtern zu begrenzen) erfolgen. Durch das Kürzen wird die Leistung beim Zeichnen verbessert, es sollte jedoch mit Vorsicht die visuelle Qualität beibehalten werden. Das Kürzen wird im Progressive Mesh SDK-Beispiel veranschaulicht.

Für Bereiche mit hoher Sichtbarkeit kann die Auflösung mithilfe der progressiven Detailebene (PLOD) erhöht werden. Dies ist eine Technik zum Aufbrechen eines einzelnen Gesichts in zwei Gesichter.

### <a name="patch-meshes"></a>Patch Meshes

Zwei spezielle Arten von Patchgitternetzen werden ebenfalls unterstützt: Rechteck- und Dreieckspatches. Das Rechteck-Patchgitternetz ist ein Patchgitternetz, dessen Kontrollpunkte in einer verwinkelten, rechteckigen Sequenz angeordnet sind. Rechteck- und Dreieckspatches werden verwendet, um Oberflächen mit hoher Ordnung zu erstellen. Sie werden nicht so häufig wie Dreiecksgitternetze verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3dx](d3dx.md)
</dt> </dl>

 

 
