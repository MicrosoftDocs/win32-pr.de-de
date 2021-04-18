---
description: Fügt der Liste der im Batch verarbeiteten Sprites ein Sprite hinzu.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: ID3DXSprite::D RAW-Methode (D3dx9core. h)
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
ms.openlocfilehash: 9cba7b12c55e7ab9f5f939347a8b500ec4965f75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364391"
---
# <a name="id3dxspritedraw-method"></a>ID3DXSprite::D RAW-Methode

Fügt der Liste der im Batch verarbeiteten Sprites ein Sprite hinzu.

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

*ptexture* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die die Sprite-Textur darstellt.

</dd> <dt>

*psrcrect* \[ in\]
</dt> <dd>

Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die den Teil der Quell Textur angibt, der für das Sprite verwendet werden soll. Wenn dieser Parameter **null** ist, wird das gesamte Quell Image für das Sprite verwendet.

</dd> <dt>

*pcenter* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf einen [**D3DXVECTOR3**](d3dxvector3.md) -Vektor, der die Mitte des Sprite identifiziert. Wenn dieses Argument **null** ist, wird der Punkt (0, 0, 0) verwendet. Dies ist die linke obere Ecke.

</dd> <dt>

*pposition* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf einen [**D3DXVECTOR3**](d3dxvector3.md) -Vektor, der die Position des Sprite angibt. Wenn dieses Argument **null** ist, wird der Punkt (0, 0, 0) verwendet. Dies ist die linke obere Ecke.

</dd> <dt>

*Farbe* \[ in\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR**](d3dcolor.md) -Typ. Die Farb-und Alphakanäle werden von diesem Wert moduliert. Der Wert 0xFFFFFFFF behält die ursprüngliche Quellfarbe und Alpha Daten bei. Verwenden Sie das [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) -Makro, um diese Farbe zu generieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Um Sprite zu skalieren, zu drehen oder zu übersetzen, rufen Sie [**ID3DXSprite:: setTransform**](id3dxsprite--settransform.md) mit einer Matrix auf, die die Werte für Skala, Drehung und Übersetzung (SRT) enthält, bevor Sie ID3DXSprite::D RAW aufrufen. Weitere Informationen zum Festlegen von SRT-Werten in einer Matrix finden Sie unter [Matrix Transformationen](transforms.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite:: GetTransform**](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
