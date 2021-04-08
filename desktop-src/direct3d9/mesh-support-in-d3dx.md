---
description: D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt. Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.
ms.assetid: 7892370f-0807-4ab7-b7cd-a7e1182e3f9c
title: Gitter Unterstützung in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0b2b1dd0e5d4c5a212005afe400bb559f1689a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957712"
---
# <a name="mesh-support-in-d3dx-direct3d-9"></a>Gitter Unterstützung in D3DX (Direct3D 9)

D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt. Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.

## <a name="meshes"></a>Gittermodelle

D3DX implementiert das Mesh-Konstrukt zum Laden, bearbeiten und renderdatei Inhalt. Bei einem Mesh handelt es sich im Grunde um eine Auflistung von Vertices, die eine Geometrie definieren Es gibt mehrere Mesh-Typen.

[**ID3DXBaseMesh**](id3dxbasemesh.md) stellt die Grundlagen bereit. [**ID3DXMesh**](id3dxmesh.md) erbt von ID3DXBaseMesh und fügt die Mesh-Optimierung mithilfe des pro-Chip-Scheitelpunkt Caches hinzu. [**ID3DXSkinInfo**](id3dxskininfo.md) bietet Unterstützung für unter Häute Netze.

[**ID3DXBaseMesh**](id3dxbasemesh.md) stellt Methoden bereit, um [**ID3DXMesh**](id3dxmesh.md) Mesh-Objekte zu bearbeiten und abzufragen, die vom basismesh erben. Dies umfasst die Vorgänge für die Erkennung, den Geometry-Puffer Abruf, Sperr-/entsperrvorgänge (Scheitelpunkt und Index) sowie das Kopieren, Rendering, Gesicht und Vertex.

> [!Note]  
> Die ID3DXPMesh-und ID3DXSPMesh-Schnittstellen (zur Unterstützung progressiver und vereinfachter Meshes), die in früheren Versionen von Direct3D 9 verfügbar waren, wurden gelöscht.

 

## <a name="mesh-architecture"></a>Mesh-Architektur

Ein Mesh enthält die Daten für ein komplexes Modell. Dabei handelt es sich um einen abstrakten Datencontainer, der Ressourcen wie Texturen und Materialien sowie Attribute wie Positionsdaten und Datenquellen enthält. Es gibt mehrere Mesh-Vorgänge, die die Zeichnungs Leistung und die Darstellung einer Oberfläche verbessern. Außerdem gibt es eine Reihe weiterer Gitter Konzepte, die sich auf die Funktionalität von Mesh-Vorgängen auswirken. Wenn Sie diese Mesh-Konzepte verstehen, damit Sie Sie anwenden können, verbessern Sie die Netzleistung

## <a name="mesh-object-data"></a>Mesh-Objektdaten

Ein Mesh enthält einen Scheitelpunkt Puffer, einen Index Puffer und einen Attribut Puffer.

-   Der Vertex-Puffer enthält die Scheitelpunkt Daten, die als Gitter Scheitel Punkte dienen.
-   Der Index Puffer enthält Scheitelpunkt Indizes für den Zugriff auf den Scheitelpunkt Puffer. Dadurch kann die Vertex-Puffergröße verringert werden, indem doppelte Vertices reduziert werden. Nur ein indiziertes Mesh verwendet den Index Puffer. Wenn ein Mesh beispielsweise aus einer Dreiecks Liste besteht, wird der Index Puffer nicht verwendet.
-   Der Attribut Puffer enthält Attributdaten. Attribute sind Eigenschaften der Mesh-Scheitel Punkte, in keiner bestimmten Reihenfolge. Ein D3DX Mesh speichert Attribute in einer Gruppe von DWords für jede Oberfläche.

### <a name="attribute-tables"></a>Attribut Tabellen

Eine Attribut Tabelle ist eine präzise Darstellung des Inhalts eines Attribut Puffers. Attribut Tabellen können durch Aufrufen einer der Optimierungsmethoden mit D3DXMESHOPT \_ attrsort erstellt werden, indem der Attribut Puffer gesperrt und mit Daten aufgefüllt wird, oder durch Aufrufen von "*". Ein Mesh enthält eine Attribut Tabelle, wenn das Mesh in Gruppen neu angeordnet wird. Dies geschieht, wenn "optimieren" aufgerufen wird, vorausgesetzt, dass eine Attribut Sortieroption (D3DXMESHOPT \_ attrsort oder höher) angegeben wird. D3DX Meshes verwenden indizierte Dreiecks Listen und werden daher mit [**IDirect3DDevice9::D rawindexedprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)gezeichnet.

