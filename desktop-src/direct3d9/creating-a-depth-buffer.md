---
description: Ein tiefen Puffer ist eine Eigenschaft des Geräts. Zum Erstellen eines tiefen Puffers, der von Direct3D verwaltet wird, legen Sie die entsprechenden Member der D3DPRESENT- \_ Parameter Struktur fest, wie im folgenden Codebeispiel gezeigt.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Erstellen eines tiefen Puffers (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa30ccba6c44d3582201ea96017a16cc903fecce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126158"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a>Erstellen eines tiefen Puffers (Direct3D 9)

Ein tiefen Puffer ist eine Eigenschaft des Geräts. Zum Erstellen eines tiefen Puffers, der von Direct3D verwaltet wird, legen Sie die entsprechenden Member der [**D3DPRESENT- \_ Parameter**](d3dpresent-parameters.md) Struktur fest, wie im folgenden Codebeispiel gezeigt.


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



Indem Sie den enableautodepthstencil-Member auf " **true**" festlegen, weisen Sie Direct3D an, die tiefen Puffer für die Anwendung zu verwalten. Beachten Sie, dass autodepthstencilformat auf ein gültiges Tiefe Puffer Format festgelegt werden muss. Das \_ Flag D3DFMT D16 gibt einen 16-Bit-Tiefen Puffer an, sofern verfügbar.

Mit dem folgenden Aufrufen der [**IDirect3D9:: kreatedevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) -Methode wird ein Gerät erstellt, das dann einen tiefen Puffer erstellt.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



Der tiefen Puffer wird automatisch als Renderziel des Geräts festgelegt. Wenn das Gerät zurückgesetzt wird, wird der tiefen Puffer automatisch zerstört und in der neuen Größe neu erstellt.

Verwenden Sie die [**IDirect3DDevice9:: foatedepthstencilsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) -Methode, um eine neue tiefen Puffer Oberfläche zu erstellen.

Verwenden Sie die [**IDirect3DDevice9:: setdepthstencilsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) -Methode, um eine neue tiefen Puffer Oberfläche für das Gerät festzulegen.

Um den tiefen Puffer in der Anwendung zu verwenden, müssen Sie den tiefen Puffer aktivieren. Weitere Informationen finden Sie unter [Aktivieren der tiefen Pufferung (Direct3D 9)](enabling-depth-buffering.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tiefen Puffer](depth-buffers.md)
</dt> </dl>

 

 
