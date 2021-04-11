---
description: Lädt formatierten Text in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.
ms.assetid: f2a4e9f5-87c5-46c0-965d-ce1535a6921d
title: ID3DXFont::P reloadtext-Methode (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 958979e3008cf9ae0b79e2de3591635187df0f12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132401"
---
# <a name="id3dxfontpreloadtext-method"></a>ID3DXFont::P reloadtext-Methode

Lädt formatierten Text in den Videospeicher, um die Effizienz des Renderings auf dem Gerät zu verbessern. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.

## <a name="syntax"></a>Syntax


```C++
HRESULT PreloadText(
  [in] LPCTSTR *pString,
  [in] INT     Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstring* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)\***

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

Der Text wird nicht auf dem Gerät gerendert. [**DrawText**](id3dxfont--drawtext.md) muss dennoch aufgerufen werden, um den Text zu erzeugen. Durch das vorab Laden von Text in den Videospeicher verwendet **DrawText** jedoch erheblich weniger CPU-Ressourcen.

Diese Methode konvertiert Zeichen intern mithilfe der GDI-Funktion [**getcharakteriplacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)in Glyphen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
