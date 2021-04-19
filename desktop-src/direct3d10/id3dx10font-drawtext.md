---
description: Formatierten Text zeichnen. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: ID3DX10Font::D rawtext-Methode (d3dx10. h)
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
ms.openlocfilehash: 5fa23684be1b63cfbd8e3d07d3578d87fdfbf46a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361207"
---
# <a name="id3dx10fontdrawtext-method"></a>ID3DX10Font::D rawtext-Methode

Formatierten Text zeichnen. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.

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

*psprite* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**

Zeiger auf ein ID3DX10Sprite-Objekt, das die Zeichenfolge enthält, die Sie zeichnen möchten. Kann **null** sein. in diesem Fall wird die Zeichenfolge von Direct3D mit einem eigenen Sprite-Objekt dargestellt. Um die Effizienz zu verbessern, sollte ein Sprite-Objekt angegeben werden, wenn ID3DX10Font::D rawtext mehrmals in einer Zeile aufgerufen werden soll.

</dd> <dt>

*pstring* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die gezeichnet werden soll. Wenn Unicode definiert ist, wird dieser Parametertyp in LPCWSTR aufgelöst. andernfalls wird der Typ zu LPCSTR aufgelöst. Wenn der count-Parameter-1 ist, muss die Zeichenfolge **null** sein.

</dd> <dt>

*Anzahl* \[ in\]
</dt> <dd>

Typ: **[ **int**](../winprog/windows-data-types.md)**

Die Anzahl der Zeichen in der Zeichenfolge. Wenn count-1 ist, wird angenommen, dass es sich bei dem pstring-Parameter um einen Zeiger auf ein Sprite handelt, das eine mit NULL endende Zeichenfolge und ID3DX10Font::D rawtext die Zeichen Anzahl automatisch berechnet.

</dd> <dt>

*vorab ausführen* \[ in\]
</dt> <dd>

Typ: **lprect**

Ein Zeiger auf eine [Rect](/previous-versions//ms536136(v=vs.85)) -Struktur, die das Rechteck in logischen Koordinaten enthält, in dem der Text formatiert werden soll. Wie bei jedem Rect-Objekt muss der Koordinaten Wert der rechten Seite des Rechtecks größer sein als der der linken Seite. Ebenso muss der Koordinaten Wert des unteren Werts größer als der obere Wert sein.

</dd> <dt>

*Format* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Gibt die Methode zum Formatieren des Texts an. Dabei kann es sich um eine beliebige Kombination der folgenden Werte handeln:



| Element                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT \_ unten<br/>             | Rechtfertigen Sie den Text am unteren Rand des Rechtecks. Dieser Wert muss mit dt \_ SingleLine kombiniert werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT \_ calcrect<br/>       | Weisen Sie DrawText an, die Breite und Höhe des Rechtecks basierend auf der Länge der Zeichenfolge, die gezeichnet werden soll, automatisch zu berechnen. Wenn mehrere Textzeilen vorhanden sind, verwendet ID3DX10Font::D rawtext die Breite des Rechtecks, auf das der prect-Parameter zeigt, und erweitert die Basis des Rechtecks, um die letzte Textzeile zu binden. Wenn nur eine Textzeile vorhanden ist, ändert ID3DX10Font::D rawtext die Rechte Seite des Rechtecks so, dass es das letzte Zeichen in der Zeile umschließt. In beiden Fällen gibt ID3DX10Font::D rawtext die Höhe des formatierten Texts zurück, aber den Text nicht.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span>DT \_ Center<br/>             | Zentrieren Sie Text horizontal im Rechteck.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT- \_ ExpandTabs<br/> | Erweitern Sie Tabulator Zeichen. Die Standardanzahl von Zeichen pro Tabstopp beträgt acht.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span>DT \_ Links<br/>                   | Text Links ausrichten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT \_ NoClip<br/>             | Zeichnen Sie ohne Clipping. ID3DX10Font::D rawtext ist etwas schneller, wenn dt \_ NoClip verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RIGHT"></span><span id="dt_right"></span>\_rechter dt<br/>                | Text rechts ausrichten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT \_ RtlReading<br/> | Zeigt Text in der Lesefolge von rechts nach Links für bidirektionalen Text an, wenn eine hebräische oder arabische Schriftart ausgewählt wird. Die Standard Lesereihenfolge für den gesamten Text ist von links nach rechts.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ SingleLine<br/> | Anzeige von Text nur in einer einzelnen Zeile. Wagen Rückläufe und Zeilen Vorschübe unterbrechen die Linie nicht.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span>DT \_ Top<br/>                      | Text der obersten rechtfertigen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT \_ vCenter<br/>          | Text vertikal zentrieren (nur einzeilige Zeile).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT- \_ WordBreak<br/>    | Wörter brechen. Zeilen werden zwischen Wörtern automatisch getrennt, wenn sich ein Wort hinter dem Rand des Rechtecks ausdehnen würde, das durch den prect-Parameter angegeben wird. Eine Wagen Rücklauf-/Zeilenvorschub Sequenz unterbricht ebenfalls die Zeile.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Farbe* \[ in\]
</dt> <dd>

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Textfarbe. Siehe [**D3DXCOLOR**](d3d10-d3dxcolor.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **int**](../winprog/windows-data-types.md)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert die Höhe des Texts in logischen Einheiten. Wenn dt \_ vCenter oder dt \_ Bottom angegeben ist, ist der Rückgabewert der Offset von vorab (oben nach unten) des gezeichneten Texts. Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

Die Parameter dieser Methode ähneln denen der [GDI-DrawText](/previous-versions//ms533909(v=vs.85)) -Funktion.

Diese Methode unterstützt sowohl ANSI-als auch Unicode-Zeichen folgen.

Wenn das DT \_ NoClip-Format nicht verwendet wird, wird der Text von dieser Methode so geklammert, dass er nicht außerhalb des angegebenen Rechtecks angezeigt wird. Es wird davon ausgegangen, dass die gesamte Formatierung mehrere Zeilen umfasst, es sei denn, das DT- \_ SingleLine-Format

Wenn die ausgewählte Schriftart für das Rechteck zu groß ist, versucht diese Methode nicht, eine kleinere Schriftart zu ersetzen.

Diese Methode unterstützt nur Schriftarten, deren escapesin und Ausrichtung gleich NULL sind.

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

 

 
