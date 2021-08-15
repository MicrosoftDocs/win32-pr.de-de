---
description: Lädt eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderns auf dem Gerät zu verbessern.
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: ID3DXFont::P reloadCharacters-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cad2a324a6a5d56ff88dd343cf091b8c4ff2b99cd829344ae91f364458ec51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295316"
---
# <a name="id3dxfontpreloadcharacters-method"></a>ID3DXFont::P reloadCharacters-Methode

Lädt eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderns auf dem Gerät zu verbessern.

## <a name="syntax"></a>Syntax


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Erste* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

ID des ersten Zeichens, das in den Videospeicher geladen werden soll.

</dd> <dt>

*Zuletzt* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

ID des letzten Zeichens, das in den Videospeicher geladen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Diese Methode generiert Texturen, die Glyphen enthalten, die die Eingabezeichen darstellen. Die Glyphen werden als eine Reihe von Dreiecken gezeichnet.

Zeichen werden nicht auf dem Gerät gerendert. [**DrawText**](id3dxfont--drawtext.md) muss weiterhin aufgerufen werden, um die Zeichen zu rendern. Durch das Vorabladen von Zeichen in den Videospeicher verwendet **DrawText** jedoch deutlich weniger CPU-Ressourcen.

Diese Methode konvertiert Zeichen intern mithilfe der GDI-Funktion [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)in Glyphen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
