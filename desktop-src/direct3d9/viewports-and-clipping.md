---
description: Konzeptionell ist ein Viewport ein zweidimensionales (2D) Rechteck, in das eine 3D-Szene projiziert wird.
ms.assetid: eddadaa1-9181-47fa-8530-44aa46fea286
title: Viewports und Clipping (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57f64d17f7abf4e370406f984fa50037be6d44e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123343"
---
# <a name="viewports-and-clipping-direct3d-9"></a>Viewports und Clipping (Direct3D 9)

Konzeptionell ist ein Viewport ein zweidimensionales (2D) Rechteck, in das eine 3D-Szene projiziert wird. In Direct3D ist das Rechteck als Koordinaten innerhalb einer Direct3D-Oberfläche vorhanden, die vom System als Renderingziel verwendet wird. Die Projektions Transformation konvertiert Vertices in das Koordinatensystem, das für den Viewport verwendet wird. Ein Viewport wird auch verwendet, um den Bereich der tiefen Werte auf einer Renderziel-Oberfläche anzugeben, in die eine Szene gerendert wird (in der Regel 0,0 bis 1,0).

## <a name="the-viewing-frustum"></a>Die Anzeige "Frustum"

Ein Anzeige Wert ist ein 3D-Volume in einer Szene, die relativ zur Kamera des Viewports positioniert ist. Die Form des Volumes wirkt sich darauf aus, wie Modelle von Kamerabereich auf den Bildschirm projiziert werden. Der häufigste Projektions Typ, eine perspektivische Projektion, ist dafür verantwortlich, dass Objekte in der Nähe der Kamera größer als Objekte in der Entfernung angezeigt werden. Zur Anzeige von Perspektiven kann der Anzeige Wert als Pyramide visualisiert werden, wobei die Kamera an der Spitze positioniert ist, wie in der folgenden Abbildung dargestellt. Diese Pyramide wird von einer Vorder-und rückwärts Clippingebene geschnitten. Das Volume innerhalb der Pyramide zwischen der Vorder-und der rückwärts clippingplane ist die Anzeige von Frustum. Objekte sind nur sichtbar, wenn Sie sich in diesem Volume befinden.

![Abbildung eines Anzeigen von Frustrum mit einem Front-und Back-clippingplan](images/frustum.png)

Wenn Sie sich vorstellen, dass Sie sich in einem dunklen Raum befinden und ein quadratisches Fenster sehen, visualisieren Sie die Anzeige von "Frustum". In dieser Analogie ist die Near Clipping-Ebene das Fenster, und die backclippingebene unterbricht Ihre Ansicht, d. h. den Wolkenkratzer auf der Straße, die Berge in der Entfernung oder überhaupt nichts. Sie können alles innerhalb der abgeschnittene Pyramide sehen, das im Fenster beginnt und mit der gesamten Unterbrechungen der Ansicht endet, und Sie können nichts anderes sehen.

Die Anzeige von "Frustum" wird durch FOV (Sicht Feld) und durch die Abstände der Vorder-und rückwärts Clippingebenen definiert, die in z-Koordinaten angegeben sind, wie im folgenden Diagramm dargestellt.

![Diagramm der Anzeige Frust](images/fovdiag.png)

In diesem Diagramm ist die Variable D der Abstand zwischen der Kamera und dem Ursprung des leer Zeichens, das im letzten Teil der Geometrie Pipeline definiert wurde (die Anzeige Transformation). Dies ist der Bereich, um den Sie die Grenzwerte für die Anzeige Frustration anordnen. Informationen dazu, wie diese D-Variable verwendet wird, um die Projektions Matrix zu erstellen, finden Sie in der [Projektions Transformation (Direct3D 9)](projection-transform.md) .

## <a name="viewport-rectangle"></a>Viewportrechteck

Sie definieren das viewportrechteck in C++ mithilfe der [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur. Die D3DVIEWPORT9-Struktur wird mit folgenden Viewport-Bearbeitungsmethoden verwendet, die von der IDirect3DDevice9-Schnittstelle verfügbar gemacht werden.

-   [**IDirect3DDevice9:: getviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
-   [**IDirect3DDevice9:: setviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)

Die D3DVIEWPORT9-Struktur enthält vier Member (X, Y, Width, Height), die den Bereich der Renderziel-Oberfläche definieren, in die eine Szene gerendert wird. Diese Werte entsprechen dem Ziel Rechteck oder dem viewportrechteck, wie im folgenden Diagramm dargestellt.

![Diagramm des Viewportrechtecks](images/destrect.png)

Die Werte, die Sie für die X-, Y-, Width-und Height-Elemente angeben, sind Bildschirm Koordinaten in Relation zur oberen linken Ecke der renderzieloberfläche. Die-Struktur definiert zwei zusätzliche Member (Minz und MaxZ), die die tiefen Bereiche angeben, in denen die Szene gerendert wird.

Direct3D geht davon aus, dass die Größe des Viewport-clippingvolumes zwischen-1,0 und 1,0 in X und zwischen 1,0 und-1,0 in Y liegt. Dabei handelt es sich um die Einstellungen, die häufig von Anwendungen in der Vergangenheit verwendet wurden. Sie können das Viewport-Seitenverhältnis vor dem Abschneiden mithilfe der [Projektions Transformation](projection-transform.md)anpassen.

> [!Note]  
> Minz und MaxZ geben die tiefen Bereiche an, in denen die Szene gerendert wird und nicht für das Abschneiden verwendet werden. In den meisten Anwendungen werden diese Member auf 0,0 und 1,0 festgelegt, damit das System in den gesamten Bereich von tiefen Werten im tiefen Puffer rendern kann. In einigen Fällen können Sie besondere Effekte erzielen, indem Sie andere tiefen Bereiche verwenden. Um beispielsweise eine Heads-Up-Anzeige in einem Spiel zu erzeugen, können Sie beide Werte auf 0,0 festlegen, um zu erzwingen, dass das Systemobjekte in einer Szene im Vordergrund ausstellt, oder Sie können beide Werte auf 1,0 festlegen, um ein Objekt zu erzeugen, das immer im Hintergrund sein sollte.

 

Die Dimensionen, die in den X-, Y-, Width-und Height-Elementen der [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur für einen Viewport verwendet werden, definieren die Position und die Dimensionen des Viewports auf der Renderziel-Oberfläche. Diese Werte befinden sich in Bildschirm Koordinaten relativ zur oberen linken Ecke der-Oberfläche.

Direct3D verwendet die Position und die Dimensionen des Viewports, um die Scheitel Punkte so zu skalieren, dass Sie an die entsprechende Position auf der Ziel Oberfläche angepasst werden. Intern fügt Direct3D diese Werte in die folgende Matrix ein, die auf jeden Scheitelpunkt angewendet wird.

![Gleichung der Matrix, die auf jeden Scheitelpunkt angewendet wird.](images/vpscale.png)

Diese Matrix skaliert Vertices gemäß den viewportdimensionen und dem gewünschten tiefenbereich und übersetzt Sie in die entsprechende Position auf der renderzieloberfläche. Außerdem wird die y-Koordinate durch die Matrix so gekippt, dass Sie einen Bildschirm Ursprung in der oberen linken Ecke anzeigt, wobei sich y nach unten vergrößert. Nachdem diese Matrix angewendet wurde, sind Scheitel Punkte immer noch homogen, d. h., Sie sind weiterhin als \[ x-, y-, z-und w-Scheitel Punkte vorhanden \] und müssen in nicht homogene Koordinaten konvertiert werden, bevor Sie an den Rasterizer gesendet werden.

> [!Note]  
> Die Viewport-Skalierungs Matrix schließt die Minz-und MaxZ-Member der [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur ein, um Vertices für den tiefenbereich \[ Minz, MaxZ zu skalieren \] . Dies stellt eine andere Semantik aus früheren Versionen von DirectX dar, in denen diese Member zum Abschneiden verwendet wurden.

 

> [!Note]  
> Anwendungen legen in der Regel Minz und MaxZ auf 0,0 bzw. 1,0 fest, damit das System in den gesamten tiefenbereich rendert. Sie können jedoch auch andere Werte verwenden, um bestimmte Auswirkungen zu erzielen. Beispielsweise können Sie beide Werte auf 0,0 festlegen, um alle Objekte im Vordergrund zu erzwingen, oder beide Werte auf 1,0 festlegen, um alle Objekte in den Hintergrund zu versetzen.

 

## <a name="clearing-a-viewport"></a>Löschen eines Viewports

Durch das Löschen des Viewports wird der Inhalt des Viewportrechtecks auf der renderzieloberfläche zurückgesetzt. Außerdem kann das Rechteck in den tiefen-und Schablonen Puffer Oberflächen gelöscht werden.

Verwenden Sie [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) , um den Viewport zu löschen. Die-Methode akzeptiert ein oder mehrere Rechtecke, die die Bereiche auf der Oberfläche definieren, die gelöscht werden. Wenn Sie den count-Parameter auf 1 festlegen und der Parameter prects auf die Adresse eines einzelnen Rechtecks, das den gesamten Viewportbereich abdeckt, wird der gesamte Viewport gelöscht. Eine weitere Möglichkeit zum Löschen des gesamten Viewports besteht darin, den Parameter "prects" auf **null** und den count-Parameter auf "0" festzulegen.

[**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) kann zum Löschen von Schablonen Bits innerhalb eines tiefen Puffers verwendet werden. Legen Sie einfach den flags-Parameter fest, um zu bestimmen, wie **IDirect3DDevice9:: Clear** mit dem Renderziel und den zugehörigen tiefen-oder Schablonen Puffern funktioniert. Mit dem D3DCLEAR \_ target-Flag wird der Viewport mit einer beliebigen RGBA-Farbe gelöscht, die Sie im Farb Argument angeben (Dies ist nicht die Material Farbe). Das \_ Flag D3DCLEAR ZBuffer löscht den tiefen Puffer in eine beliebige Tiefe, die Sie in Z: 0,0 angeben, ist die nächstgelegene Entfernung, und 1,0 ist die am weitesten entfernte. Mit dem \_ Flag D3DCLEAR Schablone werden die Schablonen Bits auf den Wert zurückgesetzt, den Sie im Schablone-Argument angeben. Sie können ganze Zahlen verwenden, die zwischen 0 und 2n-1 liegen, wobei n die Bittiefe der Schablone-Puffer ist.

In einigen Situationen kann es vorkommen, dass Sie nur in kleine Teile der Renderziel-und tiefen Puffer Oberflächen gerendert werden. Mit den Clear-Methoden können Sie auch mehrere Bereiche Ihrer Oberflächen in einem einzigen-Befehl löschen. Legen Sie hierzu den count-Parameter auf die Anzahl der zu löschenden Rechtecke fest, und geben Sie die Adresse des ersten Rechtecks in einem Array von Rechtecke im prects-Parameter an.

## <a name="set-up-the-viewport-for-clipping"></a>Einrichten des Viewports für das Clipping

Die Ergebnisse der Projektions Matrix bestimmen das clippingvolume im Projektions Bereich wie folgt:

-w<sub>c</sub><= x<sub>c</sub><= w<sub>c</sub>

-w<sub>c</sub><= y<sub>c</sub><= w<sub>c</sub>

0 <= z<sub>c</sub><= w<sub>c</sub>

Dabei stellen: x, y, z und w die Scheitelpunkt Koordinaten nach dem Anwenden der Projektions Transformation dar. Alle Scheitel Punkte, die eine x-, y-oder z-Komponente außerhalb dieser Bereiche aufweisen, werden abgeschnitten, wenn Clipping aktiviert ist (das Standardverhalten).

Mit Ausnahme von Scheitelpunkt Puffern aktivieren oder deaktivieren Anwendungen Clipping über den renderzustand [**D3DRS \_ Clipping**](./d3drenderstatetype.md) . Clipping-Informationen für Vertex-Puffer werden während der Verarbeitung generiert. Weitere Informationen finden Sie unter [Fixed Function Scheitelpunkt Processing (Direct3D 9)](fixed-function-vertex-processing.md) und [programmierbare Vertex-Verarbeitung (Direct3D 9)](programmable-vertex-processing.md).

Direct3D entfernt keine transformierten Scheitel Punkte eines primitiven von einem Scheitelpunkt Puffer, es sei denn, er stammt aus [**IDirect3DDevice9::P rocess Vertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices). Wenn Sie Ihre eigenen Transformationen durchführen und Direct3D für das Abschneiden benötigen, sollten Sie Scheitelpunkt Puffer nicht verwenden. In diesem Fall durchläuft die Anwendung die Daten, um Sie zu transformieren. Direct3D durchläuft die Daten ein zweites Mal, um Sie abzuschneiden, und dann rendert der Treiber die Daten, was ineffizient ist. Wenn die Anwendung die Daten transformiert, sollte daher auch die Daten Ausschneiden.

Wenn das Gerät vortransformierte und beleuchtete Scheitel Punkte (T&L-Scheitel Punkte) empfängt, die abgeschnitten werden müssen, um den Clipping-Vorgang auszuführen, werden die Scheitel Punkte mithilfe des Scheitel Punkts für die gegenseitige homogene w (RHW) des Scheitel Punkts und der viewportinformationen wieder in den Clippingbereich transformiert. Das Clipping wird dann ausgeführt. Nicht alle Geräte können diese Back-Transform-Funktion ausführen, um T&L-Scheitel Punkten auszuschneiden.

Mit der D3DPMISCCAPS \_ cliptlverts-Geräte Funktion wird angegeben, ob das Gerät&L-Scheitel Punkte Ausschneiden kann. Wenn diese Funktion nicht festgelegt ist, ist die Anwendung für das Abschneiden der T&L-Scheitel Punkte zuständig, die an das zu rendernde Gerät gesendet werden sollen. Das Gerät ist immer in der Lage, T&L-Scheitel Punkten im Software Scheitelpunkt Verarbeitungsmodus zu schneiden (unabhängig davon, ob das Gerät im Verarbeitungsmodus der Software Vertex erstellt oder in den Verarbeitungsmodus für Software Scheitel Punkte gewechselt wird).

Die einzige Voraussetzung für die Konfiguration der Viewport-Parameter für ein renderinggerät besteht darin, das clippingvolume des Viewports festzulegen. Zu diesem Zweck initialisieren und legen Sie clippingwerte für das clippingvolume und die renderzieloberfläche fest. Viewports werden üblicherweise zum renderingin den gesamten Bereich der renderzieloberfläche festgelegt, dies ist jedoch nicht zwingend erforderlich.

Sie können die folgenden Einstellungen für die Member der [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur verwenden, um dies in C++ zu erreichen.


```
D3DVIEWPORT9 viewData = { 0, 0, width, height, 0.0f, 1.0f };
```



Nachdem Sie Werte in der [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur festgelegt haben, wenden Sie die Viewport-Parameter auf das Gerät an, indem Sie Ihre [**IDirect3DDevice9:: setviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) -Methode aufrufen Das folgende Codebeispiel zeigt, wie dieser-Befehl aussehen könnte.


```
HRESULT hr;

hr = pd3dDevice->SetViewport(&viewData);
if(FAILED(hr))
    return hr;
```



Wenn der Aufruf erfolgreich ist, werden die Viewport-Parameter festgelegt und wirksam, wenn eine Renderingmethode das nächste Mal aufgerufen wird. Um Änderungen an den Viewport-Parametern vorzunehmen, aktualisieren Sie einfach die Werte in der [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur, und geben Sie [**IDirect3DDevice9:: setviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) erneut ein.

> [!Note]  
> Die [**D3DVIEWPORT9**](d3dviewport9.md) -Strukturmember Minz und MaxZ geben die tiefen Bereiche an, in denen die Szene gerendert wird und die nicht für das Abschneiden verwendet werden. Die meisten Anwendungen legen diese Member auf 0,0 und 1,0 fest, damit das System den gesamten Bereich von tiefen Werten im tiefen Puffer rendern kann. In einigen Fällen können Sie besondere Effekte erzielen, indem Sie andere tiefen Bereiche verwenden. Um beispielsweise eine Heads-Up-Anzeige in einem Spiel zu erzeugen, können Sie beide Werte auf 0,0 festlegen, um zu erzwingen, dass das Systemobjekte in einer Szene im Vordergrund ausstellt, oder Sie können beide Werte auf 1,0 festlegen, um ein Objekt zu erzeugen, das immer im Hintergrund sein sollte.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> </dl>

 

 
