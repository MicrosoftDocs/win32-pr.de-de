---
description: Überprüft die Parameter für die Volumetexturerstellung.
ms.assetid: 1a02cb99-2582-4d8f-aacf-67ed75f6deb8
title: D3DXCheckVolumeTextureRequirements-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVolumeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3fb285df29400ce71c439454f96e984f4fa5f53bb9c24e897d1d687778bb2044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988830"
---
# <a name="d3dxcheckvolumetexturerequirements-function"></a>D3DXCheckVolumeTextureRequirements-Funktion

Überprüft die Parameter für die Volumetexturerstellung.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCheckVolumeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pDepth,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Volumetextur zugeordnet werden soll.

</dd> <dt>

*pWidth* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf die angeforderte Breite in Pixel oder **NULL.** Gibt die korrigierte Größe zurück.

</dd> <dt>

*pHeight* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf die angeforderte Höhe in Pixel oder **NULL**. Gibt die korrigierte Größe zurück.

</dd> <dt>

*pDepth* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf die angeforderte Tiefe in Pixel oder **NULL.** Gibt die korrigierte Größe zurück.

</dd> <dt>

*pNumMipLevels* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf die Anzahl der angeforderten Mipmapebenen oder **NULL.** Gibt die korrigierte Anzahl von Mipmapebenen zurück.

</dd> <dt>

*Nutzung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Wird derzeit nicht verwendet, legen Sie auf 0 fest.

</dd> <dt>

*pFormat* \[ in, out\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)\***

Zeiger auf einen Member des [D3DFORMAT-Enumerationstyps.](d3dformat.md) Gibt das gewünschte Pixelformat oder **NULL** an. Gibt das korrigierte Format zurück.

</dd> <dt>

*Pool* \[ In\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**D3DPOOL-Enumerationstyps,**](./d3dpool.md) der die Speicherklasse beschreibt, in der die Volumetextur platziert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Wenn Parameter für diese Funktion ungültig sind, gibt diese Funktion korrigierte Parameter zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
