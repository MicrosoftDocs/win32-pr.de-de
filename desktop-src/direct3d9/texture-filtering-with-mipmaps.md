---
description: Eine Mipmap ist eine Sequenz von Texturen, von denen jede eine progressiv niedrigere Auflösungsdarstellung desselben Bilds darstellt.
ms.assetid: b64abca9-0efb-4939-849d-e75a8d0dc10b
title: Texturfilterung mit Mipmaps (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68f98c1189f130261981fdd309bb3f06bcca1e66f6e23a70e141a5abfe32f4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291638"
---
# <a name="texture-filtering-with-mipmaps-direct3d-9"></a>Texturfilterung mit Mipmaps (Direct3D 9)

Eine Mipmap ist eine Sequenz von Texturen, von denen jede eine progressiv niedrigere Auflösungsdarstellung desselben Bilds darstellt. Die Höhe und Breite jedes Bilds bzw. jeder Ebene in der Mipmap ist eine Leistung von zwei, die kleiner als die vorherige Ebene ist. Mipmaps müssen nicht quadratisch sein.

Ein hochauflösendes Mipmapbild wird für Objekte verwendet, die sich in der Nähe des Benutzers befinden. Bilder mit niedrigerer Auflösung werden verwendet, wenn das Objekt weiter entfernt erscheint. Mipmapping verbessert die Qualität gerenderte Texturen auf Kosten der Nutzung von mehr Arbeitsspeicher.

Direct3D stellt Mipmaps als Kette von angefügten Oberflächen dar. Die Textur mit der höchsten Auflösung befindet sich am Anfang der Kette und verfügt über die nächste Ebene der Mipmap als Anlage. Diese Ebene verfügt wiederum über eine Anlage, die die nächste Ebene in der Mipmap usw. ist, bis zur niedrigsten Auflösungsebene der Mipmap.

Die folgenden Abbildungen zeigen ein Beispiel für diese Ebenen. Die Bitmaptexturen stellen ein Zeichen für einen Container in einem 3D-First-Person-Spiel dar. Wenn sie als Mipmap erstellt wird, wird die Textur mit der höchsten Auflösung zuerst in der Gruppe verwendet. Jede erfolgreiche Textur im mipmap-Satz ist in Höhe und Breite um eine Potenz von 2 kleiner. In diesem Fall beträgt die Mipmap mit maximaler Auflösung 256 x 256 Pixel. Die nächste Textur ist 128 x 128. Die letzte Textur in der Kette ist 64 x 64.

Dieses Vorzeichen weist einen maximalen Abstand auf, von dem es sichtbar ist. Wenn der Benutzer weit vom Vorzeichen entfernt beginnt, zeigt das Spiel die kleinste Textur in der Mipmapkette an, in diesem Fall die 64x64-Textur.

![Abbildung einer 64 x 64-Textur eines Risikozeichens](images/mip1.jpg)

Wenn der Benutzer den Blickpunkt näher an das Vorzeichen verschiebt, werden schrittweise Texturen mit höherer Auflösung in der Mipmapkette verwendet. Die Auflösung in der folgenden Abbildung ist 128 x 128.

![Abbildung einer 128x128-Textur eines Risikozeichens](images/mip2.jpg)

Die Textur mit der höchsten Auflösung wird verwendet, wenn sich der Blickpunkt des Benutzers im minimal zulässigen Abstand zum Vorzeichen befindet, wie in der folgenden Abbildung dargestellt.

![Abbildung einer 256x256-Textur eines Risikozeichens](images/mip3.jpg)

Dies ist eine effizientere Möglichkeit, die Perspektive für Texturen zu simulieren. Anstatt eine einzelne Textur mit vielen Auflösungen zu rendern, ist es schneller, mehrere Texturen mit unterschiedlichen Auflösungen zu verwenden.

Direct3D kann bewerten, welche Textur in einem mipmap-Satz der gewünschten Ausgabe am nächsten ist, und Pixel kann dem Texelbereich zugeordnet werden. Wenn die Auflösung des endgültigen Bilds zwischen den Auflösungen der Texturen im mipmap-Satz liegt, kann Direct3D Texel in beiden Mipmaps untersuchen und deren Farbwerte kombinieren.

Um Mipmaps verwenden zu können, muss Ihre Anwendung einen Satz von Mipmaps erstellen. Anwendungen wenden Mipmaps an, indem sie das Mipmapset als erste Textur im Satz der aktuellen Texturen auswählen. Weitere Informationen finden Sie unter [Texturmischung (Direct3D 9).](texture-blending.md)

Als Nächstes muss Ihre Anwendung die Filtermethode festlegen, die Direct3D zum Beispiel für Texel verwendet. Die schnellste Methode für die Mipmapfilterung besteht darin, Direct3D das nächstgelegene Texel auswählen zu lassen. Verwenden Sie den D3DTEXF \_ POINT-Enumerationswert, um diesen auszuwählen. Direct3D kann bessere Filterergebnisse erzeugen, wenn Ihre Anwendung den \_ aufzählten D3DTEXF LINEAR-Wert verwendet. Dadurch wird die nächstgelegene Mipmap ausgewählt und dann ein gewichteter Durchschnitt der Texel berechnet, die die Position in der Textur umschwenken, der das aktuelle Pixel zugeordnet ist.

Mipmaptexturen werden in 3D-Szenen verwendet, um die zum Rendern einer Szene erforderliche Zeit zu verkürzen. Sie verbessern auch die Realität der Szene. Sie benötigen jedoch häufig große Mengen an Arbeitsspeicher.

## <a name="creating-a-set-of-mipmaps"></a>Erstellen eines Satzes von Mipmaps

Das folgende Beispiel zeigt, wie Ihre Anwendung die [**IDirect3DDevice9::CreateTexture-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) aufrufen kann, um eine Kette von fünf Mipmapebenen zu erstellen: 256x256, 128x128, 64x64, 32x32 und 16x16.


```
// This code example assumes that m_d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface

IDirect3DTexture9 * pMipMap;
m_pD3DDevice->CreateTexture(256, 256, 5, 0, D3DFMT_R8G8B8, 
    D3DPOOL_MANAGED, &pMipMap);
```



Die ersten beiden Parameter, die von [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) akzeptiert werden, sind die Größe und Breite der Textur der obersten Ebene. Der dritte Parameter gibt die Anzahl der Ebenen in der Textur an. Wenn Sie diese Einstellung auf 0 festlegen, erstellt Direct3D eine Kette von Oberflächen, von denen jede eine Leistung von zwei kleiner als die vorherige ist, bis zur kleinsten möglichen Größe von 1x1. Der vierte Parameter gibt die Verwendung für diese Ressource an. in diesem Fall wird 0 angegeben, um anzugeben, dass die Ressource nicht spezifisch verwendet wird. Der fünfte Parameter gibt das Oberflächenformat für die Textur an. Verwenden Sie einen Wert aus dem [D3DFORMAT-Enumerationstyp](d3dformat.md) für diesen Parameter. Der sechste Parameter gibt einen Member des [**D3DPOOL-Enumerationstyps**](./d3dpool.md) an, der die Speicherklasse angibt, in der die erstellte Ressource gespeichert werden soll. Sofern Sie keine dynamischen Texturen verwenden, wird D3DPOOL \_ MANAGED empfohlen. Der letzte Parameter verwendet die Adresse eines Zeigers auf eine [**IDirect3DTexture9-Schnittstelle.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)

> [!Note]  
> Jede Oberfläche in einer Mipmapkette verfügt über Dimensionen, die der Hälfte der vorherigen Oberfläche in der Kette entsprechen. Wenn die Mipmap der obersten Ebene über Dimensionen von 256 x 128 verfügt, sind die Dimensionen der Mipmap der zweiten Ebene 128 x 64, die dritte Ebene 64 x 32 usw. bis zu 1x1. Sie können keine Anzahl von Mipmapebenen in Ebenen anfordern, die dazu führen würden, dass die Breite oder Höhe einer Mipmap in der Kette kleiner als 1 ist. Im einfachen Fall einer Mipmapoberfläche der obersten Ebene von 4x2 beträgt der maximal zulässige Wert für Levels drei. Die Dimensionen der obersten Ebene sind 4x2, die Dimensionen der zweiten Ebene sind 2x1, und die Dimensionen für die dritte Ebene sind 1x1. Ein Wert größer als 3 in Ebenen führt zu einem Bruchwert in der Höhe der Mipmap der zweiten Ebene und ist daher nicht zulässig.

 

## <a name="selecting-and-displaying-a-mipmap"></a>Auswählen und Anzeigen einer Mipmap

Rufen Sie die [**IDirect3DDevice9::SetTexture-Methode**](/windows/desktop/api) auf, um den mipmap-Textursatz als erste Textur in der Liste der aktuellen Texturen festzulegen. Weitere Informationen finden Sie unter [Texturmischung (Direct3D 9).](texture-blending.md)

Nachdem Ihre Anwendung den Mipmaptextursatz ausgewählt hat, muss sie dem D3DSAMP MIPFILTER-Samplerstatus Werte aus dem [**D3DTEXTUREFILTERTYPE-Enumerationstyp**](./d3dtexturefiltertype.md) \_ zuweisen. Direct3D führt dann automatisch eine Mipmap-Texturfilterung durch. Das Aktivieren der Mipmap-Texturfilterung wird im folgenden Codebeispiel veranschaulicht.


```
m_pD3DDevice->SetTexture(0, pMipMap);
m_pD3DDevice->SetSamplerState(0, D3DSAMP_MIPFILTER, D3DTEXF_POINT);
```



Ihre Anwendung kann auch manuell eine Kette von Mipmap-Oberflächen durchlaufen, indem sie die [**IDirect3DTexture9::GetSurfaceLevel-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) verwendet und die abzurufende Mipmapebene angibt. Im folgenden Beispiel wird eine Mipmapkette von der höchsten bis zur niedrigsten Auflösung durchlaufen.


```
IDirect3DSurface9 * pSurfaceLevel;
for (int iLevel = 0; iLevel < pMipMap->GetLevelCount(); iLevel++)
{
    pMipMap->GetSurfaceLevel(iLevel, &pSurfaceLevel);
    // Process this level
    pSurfaceLevel->Release();
}
```



Anwendungen müssen manuell eine Mipmapkette durchlaufen, um Bitmapdaten in jede Oberfläche in der Kette zu laden. Dies ist in der Regel der einzige Grund, die Kette zu durchlaufen. Eine Anwendung kann die Anzahl der Ebenen in einer Mipmap abrufen, indem [**sie IDirect3DBaseTexture9::GetLevelCount aufruft.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getlevelcount)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturfilterung](texture-filtering.md)
</dt> </dl>

 

 
