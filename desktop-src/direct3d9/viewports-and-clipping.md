---
description: Konzeptionell ist ein Viewport ein zweidimensionales Rechteck (2D), in das eine 3D-Szene projiziert wird.
ms.assetid: eddadaa1-9181-47fa-8530-44aa46fea286
title: Viewports und Clipping (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6ed7cd5e5a8a3116c07c5b88f3e665e7ba7de7c6dd1d3cd7bf55f936e60386
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068850"
---
# <a name="viewports-and-clipping-direct3d-9"></a>Viewports und Clipping (Direct3D 9)

Konzeptionell ist ein Viewport ein zweidimensionales Rechteck (2D), in das eine 3D-Szene projiziert wird. In Direct3D ist das Rechteck als Koordinaten innerhalb einer Direct3D-Oberfläche vorhanden, die das System als Renderingziel verwendet. Die Projektionstransformation konvertiert Scheitelungen in das Koordinatensystem, das für den Viewport verwendet wird. Ein Viewport wird auch verwendet, um den Bereich der Tiefenwerte auf einer Renderzieloberfläche anzugeben, in dem eine Szene gerendert wird (in der Regel 0,0 bis 1,0).

## <a name="the-viewing-frustum"></a>Das Anzeigen von Frustum

Ein Frustum für die Anzeige ist ein 3D-Volume in einer Szene, die relativ zur Kamera des Viewports positioniert ist. Die Form des Volumes wirkt sich darauf aus, wie Modelle vom Kameraraum auf den Bildschirm projiziert werden. Der gängigste Projektionstyp, eine Perspektivprojektion, ist dafür verantwortlich, dass Objekte in der Nähe der Kamera größer als Objekte in der Entfernung erscheinen. Für die Perspektivenanzeige kann das Frustum der Anzeige als Pyramide visualisiert werden, und die Kamera wird an der Spitze positioniert, wie in der folgenden Abbildung dargestellt. Diese Pyramide wird von einer Front- und Back-Clippingebene überschneidet. Das Volumen innerhalb der Pyramide zwischen der vorderen und der zurücken Beschneidungsebene ist das Frustum der Anzeige. Objekte sind nur sichtbar, wenn sie sich auf diesem Volume befinden.

![Abbildung eines Frustrums mit einem Front- und Back-Clippingplan](images/frustum.png)

Wenn Sie sich vorstellen, dass Sie in einem dunklen Raum stehen und ein quadratisches Fenster durchsichten, visualisieren Sie ein Frustum. In dieser Analogie ist die nah beschneidende Ebene das Fenster, und die Zurück-Clippingebene unterbricht schließlich Ihre Ansicht – die Abstände über die Straße, die Klammer in der Entfernung oder überhaupt nichts. Sie sehen alles innerhalb der abgeschnittenen Pyramid, die am Fenster beginnt und mit dem endet, was Ihre Ansicht unterbricht, und Sie können nichts anderes sehen.

Das Frustum für die Anzeige wird durch fov (Sichtfeld) und durch die Entfernungen der Clippingebenen "front" und "back" definiert, die in Z-Koordinaten angegeben sind, wie im folgenden Diagramm dargestellt.

![Diagramm des Frustums beim Anzeigen](images/fovdiag.png)

In diesem Diagramm ist die Variable D der Abstand zwischen der Kamera und dem Ursprung des Raumes, der im letzten Teil der Geometriepipeline definiert wurde – der Ansichtstransformation. Dies ist der Bereich, um den Sie die Grenzen Ihres Fruststums für die Anzeige anordnen. Informationen dazu, wie diese D-Variable zum Erstellen der Projektionsmatrix verwendet wird, finden Sie unter [Projektionstransformation (Direct3D 9).](projection-transform.md)

## <a name="viewport-rectangle"></a>Viewport-Rechteck

Sie definieren das Viewportrechteck in C++ mithilfe der [**D3DVIEWPORT9-Struktur.**](d3dviewport9.md) Die D3DVIEWPORT9-Struktur wird mit den folgenden Viewport-Manipulationsmethoden verwendet, die von der IDirect3DDevice9-Schnittstelle verfügbar gemacht werden.

-   [**IDirect3DDevice9::GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
-   [**IDirect3DDevice9::SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)

Die D3DVIEWPORT9-Struktur enthält vier Elemente ( X, Y, Width, Height), die den Bereich der Renderzieloberfläche definieren, in dem eine Szene gerendert wird. Diese Werte entsprechen dem Zielrechteck oder Viewportrechteck, wie im folgenden Diagramm dargestellt.

![Diagramm des Viewportrechtecks](images/destrect.png)

Die Werte, die Sie für die Elemente X, Y, Width und Height angeben, sind Bildschirmkoordinaten relativ zur oberen linken Ecke der Renderzieloberfläche. Die -Struktur definiert zwei zusätzliche Member (MinZ und MaxZ), die die Tiefenbereiche angeben, in denen die Szene gerendert wird.

Direct3D geht davon aus, dass das Viewport-Clipping-Volume von -1,0 bis 1,0 in X und von 1,0 bis -1,0 in Y reicht. Dies waren die Einstellungen, die in der Vergangenheit am häufigsten von Anwendungen verwendet wurden. Sie können das Viewport-Seitenverhältnis vor dem Clipping mithilfe der [Projektionstransformation anpassen.](projection-transform.md)

> [!Note]  
> MinZ und MaxZ geben die Tiefenbereiche an, in denen die Szene gerendert und nicht zum Ausschneiden verwendet wird. Die meisten Anwendungen legen diese Member auf 0,0 und 1,0 fest, damit das System den gesamten Bereich der Tiefenwerte im Tiefenpuffer rendern kann. In einigen Fällen können Sie Sondereffekte erzielen, indem Sie andere Tiefenbereiche verwenden. Wenn Sie z. B. eine Kopf-auf-Anzeige in einem Spiel rendern möchten, können Sie beide Werte auf 0,0 festlegen, um das System zu zwingen, Objekte in einer Szene im Vordergrund zu rendern, oder Sie können beide auf 1,0 festlegen, um ein Objekt zu rendern, das sich immer im Hintergrund befindet.

 

Die Dimensionen, die in den X-, Y-, Width- und Height-Membern der [**D3DVIEWPORT9-Struktur**](d3dviewport9.md) für einen Viewport verwendet werden, definieren die Position und die Abmessungen des Viewports auf der Renderzieloberfläche. Diese Werte befinden sich in Bildschirmkoordinaten relativ zur oberen linken Ecke der Oberfläche.

Direct3D verwendet die Viewportposition und -dimensionen, um die Scheitelungen so zu skalieren, dass sie eine gerenderte Szene an die entsprechende Position auf der Zieloberfläche passen. Intern fügt Direct3D diese Werte in die folgende Matrix ein, die auf jeden Scheitelpunkt angewendet wird.

![Gleichung der Matrix, die auf jeden Scheitelpunkt angewendet wird](images/vpscale.png)

Diese Matrix skaliert Vertices entsprechend den Viewportdimensionen und dem gewünschten Tiefenbereich und übersetzt sie an die entsprechende Position auf der Renderzieloberfläche. Die Matrix kippt auch die y-Koordinate, um einen Bildschirmabstieg in der oberen linken Ecke mit y nach unten zu reflektieren. Nachdem diese Matrix angewendet wurde, sind Scheitelungen immer noch homogen, d.&nd; sie sind immer noch als \[ x,y,z,w Vertices vorhanden und müssen in nicht homogene Koordinaten konvertiert werden, bevor sie an den Rasterizer gesendet \] werden.

> [!Note]  
> Die Viewportskalierungsmatrix umfasst die MinZ- und MaxZ-Member der [**D3DVIEWPORT9-Struktur,**](d3dviewport9.md) um Scheitelungen so zu skalieren, dass sie an den Tiefenbereich \[ MinZ, MaxZ \] passen. Dies stellt eine andere Semantik als frühere Versionen von DirectX dar, in denen diese Member für die Beschneidung verwendet wurden.

 

> [!Note]  
> Anwendungen legen in der Regel MinZ und MaxZ auf 0,0 bzw. 1,0 fest, damit das System im gesamten Tiefenbereich gerendert wird. Sie können jedoch andere Werte verwenden, um bestimmte Auswirkungen zu erzielen. Sie können beispielsweise beide Werte auf 0,0 festlegen, um alle Objekte im Vordergrund zu erzwingen, oder beide auf 1,0 festlegen, um alle Objekte im Hintergrund zu rendern.

 

## <a name="clearing-a-viewport"></a>Löschen eines Viewports

Durch das Löschen des Viewports wird der Inhalt des Viewportrechtecks auf der Renderzieloberfläche zurückgesetzt. Sie kann auch das Rechteck in den Tiefen- und Schablonenpufferoberflächen löschen.

Verwenden [**Sie IDirect3DDevice9::Clear,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) um den Viewport zu löschen. Die -Methode akzeptiert ein oder mehrere Rechtecke, die die Bereiche auf der Zu löschenden Oberfläche definieren. Wenn Sie den Count-Parameter auf 1 und den pRects-Parameter auf die Adresse eines einzelnen Rechtecks festlegen, das den gesamten Viewportbereich abdeckt, wird der gesamte Viewport klar. Eine weitere Möglichkeit, den gesamten Viewport zu löschen, besteht im Festlegen des pRects-Parameters auf **NULL** und des Count-Parameters auf 0.

[**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) kann zum Löschen von Schablonenbits innerhalb eines Tiefenpuffers verwendet werden. Legen Sie einfach den Flags-Parameter fest, um zu bestimmen, wie **IDirect3DDevice9::Clear** mit dem Renderziel und allen zugeordneten Tiefen- oder Schablonenpuffern funktioniert. Das D3DCLEAR TARGET-Flag gibt den Viewport mit einer beliebigen RGBA-Farbe frei, die Sie im Color-Argument angeben (dies ist \_ nicht die Materialfarbe). Das D3DCLEAR ZBUFFER-Flag leert den Tiefenpuffer in einer beliebigen Tiefe, die Sie in Z angeben: 0,0 ist die nächstgelegene Entfernung, und \_ 1,0 ist die längste. Das D3DCLEAR-STENCIL-Flag setzt die Schablonenbits auf den Wert zurück, den Sie \_ im Schablonenargument angeben. Sie können ganze Zahlen im Bereich von 0 bis 2n-1 verwenden, wobei n die Bittiefe des Schablonenpuffers ist.

In einigen Situationen werden Sie möglicherweise nur in kleine Teile der Renderziel- und Tiefenpufferoberflächen gerendert. Mit den clear-Methoden können Sie auch mehrere Bereiche Ihrer Oberflächen in einem einzigen Aufruf löschen. Legen Sie hierzu den Count-Parameter auf die Anzahl von Rechtecke fest, die Sie löschen möchten, und geben Sie die Adresse des ersten Rechtecks in einem Array von Rechtecke im pRects-Parameter an.

## <a name="set-up-the-viewport-for-clipping"></a>Einrichten des Viewports für Clipping

Die Ergebnisse der Projektionsmatrix bestimmen das Clippingvolumen im Projektionsraum wie:

-w<sub>c</sub><= x<sub>c</sub><= w<sub>c</sub>

-w<sub>c</sub><= y<sub>c</sub><= w<sub>c</sub>

0 <= z<sub>c</sub><= w<sub>c</sub>

Dabei stellen x, y, z und w die Scheitelpunktkoordinaten dar, nachdem die Projektionstransformation angewendet wurde. Alle Scheitelzeichen, die eine x-, y- oder z-Komponente außerhalb dieser Bereiche haben, werden abgeschnitten, wenn clipping aktiviert ist (Standardverhalten).

Mit Ausnahme von Scheitelpunktpuffern aktivieren oder deaktivieren Anwendungen das Clipping über den [**D3DRS \_ CLIPPING-Renderzustand.**](./d3drenderstatetype.md) Clippinginformationen für Scheitelpunktpuffer werden während der Verarbeitung generiert. Weitere Informationen finden Sie unter Vertexverarbeitung fester Funktionen [(Direct3D 9)](fixed-function-vertex-processing.md) und [Programmable Vertex Processing (Direct3D 9).](programmable-vertex-processing.md)

Direct3D beschneidet transformierte Scheitelpunkte eines Primitiven nicht aus einem Scheitelpunktpuffer, es sei denn, er stammt von [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices). Wenn Sie Ihre eigenen Transformationen verwenden und Direct3D für die Beschneidung benötigen, sollten Sie keine Scheitelpunktpuffer verwenden. In diesem Fall durchläuft die Anwendung die Daten, um sie zu transformieren. Direct3D durchläuft die Daten ein zweites Mal, um sie zu beschneiden, und dann rendert der Treiber die Daten, was ineffizient ist. Wenn die Anwendung die Daten transformiert, sollte also auch die Daten beschneiden.

Wenn das Gerät vorab transformierte und beleuchtete Scheitelpunkte (T&L Vertices) empfängt, die abgeschnitten werden müssen, werden die Scheitelpunkte mithilfe des reziproken homogenen w (RHW) des Scheitelpunkts und der Viewportinformationen wieder in den Clippingbereich transformiert. Das Clipping wird dann ausgeführt. Nicht alle Geräte können diese Rücktransformation durchführen, um T&L-Scheitelungen zu beschneiden.

Die D3DPMISCCAPS CLIPTLVERTS-Gerätefunktion gibt an, ob das Gerät in der Lage ist, \_ T-&L-Scheitelungen zu beschneiden. Wenn diese Funktion nicht festgelegt ist, ist die Anwendung dafür verantwortlich, die T&L-Scheitelungen zu beschneiden, die sie an das zu renderende Gerät senden möchte. Das Gerät ist immer in der Lage, T&L-Scheitelpunkte im Softwarevertexverarbeitungsmodus zu beschneiden (unabhängig davon, ob das Gerät im Softwarevertexverarbeitungsmodus erstellt oder in den Software-Scheitelpunktverarbeitungsmodus umgeschaltet wird).

Die einzige Anforderung zum Konfigurieren der Viewportparameter für ein Renderinggerät ist das Festlegen des Ausschneidevolumens des Viewports. Hierzu initialisieren und legen Sie Beschneidungswerte für das Ausschneidevolumen und für die Renderzieloberfläche fest. Viewports werden häufig so eingerichtet, dass sie im vollständigen Bereich der Renderzieloberfläche gerendert werden. Dies ist jedoch nicht erforderlich.

Sie können die folgenden Einstellungen für die Member der [**D3DVIEWPORT9-Struktur**](d3dviewport9.md) verwenden, um dies in C++ zu erreichen.


```
D3DVIEWPORT9 viewData = { 0, 0, width, height, 0.0f, 1.0f };
```



Nachdem Sie Werte in der [**D3DVIEWPORT9-Struktur**](d3dviewport9.md) festgelegt haben, wenden Sie die Viewportparameter auf das Gerät an, indem Sie die [**IDirect3DDevice9::SetViewport-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) aufrufen. Das folgende Codebeispiel zeigt, wie dieser Aufruf aussehen könnte.


```
HRESULT hr;

hr = pd3dDevice->SetViewport(&viewData);
if(FAILED(hr))
    return hr;
```



Wenn der Aufruf erfolgreich ist, werden die Viewportparameter festgelegt und treten beim nächsten Aufruf einer Renderingmethode in Kraft. Um Änderungen an den Viewportparametern vorzunehmen, aktualisieren Sie einfach die Werte in der [**D3DVIEWPORT9-Struktur,**](d3dviewport9.md) und rufen [**Sie IDirect3DDevice9::SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) erneut auf.

> [!Note]  
> Die [**D3DVIEWPORT9-Strukturmitglieder**](d3dviewport9.md) MinZ und MaxZ geben die Tiefenbereiche an, in denen die Szene gerendert und nicht zum Ausschneiden verwendet wird. Die meisten Anwendungen legen diese Member auf 0,0 und 1,0 fest, damit das System den gesamten Bereich der Tiefenwerte im Tiefenpuffer rendern kann. In einigen Fällen können Sie spezielle Effekte erzielen, indem Sie andere Tiefenbereiche verwenden. Wenn Sie beispielsweise eine Kopf-auf-Kopf-Anzeige in einem Spiel rendern möchten, können Sie beide Werte auf 0,0 festlegen, um das System zum Rendern von Objekten in einer Szene im Vordergrund zu zwingen, oder Sie können beide werte auf 1.0 festlegen, um ein Objekt zu rendern, das sich immer im Hintergrund befinden sollte.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> </dl>

 

 
