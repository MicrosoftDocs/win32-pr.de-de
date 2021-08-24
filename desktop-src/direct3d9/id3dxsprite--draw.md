---
description: Fügt der Liste der Batch-Sprites einen Sprite hinzu.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: ID3DXSprite::D raw-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d453a2e03538b7601b5f73033a4749430e8812ef317a90816cac220e61695279
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747370"
---
# <a name="id3dxspritedraw-method"></a>ID3DXSprite::D raw-Methode

Fügt der Liste der Batch-Sprites einen Sprite hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTexture* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf eine [**IDirect3DTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) die die Spritetextur darstellt.

</dd> <dt>

*pSrcRect* \[ In\]
</dt> <dd>

Typ: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die den Teil der Quelltextur angibt, der für den Sprite verwendet werden soll. Wenn dieser Parameter **NULL** ist, wird das gesamte Quellbild für den Sprite verwendet.

</dd> <dt>

*pCenter* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf einen [**D3DXVECTOR3-Vektor,**](d3dxvector3.md) der die Mitte des Sprite identifiziert. Wenn dieses Argument **NULL** ist, wird der Punkt (0,0,0) verwendet, bei dem es sich um die linke obere Ecke handelt.

</dd> <dt>

*pPosition* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf einen [**D3DXVECTOR3-Vektor,**](d3dxvector3.md) der die Position des Sprite identifiziert. Wenn dieses Argument **NULL** ist, wird der Punkt (0,0,0) verwendet, bei dem es sich um die linke obere Ecke handelt.

</dd> <dt>

*Farbe* \[ In\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR-Typ.**](d3dcolor.md) Die Farb- und Alphakanäle werden durch diesen Wert moduliert. Der Wert 0xFFFFFFFF behält die ursprüngliche Quellfarbe und die Alphadaten bei. Verwenden Sie das [**D3DCOLOR \_ RGBA-Makro,**](d3dcolor-rgba.md) um diese Farbe zu generieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Um einen Sprite zu skalieren, zu drehen oder zu übersetzen, rufen Sie [**ID3DXSprite::SetTransform**](id3dxsprite--settransform.md) mit einer Matrix auf, die die SRT-Werte (Scale, Rotate, Translate) enthält, bevor Sie ID3DXSprite::D raw aufrufen. Informationen zum Festlegen von SRT-Werten in einer Matrix finden Sie unter [Matrixtransformationen.](transforms.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::GetTransform**](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
