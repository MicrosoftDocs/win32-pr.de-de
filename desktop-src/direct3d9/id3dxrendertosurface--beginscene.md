---
description: Beginnt eine Szene.
ms.assetid: 8125c592-b985-42f7-8644-59ba93a1c517
title: 'ID3DXRenderToSurface:: BeginScene-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.BeginScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5aa2229e88123cc1d52f65f1edf032c46f819229
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364392"
---
# <a name="id3dxrendertosurfacebeginscene-method"></a>ID3DXRenderToSurface:: BeginScene-Methode

Beginnt eine Szene.

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginScene(
  [in]       LPDIRECT3DSURFACE9 pSurface,
  [in] const D3DVIEWPORT9       *pViewport
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSurface* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Zeiger auf eine [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle, die die Renderoberfläche darstellt.

</dd> <dt>

*pviewport* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DVIEWPORT9**](d3dviewport9.md) \***

Zeiger auf eine [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur, die den Viewport für die Szene beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall. D3DERR \_ outo-videomemory D3DXERR \_ InvalidData E \_ outoken-Speicher

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> <dt>

[**ID3DXRenderToSurface:: EndScene**](id3dxrendertosurface--endscene.md)
</dt> </dl>

 

 
