---
description: Zeichnet formatierten Text. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: ID3DXFont::D rawtext-Methode (D3dx9core. h)
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
ms.openlocfilehash: 96636c372ee48d516286935f03d80b8e9815ffc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219506"
---
# <a name="id3dxfontdrawtext-method"></a>ID3DXFont::D rawtext-Methode

Zeichnet formatierten Text. Diese Methode unterstützt ANSI-und Unicode-Zeichen folgen.

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

*psprite* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXSPRITE**](id3dxsprite.md)**

Zeiger auf ein [**ID3DXSprite**](id3dxsprite.md) -Objekt, das die Zeichenfolge enthält. Kann **null** sein. in diesem Fall wird die Zeichenfolge von Direct3D mit einem eigenen Sprite-Objekt dargestellt. Um die Effizienz zu verbessern, sollte ein Sprite-Objekt angegeben werden, wenn **DrawText** mehrmals in einer Zeile aufgerufen werden soll.

</dd> <dt>

*pstring* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die gezeichnet werden soll. Wenn der count-Parameter-1 ist, muss die Zeichenfolge mit Null beendet werden.

</dd> <dt>

*Anzahl* \[ in\]
</dt> <dd>

Typ: **[ **int**](../winprog/windows-data-types.md)**

Gibt die Anzahl von Zeichen in der Zeichenfolge an. Wenn count den Wert-1 hat, wird angenommen, dass der pstring-Parameter ein Zeiger auf eine auf NULL endende Zeichenfolge ist, und **DrawText** berechnet automatisch die Zeichen Anzahl.

</dd> <dt>

*vorab ausführen* \[ in\]
</dt> <dd>

Typ: **[ **lprect**](../winprog/windows-data-types.md)**

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das Rechteck in logischen Koordinaten enthält, in dem der Text formatiert werden soll. Der Koordinaten Wert der rechten Seite des Rechtecks muss größer sein als der Wert der linken Seite. Ebenso muss der Koordinaten Wert des unteren Werts größer als der obere Wert sein.

</dd> <dt>

*Format* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt die Methode zum Formatieren des Texts an. Dabei kann es sich um eine beliebige Kombination der folgenden Werte handeln:



| Wert                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <dt>**DT \_ unten**</dt> </dl>             | Rechtfertigt den Text am unteren Rand des Rechtecks. Dieser Wert muss mit dt \_ SingleLine kombiniert werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <dt>**DT \_ calcrect**</dt> </dl>       | Bestimmt die Breite und Höhe des Rechtecks. Wenn mehrere Textzeilen vorhanden sind, verwendet **DrawText** die Breite des Rechtecks, auf das der prect-Parameter zeigt, und erweitert die Basis des Rechtecks, um die letzte Textzeile zu binden. Wenn nur eine Textzeile vorhanden ist, ändert **DrawText** die Rechte Seite des Rechtecks, sodass es das letzte Zeichen in der Zeile umschließt. In beiden Fällen gibt **DrawText** die Höhe des formatierten Texts zurück, zeichnet den Text jedoch nicht.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <dt>**DT \_ Center**</dt> </dl>             | Zentriert den Text horizontal im Rechteck.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <dt>**DT- \_ ExpandTabs**</dt> </dl> | Erweitert Tabstoppzeichen. Die Standardanzahl von Zeichen pro Tabstopp beträgt acht.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <dt>**DT \_ Links**</dt> </dl>                   | Richtet den Text auf der linken Seite aus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <dt>**DT \_ NoClip**</dt> </dl>             | Zeichnet ohne Clipping. **DrawText** ist etwas schneller, wenn dt \_ NoClip verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <dt>**\_rechter dt**</dt> </dl>                | Richtet den Text rechts bünne aus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <dt>**DT \_ RtlReading**</dt> </dl> | Zeigt Text in der Lesefolge von rechts nach Links für bidirektionalen Text an, wenn eine hebräische oder arabische Schriftart ausgewählt wird. Die Standard Lesereihenfolge für den gesamten Text ist von links nach rechts.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <dt>**DT \_ SingleLine**</dt> </dl> | Zeigt nur Text in einer einzelnen Zeile an. Wagen Rückläufe und Zeilen Vorschübe unterbrechen die Linie nicht.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <dt>**DT \_ Top**</dt> </dl>                      | Text mit oberster Rechtfertigung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <dt>**DT \_ vCenter**</dt> </dl>          | Zentriert Text vertikal (nur einzeilige Linie).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <dt>**DT- \_ WordBreak**</dt> </dl>    | Umbricht Wörter. Zeilen werden zwischen Wörtern automatisch getrennt, wenn sich ein Wort hinter dem Rand des Rechtecks ausdehnen würde, das durch den prect-Parameter angegeben wird. Eine Wagen Rücklauf-/Zeilenvorschub Sequenz unterbricht ebenfalls die Zeile.<br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Farbe* \[ in\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

Textfarbe. Weitere Informationen finden Sie unter [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **int**](../winprog/windows-data-types.md)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert die Höhe des Texts in logischen Einheiten. Wenn dt \_ vCenter oder dt \_ Bottom angegeben ist, ist der Rückgabewert der Offset von vorab (oben nach unten) des gezeichneten Texts. Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

Die Parameter dieser Methode ähneln denen der GDI- [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) -Funktion.

Diese Methode unterstützt sowohl ANSI-als auch Unicode-Zeichen folgen.

Diese Methode muss in einer [**BeginScene**](/windows/desktop/api) aufgerufen werden... [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) -Block. Die einzige Ausnahme ist, wenn eine Anwendung **DrawText** mit dt \_ calcrect aufruft, um die Größe eines bestimmten texttexts zu berechnen.

Wenn das DT \_ NoClip-Format nicht verwendet wird, wird der Text von dieser Methode so geklammert, dass er nicht außerhalb des angegebenen Rechtecks angezeigt wird. Es wird davon ausgegangen, dass die gesamte Formatierung mehrere Zeilen umfasst, es sei denn, das DT- \_ SingleLine-Format

Wenn die ausgewählte Schriftart für das Rechteck zu groß ist, versucht diese Methode nicht, eine kleinere Schriftart zu ersetzen.

Diese Methode unterstützt nur Schriftarten, deren escapesin und Ausrichtung gleich NULL sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
