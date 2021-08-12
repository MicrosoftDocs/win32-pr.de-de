---
description: Viele Rendering- und Inhaltsgenerierungstechniken erfordern eine eindeutige, nicht überlappende Karte eines 2D-Signals (z. B. einer Textur) in einem Gitternetz.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Verwenden von UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9516223f6d299f42adf19073dc103e7e13b37d49d2f323d6620b46421be1f722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290625"
---
# <a name="using-uvatlas-direct3d-9"></a>Verwenden von UVAtlas (Direct3D 9)

> [!NOTE]
> UVAtlas wurde ursprünglich in der veralteten D3DX9-Utilty-Bibliothek ausgeliefert. Die neueste Version ist unter [UV Atlas Command-Line Tool (uvatlas.exe) verfügbar.](https://github.com/Microsoft/UVAtlas)

Viele Rendering- und Inhaltsgenerierungstechniken erfordern eine eindeutige, nicht überlappende Karte eines 2D-Signals (z. B. einer Textur) in einem Gitternetz. Zu diesen Techniken gehören:

-   Normal/Verschiebungszuordnung
-   TEXTURRAUM-PRT-Simulationen und LightMaps
-   Oberflächengemälde
-   Texturraumbeleuchtung

Das manuelle Generieren einer eindeutigen UV-Zuordnung ist oft zeitaufwändig und mühsam. Dies gilt insbesondere dann, wenn die Eingabegeometrie komplex ist und eine effiziente/geringe Texturraumauslastung gewünscht ist. Die folgende Abbildung zeigt ein Beispielgitternetz und den entsprechenden Texturatlas.

![Zeigt ein Beispielgitternetz und den entsprechenden Texturatlas.](images/uvatlas1.jpg)

Dieses Beispiel zeigt ein Gitternetz (auf der linken Seite) und die entsprechende Uv-Raum-Normalkarte (auf der rechten Seite). Beachten Sie, dass der Texturatlas mehrere Gruppen oder Cluster mit Daten enthält. Jeder Cluster wird als Diagramm bezeichnet, und im obigen Beispiel enthält displays die normalen Daten für einen Teil des Gitters.

Die D3DX UVAtlas-APIs generieren automatisch einen optimalen, nicht überlappenden Texturatlas. Die APIs stellen Eingabeparameter zur Verfügung, mit denen Sie:

-   Minimieren Sie Texturstreckung, Verzerrung und Unterzeichnung.
-   Maximieren Sie die Texturraum-Packdichte für eine effiziente Nutzung des Arbeitsspeichers.
-   Stellen Sie eine gleichmäßige Stichprobenentnahme über das Gitternetz hinweg zur Verfügung, wodurch Diskontinuitäten bei der Samplinghäufigkeit minimiert werden.

## <a name="how-uvatlas-works"></a>Funktionsweise von UVAtlas

Die UVAtlas-APIs (siehe [UVAtlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generieren einen Texturatlas, indem sie eine Oberfläche in Diagramme partitionieren und die Diagramme in einen Texturatlas packen. Verwenden [**Sie D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) und [**D3DXUVAtlasPack,**](d3dxuvatlaspack.md) um diese Schritte separat durchzuführen. oder verwenden [**Sie D3DXUVAtlasCreate,**](d3dxuvatlascreate.md) um einen einzelnen Aufruf zu partitionieren, zu parametrisieren und zu packen.

-   [Partitionieren und Parametrisieren eines Gitters](#partitioning-and-parameterizing-a-mesh)
-   [Verwenden integrierter Metriktensoren zum Steuern der Parametrisierung](#using-integrated-metric-tensors-to-control-parameterization)
-   [Verwenden von Adjacency-Daten für vom Benutzer angegebene Erker](#using-adjacency-data-for-user-specified-creases)
-   [Packen von Diagrammen in einen Atlas](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a>Partitionieren und Parametrisieren eines Gitters

Zuerst wird das Gitternetz in Diagramme partitioniert, dann wird jedes Diagramm in einen eigenen \[ 0,1 \] UV-Raum parametrisiert. Ein Zylinder kann mit einem Diagramm parametrisiert werden. Eine Kugel erfordert dagegen zwei Diagramme, wie in der folgenden Abbildung dargestellt.

![Abbildung einer in zwei Diagramme partitionierten Kugel](images/uvatlas3.jpg)

Ein Gitternetz, das mit einem einzelnen Diagramm parametrisiert werden kann, wird als "homeomorph zu einem Datenträger" klassifiziert, was bedeutet, dass Sie einen unendlich flexiblen, unendlich stretchbaren Datenträger über das Diagramm verteilen und die Geometrie perfekt abdecken können. Dieses Stretching, das als Homeomorphie bezeichnet wird, ist eine bidirektionale Funktion. Das bedeutet, dass Sie von einer Parametrisierung zur anderen wechseln können, ohne Informationen zu verlieren.

Sehr wenige reale Gitternetze können in zwei Dimensionen parametrisiert werden, ohne das Gitternetz in Cluster oder Diagramme zu trennen. Die folgende Abbildung zeigt ein weiteres Beispielgitternetz und den entsprechenden Texturatlas.

![Zeigt ein Beispielgitternetz mit verschiedenen Formen und dem entsprechenden Texturatlas.](images/uvatlas2.jpg)

Es gibt zwei Parameter, die die Anzahl der erstellten Diagramme bestimmen:

-   Die maximale Anzahl von Diagrammen, die für den Atlas zulässig sind
-   Die maximal zulässige Stretchingmenge für jedes Diagramm

Der Umfang der Streckung bestimmt die Anzahl der generierten Diagramme und die Gesamtqualität der Stichprobenentnahme. Die Streckung reicht von 0,0 (ohne Stretching) bis 1,0 (beliebige Stretchingmenge). D3DXUVAtlasCreate und D3DXUVAtlasPartition geben die maximale Streckung zurück, die vom Algorithmus generiert wurde. Die folgende Abbildung zeigt ein weiteres Beispielgitternetz und den entsprechenden Texturatlas.

![Abbildung eines Beispielgitters und des entsprechenden Texturatlas](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a>Verwenden integrierter Metriktensoren zum Steuern der Parametrisierung

Die Texturraumpriorisierung kann pro Dreieck angegeben werden. Integrierte Metriktensoren können bereitgestellt werden, um zu steuern, wie Dreiecke im resultierenden Texturraumatlas gestreckt werden. IMTs können direkt angegeben oder basierend auf einem Eingabesignal mithilfe der D3DX IMT-Berechnungsfunktionen berechnet werden. Ein integrierter Metrik-Tensor (oder IMT) ist eine symmetrische 2x2-Matrix, die beschreibt, wie ein Dreieck im Atlas gestreckt wird. Jeder IMT wird durch 3 Gleitkommakomma definiert. Rufen Sie sie auf (a,b,c). Sie können wie hier dargestellt in einer symmetrischen 2x2-Matrix angeordnet werden:


```
a b
b c
```



Anschließend kann der IMT verwendet werden, um den Abstand zwischen zwei Vektoren zu finden. Bei zwei Vektoren v1 und v2, wobei :


```
vector v1
vector v2 = v1 + (s,t)
```



Der Abstand zwischen v1 und v2 kann wie folgt berechnet werden:


```
sqrt((s, t) * M * (s, t)^T)
```



Anders ausgedrückt: Der Vektor (s,t) könnte die Größe der Streckung in beliebiger Richtung im U-V-Raum sein. In diesem Fall ist der s-Vektor eine Richtung vom ersten zum zweiten Scheitelpunkt, und t ist das Kreuzprodukt von normal und s. Zum Beispiel:


```
(1,1) * (1,1) = (2,2)
        (1,1)
IMT(1,1,1) scales by 2
```




```
(1,-1) * (1,1) = (0,0)
         (1,1)
IMT(2,0,2) scales by 2 with no shearing
```



IMTs können direkt angegeben oder basierend auf einem Eingabesignal mithilfe der D3DX IMT-Berechnungsfunktionen berechnet werden: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal und D3DXComputeIMTFromTexture-Grafiken. \_

Geben Sie IMT-Daten direkt an, wenn Sie steuern möchten, wie Texturraum einzelnen Dreiecken zugeordnet wird. Ordnen Sie dadurch wichtigen Bereichen eines Gitters (z. B. dem Gesicht oder dem Logo einer Figur oder Bereichen einer Szene in der Nähe des Fußwegs eines Spielers) mehr Fläche im Atlas zu. Durch Angeben von IMTs, bei denen es sich um Vielfache der Identitätsmatrix handelt, werden die resultierenden Dreiecke im Texturraum einheitlich skaliert.

Beispielsweise können Sie bei einer auflösungsintensiven normal-Karte IMT berechnen, um mehr Texturraum für Bereiche mit einem Signal mit höherer Frequenz in der normalen Karte zu bieten. Dreiecke, die "flach" sind (die konstanten Regionen der ursprünglichen normalen Karte zugeordnet sind), erhalten weniger Texturraum. Dreiecke, die eine große Menge normaler Kartendetails enthalten, erhalten im Endergebnis mehr Texturbereich. Anschließend können Sie die normale Karte in einer kleineren Textur neusampeln, aber Details verwalten, oder Sie können die normale Karte mit der besseren UV-Zuordnung neu kompilieren.

### <a name="using-adjacency-data-for-user-specified-creases"></a>Verwenden von Adjacency-Daten für vom Benutzer angegebene Erker

Für die Partitionierungsfunktion können benutzerdefinierte Informationen zur Adjazienz bereitgestellt werden, um vordefinierte Rillen im Gitternetz zu beschreiben und so eine Diagrammgrenze zwischen angrenzenden Gesichtern zu definieren. Dies ist eine einfache Möglichkeit für den Aufrufer, eine eigene Diagrammpartitionierung als Eingabe in den Algorithmus anzugeben, wodurch Diagramme weiter verfeinert werden, um die Streckung unter den maximal zulässigen Wert zu bringen.

### <a name="example"></a>Beispiel

In diesem Beispiel wird veranschaulicht, wie Sie die UVAtlas-APIs und den DirectX-Viewer (Dxviewer.exe) verwenden können, um Diskontinuitäten in Ihrem Modell zu finden und zu beheben, die sich erheblich auf die Größe Ihres Texturatlas auswirken können. Sie können sich Dxviewer.exe DirectX SDK darüber informieren. Dxviewer.exe version august 2009 aus dem DirectX SDK entfernt wurde, benötigen Sie mindestens das DirectX SDK vom August 2009, um es zu erhalten. Informationen zum DirectX SDK finden Sie unter [Wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

Angenommen, Sie haben mit einem Modell in Ihrer bevorzugten Software für die Inhaltsgenerierung begonnen (in diesem Beispiel wird ein in Maya erstelltes Hauptmodell verwendet). Exportieren Sie das texturierte Modell in eine X-Datei, und erstellen Sie mit D3DXUVAtlasCreate einen Texturatlas. Der resultierende Texturatlas würde in etwa wie in der folgenden Abbildung aussehen.

![Abbildung eines Atlass für ein Darstellungsmodell](images/uvatlas5.jpg)

Der Atlas verfügt über 22 Diagramme und eine maximale Streckenzahl von 0,994.

Sehen Sie sich nun das texturierte Modell an, um zu sehen, wie gut der Texturatlas der Geometrie zu ordnet. Laden Sie dazu das Modell in das Viewertool:

-   Öffnen Sie das Viewertool aus den DirectX-Hilfsprogrammen.
-   Laden Sie die X-Datei, indem Sie auf die Schaltfläche Öffnen klicken.
-   Aktivieren Sie die Anzeigeoption crease, indem Sie auf die Schaltfläche Ansicht klicken und Im Popup auf Creases (Erstellen) klicken.

Die folgende Abbildung zeigt, was im Viewertool angezeigt werden sollte.

![Abbildung eines texturierten Gitters im Viewertool](images/uvatlas6c.jpg)

Jede Linie ist eine Linie, die eine angrenzende Kante zwischen zwei Diagrammen im Texturatlas ist. Die Anzahl der vom Algorithmus generierten Diagramme wird durch geringfügige Unterschiede verursacht, möglicherweise aufgrund von Diskontinuitäten in den Normalzahlen. Diese kleinen Unterschiede können durch unterschiedliche Daten verringert werden, d.&a; daten, die nahezu gleich sind. So führen Sie die Normalen und Skinweights aus:

-   Führen Sie das DirectX Ops-Tool (dxops.exe) mit der folgenden Befehlszeile im Gittermodell aus (ersetzen Sie "modelName.x" durch den Namen Ihres Modells):
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

Dies vergleicht die Normal- und Skinweights, und wenn sie sich im Wert um weniger als 2,01 unterscheiden, werden die Daten gleich gemacht. Die folgenden Abbildungen zeigen eine nah am Auge, um die Rillen vor der Brille (auf der linken Seite) und die Rillen nach der Brille (auf der rechten Seite) zu sehen:

![Abbildung von Erbungen vor dem Schweissen](images/uvatlas6a.jpg)![Abbildung von Erbungen nach einer Darstellung](images/uvatlas6b.jpg)

Abbildung 7: Entfernen von Erderien nach 300%%0

In diesem Beispiel wurden 86 Scheitelungen aus dem Eingabegitternetz entfernt. Mit weniger Rillen im Gitternetz können Sie den Atlas neu generieren, wie in der folgenden Abbildung dargestellt.

![Abbildung des neuen Atlas mit entfernten Rillen](images/uvatlas8.jpg)

Der Atlas verfügt nur über 7 Diagramme und eine maximale Stretchingdauer von ungefähr 0,0776. Der neue Atlas passt jetzt in eine kleinere Textur (in diesem Beispiel etwa 30 % kleiner).

### <a name="packing-charts-into-an-atlas"></a>Packen von Diagrammen in einen Atlas

Nachdem ein Gitternetz in individuell parametrisierte Diagramme partitioniert wurde, müssen die Diagramme effizient in eine einzelne Texturkarte gepackt werden. Dies wird als zweiter Schritt von D3DXUVAtlasCreate ausgeführt oder kann explizit durch Aufrufen von D3DXUVAtlasPack aufgerufen werden.

Gepackte Diagramme werden durch eine benutzerdefinierte Bundstegbreite getrennt. Die Gutterbreite entspricht der Trennung zwischen Diagrammen und ermöglicht bilineare Interpolation und Mip-Zuordnung, um das Rendern von Artefakten an Diagrammgrenzen zu vermeiden. D3DX stellt eine Schnittstelle zum automatischen Ausfüllen dieser Gutter bereit. Weitere Informationen finden Sie unter [**ID3DXTextureGutterHelper.**](id3dxtexturegutterhelper.md)

## <a name="integrating-uvatlas-into-your-pipeline"></a>Integrieren von UVAtlas in Ihre Pipeline

Diese Funktionen können nicht nur vor dem Zeichnen von Texturen aufgerufen werden, sie können auch in eine automatisierte Grafikpipeline integriert werden. Beispielsweise kann ein UVAtlas-Aufruf automatisch ausgegeben werden, nachdem eine Ressource aktualisiert wurde, bevor eine PRT-Simulation oder ein normaler Zuordnungsdurchlauf durchgeführt wird. Dadurch wird vermieden, dass die UV-Zuordnung eines Objekts manuell repariert werden muss, wenn die Topologie des Gittermodells geändert wurde.

Informationen zur Verwendung der UVAtlas-Funktionen finden Sie unter [UV Atlas Command-Line Tool (uvatlas.exe).](https://github.com/Microsoft/UVAtlas)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Weiterführende Themen](advanced-topics.md)
</dt> </dl>

 

 