Attribut Tabellen werden als Ergebnis des Abrufs von "optimieren" erstellt. Die Gesichter müssen nicht nebeneinander angeordnet werden, da Sie durch die Optimierung so angeordnet werden, dass Sie nebeneinander angeordnet werden. Beispielsweise könnten die Hände eines menschlichen Netzes dasselbe Attribut verwenden. Mit der ID können die Gesichter in Gruppen sortiert werden. Meshes von x-Dateien haben automatisch Attribute für Material-und Textur Eigenschaften generiert. Sie müssen optimieren (attrsort) oder die effektivere Optimierung (vertexcache) aufrufen, um eine gute Leistung zu erzielen. Die Ladefunktionen versuchen, die Daten in der exakten Form darzustellen, in der Sie gespeichert wurden. Wenn Sie ein Vertex-Puffer-/indexpufferbasiertes Mesh verwenden, stellt die Mesh-API Optimierungs Funktionen bereit und zeigt Transformationen mit geringem mehr Aufwand an.

Die Optimierungs Typen sind kumulativ, beginnend mit dem am wenigsten optimalen (D3DXMESHOPT \_ Compact) und dem optimalen (D3DXMESHOPT \_ ignoreverts). D3DXMESHOPT \_ stripreorder führt eine Komprimierung und Attribut Sortierung aus. D3DXMESHOPT \_ vertexcache wird immer empfohlen, auch auf Geräten ohne einen echten Vertex-Cache.

## <a name="application-data"></a>Anwendungsdaten

Anwendungsdaten sind Mesh-Daten, die von einer Anwendung verwaltet werden. Zwischen den Vertex-Netz Daten und den von diesen Puffern verwalteten Daten besteht eine enge Kopplung.

Der Materialpuffer enthält n Material. Die Materialien werden von der Load-Funktion zurückgegeben, wenn die x-Datei geladen wird. Jede Teilmenge kann über eigene Materialien und Texturen verfügen. Der Materialpuffer ist statisch.

Der angrenzenpuffer enthält Informationen über Kanten, Gesichter und angrenzende Flächen. Einige Gitter Vorgänge hängen davon ab, welche Gesichter nebeneinander angeordnet sind. Diese Informationen, die als "Informationsdaten" bezeichnet werden, werden in einem zutreffende Puffer aufbewahrt. Sie ist nicht Teil des Netzes, wird jedoch von der Anwendung verwaltet und muss bei Bedarf für die Mesh-Methoden bereitgestellt werden.

Der Effekt-instanzpuffer enthält eine Liste von Effekt Instanzen. Eine Effekt Instanz speichert den Zustand. Diese Zustandsinformationen werden verwendet, um die Pipeline zu initialisieren. Eine Effekt Instanz enthält in der Tat Name/Wert-Paare.

## <a name="advanced-mesh-topics"></a>Erweiterte Mesh-Themen

Optimierte Meshs bauen auf der grundlegenden Mesh-Funktionalität auf und fügen die Vertex-Cache-Optimierungs Funktion mit zwei Methoden hinzu: optimieren, wodurch ein neues Mesh erstellt wird, und OptimizeInPlace, das das ursprüngliche Mesh ändert.

D3DXGeneratePMesh verwendet den D3DX-Vereinfachungs Algorithmus, um ein progressives Mesh aus dem eingabemesh zu generieren. D3DXSimplifyMesh generiert mit dem gleichen Vereinfachungs Algorithmus ein standardmesh der angegebenen Detailebene aus einem eingabemesh. Der Benutzer hat die Kontrolle über die Fehler Metrik, die durch die pro-Vertex-Komponente angegebenen Gewichtungen und Gewichtungen pro Scheitelpunkt angegeben wird. Die Gewichtungen pro Komponente werden mit dem Komponenten Anteil von Fehlern multipliziert, die pro edgeknoten berechnet werden. Pro-Vertex-Gewichtungen werden mit dem Fehler Metrikwert multipliziert, der für das Entfernen dieses Scheitel Punkts festgelegt wurde. Wenn Sie z. b. nie möchten, dass ein Scheitelpunkt entfernt wird, legen Sie die Gewichtung dieses bestimmten Scheitel Punkts auf einen großen Wert fest. Wenn Sie es zuvor entfernen möchten, legen Sie es auf einen kleinen Wert fest (weniger als 1).

