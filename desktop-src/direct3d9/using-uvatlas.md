---
description: Viele Renderingverfahren und Inhalts Generierungs Techniken erfordern eine eindeutige, nicht überlappende Zuordnung eines 2D-Signals (z. b. eine Textur) zu einem Mesh.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Verwenden von uvatlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b335dd6ea94a3db0c0760b0d07a0b8df3fe4c7c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104218903"
---
# <a name="using-uvatlas-direct3d-9"></a>Verwenden von uvatlas (Direct3D 9)

Viele Renderingverfahren und Inhalts Generierungs Techniken erfordern eine eindeutige, nicht überlappende Zuordnung eines 2D-Signals (z. b. eine Textur) zu einem Mesh. Diese Techniken umfassen Folgendes:

-   Normale/Verschiebungs Zuordnung
-   Simulationen für Textur Raum-PRT und helle Karten
-   Oberflächendarstellung
-   Textur Raumbeleuchtung

Das manuelle Erstellen einer eindeutigen UV-Zuordnung ist oft zeitaufwändig und mühsam. Dies trifft vor allem dann zu, wenn die Eingabe Geometrie Komplex ist und eine effiziente/niedrige Verzerrung der Textur Raumauslastung gewünscht wird. Die folgende Abbildung zeigt ein Beispiel Netz und den zugehörigen Textur Atlas.

![Zeigt ein Beispiel Netz und den zugehörigen Textur Atlas an.](images/uvatlas1.jpg)

Dieses Beispiel zeigt ein Mesh (auf der linken Seite) und die entsprechende UV-Leerraum-normale Karte (auf der rechten Seite). Beachten Sie, dass der Textur Atlas mehrere Gruppen oder Cluster von Daten enthält. Jeder Cluster wird als Diagramm bezeichnet, und im obigen Beispiel enthält die Anzeige die normalen Daten für einen Teil des Netzes.

Die D3DX uvatlas-APIs generieren automatisch einen optimalen, nicht überlappenden Textur Atlas. Die APIs bieten Eingabeparameter, die Folgendes ermöglichen:

-   Minimieren Sie Textur Streckung, Verzerrung und Unterstichprobe.
-   Maximieren Sie die Dichte der Textur Raum Komprimierung für die effiziente Arbeitsspeicher Nutzung.
-   Stellen Sie eine gleichmäßige Stichprobenentnahme im Mesh bereit, wodurch Diskontinuitäten bei der Stichproben Häufigkeit minimiert werden

## <a name="how-uvatlas-works"></a>Funktionsweise von uvatlas

