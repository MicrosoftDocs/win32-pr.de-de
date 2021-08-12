---
description: Erstellt eine leere Textur und passt die aufrufenden Parameter nach Bedarf an.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: D3DXCreateTexture-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6264be0712f5ac7f30a9882efde5c66e1e75404634e77d6b72d2313ba016fd6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299255"
---
# <a name="d3dxcreatetexture-function"></a>D3DXCreateTexture-Funktion

Erstellt eine leere Textur und passt die aufrufenden Parameter nach Bedarf an.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Textur zugeordnet werden soll.

</dd> <dt>

*Breite* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Breite in Pixel. Wenn dieser Wert 0 ist, wird der Wert 1 verwendet. Siehe Hinweise.

</dd> <dt>

*Höhe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Höhe in Pixel. Wenn dieser Wert 0 ist, wird der Wert 1 verwendet. Siehe Hinweise.

</dd> <dt>

*MipLevels* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der angeforderten MIP-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, wird eine vollständige Mipmapkette erstellt.

</dd> <dt>

*Nutzung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)oder **D3DUSAGE \_ DYNAMIC**. Das Festlegen dieses Flags auf **D3DUSAGE \_ RENDERTARGET** gibt an, dass die Oberfläche durch Aufrufen der [**SetRenderTarget-Methode**](/windows/desktop/api) als Renderziel verwendet werden soll. Wenn **D3DUSAGE \_ RENDERTARGET** oder **D3DUSAGE \_ DYNAMIC** angegeben ist, sollte die Anwendung überprüfen, ob das Gerät diesen Vorgang unterstützt, indem [**CheckDeviceFormat aufruft.**](/windows/desktop/api) Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden von dynamischen Texturen.](performance-optimizations.md)

</dd> <dt>

*Formatieren* \[ In\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [aufzählten D3DFORMAT-Typs,](d3dformat.md) der das angeforderte Pixelformat für die Textur beschreibt. Die zurückgegebene Textur kann ein anderes Format als die angegebene aufweisen, wenn das Gerät das angeforderte Format nicht unterstützt. Anwendungen sollten das Format der zurückgegebenen Textur überprüfen, um zu überprüfen, ob sie dem angeforderten Format entspricht.

</dd> <dt>

*Pool* \[ In\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**aufzählten D3DPOOL-Typs,**](./d3dpool.md) der die Speicherklasse beschreibt, in der die Textur platziert werden soll.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) die das erstellte Texturobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Intern verwendet D3DXCreateTexture [**D3DXCheckTextureRequirements,**](d3dxchecktexturerequirements.md) um die aufrufenden Parameter anzupassen. Daher sind Aufrufe von D3DXCreateTexture häufig erfolgreich, wenn Aufrufe von [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) fehlschlagen würden.

Wenn sowohl Height als auch Width auf [D3DX \_ DEFAULT](other-d3dx-constants.md)festgelegt sind, wird für beide Parameter der Wert 256 verwendet. Wenn Height oder Width auf D3DX DEFAULT festgelegt ist und der andere Parameter auf einen numerischen Wert festgelegt ist, ist die Textur quadratisch, und die Höhe und Breite sind gleich dem numerischen \_ Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texturfunktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