[**ID3DXSkinInfo**](id3dxskininfo.md) unterstützt gehäutige Zeichen. Ein gehäutenes Zeichen wird durch einen Satz von Netzen und einen Satz von Knochen definiert, die die Scheitel Punkte der Netzen beeinflussen. Die Knochen werden als Transformations Hierarchie dargestellt. Für jedes Mesh gibt es eine Matrix für jeden betroffenen Knochen, wodurch das Mesh in den lokalen Koordinaten Bereich des Knotens transformiert wird. Diese Matrix ist die Leerraum Transformation für das Mesh. Dies wird zu dem Zeitpunkt definiert, zu dem das Gerüst dem Mesh im Erstellungs Prozess zugeordnet ist.

### <a name="skinning"></a>Skinning

Das Skinning ist eine Technik zum Transformieren von Mesh-Scheitel Punkten mithilfe von Knochen. Die Knochen sind in der Regel in einem hierarchischen Gerüst angeordnet, ähnlich den Knochen in einem menschlichen Körper. Objekt Scheitel Punkte werden dann den Knochen zugeordnet, wie z. b. das Anfügen von Skin an die Knochen. Wenn die Knochen transformiert werden, wird die Skin ebenfalls transformiert.

Häufende Netze verwenden zum beeinflussen einer Reihe von Scheitel Punkten. Die Daten der Daten zur Datenverarbeitung werden vom Benutzer bereitgestellt, um zu beeinflussen, wie die Knochen SRT werden. Das Mesh verwendet die transformierten Knochen, um die Scheitel Punkte zu beeinflussen, die mit den Knochen verknüpft sind. Paletten sind Arrays von SRT-Transformationen. Paletten werden oft als Matrizen implementiert, Sie können jedoch SRT-Werte enthalten.

### <a name="progressive-mesh-trimming"></a>Progressive Gitter Kürzung

Detail Bereiche können Vertices verlieren, die die gerenderte Darstellung der Oberfläche nicht ändern. Dies gilt insbesondere für Objekte, die sich weiter von der Kamera unter bewegen. Dies wird als Detailgrad bezeichnet. Benutzer verfügen über rendersteuerelemente auf API-Ebene zum Festlegen der Detailebene, um die renderingeffizienz zu maximieren.

Progressive Mesh-Objekte beginnen mit einer hohen Anzahl von Gesichtern und vereinfachen die Anzahl der Gesichter mithilfe der Vereinfachung. Ein progressives Mesh, das View Independent ist, wird als Ansichts unabhängiges progressives Mesh (vipm) bezeichnet.

Eine andere Möglichkeit, die Anzahl der Gesichter zu reduzieren, ist die Kürzung Dadurch werden Vertices und Gesichter aus dem Mesh entfernt. Die Kürzung kann am höchsten Ende erfolgen (um die maximale Anzahl von Gesichtern einzuschränken) oder am unteren Ende (um die minimale Anzahl von Gesichtern einzuschränken). Durch die Kürzung wird die Leistung des Zieh Elements verbessert, aber es sollte darauf geachtet werden, die visuelle Qualität beizubehalten. Die Kürzung wird im Beispiel für das Progressive Mesh SDK veranschaulicht.

Bei Bereichen mit hoher Sichtbarkeit kann die Auflösung mithilfe der progressiven Detailebene (plod) gesteigert werden. Dies ist eine Technik, mit der ein einzelnes Gesicht in zwei Gesichter unterteilt wird.

### <a name="patch-meshes"></a>Patchmeshes

Zwei spezialisierte Typen von patchnetzen werden ebenfalls unterstützt: Rechteck-und Dreiecks Patches. Das Rechteck patchmesh ist ein patchmesh, dessen Steuerungs Punkte in einer sich Reihenfolge, rechteckigen Sequenz angeordnet werden. Rechteck-und Dreiecks Patches werden verwendet, um hochwertige Oberflächen zu erstellen. Sie werden nicht so häufig als Dreiecksnetze verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 