Die uvatlas-APIs (siehe [uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generieren einen Textur Atlas, indem eine Oberfläche in Diagramme partitioniert und die Diagramme in einen Textur Atlas verpackt werden. Verwenden Sie [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) und [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) , um diese Schritte separat auszuführen. oder verwenden Sie [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) , um einen einzelnen-Befehl zu partitionieren, zu parametrisieren und zu verpacken.

-   [Partitionieren und parametrialisieren eines Netzes](#partitioning-and-parameterizing-a-mesh)
-   [Verwenden integrierter metriktensoren zum Steuern der Parametrisierung](#using-integrated-metric-tensors-to-control-parameterization)
-   [Verwenden von Daten für benutzerdefinierte Aliasnamen](#using-adjacency-data-for-user-specified-creases)
-   [Packen von Diagrammen in einen Atlas](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a>Partitionieren und parametrialisieren eines Netzes

Zuerst wird das Mesh in Diagramme partitioniert, dann wird jedes Diagramm in seinen eigenen \[ , 0, 1- \] UV-Bereich parametrisiert. Ein Zylinder kann mit einem Diagramm parametrisiert werden. eine Kugel auf der anderen Seite erfordert zwei Diagramme, wie in der folgenden Abbildung dargestellt.

![Abbildung einer in zwei Diagrammen partitionierten Kugel](images/uvatlas3.jpg)

Ein Mesh, das mit einem einzelnen Diagramm parametrisiert werden kann, wird als "homeomorph to a Disk" klassifiziert, d. h., Sie könnten einen unendlich flexiblen, unendlich streiebaren Datenträger über das Diagramm verteilen und die Geometrie perfekt abdecken. Diese Streckung, die als homeomorphism bezeichnet wird, ist eine bidirektionale Funktion. Dies bedeutet, dass Sie von einer Parametrisierung zum anderen wechseln können, ohne dass Informationen verloren gehen.

Sehr wenige reale Netze können in zwei Dimensionen parametrisiert werden, ohne das Mesh in Cluster oder Diagramme zu unterteilen. Die folgende Abbildung zeigt ein weiteres Beispiel Mesh und den zugehörigen Textur Atlas.

![Zeigt ein Beispiel Netz mit unterschiedlichen Formen und dem zugehörigen Textur Atlas.](images/uvatlas2.jpg)

Es gibt zwei Parameter, die die Anzahl der erstellten Diagramme bestimmen:

-   Die maximale Anzahl von Diagrammen, die für den Atlas zulässig sind.
-   Die maximal zulässige Streckung für jedes Diagramm.

Der Umfang der Streckung bestimmt die Anzahl der generierten Diagramme und die Gesamtqualität der Stichprobenentnahme. Stretch reicht von 0,0 (keine Streckung) bis 1,0 (beliebige Streckung). D3DXUVAtlasCreate und D3DXUVAtlasPartition geben die maximale Streckung zurück, die vom Algorithmus generiert wird. Die folgende Abbildung zeigt ein weiteres Beispiel Mesh und den zugehörigen Textur Atlas.

![Abbildung eines Beispiel Netzes und des zugehörigen Textur Atlas](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a>Verwenden integrierter metriktensoren zum Steuern der Parametrisierung

Die Priorisierung von Textur Raum kann pro Dreieck angegeben werden. Integrierte metriktensoren können bereitgestellt werden, um zu steuern, wie Dreiecke im resultierenden Textur Raum-Atlas gestreckt werden. IMT kann mithilfe der D3DX IMT-Berechnungsfunktionen direkt oder basierend auf einem Eingabe Signal angegeben werden. Ein integrierter metriktensor (oder IMT) ist eine symmetrische 2 x 2-Matrix, die beschreibt, wie ein Dreieck im Atlas gestreckt wird. Jedes IMT wird durch drei Gleit Komma Werte definiert und ruft Sie auf (a, b, c). Sie können wie folgt in einer symmetrischen 2 x 2-Matrix angeordnet werden:


```
a b
b c
```



Anschließend kann der IMT verwendet werden, um den Abstand zwischen zwei Vektoren zu ermitteln. Zwei Vektoren v1 und v2, wobei Folgendes gilt:


```
vector v1
vector v2 = v1 + (s,t)
```



Der Abstand zwischen V1 und v2 kann wie folgt berechnet werden:


```
sqrt((s, t) * M * (s, t)^T)
```



Dies bedeutet, dass der Vektor (s, t) die Größe der Streckung in beliebiger Richtung in u-v-Raum aufweisen kann. In diesem Fall ist der s-Vektor eine Richtung vom ersten zum zweiten Scheitelpunkt, und t ist das Kreuz Produkt des normalen und des s. Beispiel:


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



IMT kann mithilfe der D3DX IMT-Berechnungsfunktionen (D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal und D3DXComputeIMTFromTexture) direkt oder basierend auf einem Eingabe Signal angegeben werden \_ .

Geben Sie IMT-Daten direkt an, wenn Sie steuern möchten, wie der Textur Raum einzelnen Dreiecken zugeordnet wird. Auf diese Weise weisen Sie den wichtigen Bereichen eines Netzes (z. b. das Gesicht oder das Brust Logo eines Zeichens oder die Bereiche einer Szene in der Nähe des Walking-Pfades eines Players) mehr Bereiche zu. Durch die Angabe von IMT, die Vielfache der Identitätsmatrix sind, werden die resultierenden Dreiecke im Textur Bereich einheitlich skaliert.

Wenn Sie z. b. eine hochauflösende normale Karte haben, können Sie IMT berechnen, um mehr Textur Raum für Bereiche mit höherem Frequenz Signal in der normalen Karte bereitzustellen. Dreiecke, die "Flat" sind (die Konstanten Bereichen der ursprünglichen normalen Karte zugeordnet sind) erhalten weniger Textur Bereich. Dreiecke, die eine große Anzahl von normalkarten Details enthalten, erhalten im Endergebnis mehr Textur Bereich. Anschließend können Sie die normale Zuordnung in eine kleinere Textur übernehmen, aber die Details beibehalten, oder Sie können die normale Karte mit der optimalen UV-Zuordnung neu berechnen.

### <a name="using-adjacency-data-for-user-specified-creases"></a>Verwenden von Daten für benutzerdefinierte Aliasnamen

Benutzerdefinierte Informations Informationen können für die Partitionierungsfunktion bereitgestellt werden, um vordefinierte Aliase im Mesh zu beschreiben, und definieren somit eine Diagramm Grenze zwischen angrenzenden Gesichtern. Dies ist eine einfache Möglichkeit für den Aufrufer, seine eigene Diagramm Partitionierung als Eingabe in den Algorithmus anzugeben, wodurch Diagramme weiter verfeinert werden, um die Streckung unter den maximal zulässigen Wert zu bringen.

### <a name="example"></a>Beispiel

In diesem Beispiel wird veranschaulicht, wie Sie mit den uvatlas-APIs und dem DirectX-Viewer (Dxviewer.exe) Diskontinuitäten in Ihrem Modell suchen und beheben können, die sich erheblich auf die Größe Ihres Textur Atlas auswirken können. Sie erhalten Dxviewer.exe und erfahren mehr über das DirectX SDK. Dxviewer.exe wurde nach der Version von August 2009 aus dem DirectX SDK entfernt. damit Sie es erhalten, benötigen Sie mindestens das DirectX SDK vom August 2009. Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).

Angenommen, Sie haben mit einem Modell in Ihrer bevorzugten Inhalts Generierungs Software gestartet (in diesem Beispiel wird ein in Maya erstelltes Zwerg Hauptmodell verwendet). Exportieren Sie das strukturierte Modell in eine x-Datei, und erstellen Sie einen Textur Atlas mit D3DXUVAtlasCreate. Der resultierende Textur Atlas würde in etwa wie in der folgenden Abbildung aussehen.

![Abbildung eines Atlas für ein Zwerg Modell](images/uvatlas5.jpg)

Der Atlas verfügt über 22 Diagramme und eine maximale Streckung von 0,994.

Sehen Sie sich nun das strukturierte Modell an, um zu sehen, wie gut der Geometrie Text der Geometrie zugeordnet wird. Laden Sie dazu das Modell in das Viewer-Tool:

-   Öffnen Sie das Viewer-Tool über die DirectX-Hilfsprogramme.
-   Laden Sie die x-Datei, indem Sie auf die Schaltfläche Öffnen klicken.
-   Aktivieren Sie die Option Anzeige aktivieren, indem Sie auf die Schaltfläche Ansicht klicken und im Popup Fenster die Option zum Auswählen von "

In der folgenden Abbildung wird gezeigt, was im Viewer-Tool angezeigt werden sollte.

![Abbildung eines strukturierten Netzes im Viewer-Tool](images/uvatlas6c.jpg)

Jede Zeile ist eine krease, bei der es sich um einen angrenzenden Rand zwischen zwei Diagrammen im Textur Atlas handelt. Die Anzahl der vom Algorithmus generierten Diagramme wird durch geringfügige Unterschiede verursacht, die möglicherweise aufgrund von Diskontinuitäten in den normalen auftreten. Diese kleinen Unterschiede können durch das Schweißen von Daten reduziert werden, d. h. durch das Erzwingen von Daten, die nahezu gleich sind. So Verschweißen Sie die normale und die skingewichtungen:

-   Führen Sie das DirectX OPS (dxops.exe)-Tool mit der folgenden Befehlszeile im Mesh aus (ersetzen Sie "modelname. x" durch den Namen des Modells):
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

Dadurch werden die normale und skingewichtungen verglichen, und wenn Sie sich im Wert um weniger als 2,01 unterscheiden, werden die Daten gleich. In den folgenden Abbildungen wird eine schließende Ansicht angezeigt, um die vor dem Schweißen (auf der linken Seite) und die Lösch Vorgängen nach dem Schweißen (auf der rechten Seite) Vorgängen anzuzeigen:

![Abbildung der Aliase vor dem Schweißen](images/uvatlas6a.jpg)![Abbildung der Aliase nach dem Schweißen](images/uvatlas6b.jpg)

Abbildung 7: Entfernen von Aliasen durch Schweißen

In diesem Beispiel wurden 86 Vertices aus dem eingabemesh entfernt. Mit weniger kreasen im Mesh können Sie den Atlas neu generieren, wie in der folgenden Abbildung dargestellt.

![Abbildung des neuen Atlas mit entfernten löschenden](images/uvatlas8.jpg)

Der Atlas verfügt nur über 7 Diagramme und eine maximale Streckung von ungefähr 0,0776. Der neue Atlas passt nun in eine kleinere Textur (etwa 30% kleiner in diesem Beispiel).

### <a name="packing-charts-into-an-atlas"></a>Packen von Diagrammen in einen Atlas

Nachdem ein Mesh in einzeln parametrisierte Diagramme partitioniert wurde, müssen die Diagramme effizient in eine einzelne Textur Zuordnung gepackt werden. Dies wird als zweiter Schritt von D3DXUVAtlasCreate ausgeführt oder kann explizit durch Aufrufen von D3DXUVAtlasPack aufgerufen werden.

Gepackte Diagramme werden durch eine benutzerdefinierte Breite getrennt. Der bundgerbreite ist die Menge der Trennung zwischen Diagrammen und ermöglicht die bilineare Interpolations-und MIP-Zuordnung, um das Rendern von Artefakten an Diagramm Grenzen zu vermeiden. D3DX stellt eine Schnittstelle zum automatischen Ausfüllen dieser Bundstege bereit. Weitere Informationen finden Sie unter [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .

## <a name="integrating-uvatlas-into-your-pipeline"></a>Integrieren von uvatlas in ihre Pipeline

Diese Funktionen können nicht nur vor dem Textur zeichnen, sondern auch in eine automatisierte Grafik Pipeline integriert werden. Beispielsweise kann ein uvatlas-Befehl automatisch ausgegeben werden, nachdem ein Objekt aktualisiert wurde, bevor eine PRT-Simulation oder ein normaler Zuordnungs Durchlauf durchgeführt wird. Dadurch wird vermieden, dass die UV-Zuordnung eines Objekts manuell repariert werden muss, wenn die Topologie des Netzes geändert wurde.

Eine Beispiel Verwendung der uvatlas-Funktionen finden Sie im [Command-Line Tool für UV-Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Themen](advanced-topics.md)
</dt> </dl>

 

 
