---
description: Gibt Informationen zur Platzierung und Ausrichtung eines Glyphen in einer Zeichenzelle zurück.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: ID3DX10Font::GetGlyphData-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eaabcd6de2acf5ec86ab8c9a47d4224ed230104fe189816abd9d02fd3ac09596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302890"
---
# <a name="id3dx10fontgetglyphdata-method"></a>ID3DX10Font::GetGlyphData-Methode

Gibt Informationen zur Platzierung und Ausrichtung eines Glyphen in einer Zeichenzelle zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Glyph* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Glyphenbezeichner.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***

Adresse eines Zeigers auf ein ID3D10Texture-Objekt, das das Glyphen enthält.

</dd> <dt>

*pBlackBox* \[ In\]
</dt> <dd>

Typ: **[ **RECT**](/previous-versions//dd162897(v=vs.85))\***

Zeiger auf das kleinste Rechteckobjekt, das das Glyphen vollständig umschließt. Weitere Informationen [finden Sie unter RECT](/previous-versions//ms536136(v=vs.85)).

</dd> <dt>

*pCellInc* \[ In\]
</dt> <dd>

Typ: **\* POINT**

Zeiger auf den zweidimensionalen Vektor, der den Ursprung der aktuellen Zeichenzelle mit dem Ursprung der nächsten Zeichenzelle verbindet. Weitere Informationen [finden Sie unter POINT](/previous-versions//ms536119(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
