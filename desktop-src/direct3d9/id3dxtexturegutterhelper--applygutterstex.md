---
description: Wendet die-Guster auf ein IDirect3DTexture9-Textur Objekt an.
ms.assetid: e8f4a4cf-4d3b-419b-9486-08aa3bd3d8a4
title: 'ID3DXTextureGutterHelper:: applygutterstex-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c15bbc981bad3a670923e24e7d0745e91d0d9fcf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961640"
---
# <a name="id3dxtexturegutterhelperapplygutterstex-method"></a>ID3DXTextureGutterHelper:: applygutterstex-Methode

Wendet die-Guster auf ein [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Textur Objekt an.

## <a name="syntax"></a>Syntax


```C++
HRESULT ApplyGuttersTex(
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptexture* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf ein [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Textur Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, D3DERR \_ wasstilldrawing, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

[**Class 2 texeln**](id3dxtexturegutterhelper.md) werden durch das erneute Sampling von Class 1 und 4 texeln generiert.

Breite und Höhe der Textur müssen mit den von [**ID3DXTextureGutterHelper:: getWidth**](id3dxtexturegutterhelper--getwidth.md) und [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md)zurückgegebenen Zeichen identisch sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
