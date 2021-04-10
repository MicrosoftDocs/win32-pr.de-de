---
description: Laden Sie formatierten Text in den Videospeicher, um die Effizienz beim Rendern auf das Gerät zu verbessern. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: ID3DX10Font::P reloadtext-Methode (d3dx10. h)
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
ms.openlocfilehash: c7294fb7e86b3532960a34a15e1118dc33f748f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219533"
---
# <a name="id3dx10fontpreloadtext-method"></a>ID3DX10Font::P reloadtext-Methode

Laden Sie formatierten Text in den Videospeicher, um die Effizienz beim Rendern auf das Gerät zu verbessern. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.

## <a name="syntax"></a>Syntax


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstring* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die in den Videospeicher geladen werden soll. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Datentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*Anzahl* \[ in\]
</dt> <dd>

Typ: **[ **int**](../winprog/windows-data-types.md)**

Anzahl der Zeichen in der Text Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufzurufen in preloadtextw aufgelöst. Andernfalls wird der Funktions Aufrufwert in preloadtexta aufgelöst, da ANSI-Zeichen folgen verwendet werden.

Diese Methode generiert Texturen, die Symbole enthalten, die den Eingabetext darstellen. Die Symbole werden als eine Reihe von Dreiecken gezeichnet.

Der Text wird nicht auf dem Gerät gerendert. ID3DX10Font::D rawtext muss nach wie vor aufgerufen werden, um den Text zu erzeugen. Durch das vorab Laden von Text in den Videospeicher verwendet ID3DX10Font::D rawtext erheblich weniger CPU-Ressourcen.

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

 

 
