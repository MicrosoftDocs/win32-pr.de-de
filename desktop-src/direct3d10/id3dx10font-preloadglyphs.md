---
description: Laden Sie eine Reihe von Glyphen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: ID3DX10Font::P reloadGlyphs-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadGlyphs
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 358523135db83f2ec7f973fce403a44d2f0ece82ab60cf9527cb612ccde61e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540336"
---
# <a name="id3dx10fontpreloadglyphs-method"></a>ID3DX10Font::P reloadGlyphs-Methode

Laden Sie eine Reihe von Glyphen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.

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

ID des ersten Glyphen, das in den Videospeicher geladen werden soll.

</dd> <dt>

*Letzte* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

ID des letzten Glyphen, das in den Videospeicher geladen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Diese Methode generiert Texturen, die die Eingabe-Glyphen enthalten. Die Glyphen werden als eine Reihe von Dreiecken gezeichnet.

Glyphen werden nicht auf dem Gerät gerendert. ID3DX10Font::D rawText muss weiterhin aufgerufen werden, um die Glyphen zu rendern. Durch das Vorabladen von Glyphen in den Videospeicher verwendet ID3DX10Font::D rawText jedoch deutlich weniger CPU-Ressourcen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
