---
description: Laden Sie eine Reihe von Symbolen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: ID3DX10Font::P reloadglyphs-Methode (d3dx10. h)
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
ms.openlocfilehash: fdb67b8a25912c6efc49ef27082d3b6b4e843b33
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355192"
---
# <a name="id3dx10fontpreloadglyphs-method"></a>ID3DX10Font::P reloadglyphs-Methode

Laden Sie eine Reihe von Symbolen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.

## <a name="syntax"></a>Syntax


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zuerst* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

ID des ersten Symbols, das in den Videospeicher geladen werden soll.

</dd> <dt>

*Letzter* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

ID des letzten Symbols, das in den Videospeicher geladen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Diese Methode generiert Texturen, die die Eingabe Symbole enthalten. Die Symbole werden als eine Reihe von Dreiecken gezeichnet.

Symbole werden nicht auf dem Gerät gerendert. ID3DX10Font::D rawtext muss nach wie vor aufgerufen werden, um die Symbole zu erzeugen. Durch das vorab Laden von Symbolen in den Videospeicher verwendet ID3DX10Font::D rawtext erheblich weniger CPU-Ressourcen.

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

 

 
