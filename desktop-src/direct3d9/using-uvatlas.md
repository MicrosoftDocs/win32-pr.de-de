---
description: Viele Rendering- und Inhaltsgenerierungstechniken erfordern eine eindeutige, nicht überlappende Karte eines 2D-Signals (z. B. einer Textur) auf einem Gitternetz.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Verwenden von UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8faeaa0a416f6f062c81c4101ff47d5222ca75d
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826328"
---
# <a name="using-uvatlas-direct3d-9"></a>Verwenden von UVAtlas (Direct3D 9)

> [!NOTE]
> UVAtlas wurde ursprünglich in der jetzt veralteten D3DX9-Utilty-Bibliothek ausgeliefert. Die neueste Version ist unter [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas)verfügbar.

Viele Rendering- und Inhaltsgenerierungstechniken erfordern eine eindeutige, nicht überlappende Karte eines 2D-Signals (z. B. einer Textur) auf einem Gitternetz. Zu diesen Techniken gehören:

-   Normal-/Verschiebungszuordnung
-   Texturraum-PRT-Simulationen und Lichtkarten
-   Oberflächenzeichnung
-   Texturraumbeleuchtung

Das manuelle Generieren einer eindeutigen UV-Zuordnung ist oft zeitaufwändig und mühsam. Dies gilt insbesondere, wenn die Eingabegeometrie komplex ist und eine effiziente/verzerrungsfreie Texturraumnutzung gewünscht ist. Die folgende Abbildung zeigt ein Beispielgitternetz und den entsprechenden Texturat atlas.

![Zeigt ein Beispielgitternetz und den entsprechenden Texturat atlas.](images/uvatlas1.jpg)

Dieses Beispiel zeigt ein Gitternetz (links) und die entsprechende Normalkarte des UV-Raumes (auf der rechten Seite). Beachten Sie, dass der Texturat atlas mehrere Gruppen oder Cluster von Daten enthält. Jeder Cluster wird als Diagramm bezeichnet und enthält im obigen Beispiel die normalen Daten für einen Teil des Gitternetzes.

Die D3DX UVAtlas-APIs generieren automatisch einen optimalen, nicht überlappenden Texturat atlas. Die APIs stellen Eingabeparameter bereit, die Folgendes ermöglichen:

-   Minimieren Sie Texturstreckung, Verzerrung und Untersampling.
-   Maximieren der Texturraum-Komprimierungsdichte zur effizienten Verwendung des Arbeitsspeichers.
-   Stellen Sie eine gleichmäßige Stichprobenentnahme über das Gitternetz bereit, um Diskontinuitäten bei der Stichprobenhäufigkeit zu minimieren.

## <a name="how-uvatlas-works"></a>Funktionsweise von UVAtlas

Die UVAtlas-APIs (siehe [UVAtlas-Funktionen)](dx9-graphics-reference-d3dx-functions-uvatlas.md)generieren einen Texturat atlas, indem sie eine Oberfläche in Diagramme partitionieren und die Diagramme in einen Texturat atlas packen. Verwenden Sie [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) und [**D3DXUVAtlasPack,**](d3dxuvatlaspack.md) um diese Schritte separat auszuführen. oder verwenden [**Sie D3DXUVAtlasCreate,**](d3dxuvatlascreate.md) um einen einzelnen Aufruf zu partitionieren, zu parametrisieren und zu packen.

