---
description: Gibt Informationen zur Platzierung und Ausrichtung eines Glyphen in einer Zeichenzelle zurück.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: ID3DXFont::GetGlyphData-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetGlyphData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7981e10497dc263a60ae2d5e176fd4d95746b3193d7a5b606aea16afa1188ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629889"
---
# <a name="id3dxfontgetglyphdata-method"></a>ID3DXFont::GetGlyphData-Methode

Gibt Informationen zur Platzierung und Ausrichtung eines Glyphen in einer Zeichenzelle zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetGlyphData(
  [in]  UINT               Glyph,
  [out] LPDIRECT3DTEXTURE9 *ppTexture,
  [out] RECT               *pBlackBox,
  [out] POINT              *pCellInc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Glyphe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Glyphenbezeichner.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Adresse eines Zeigers auf ein [**IDirect3DTexture9-Objekt,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) das das Glyphen enthält.

</dd> <dt>

*pBlackBox* \[ out\]
</dt> <dd>

Typ: **[ **RECT**](/previous-versions//dd162897(v=vs.85))\***

Zeiger auf das kleinste Rechteckobjekt, das das Glyphe vollständig umschließt.

</dd> <dt>

*pCellInc* \[ out\]
</dt> <dd>

Typ: **[ **POINT**](../winprog/windows-data-types.md)\***

Zeiger auf den zweidimensionalen Vektor, der den Ursprung der aktuellen Zeichenzelle mit dem Ursprung der nächsten Zeichenzelle verbindet. Weitere Informationen finden Sie unter [**POINT**](../winprog/windows-data-types.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
