---
description: Kubische Umgebungs Zuordnungen (manchmal auch als Cubemaps bezeichnet) sind Texturen, die Bilddaten enthalten, die die Szene darstellen, die ein Objekt umgibt, als ob sich das Objekt in der Mitte eines Cubes befand.
ms.assetid: 4879d59b-e6d3-4811-ab2c-bcce8f214e1c
title: Kubische Umgebungs Zuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecac83db067224195883485bcbd282aa82ae4b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393210"
---
# <a name="cubic-environment-mapping-direct3d-9"></a>Kubische Umgebungs Zuordnung (Direct3D 9)

Kubische Umgebungs Zuordnungen (manchmal auch als Cubemaps bezeichnet) sind Texturen, die Bilddaten enthalten, die die Szene darstellen, die ein Objekt umgibt, als ob sich das Objekt in der Mitte eines Cubes befand. Jedes Gesicht der kubischen Umgebungs Zuordnung deckt ein 90-Grad-Feld der Sicht in horizontaler und vertikaler Sicht ab, und es gibt sechs Gesichter pro cubemap. Die Ausrichtung der Flächen wird in der folgenden Abbildung dargestellt.

![Abbildung eines Cubes mit zentralen Koordinatenachsen, der in den Cube-Gesichtern senkrecht ist](images/cubemap-cube.png)

Jedes Gesicht des Cubes ist senkrecht zur x/y-, y/z-oder x/z-Ebene im Raum der Welt ausgerichtet. In der folgenden Abbildung wird gezeigt, wie die einzelnen Ebenen einem Gesicht entsprechen.

![Abbildung der Cube-Gesichter mit Koordinaten Projektionen von Ebenen](images/cube-faces.png)

Kubische Umgebungs Zuordnungen werden als eine Reihe von Textur Objekten implementiert. Anwendungen können statische Bilder für die Zuordnung von kubischen Umgebungen verwenden, oder Sie können in die Flächen der cubemap hinein Rendering werden, um eine dynamische Umgebungs Zuordnung auszuführen. Diese Technik erfordert, dass die cubezuordnungs-Oberflächen gültige renderzieloberflächen darstellen, die mit dem \_ festgelegten Flag D3DUSAGE renderTarget erstellt werden.

Die Gesichter einer cubemap müssen keine äußerst detaillierten Renderings der umgebenden Szene enthalten. In den meisten Fällen werden Umgebungs Zuordnungen auf gekrümmte Oberflächen angewendet. Aufgrund der von den meisten Anwendungen verwendeten Krümmung wird die resultierende reflektierenden Verzerrung in der Umgebungs Zuordnung in Bezug auf Arbeitsspeicher und renderingaufwand in Bezug auf den Arbeitsspeicher verschwendet.

## <a name="mipmapped-cubic-environment-maps"></a>Mipzugeordnete kubische Umgebungs Zuordnungen

Cubemaps können mipzugeordnet werden. Legen Sie zum Erstellen einer mipzugeordneten cubemap den Levels-Parameter der Methode " [**kreatecubetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) " auf die gewünschte Anzahl von Ebenen fest. Sie können die Topografie dieser Oberflächen wie in der folgenden Abbildung dargestellt sehen.

![Diagramm einer mipzugeordneten cubemap mit n MIP-Ebenen](images/cubemap-mipped.png)

Anwendungen, die mipzugeordnete kubische Umgebungs Zuordnungen erstellen, können auf jedes Gesicht zugreifen, indem Sie die [**getcubemapsurface**](/windows/desktop/api) -Methode aufrufen. Legen Sie zunächst den entsprechenden Wert aus dem enumerierten Typ [**D3DCUBEMAP \_ Gesichter**](./d3dcubemap-faces.md) fest, wie unter [Erstellen von kubischen Umgebungskarten Oberflächen (Direct3D 9)](creating-cubic-environment-map-surfaces.md)erläutert. Wählen Sie als nächstes die Ebene aus, die abgerufen werden soll, indem Sie den Parameter **getcubemapsurface** Level auf die gewünschte MipMap-Ebene festlegen. Beachten Sie, dass 0 dem Bild der obersten Ebene entspricht.

## <a name="texture-coordinates-for-cubic-environment-maps"></a>Texturkoordinaten für die Karten der kubischen Umgebung

Texturkoordinaten, die eine kubische Umgebungs Zuordnung indizieren, sind keine einfachen u-, v-Stil Koordinaten, die verwendet werden, wenn Standard Texturen angewendet werden. In der Tat werden bei kubischen Umgebungs Zuordnungen überhaupt keine Texturkoordinaten verwendet. Anstelle eines Satzes von Texturkoordinaten benötigen kubische Umgebungs Zuordnungen einen 3D-Vektor. Sie müssen darauf achten, dass Sie ein ordnungsgemäßes Scheitelpunkt Format angeben. Zusätzlich zur Angabe des Systems, wie viele Sätze von Texturkoordinaten von der Anwendung verwendet werden, müssen Sie Informationen über die Anzahl der Elemente in jeder Gruppe bereitstellen. Direct3D bietet zu diesem Zweck den [**D3DFVF \_ texcoordsizen**](d3dfvf-texcoordsizen.md) -Satz von Makros. Diese Makros akzeptieren einen einzelnen Parameter, der den Index des Texturkoordinaten Satzes identifiziert, für den die Größe beschrieben wird. Im Fall eines 3D-Vektors fügen Sie das durch das D3DFVF TEXCOORDSIZE3-Makro erstellte Bitmuster ein \_ . Im folgenden Codebeispiel wird gezeigt, wie dieses Makro verwendet wird.


