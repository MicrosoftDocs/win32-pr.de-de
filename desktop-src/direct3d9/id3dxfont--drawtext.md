---
description: Zeichnet formatierten Text. Diese Methode unterstützt ANSI- und Unicode-Zeichenfolgen.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: ID3DXFont::D rawText-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.DrawText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d2a0b2dc61e2dd2a41f5a2fe864973fca91a5e471c75d6afc353c147f7a00fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987420"
---
# <a name="id3dxfontdrawtext-method"></a>ID3DXFont::D rawText-Methode

Zeichnet formatierten Text. Diese Methode unterstützt ANSI- und Unicode-Zeichenfolgen.

## <a name="syntax"></a>Syntax


```C++
INT DrawText(
  [in] LPD3DXSPRITE pSprite,
  [in] LPCTSTR      pString,
  [in] INT          Count,
  [in] LPRECT       pRect,
  [in] DWORD        Format,
  [in] D3DCOLOR     Color
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSprite* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXSPRITE**](id3dxsprite.md)**

Zeiger auf ein [**ID3DXSprite-Objekt,**](id3dxsprite.md) das die Zeichenfolge enthält. Kann **NULL sein.** In diesem Fall rendert Direct3D die Zeichenfolge mit einem eigenen Sprite-Objekt. Um die Effizienz zu verbessern, sollte ein Sprite-Objekt angegeben werden, wenn **DrawText** mehr als einmal in einer Zeile aufgerufen werden soll.

</dd> <dt>

*pString* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine zu zeichnende Zeichenfolge. Wenn der Count-Parameter -1 ist, muss die Zeichenfolge null-terminiert sein.

</dd> <dt>

*Anzahl* \[ In\]
</dt> <dd>

Typ: **[ **INT**](../winprog/windows-data-types.md)**

Gibt die Anzahl von Zeichen in der Zeichenfolge an. Wenn Count -1 ist, wird angenommen, dass der pString-Parameter ein Zeiger auf eine auf NULL terminierte Zeichenfolge ist, und **DrawText** berechnet die Zeichenanzahl automatisch.

</dd> <dt>

*pRect* \[ In\]
</dt> <dd>

Typ: **[ **LPRECT**](../winprog/windows-data-types.md)**

Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die das Rechteck in logischen Koordinaten enthält, in dem der Text formatiert werden soll. Der Koordinatenwert der rechten Seite des Rechtecks muss größer als der wert der linken Seite sein. Ebenso muss der Koordinatenwert des unteren -Werts größer als der des oberen Werts sein.

</dd> <dt>

*Formatieren* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt die Methode zum Formatieren des Texts an. Dies kann eine beliebige Kombination der folgenden Werte sein:



| Wert                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <dt>**DT \_ BOTTOM**</dt> </dl>             | Gerechtfertigt den Text am unteren Rand des Rechtecks. Dieser Wert muss mit DT \_ SINGLELINE kombiniert werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <dt>**DT \_ CALCRECT**</dt> </dl>       | Bestimmt die Breite und Höhe des Rechtecks. Wenn mehrere Textzeilen enthalten sind, verwendet **DrawText** die Breite des Rechtecks, auf das der pRect-Parameter zeigt, und erweitert die Basis des Rechtecks so, dass die letzte Textzeile gebunden wird. Wenn nur eine Textzeile enthalten ist, ändert **DrawText** die rechte Seite des Rechtecks so, dass es das letzte Zeichen in der Zeile umgibt. In beiden Fällen gibt **DrawText** die Höhe des formatierten Texts zurück, aber nicht den Text.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <dt>**DT \_ CENTER**</dt> </dl>             | Centert Text horizontal im Rechteck.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <dt>**DT \_ EXPANDTABS**</dt> </dl> | Erweitert Tabstoppzeichen. Die Standardanzahl von Zeichen pro Tabstopp beträgt acht.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <dt>**DT \_ LEFT**</dt> </dl>                   | Richtet Text links aus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <dt>**DT \_ NOCLIP**</dt> </dl>             | Zeichnet ohne Clipping. **DrawText** ist etwas schneller, wenn DT \_ NOCLIP verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <dt>**DT \_ RIGHT**</dt> </dl>                | Richtet Text rechts aus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <dt>**DT \_ RTLREADING**</dt> </dl> | Zeigt Text in der Leserichtung von rechts nach links für bidirektionalen Text an, wenn eine hebräische oder arabische Schriftart ausgewählt ist. Die Standardlese reihenfolge für den text-Text ist von links nach rechts.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <dt>**DT \_ SINGLELINE**</dt> </dl> | Zeigt nur Text in einer einzelnen Zeile an. Wagenrücklauf und Zeilenfeeds unterbricht die Zeile nicht.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <dt>**DT \_ TOP**</dt> </dl>                      | Der Text wird am anfang gerechtfertigt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <dt>**DT \_ VCENTER**</dt> </dl>          | Centert Text vertikal (nur eine Zeile).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <dt>**DT \_ WORDBREAK**</dt> </dl>    | Unterbricht Wörter. Zeilen werden automatisch zwischen Wörtern unterbrochen, wenn sich ein Wort über den Rand des Rechtecks erstreckt, das durch den pRect-Parameter angegeben wird. Eine Wagenrücklauf-/Zeilenfeedsequenz unterbricht auch die Zeile.<br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Farbe* \[ In\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

Farbe des Texts. Weitere Informationen finden Sie unter [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **INT**](../winprog/windows-data-types.md)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Höhe des Texts in logischen Einheiten. Wenn DT VCENTER oder DT BOTTOM angegeben ist, ist der Rückgabewert der Offset von pRect (von oben nach \_ \_ unten) des gezeichneten Texts. Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

Die Parameter dieser Methode sind denen der GDI [**DrawText-Funktion sehr**](/windows/win32/api/winuser/nf-winuser-drawtext) ähnlich.

Diese Methode unterstützt sowohl ANSI- als auch Unicode-Zeichenfolgen.

Diese Methode muss innerhalb einer [**BeginScene... aufgerufen werden.**](/windows/desktop/api) [**EndScene-Block.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) Die einzige Ausnahme ist, wenn eine Anwendung **DrawText** mit DT CALCRECT aufruft, um die Größe eines \_ bestimmten Textblocks zu berechnen.

Sofern nicht das DT NOCLIP-Format verwendet wird, schneide diese Methode den Text so ab, dass er nicht außerhalb des \_ angegebenen Rechtecks angezeigt wird. Es wird davon ausgegangen, dass alle Formatierungen mehrere Zeilen haben, es sei denn, das DT \_ SINGLELINE-Format ist angegeben.

Wenn die ausgewählte Schriftart zu groß für das Rechteck ist, versucht diese Methode nicht, eine kleinere Schriftart zu ersetzen.

Diese Methode unterstützt nur Schriftarten, deren Escape- und Ausrichtungsformat 0 (null) ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
