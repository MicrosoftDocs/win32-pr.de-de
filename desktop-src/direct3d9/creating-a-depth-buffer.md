---
description: Ein Tiefenpuffer ist eine Eigenschaft des Geräts. Um einen Tiefenpuffer zu erstellen, der von Direct3D verwaltet wird, legen Sie die entsprechenden Member der D3DPRESENT \_ PARAMETERS-Struktur fest, wie im folgenden Codebeispiel gezeigt.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Erstellen eines Tiefenpuffers (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2f79e6ad32aa2c10b92d0233f85d86744d0a2c562b1991c89990d61bad506c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527922"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a>Erstellen eines Tiefenpuffers (Direct3D 9)

Ein Tiefenpuffer ist eine Eigenschaft des Geräts. Um einen Tiefenpuffer zu erstellen, der von Direct3D verwaltet wird, legen Sie die entsprechenden Member der [**D3DPRESENT \_ PARAMETERS-Struktur**](d3dpresent-parameters.md) fest, wie im folgenden Codebeispiel gezeigt.


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



Indem Sie den EnableAutoDepthStencil-Member auf **TRUE** festlegen, weisen Sie Direct3D an, Tiefenpuffer für die Anwendung zu verwalten. Beachten Sie, dass AutoDepthStencilFormat auf ein gültiges Tiefenpufferformat festgelegt werden muss. Das D3DFMT \_ D16-Flag gibt einen 16-Bit-Tiefenpuffer an, sofern verfügbar.

Der folgende Aufruf der [**IDirect3D9::CreateDevice-Methode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) erstellt ein Gerät, das dann einen Tiefenpuffer erstellt.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



Der Tiefenpuffer wird automatisch als Renderziel des Geräts festgelegt. Wenn das Gerät zurückgesetzt wird, wird der Tiefenpuffer automatisch zerstört und in der neuen Größe neu erstellt.

Um eine neue Tiefenpufferoberfläche zu erstellen, verwenden Sie die [**IDirect3DDevice9::CreateDepthStencilSurface-Methode.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)

Verwenden Sie die [**IDirect3DDevice9::SetDepthStencilSurface-Methode,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) um eine neue Tiefenpufferoberfläche für das Gerät festzulegen.

Um den Tiefenpuffer in Ihrer Anwendung zu verwenden, müssen Sie den Tiefenpuffer aktivieren. Weitere Informationen finden Sie unter [Aktivieren der Tiefenpufferung (Direct3D 9).](enabling-depth-buffering.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tiefenpuffer](depth-buffers.md)
</dt> </dl>

 

 
