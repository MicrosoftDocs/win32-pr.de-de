---
description: Gibt Informationen über die Platzierung und Ausrichtung eines Symbols in einer Zeichen Zelle zurück.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: 'ID3DX10Font:: getglyphdata-Methode (d3dx10. h)'
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
ms.openlocfilehash: 530206c4f351cb1ef073639a21dfa37e43af5bae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365118"
---
# <a name="id3dx10fontgetglyphdata-method"></a>ID3DX10Font:: getglyphdata-Methode

Gibt Informationen über die Platzierung und Ausrichtung eines Symbols in einer Zeichen Zelle zurück.

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

*Glyphe* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Glyphe-Bezeichner.

</dd> <dt>

*pptexture* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***

Adresse eines Zeigers auf ein ID3D10Texture-Objekt, das das Symbol enthält.

</dd> <dt>

*pblackbox* \[ in\]
</dt> <dd>

Typ: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***

Zeiger auf das kleinste Rechteck Objekt, das das Symbol vollständig einschließt. Siehe [Rect](/previous-versions//ms536136(v=vs.85)).

</dd> <dt>

*pcellinc* \[ in\]
</dt> <dd>

Typ: **Punkt \***

Ein Zeiger auf den zweidimensionalen Vektor, der den Ursprung der aktuellen Zeichen Zelle mit dem Ursprung der nächsten Zeichen Zelle verbindet. Siehe [Punkt](/previous-versions//ms536119(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