```
// Create a flexible vertex format descriptor for a vertex that contains
//   a position, normal, and one set of 3D texture coordinates.

DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 | D3DFVF_TEXCOORDSIZE3(0); 
```



In einigen Fällen, z. b. bei der diffuses Licht Zuordnung, verwenden Sie den Vertex-Zeichenbereich für den Vektor. In anderen Fällen, z. b. in der Glanz Umgebungs Zuordnung, verwenden Sie einen Reflektionsvektor. Da transformierte Vertex-Normale weitgehend verstanden werden, konzentrieren sich die Informationen hier auf das Berechnen eines reflektionvevektors.

Wenn Sie einen reflektionvektor selbst berechnen, müssen Sie die Position der einzelnen Scheitel Punkte und einen Vektor vom Standpunkt bis zu diesem Scheitelpunkt verstehen. Direct3D kann die reflektionvektoren für Ihre Geometrie automatisch berechnen. Die Verwendung dieser Funktion spart Speicherplatz, da Sie keine Texturkoordinaten für die Umgebungs Zuordnung einschließen müssen. Außerdem wird die Bandbreite reduziert, und im Fall eines T&L HAL-Geräts kann es deutlich schneller sein als die Berechnungen, die Ihre Anwendung selbst durchführen kann. Um dieses Feature zu verwenden, legen Sie in der Textur Phase, in der die kubische Umgebungs Zuordnung enthalten ist, den \_ Status D3DTSS texcoordindex Textur Phase auf eine Kombination aus dem D3DTSS \_ TCI \_ cameraspacereflectionvector-Member von [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) und dem Index eines Texturkoordinaten Satzes fest. In einigen Situationen, z. b. bei der diffuses Licht Zuordnung, können Sie den D3DTSS \_ TCI \_ cameraspacenormale-Member von **D3DTEXTURESTAGESTATETYPE** verwenden, der bewirkt, dass das System den transformierten Scheitelpunkt (Scheitelpunkt) als Adressierungs Vektor für die Textur verwendet. Der Index wird nur vom System verwendet, um den Wrapping Modus für die Textur zu bestimmen.

Das folgende Codebeispiel zeigt, wie dieser Wert verwendet wird.


```
// The m_d3dDevice variable is a valid pointer
// to an IDirect3DDevice9 interface.

// Automatically generate texture coordinates for stage 2.
// This assumes that stage 2 is assigned a cube map.
// Use the wrap mode from the texture coordinate set at index 1.

m_d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX,
                                   D3DTSS_TCI_CAMERASPACEREFLECTIONVECTOR | 1); 
```



Wenn Sie die automatische Generierung von Texturkoordinaten aktivieren, verwendet das System eines von zwei Formeln, um den reflektionvektor für jeden Scheitelpunkt zu berechnen. Wenn der D3DRS \_ localviewer-Rendering-Zustand auf **true** festgelegt ist, wird die folgende Formel verwendet.

![Formel des reflektionvevektors (r = 2 (EXN) n-e)](images/reflection-vector-local.png)

In der vorangehenden Formel ist R der zu berechnende reflektionvektor, E ist der normalisierte Positions-zu-Auge-Vektor, und N ist der Vertex-Raum des Kamera Raums.

Wenn der D3DRS \_ localviewer-Rendering-Zustand auf **false** festgelegt ist, verwendet das System die folgende Formel.

![Formel des reflektionvevektors (r = 2nzn-i)](images/reflection-vector-nonlocal.png)

Die R-und N-Elemente in dieser Formel sind mit der vorherigen Formel identisch. Das N<sub>Z</sub> -Element ist der Raum z des Scheitel Punkts normal, und ich bin der Vektor (0, 0, 1) eines unendlich entfernten Standpunkts. Das System verwendet den reflektionvektor aus beiden Formeln, um die entsprechende Oberfläche der cubemap auszuwählen und zu adressieren.

> [!Note]  
> In den meisten Fällen sollten Anwendungen die automatische Normalisierung von Scheitelpunkt normalen aktivieren. Legen Sie zu diesem Zweck D3DRS \_ normalizenormals auf **true** fest. Wenn Sie diesen renderzustand nicht aktivieren, unterscheidet sich die Darstellung der Umgebungs Zuordnung erheblich von dem, was Sie möglicherweise erwarten.

 

Weitere Informationen finden Sie im folgenden Thema.

-   [Erstellen von kubischen Umgebungs Zuordnungs Oberflächen (Direct3D 9)](creating-cubic-environment-map-surfaces.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Umgebungs Zuordnung](environment-mapping.md)
</dt> </dl>

 

 
