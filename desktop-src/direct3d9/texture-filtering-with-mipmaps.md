---
description: Eine MipMap ist eine Sequenz von Texturen, von denen jede eine progressiv niedrigere Auflösungs Darstellung desselben Bilds ist.
ms.assetid: b64abca9-0efb-4939-849d-e75a8d0dc10b
title: Textur Filterung mit Mipmaps (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc109ae6de93a26b5d5e5b90e948761e92ee92c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104570367"
---
# <a name="texture-filtering-with-mipmaps-direct3d-9"></a>Textur Filterung mit Mipmaps (Direct3D 9)

Eine MipMap ist eine Sequenz von Texturen, von denen jede eine progressiv niedrigere Auflösungs Darstellung desselben Bilds ist. Die Höhe und Breite jedes Bilds (oder einer Ebene) in MipMap ist eine Potenz von zwei kleiner als die vorherige Ebene. Mipmaps müssen nicht quadratisch sein.

Für Objekte, die sich in der Nähe des Benutzers befinden, wird ein MipMap-Bild mit hoher Auflösung verwendet. Images mit niedrigerer Auflösung werden verwendet, wenn das Objekt weiter entfernt wird. MIPmapping verbessert die Qualität der gerenderten Texturen auf Kosten der Verwendung von mehr Arbeitsspeicher.

Direct3D stellt Mipmaps als Kette angefügter Oberflächen dar. Die Auflösung mit der höchsten Auflösung befindet sich an der Spitze der Kette und verfügt über die nächste Ebene der MipMap als Anlage. Diese Ebene verfügt wiederum über eine Anlage, die die nächste Ebene in der MipMap ist, usw., bis zur niedrigsten Auflösungsebene der MipMap.

Die folgenden Abbildungen zeigen ein Beispiel für diese Ebenen. Die Bitmap-Texturen stellen ein Zeichen für einen Container in einem 3D-Spiel für erste Personen dar. Beim Erstellen als MipMap ist die höchste Auflösungs Textur zuerst in der Menge. Jede nachfolgende Textur im MipMap-Satz ist kleiner in Höhe und Breite mit einer Potenz von 2. In diesem Fall beträgt die MipMap mit der maximalen Auflösung 256 Pixel um 256 Pixel. Die nächste Textur ist 128 x 128. Die letzte Textur in der Kette ist 64x64.

Dieses Vorzeichen hat eine maximale Entfernung, von der es sichtbar ist. Wenn der Benutzer weit vom Vorzeichen entfernt wird, zeigt das Spiel die kleinste Textur in der MipMap-Kette an, in diesem Fall die 64 x 64-Textur.

![Abbildung einer 64 x 64-Textur eines Gefährdungs Zeichens](images/mip1.jpg)

Wenn der Benutzer die Sicht näher zum Vorzeichen verschiebt, werden in der MipMap-Kette progressiv Hochauflösende Texturen verwendet. Die Auflösung in der folgenden Abbildung ist 128 x 128.

![Abbildung einer 128 x 128-Textur eines Gefährdungs Zeichens](images/mip2.jpg)

Die Textur mit der höchsten Auflösung wird verwendet, wenn der Sicht des Benutzers den minimal zulässigen Abstand zum Vorzeichen hat, wie in der folgenden Abbildung dargestellt.

![Abbildung einer 256x256-Textur eines Gefährdungs Zeichens](images/mip3.jpg)

Dies ist eine effizientere Methode, um die Perspektive für Texturen zu simulieren. Anstatt eine einzelne Textur mit vielen Auflösungen zu erzeugen, ist es schneller, mehrere Texturen in unterschiedlichen Auflösungen zu verwenden.

Direct3D kann beurteilen, welche Textur in einem MipMap-Satz der nächsten Auflösung der gewünschten Ausgabe entspricht, und er kann Pixel in seinen texspace zuordnen. Wenn die Auflösung des endgültigen Bilds zwischen den Auflösungen der Texturen im MipMap-Satz liegt, kann Direct3D texeln in beiden Mipmaps untersuchen und deren Farbwerte miteinander vermischen.

Um Mipmaps verwenden zu können, muss die Anwendung einen Satz von Mipmaps erstellen. Anwendungen wenden Mipmaps an, indem Sie den Mipmap-Satz als erste Textur im Satz der aktuellen Texturen auswählen. Weitere Informationen finden Sie unter [Textur blending (Direct3D 9)](texture-blending.md).

Als nächstes muss Ihre Anwendung die von Direct3D verwendete Filtermethode für Sample Texels festlegen. Die schnellste Methode zum Filtern von MipMap besteht darin, dass Direct3D das nächste texterezeichen ausgewählt hat. Verwenden Sie den D3DTEXF \_ Point-Enumerationswert, um diesen auszuwählen. Direct3D kann bessere Filter Ergebnisse erzielen, wenn die Anwendung den D3DTEXF- \_ linearen Enumerationswert verwendet. Dadurch wird die nächstgelegene MipMap ausgewählt und dann ein gewichteter Durchschnitt der textecke berechnet, der die Position in der Textur umgibt, der das aktuelle Pixel zugeordnet ist.

MipMap-Texturen werden in 3D-Szenen verwendet, um die Zeit zu verkürzen, die zum Rendering einer Szene benötigt wird. Außerdem verbessern Sie die Realismus der Szene. Allerdings benötigen Sie häufig große Mengen an Arbeitsspeicher.

## <a name="creating-a-set-of-mipmaps"></a>Erstellen eines Satzes von Mipmaps

Das folgende Beispiel zeigt, wie Ihre Anwendung die [**IDirect3DDevice9::**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) up-Textur-Methode aufrufen kann, um eine Kette von fünf MipMap-Ebenen zu erstellen: 256 x 256, 128 x 128, 64x64, 32x32 und 16x16.


```
// This code example assumes that m_d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface

IDirect3DTexture9 * pMipMap;
m_pD3DDevice->CreateTexture(256, 256, 5, 0, D3DFMT_R8G8B8, 
    D3DPOOL_MANAGED, &pMipMap);
```



Die ersten beiden Parameter, die von [**IDirect3DDevice9:: kreatetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) akzeptiert werden, sind die Größe und Breite der Textur der obersten Ebene. Der dritte Parameter gibt die Anzahl der Ebenen in der Textur an. Wenn Sie diese Einstellung auf 0 (null) festlegen, erstellt Direct3D eine Kette von Oberflächen, von denen jede eine Potenz von zwei kleiner als die vorherige ist, bis zur kleinsten möglichen Größe von 1x1. Der vierte Parameter gibt die Verwendung für diese Ressource an. in diesem Fall wird 0 angegeben, um eine bestimmte Verwendung für die Ressource anzugeben. Der fünfte Parameter gibt das Oberflächen Format für die Textur an. Verwenden Sie für diesen Parameter einen Wert aus dem [D3DFORMAT](d3dformat.md) -Enumerationstyp. Der sechste Parameter gibt einen Member des [**D3DPOOL**](./d3dpool.md) -enumerierten Typs an, der die Speicher Klasse angibt, in die die erstellte Ressource platziert werden soll. Wenn Sie keine dynamischen Texturen verwenden, \_ wird D3DPOOL Managed empfohlen. Der letzte Parameter übernimmt die Adresse eines Zeigers auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle.

> [!Note]  
> Jede Oberfläche in einer MipMap-Kette hat Dimensionen, die eine halbe der vorherigen Oberfläche in der Kette sind. Wenn die MipMap der obersten Ebene über Dimensionen von 256x128 verfügt, sind die Dimensionen der MipMap der zweiten Ebene 128 x 64, die dritte Ebene 64 x 32 usw. bis zu 1 x1. Es ist nicht möglich, eine Reihe von MipMap-Ebenen in Ebenen anzufordern, die bewirken, dass die Breite oder Höhe einer beliebigen MipMap in der Kette kleiner als 1 ist. Im einfachen Fall einer MipMap-Oberfläche der obersten Ebene von 4x2 beträgt der maximal zulässige Wert drei. Die Dimensionen der obersten Ebene sind 4 x 2, die Dimensionen der zweiten Ebene sind 2 x 1, und die Dimensionen für die dritte Ebene sind 1x1. Ein Wert, der größer als 3 in Ebenen ist, führt zu einem Bruch Wert in der Höhe der MipMap der zweiten Ebene und ist daher nicht zulässig.

 

## <a name="selecting-and-displaying-a-mipmap"></a>Auswählen und Anzeigen einer MipMap

Aufrufen der [**IDirect3DDevice9:: SetTexture**](/windows/desktop/api) -Methode, um den Mipmap-Textur Satz als erste Textur in der Liste der aktuellen Texturen festzulegen. Weitere Informationen finden Sie unter [Textur blending (Direct3D 9)](texture-blending.md).

Nachdem die Anwendung den Mipmap-Textur Satz ausgewählt hat, muss Sie dem D3DSAMP [](./d3dtexturefiltertype.md) MipFilter-samplerstatus Werte vom D3DTEXTUREFILTERTYPE-Enumerationstyp zuweisen \_ . Direct3D führt dann automatisch eine MipMap-Textur Filterung aus. Das Aktivieren der MipMap-Textur Filterung wird im folgenden Codebeispiel veranschaulicht.


```
m_pD3DDevice->SetTexture(0, pMipMap);
m_pD3DDevice->SetSamplerState(0, D3DSAMP_MIPFILTER, D3DTEXF_POINT);
```



Die Anwendung kann eine Kette von MipMap-Oberflächen auch manuell durchlaufen, indem Sie die [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) -Methode verwendet und die abzurufende MipMap-Ebene angibt. Im folgenden Beispiel wird eine MipMap-Kette von der höchsten zur niedrigsten Auflösung durchlaufen.


```
IDirect3DSurface9 * pSurfaceLevel;
for (int iLevel = 0; iLevel < pMipMap->GetLevelCount(); iLevel++)
{
    pMipMap->GetSurfaceLevel(iLevel, &pSurfaceLevel);
    // Process this level
    pSurfaceLevel->Release();
}
```



Anwendungen müssen manuell eine MipMap-Kette durchlaufen, um Bitmapdaten in jede Oberfläche in der Kette zu laden. Dies ist in der Regel der einzige Grund für die Durchquerung der Kette. Eine Anwendung kann die Anzahl der Ebenen in einer MipMap abrufen, indem [**IDirect3DBaseTexture9:: getlevelcount**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getlevelcount)aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Filterung](texture-filtering.md)
</dt> </dl>

 

 
