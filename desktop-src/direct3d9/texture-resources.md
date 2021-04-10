---
description: Textur Ressourcen werden in der IDirect3DTexture9-Schnittstelle implementiert. Um einen Zeiger auf eine Textur Schnittstelle zu erhalten, rufen Sie die IDirect3DDevice9::-Methode oder eine der folgenden D3DX-Funktionen auf.
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Textur Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14134ca53b7735426e3f01340308282858da5516
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213975"
---
# <a name="texture-resources-direct3d-9"></a>Textur Ressourcen (Direct3D 9)

Textur Ressourcen werden in der [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle implementiert. Um einen Zeiger auf eine Textur Schnittstelle zu erhalten, rufen Sie die [**IDirect3DDevice9::**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) -Methode oder eine der folgenden D3DX-Funktionen auf.

-   [**D3DXCreateTexture**](d3dxcreatetexture.md)
-   [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
-   [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
-   [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md)
-   [**D3DXCreateTextureFromFileInMemoryEx**](d3dxcreatetexturefromfileinmemoryex.md)
-   [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md)
-   [**D3DXCreateTextureFromResourceEx**](d3dxcreatetexturefromresourceex.md)

Im folgenden Codebeispiel wird [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) verwendet, um eine Textur aus Tiger.bmp zu laden.


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



Der erste Parameter, den [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) annimmt, ist ein Zeiger auf eine [**IDirect3DDevice9**](/windows/desktop/api) -Schnittstelle. Der zweite Parameter teilt Direct3D den Namen der Datei, aus der die Textur geladen werden soll. Der dritte Parameter übernimmt die Adresse eines Zeigers auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.

## <a name="rendering-with-texture-resources"></a>Rendering mit Textur Ressourcen

Direct3D unterstützt mehrere Textur-Mischungen durch das Konzept von Textur Stufen. Jede Textur Phase enthält eine Textur und Vorgänge, die für die Textur ausgeführt werden können. Die Texturen in den Textur Stufen bilden den Satz der aktuellen Texturen. Weitere Informationen finden Sie unter [Textur blending (Direct3D 9)](texture-blending.md). Der Zustand jeder Textur wird in der Textur Phase gekapselt.

In einer C++-Anwendung muss der Zustand jeder Textur mit der [**IDirect3DDevice9:: settexturestagestate**](/windows/desktop/api) -Methode festgelegt werden. Übergeben Sie die Phasen Nummer (0-7) als Wert des ersten Parameters. Legen Sie den Wert des zweiten Parameters auf einen Member des [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) -Enumerationstyps fest. Der letzte Parameter ist der Zustandswert für den jeweiligen Textur Zustand.

Mithilfe von Textur Schnittstellen Zeigern kann die Anwendung eine Mischung von bis zu acht Texturen darstellen. Legen Sie die aktuellen Texturen fest, indem Sie die [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -Methode aufrufen. Direct3D vermischt alle aktuellen Texturen mit den primitiven, die Sie rendert.

> [!Note]  
> Die [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -Methode erhöht den Verweis Zähler der zugewiesenen Textur Oberfläche. Wenn die Textur nicht mehr benötigt wird, sollten Sie die Textur in der entsprechenden Phase auf **null** festlegen. Wenn Sie dies nicht tun, wird die Oberfläche nicht freigegeben, was zu einem Speicherfehler führt.

 

Die Anwendung kann den texturwrapping Zustand für die aktuellen Texturen durch Aufrufen der [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode festlegen. Übergeben Sie einen Wert von D3DRS \_ WRAP0 bis D3DRS \_ WRAP7 als Wert des ersten Parameters, und verwenden Sie eine Kombination der \_ Flags D3DWRAPCOORD 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD \_ 2 und D3DWRAPCOORD \_ 3, um das Umleiten in den Richtungen u, v oder w zu ermöglichen.

Die Anwendung kann auch die Textur Perspektive und die Textur Filter Zustände festlegen. Weitere Informationen finden Sie unter [Textur Filterung (Direct3D 9)](texture-filtering.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