-   [Partitionieren und Parametrisieren eines Gitternetzes](#partitioning-and-parameterizing-a-mesh)
-   [Verwenden integrierter Metrik tensors zum Steuern der Parametrisierung](#using-integrated-metric-tensors-to-control-parameterization)
-   [Verwenden von Adjazenzdaten für vom Benutzer angegebene Errungen](#using-adjacency-data-for-user-specified-creases)
-   [Packen von Diagrammen in einen Atlas](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a>Partitionieren und Parametrisieren eines Gitternetzes

Zuerst wird das Gitternetz in Diagramme partitioniert, dann wird jedes Diagramm in einen eigenen \[ 0,1 \] UV-Raum parametrisiert. Ein Zylinder kann durch ein Diagramm parametrisiert werden. Eine Kugel hingegen erfordert zwei Diagramme, wie in der folgenden Abbildung dargestellt.

![Abbildung einer In zwei Diagramme partitionierten Kugel](images/uvatlas3.jpg)

Ein Gitternetz, das mit einem einzelnen Diagramm parametrisiert werden kann, wird als "homeomorph zu einem Datenträger" klassifiziert. Das bedeutet, dass Sie einen unendlich flexiblen, unendlich stretchbaren Datenträger über das Diagramm verteilen und die Geometrie perfekt abdecken können. Diese Stretchingfunktion, die als Homeomorphie bezeichnet wird, ist eine bidirektionale Funktion. Das bedeutet, dass Sie von einer Parametrisierung zur anderen wechseln können, ohne Informationen zu verlieren.

Sehr wenige reale Gitternetze können in zwei Dimensionen parametrisiert werden, ohne das Gitternetz in Cluster oder Diagramme zu unterteilen. Die folgende Abbildung zeigt ein weiteres Beispielgitternetz und den entsprechenden Texturat atlas.

![Zeigt ein Beispielgitternetz mit unterschiedlichen Formen und dem entsprechenden Texturat atlas.](images/uvatlas2.jpg)

Es gibt zwei Parameter, die die Anzahl der erstellten Diagramme bestimmen:

-   Die maximale Anzahl von Diagrammen, die für den Atlas zulässig sind
-   Die maximal zulässige Stretchingmenge für jedes Diagramm.

Die Stretchingmenge bestimmt die Anzahl der generierten Diagramme und die Gesamtqualität der Stichprobenentnahme. Die Stretchingspanne reicht von 0,0 (ohne Stretching) bis 1,0 (beliebiger Stretchingwert). D3DXUVAtlasCreate und D3DXUVAtlasPartition geben die maximale Stretchingdauer zurück, die vom Algorithmus generiert wird. Die folgende Abbildung zeigt ein weiteres Beispielgitternetz und den entsprechenden Texturat atlas.

![Abbildung eines Beispielgitters und des entsprechenden Texturat atlas](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a>Verwenden integrierter Metrik tensors zum Steuern der Parametrisierung

Die Priorisierung des Texturraums kann auf Dreiecksbasis angegeben werden. Integrierte Metriktensoren können bereitgestellt werden, um zu steuern, wie Dreiecke im resultierenden Texturraumat atlas gestreckt werden. IMT-Dateien können mithilfe der D3DX IMT-Berechnungsfunktionen direkt angegeben oder basierend auf einem Eingabesignal berechnet werden. Ein integrierter Metrik tensor (oder IMT) ist eine symmetrische 2x2-Matrix, die beschreibt, wie ein Dreieck im Atlas gestreckt wird. Jedes IMT wird durch drei Gleitkommazeichen definiert, die sie aufrufen (a,b,c). Sie können in einer symmetrischen 2x2-Matrix wie folgt angeordnet werden:


```
a b
b c
```



Anschließend kann das IMT verwendet werden, um den Abstand zwischen zwei Vektoren zu ermitteln. Gibt die beiden Vektoren v1 und v2 an, wobei :


```
vector v1
vector v2 = v1 + (s,t)
```



Der Abstand zwischen v1 und v2 kann wie folgt berechnet werden:


```
sqrt((s, t) * M * (s, t)^T)
```



Anders ausgedrückt: Der Vektor (s,t) könnte die Größe der Stretchung in beliebiger Richtung im u-v-Raum sein. In diesem Fall ist der s-Vektor eine Richtung vom ersten zum zweiten Scheitelpunkt, und t ist das Kreuzprodukt von normal und s. Zum Beispiel:


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



IMT-Dateien können direkt oder basierend auf einem Eingabesignal mithilfe der D3DX IMT-Berechnungsfunktionen angegeben oder berechnet werden: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal und D3DXComputeIMTFromTexture. \_

Geben Sie IMT-Daten direkt an, wenn Sie steuern möchten, wie Texturraum einzelnen Dreiecken zugeordnet wird. Ordnen Sie auf diese Weise wichtigen Bereichen eines Gitternetzes (z. B. dem Gesicht oder dem Logo eines Zeichens oder Bereichen einer Szene in der Nähe des Fußpfads eines Spielers) mehr Bereiche im Atlas zu. Durch Angeben von IMT-Dateien, bei denen es sich um Vielfache der Identitätsmatrix handelt, werden die resultierenden Dreiecke gleichmäßig im Texturraum skaliert.

Beispielsweise können Sie bei einer normalen Karte mit hoher Auflösung IMT berechnen, um mehr Texturraum für Bereiche mit höherer Frequenz in der normalen Karte bereitzustellen. Dreiecke, die "flach" sind (die konstanten Bereichen der ursprünglichen normalen Karte zugeordnet sind), erhalten weniger Texturraum. Dreiecke, die viele normale Kartendetails enthalten, erhalten mehr Texturbereich im Endergebnis. Sie können dann die normale Karte in einer kleineren Textur neu zusammensetzen, aber Details beibehalten, oder Sie können die normale Karte mit der optimaleren UV-Zuordnung neu zusammensetzen.

### <a name="using-adjacency-data-for-user-specified-creases"></a>Verwenden von Adjazenzdaten für vom Benutzer angegebene Errungen

Benutzerdefinierte Adjazenzinformationen können der Partitionierungsfunktion bereitgestellt werden, um vordefinierte Erstellungen im Gitternetz zu beschreiben und so eine Diagrammgrenze zwischen angrenzenden Gesichtern zu definieren. Dies ist eine einfache Möglichkeit für den Aufrufer, seine eigene Diagrammpartitionierung als Eingabe in den Algorithmus anzugeben. Dadurch werden Diagramme weiter verfeinern, um die Stretchung unter das maximal zulässige Maximum zu bringen.

### <a name="example"></a>Beispiel

In diesem Beispiel wird veranschaulicht, wie Sie die UVAtlas-APIs und den DirectX-Viewer (Dxviewer.exe) verwenden können, um Diskontinuitäten in Ihrem Modell zu finden und zu beheben, die sich erheblich auf die Größe Ihres Texturat atlas auswirken können. Sie können Dxviewer.exe abrufen und sich über das DirectX SDK darüber informieren. Dxviewer.exe wurde nach der Version vom August 2009 aus dem DirectX SDK entfernt, sodass Sie mindestens das DirectX SDK vom August 2009 benötigen, um es zu erhalten. Informationen zum DirectX SDK finden Sie unter [Wo befindet sich das DirectX SDK?](../directx-sdk--august-2009-.md).

Angenommen, Sie haben mit einem Modell in Ihrer bevorzugten Software zum Generieren von Inhalten begonnen (in diesem Beispiel wird ein in Maya erstelltes Head-Modell verwendet). Exportieren Sie das texturierte Modell in eine X-Datei, und erstellen Sie mit D3DXUVAtlasCreate einen Texturat atlas. Der resultierende Texturat atlas würde in etwa wie in der folgenden Abbildung aussehen.

![Abbildung eines Atlas für ein Modell](images/uvatlas5.jpg)

Der Atlas verfügt über 22 Diagramme und eine maximale Streckung von 0,994.

Sehen Sie sich nun das texturierte Modell an, um zu sehen, wie gut der Texturat atlas der Geometrie zugeordnet ist. Laden Sie dazu das Modell in das Viewer-Tool:

-   Öffnen Sie das Viewer-Tool über die DirectX-Hilfsprogramme.
-   Laden Sie die X-Datei, indem Sie auf die Schaltfläche Öffnen klicken.
-   Aktivieren Sie die Anzeigeoption "Erstellen", indem Sie auf die Schaltfläche "Ansicht" klicken und im Popupfenster "Creases" auswählen.

Die folgende Abbildung zeigt, was im Viewer-Tool angezeigt werden sollte.

![Abbildung eines texturierten Gitters im Viewer-Tool](images/uvatlas6c.jpg)

Jede Linie ist eine Faltung, die einen angrenzenden Rand zwischen zwei Diagrammen im Texturat atlas darstellt. Die Anzahl der vom Algorithmus generierten Diagramme wird durch geringfügige Unterschiede verursacht, die möglicherweise auf Diskontinuitäten in den Normalitäten zurückzuführen sind. Diese kleinen Unterschiede können durch Verarbeitungsdaten reduziert werden, d. h. das Erzwingen von Daten, die fast gleich sind. So bestärken Sie die Normalitäten und Die Skinweights:

-   Führen Sie das DirectX Ops-Tool (dxops.exe) mit der folgenden Befehlszeile im Netz aus (ersetzen Sie dabei "modelName.x" durch den Namen Ihres Modells):
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

Dies vergleicht die Normalwerte und Skinweights, und wenn sie sich im Wert um weniger als 2,01 unterscheiden, werden die Daten gleich gemacht. Die folgenden Abbildungen zeigen eine Nahaufnahme des Auges, um die Erbildungen vor dem Strahl (auf der linken Seite) und die Erbildungen nach der Brille (auf der rechten Seite) zu sehen:

![Abbildung von Erbildungen vor dem Abschluss](images/uvatlas6a.jpg)![Abbildung der Erbildungen nach dem Abschluss](images/uvatlas6b.jpg)

Abbildung 7: Entfernen von Errungen nach 160000000000000000000000

In diesem Beispiel wurden 86 Scheitelpunkte aus dem Eingabegitter entfernt. Mit weniger Errungen im Gitternetz können Sie den Atlas neu generieren, wie in der folgenden Abbildung dargestellt.

![Abbildung des neuen Atlas mit entfernten Erbildungen](images/uvatlas8.jpg)

Der Atlas verfügt nur über 7 Diagramme und eine maximale Streckung von ca. 0,0776. Der neue Atlas passt jetzt in eine kleinere Textur (in diesem Beispiel etwa 30 % kleiner).

### <a name="packing-charts-into-an-atlas"></a>Packen von Diagrammen in einen Atlas

Nachdem ein Gitternetz in einzeln parametrisierte Diagramme partitioniert wurde, müssen die Diagramme effizient in eine einzelne Texturkarte gepackt werden. Dies wird als zweiter Schritt von D3DXUVAtlasCreate ausgeführt oder kann explizit durch Aufrufen von D3DXUVAtlasPack aufgerufen werden.

Gepackte Diagramme werden durch eine benutzerdefinierte Bundstegbreite getrennt. Die Gutterbreite entspricht der Trennung zwischen Diagrammen und ermöglicht bilineare Interpolation und Mip-Zuordnung, um das Rendern von Artefakten an Diagrammgrenzen zu vermeiden. D3DX stellt eine Schnittstelle zum automatischen Ausfüllen dieser Gutter bereit. Weitere Informationen finden Sie unter [**ID3DXTextureGutterHelper.**](id3dxtexturegutterhelper.md)

## <a name="integrating-uvatlas-into-your-pipeline"></a>Integrieren von UVAtlas in Ihre Pipeline

Diese Funktionen können nicht nur vor dem Zeichnen von Texturen als Interpreten aufgerufen werden, sie können auch in eine automatisierte Grafikpipeline integriert werden. Beispielsweise kann ein UVAtlas-Aufruf automatisch ausgegeben werden, nachdem ein Medienobjekt aktualisiert wurde, bevor eine PRT-Simulation oder ein normaler Zuordnungsdurchlauf ausgeführt wird. Dadurch wird vermieden, dass die UV-Zuordnung eines Objekts manuell repariert werden muss, wenn die Topologie des Gittermodells geändert wurde.

Informationen zur Verwendung der UVAtlas-Funktionen finden Sie im UV [Atlas Command-Line Tool (uvatlas.exe).](https://github.com/Microsoft/UVAtlas)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Weiterführende Themen](advanced-topics.md)
</dt> </dl>

 

 
