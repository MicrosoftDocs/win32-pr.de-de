---
title: LB_SELECTSTRING Meldung (Winuser. h)
description: Durchsucht ein Listenfeld nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt. Wenn ein übereinstimmendes Element gefunden wird, wird das Element ausgewählt.
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- Windows-Steuerelemente für LB_SELECTSTRING Meldung
topic_type:
- apiref
api_name:
- LB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5963ea6530038e17bc7f23d9ab66eba14ca0b05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478549"
---
# <a name="lb_selectstring-message"></a>LB- \_ SelectString-Nachricht

Durchsucht ein Listenfeld nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt. Wenn ein übereinstimmendes Element gefunden wird, wird das Element ausgewählt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index des Elements vor dem ersten zu durchsuchenden Element. Wenn die Suche das Ende des Listen Felds erreicht, wird Sie von der obersten Position des Listen Felds zurück zu dem durch den *wParam* -Parameter angegebenen Element weiter angezeigt. Wenn *wParam* den Wert-1 hat, wird das gesamte Listenfeld von Anfang an durchsucht.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die NULL-terminierte Zeichenfolge, die das Präfix enthält, nach dem gesucht werden soll. Die Suche erfolgt unabhängig von der Groß-/Kleinschreibung, sodass diese Zeichenfolge eine beliebige Kombination von Groß-und Kleinbuchstaben enthalten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Suche erfolgreich ist, ist der Rückgabewert der Index des ausgewählten Elements. Wenn die Suche nicht erfolgreich ist, lautet der Rückgabewert "lb err", \_ und die aktuelle Auswahl wird nicht geändert.

## <a name="remarks"></a>Bemerkungen

Das Listenfeld wird ggf. mit einem Bildlauf ausgeführt, um das ausgewählte Element in der Ansicht anzuzeigen.

Verwenden Sie diese Meldung nicht mit einem Listenfeld, das die " [**lbs \_ multiplesel**](list-box-styles.md) "-oder " [**lbs \_ extendedsel**](list-box-styles.md) "-Stile aufweist.

Ein Element wird nur ausgewählt, wenn die ursprünglichen Zeichen vom Startpunkt den Zeichen in der durch den *LPARAM* -Parameter angegebenen Zeichenfolge entsprechen.

Wenn im Listenfeld der vom Besitzer gezeichnete Stil, jedoch nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, hängt die von **lb \_ SelectString** ausgeführte Aktion davon ab, ob der [**lbs- \_ Sortier**](list-box-styles.md) Stil verwendet wird. Wenn **lbs \_ Sort** verwendet wird, sendet das System [**WM \_ compareitem**](wm-compareitem.md) -Nachrichten an den Listenfeld Besitzer, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt. Andernfalls versucht **lb \_ SelectString** , ein Element zu finden, das über einen Long-Wert verfügt (angegeben als *LPARAM* -Parameter der [**lb \_ AddString**](lb-addstring.md) -oder [**lb \_ InsertString**](lb-insertstring.md) -Nachricht), der mit dem *LPARAM* -Parameter übereinstimmt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**LB- \_ AddString**](lb-addstring.md)
</dt> <dt>

[**LB- \_ FindString**](lb-findstring.md)
</dt> <dt>

[**LB- \_ InsertString**](lb-insertstring.md)
</dt> </dl>

 

 





