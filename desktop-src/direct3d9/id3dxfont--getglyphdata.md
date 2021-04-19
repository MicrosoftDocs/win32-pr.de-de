---
description: Gibt Informationen über die Platzierung und die Ausrichtung eines Symbols in einer Zeichen Zelle zurück.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: 'ID3DXFont:: getglyphdata-Methode (D3dx9core. h)'
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
ms.openlocfilehash: 31f8d2e9d61cd7a8d6bd96fbdd3f6f6a7d895568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355182"
---
# <a name="id3dxfontgetglyphdata-method"></a>ID3DXFont:: getglyphdata-Methode

Gibt Informationen über die Platzierung und die Ausrichtung eines Symbols in einer Zeichen Zelle zurück.

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

*Glyphe* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Glyphe-Bezeichner.

</dd> <dt>

*pptexture* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Adresse eines Zeigers auf ein [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Objekt, das das Symbol enthält.

</dd> <dt>

*pblackbox* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***

Zeiger auf das kleinste Rechteck Objekt, das das Symbol vollständig einschließt.

</dd> <dt>

*pcellinc* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **Punkt**](../winprog/windows-data-types.md)\***

Ein Zeiger auf den zweidimensionalen Vektor, der den Ursprung der aktuellen Zeichen Zelle mit dem Ursprung der nächsten Zeichen Zelle verbindet. Siehe [**Punkt**](../winprog/windows-data-types.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
