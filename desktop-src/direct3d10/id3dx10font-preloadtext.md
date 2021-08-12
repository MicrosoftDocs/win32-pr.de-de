---
description: Laden Sie formatierten Text in den Videospeicher, um die Effizienz des Renderns auf dem Gerät zu verbessern. Diese Methode unterstützt ANSI- und Unicode-Zeichenfolgen.
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: ID3DX10Font::P reloadText-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 23c7a3a8ce8ed3534a7369f167ce1045d200cbaeea1aa80653e05412ffa978e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302845"
---
# <a name="id3dx10fontpreloadtext-method"></a>ID3DX10Font::P reloadText-Methode

Laden Sie formatierten Text in den Videospeicher, um die Effizienz des Renderns auf dem Gerät zu verbessern. Diese Methode unterstützt ANSI- und Unicode-Zeichenfolgen.

## <a name="syntax"></a>Syntax


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pString* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die in den Videospeicher geladen werden soll. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Datentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*Anzahl* \[ In\]
</dt> <dd>

Typ: **[ **INT**](../winprog/windows-data-types.md)**

Anzahl der Zeichen in der Textzeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in PreloadTextW aufgelöst. Andernfalls wird der Funktionsaufruf in PreloadTextA aufgelöst, da ANSI-Zeichenfolgen verwendet werden.

Diese Methode generiert Texturen, die Glyphen enthalten, die den Eingabetext darstellen. Die Glyphen werden als eine Reihe von Dreiecken gezeichnet.

Text wird nicht auf dem Gerät gerendert. ID3DX10Font::D rawText muss weiterhin aufgerufen werden, um den Text zu rendern. Durch das Vorabladen von Text in den Videospeicher beansprucht ID3DX10Font::D rawText jedoch deutlich weniger CPU-Ressourcen.

Diese Methode konvertiert Zeichen intern mithilfe der GDI-Funktion [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85))in Glyphen.

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

 

 
