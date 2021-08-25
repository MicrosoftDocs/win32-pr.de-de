---
description: Wendet Gutter auf ein IDirect3DTexture9-Texturobjekt an.
ms.assetid: e8f4a4cf-4d3b-419b-9486-08aa3bd3d8a4
title: ID3DXTextureGutterHelper::ApplyGuttersTex-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: a289eede9b55a3560408caf71a20aaf1811bb82780488b886cade8aaa5e96d75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893240"
---
# <a name="id3dxtexturegutterhelperapplygutterstex-method"></a>ID3DXTextureGutterHelper::ApplyGuttersTex-Methode

Wendet Gutter auf ein [**IDirect3DTexture9-Texturobjekt**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT ApplyGuttersTex(
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTexture* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf ein [**IDirect3DTexture9-Texturobjekt.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ WASDRAWING, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

[**Texel**](id3dxtexturegutterhelper.md) der Klasse 2 werden durch Resampling der Klassen 1 und 4 generiert.

Breite und Höhe der Textur müssen mit denen identisch sein, die von [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md) und [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md)zurückgegeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
