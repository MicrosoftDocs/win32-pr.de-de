---
description: Texturressourcen werden in der IDirect3DTexture9-Schnittstelle implementiert. Um einen Zeiger auf eine Texturschnittstelle zu erhalten, rufen Sie die IDirect3DDevice9::CreateTexture-Methode oder eine der folgenden D3DX-Funktionen auf.
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Texturressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230caaa352a50644a6580c8aae28f18882425e40d9378cbafee1980cf317aa46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290688"
---
# <a name="texture-resources-direct3d-9"></a>Texturressourcen (Direct3D 9)

Texturressourcen werden in der [**IDirect3DTexture9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) implementiert. Um einen Zeiger auf eine Texturschnittstelle zu erhalten, rufen Sie die [**IDirect3DDevice9::CreateTexture-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) oder eine der folgenden D3DX-Funktionen auf.

-   [**D3DXCreateTexture**](d3dxcreatetexture.md)
-   [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
-   [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
-   [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md)
-   [**D3DXCreateTextureFromFileInMemoryEx**](d3dxcreatetexturefromfileinmemoryex.md)
-   [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md)
-   [**D3DXCreateTextureFromResourceEx**](d3dxcreatetexturefromresourceex.md)

Im folgenden Codebeispiel wird [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) verwendet, um eine Textur aus einem Tiger.bmp.


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



Der erste Parameter, [**den D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) akzeptiert, ist ein Zeiger auf eine [**IDirect3DDevice9-Schnittstelle.**](/windows/desktop/api) Der zweite Parameter teilt Direct3D den Namen der Datei mit, aus der die Textur geladen werden soll. Der dritte Parameter verwendet die Adresse eines Zeigers auf eine [**IDirect3DTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) die das erstellte Texturobjekt darstellt.

## <a name="rendering-with-texture-resources"></a>Rendering mit Texturressourcen

Direct3D unterstützt mehrere Texturmischungen durch das Konzept von Texturstufen. Jede Texturphase enthält eine Textur und Vorgänge, die für die Textur ausgeführt werden können. Die Texturen in den Texturstufen bilden den Satz der aktuellen Texturen. Weitere Informationen finden Sie unter [Texturmischung (Direct3D 9).](texture-blending.md) Der Zustand jeder Textur wird in ihrer Texturphase gekapselt.

In einer C++-Anwendung muss der Zustand jeder Textur mit der [**IDirect3DDevice9::SetTextureStageState-Methode festgelegt**](/windows/desktop/api) werden. Übergeben Sie die Phasennummer (0-7) als Wert des ersten Parameters. Legen Sie den Wert des zweiten Parameters auf einen Member des [**aufzählten D3DTEXTURESTAGESTATETYPE-Typs**](./d3dtexturestagestatetype.md) fest. Der letzte Parameter ist der Zustandswert für den bestimmten Texturzustand.

Mithilfe von Texturschnittstellenzeigen kann Ihre Anwendung eine Mischung aus bis zu acht Texturen rendern. Legen Sie die aktuellen Texturen fest, indem Sie die [**IDirect3DDevice9::SetTexture-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) aufrufen. Direct3D kombiniert alle aktuellen Texturen mit den Primitiven, die es rendert.

> [!Note]  
> Die [**IDirect3DDevice9::SetTexture-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) erhöht die Verweisanzahl der Texturoberfläche, die zugewiesen wird. Wenn die Textur nicht mehr benötigt wird, sollten Sie die Textur in der entsprechenden Phase auf **NULL festlegen.** Wenn Sie dies nicht tun, wird die Oberfläche nicht freigegeben, was zu einem Arbeitsspeicherverlust führt.

 

Ihre Anwendung kann den Texturumbruchzustand für die aktuellen Texturen festlegen, indem sie die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aufruft. Übergeben Sie einen Wert von D3DRS WRAP0 bis D3DRS WRAP7 als Wert des ersten Parameters, und verwenden Sie eine Kombination der \_ \_ Flags D3DWRAPCOORD \_ 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD 2 und \_ D3DWRAPCOORD 3, um das Umschließen in der \_ u-, v- oder w-Richtung zu aktivieren.

Ihre Anwendung kann auch die Texturperspektive und den Texturfilterungszustände festlegen. Weitere Informationen [finden Sie unter Texturfilterung (Direct3D 9).](texture-filtering.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
