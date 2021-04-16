---
description: Erstellt eine leere Textur und passt die aufrufenden Parameter nach Bedarf an.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: D3DXCreateTexture-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: ecbd5cbb94355af9c1e51e6c7e8fc31a862b03be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530917"
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

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.

</dd> <dt>

*Breite* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Breite in Pixel. Wenn dieser Wert 0 ist, wird der Wert 1 verwendet. Siehe Hinweise.

</dd> <dt>

*Höhe* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Höhe in Pixel. Wenn dieser Wert 0 ist, wird der Wert 1 verwendet. Siehe Hinweise.

</dd> <dt>

*Miplevels* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der angeforderten Mip-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.

</dd> <dt>

*Verwendung* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ renderTarget**](d3dusage.md)oder **D3DUSAGE \_ Dynamic**. Wenn dieses Flag auf **D3DUSAGE \_ renderTarget** festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll, indem die [**SetRenderTarget**](/windows/desktop/api) -Methode aufgerufen wird. Wenn entweder **D3DUSAGE \_ renderTarget** oder **D3DUSAGE \_ Dynamic** angegeben ist, muss die Anwendung überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/desktop/api)unterstützt. Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden dynamischer Texturen](performance-optimizations.md).

</dd> <dt>

*Format* \[ in\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die Textur beschreibt. Die zurückgegebene Textur kann ein anderes Format aufweisen als das angegebene Format, wenn das Gerät das angeforderte Format nicht unterstützt. Anwendungen sollten das Format der zurückgegebenen Textur überprüfen, um festzustellen, ob es mit dem angeforderten Format übereinstimmt.

</dd> <dt>

*Pool* \[ in\]
</dt> <dd>

Typ: **[ **D3DPOOL**](./d3dpool.md)**

Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Textur platziert werden soll.

</dd> <dt>

*pptexture* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Adresse eines Zeigers auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Intern verwendet D3DXCreateTexture [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) , um die aufrufenden Parameter anzupassen. Daher sind Aufrufe von D3DXCreateTexture oft erfolgreich, wenn Aufrufe von " [**kreatetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) " fehlschlagen.

Wenn sowohl Height als auch Width auf [D3DX \_ default](other-d3dx-constants.md)festgelegt ist, wird für beide Parameter der Wert 256 verwendet. Wenn entweder Height oder Width auf D3DX Default festgelegt ist \_ und der andere Parameter auf einen numerischen Wert festgelegt ist, ist die Textur quadratisch, wobei die Höhe und die Breite dem numerischen Wert entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
