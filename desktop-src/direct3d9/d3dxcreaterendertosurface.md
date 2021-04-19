---
description: Erstellt eine Renderoberfläche.
ms.assetid: 35e0007e-c405-46e1-a52b-625adc84732b
title: D3DXCreateRenderToSurface-Funktion (D3dx9core. h)
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
ms.openlocfilehash: 6fc64cbc65d30838db2105e0458d3553247f1ab1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363140"
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

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das Gerät, das der Renderoberfläche zugeordnet werden soll.

</dd> <dt>

*Breite* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Breite der Renderoberfläche in Pixel.

</dd> <dt>

*Höhe* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Höhe der Renderoberfläche in Pixel.

</dd> <dt>

*Format* \[ in\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Pixel Format der Renderoberfläche beschreibt.

</dd> <dt>

*Depthstencil* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

**True** gibt an, dass die Renderoberfläche eine tiefen Schablone unterstützt. Andernfalls ist dieser Member auf **false** festgelegt. Mit dieser Funktion wird ein neuer tiefen Puffer erstellt.

</dd> <dt>

*Depthstencilformat* \[ in\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Wenn *depthstencil* auf **true** festgelegt ist, ist dieser Parameter ein Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das tiefen Schablone-Format der Renderoberfläche beschreibt.

</dd> <dt>

*pprenderumsurface* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***

Adresse eines Zeigers auf eine [**ID3DXRenderToSurface**](id3dxrendertosurface.md) -Schnittstelle, die die erstellte Renderoberfläche darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
