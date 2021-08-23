---
description: Erstellt eine Renderoberfläche.
ms.assetid: 35e0007e-c405-46e1-a52b-625adc84732b
title: D3DXCreateRenderToSurface-Funktion (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 632225dcad44324f88d8c126eb3f74d7779ff5ec698581514717dc1e0c54d3f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988630"
---
# <a name="d3dxcreaterendertosurface-function"></a>D3DXCreateRenderToSurface-Funktion

Erstellt eine Renderoberfläche.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateRenderToSurface(
  _In_  LPDIRECT3DDEVICE9     pDevice,
  _In_  UINT                  Width,
  _In_  UINT                  Height,
  _In_  D3DFORMAT             Format,
  _In_  BOOL                  DepthStencil,
  _In_  D3DFORMAT             DepthStencilFormat,
  _Out_ LPD3DXRENDERTOSURFACE *ppRenderToSurface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das Gerät, das der Renderoberfläche zugeordnet werden soll.

</dd> <dt>

*Breite* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Breite der Renderoberfläche in Pixel.

</dd> <dt>

*Höhe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Höhe der Renderoberfläche in Pixel.

</dd> <dt>

*Formatieren* \[ In\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [aufzählten D3DFORMAT-Typs,](d3dformat.md) der das Pixelformat der Renderoberfläche beschreibt.

</dd> <dt>

*Tiefenstencil* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

True **gibt an,** dass die Renderoberfläche eine Tiefen-Schablonenoberfläche unterstützt. Andernfalls wird dieser Member auf **FALSE festgelegt.** Diese Funktion erstellt einen neuen Tiefenpuffer.

</dd> <dt>

*DepthStencilFormat* \[ In\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Wenn *DepthStencil* auf **TRUE** festgelegt ist, ist dieser Parameter ein Member des aufzählten [D3DFORMAT-Typs,](d3dformat.md) der das Tiefen-Schablonenformat der Renderoberfläche beschreibt.

</dd> <dt>

*ppRenderToSurface* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***

Adresse eines Zeigers auf eine [**ID3DXRenderToSurface-Schnittstelle,**](id3dxrendertosurface.md) die die erstellte Renderoberfläche darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
