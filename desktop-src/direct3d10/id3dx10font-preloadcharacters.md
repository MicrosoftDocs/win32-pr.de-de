---
description: Laden Sie eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.
ms.assetid: 935a6248-e6b7-4fce-aaa7-b7f0c94c1f79
title: ID3DX10Font::P reloadcharacters-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadCharacters
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fafa34d4a243e254e929f7c9a1d65d2a3fb9c8dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361868"
---
# <a name="id3dx10fontpreloadcharacters-method"></a>ID3DX10Font::P reloadcharacters-Methode

Laden Sie eine Reihe von Zeichen in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern.

## <a name="syntax"></a>Syntax


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zuerst* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

ID des ersten Zeichens, das in den Videospeicher geladen werden soll.

</dd> <dt>

*Letzter* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

ID des letzten Zeichens, das in den Videospeicher geladen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Diese Methode generiert Texturen mit Symbolen, die die Eingabezeichen darstellen. Die Symbole werden als eine Reihe von Dreiecken gezeichnet.

Zeichen werden nicht auf dem Gerät gerendert. ID3DX10Font::D rawtext muss nach wie vor aufgerufen werden, um die Zeichen zu erzeugen. Durch das vorab Laden von Zeichen in den Videospeicher verwendet ID3DX10Font::D rawtext erheblich weniger CPU-Ressourcen.

Diese Methode konvertiert Zeichen intern mithilfe der GDI-Funktion [getcharakteriplacement](/previous-versions//ms534004(v=vs.85))in Glyphen.

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

 

 
