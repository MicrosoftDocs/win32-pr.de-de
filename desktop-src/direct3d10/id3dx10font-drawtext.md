---
description: Zeichnen von formatiertem Text. Diese Methode unterstützt ANSI- und Unicode-Zeichenfolgen.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: ID3DX10Font::D rawText-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.DrawText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1eabe3a88fb3d38021eee8f186baed1d8403d18026d4d1704d520ad3c8b8f72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303170"
---
# <a name="id3dx10fontdrawtext-method"></a>ID3DX10Font::D rawText-Methode

Zeichnen von formatiertem Text. Diese Methode unterstützt ANSI- und Unicode-Zeichenfolgen.

## <a name="syntax"></a>Syntax


```C++
INT DrawText(
  [in] LPD3DX10SPRITE pSprite,
  [in] LPCTSTR        pString,
  [in] INT            Count,
  [in] LPRECT         pRect,
  [in] UINT           Format,
  [in] D3DXCOLOR      Color
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSprite* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**

Zeiger auf ein ID3DX10Sprite-Objekt, das die zu zeichnende Zeichenfolge enthält. Kann **NULL sein.** In diesem Fall rendert Direct3D die Zeichenfolge mit einem eigenen Sprite-Objekt. Zur Verbesserung der Effizienz sollte ein Sprite-Objekt angegeben werden, wenn ID3DX10Font::D rawText mehr als einmal in einer Zeile aufgerufen werden soll.

</dd> <dt>

*pString* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine zu zeichnende Zeichenfolge. Wenn UNICODE definiert ist, wird dieser Parametertyp in eine LPCWSTR-Datei auflösen, andernfalls wird der Typ in eine LPCSTR-Datei auflösen. Wenn der Count-Parameter -1 ist, muss die Zeichenfolge **NULL-terminiert** sein.

</dd> <dt>

*Anzahl* \[ In\]
</dt> <dd>

Typ: **[ **INT**](../winprog/windows-data-types.md)**

Die Anzahl der Zeichen in der Zeichenfolge. Wenn Count -1 ist, wird angenommen, dass der pString-Parameter ein Zeiger auf ein Sprite ist, das eine NULL-terminierte Zeichenfolge enthält, und ID3DX10Font::D rawText berechnet die Zeichenanzahl automatisch.

</dd> <dt>

*pRect* \[ In\]
</dt> <dd>

Typ: **LPRECT**

Zeiger auf eine [RECT-Struktur,](/previous-versions//ms536136(v=vs.85)) die das Rechteck in logischen Koordinaten enthält, in dem der Text formatiert werden soll. Wie bei jedem RECT-Objekt muss der Koordinatenwert der rechten Seite des Rechtecks größer als der wert der linken Seite sein. Ebenso muss der Koordinatenwert des unteren -Werts größer als der des oberen Werts sein.

</dd> <dt>

*Formatieren* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Geben Sie die Methode zum Formatieren des Texts an. Dies kann eine beliebige Kombination der folgenden Werte sein:



| Element                                                                                      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT \_ BOTTOM<br/>             | Rechtfertigen Sie den Text am unteren Rand des Rechtecks. Dieser Wert muss mit DT \_ SINGLELINE kombiniert werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT \_ CALCRECT<br/>       | Weisen Sie DrawText an, die Breite und Höhe des Rechtecks basierend auf der Länge der zu zeichnenden Zeichenfolge automatisch zu berechnen. Wenn mehrere Textzeilen enthalten sind, verwendet ID3DX10Font::D rawText die Breite des Rechtecks, auf das der pRect-Parameter zeigt, und erweitert die Basis des Rechtecks, um die letzte Textzeile zu gebundene. Wenn nur eine Textzeile enthalten ist, ändert ID3DX10Font::D rawText die rechte Seite des Rechtecks, sodass es das letzte Zeichen in der Zeile umgibt. In beiden Fällen gibt ID3DX10Font::D rawText die Höhe des formatierten Texts zurück, aber nicht den Text.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span>DT \_ CENTER<br/>             | Zentriert Text horizontal im Rechteck.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT \_ EXPANDTABS<br/> | Erweitern Sie Tabstoppzeichen. Die Standardanzahl von Zeichen pro Tabstopp beträgt acht.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span>DT \_ LEFT<br/>                   | Richten Sie Text links aus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT \_ NOCLIP<br/>             | Zeichnen ohne Clipping. ID3DX10Font::D rawText ist etwas schneller, wenn DT \_ NOCLIP verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RIGHT"></span><span id="dt_right"></span>DT \_ RIGHT<br/>                | Richten Sie Text rechts aus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT \_ RTLREADING<br/> | Anzeigen von Text in Leserichtung von rechts nach links für bidirektionalen Text, wenn eine hebräische oder arabische Schriftart ausgewählt ist. Die Standardlese reihenfolge für den text-Text ist von links nach rechts.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ SINGLELINE<br/> | Anzeigen von Text nur in einer einzelnen Zeile. Wagenrücklauf und Zeilenfeeds unterbricht die Zeile nicht.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span>DT \_ TOP<br/>                      | Text mit oberster Begründung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT \_ VCENTER<br/>          | Text vertikal zentriert (nur eine Zeile).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT \_ WORDBREAK<br/>    | Wörter unterbricht. Zeilen werden automatisch zwischen Wörtern unterbrochen, wenn sich ein Wort über den Rand des Rechtecks erstreckt, das durch den pRect-Parameter angegeben wird. Eine Wagenrücklauf-/Zeilenfeedsequenz unterbricht auch die Zeile.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Farbe* \[ In\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Farbe des Texts. Siehe [**D3DXCOLOR**](d3d10-d3dxcolor.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **INT**](../winprog/windows-data-types.md)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Höhe des Texts in logischen Einheiten. Wenn DT VCENTER oder DT BOTTOM angegeben ist, ist der Rückgabewert der Offset von pRect (von oben nach \_ \_ unten) des gezeichneten Texts. Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

Die Parameter dieser Methode sind denen der [GDI DrawText-Funktion sehr](/previous-versions//ms533909(v=vs.85)) ähnlich.

Diese Methode unterstützt sowohl ANSI- als auch Unicode-Zeichenfolgen.

Sofern nicht das DT NOCLIP-Format verwendet wird, schneide diese Methode den Text so ab, dass er nicht außerhalb des \_ angegebenen Rechtecks angezeigt wird. Es wird davon ausgegangen, dass alle Formatierungen mehrere Zeilen haben, es sei denn, das DT \_ SINGLELINE-Format ist angegeben.

Wenn die ausgewählte Schriftart zu groß für das Rechteck ist, versucht diese Methode nicht, eine kleinere Schriftart zu ersetzen.

Diese Methode unterstützt nur Schriftarten, deren Escape- und Ausrichtungsformat 0 (null) ist.

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

 

 
