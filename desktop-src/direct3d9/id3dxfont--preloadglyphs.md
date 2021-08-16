---
description: Lädt eine Reihe von Glyphen in den Videospeicher, um die Effizienz des Renderns auf dem Gerät zu verbessern.
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: ID3DXFont::P reloadGlyphs-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea422a6e0b0ecfda6b4eb03a0636eb013d8c840c96cec6f1c482589de29f3c76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563930"
---
# <a name="id3dxfontpreloadglyphs-method"></a>ID3DXFont::P reloadGlyphs-Methode

Lädt eine Reihe von Glyphen in den Videospeicher, um die Effizienz des Renderns auf dem Gerät zu verbessern.

## <a name="syntax"></a>Syntax


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Erste* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

ID des ersten Glyphens, das in den Videospeicher geladen werden soll.

</dd> <dt>

*Zuletzt* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

ID des letzten Glyphens, das in den Videospeicher geladen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Diese Methode generiert Texturen, die die Eingabeglyphen enthalten. Die Glyphen werden als eine Reihe von Dreiecken gezeichnet.

Glyphen werden nicht auf dem Gerät gerendert. [**DrawText**](id3dxfont--drawtext.md) muss weiterhin aufgerufen werden, um die Glyphen zu rendern. Durch das Vorabladen von Glyphen in den Videospeicher verwendet **DrawText** jedoch deutlich weniger CPU-Ressourcen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
