---
title: CB_SELECTSTRING Meldung (Winuser.h)
description: Durchsucht die Liste eines Kombinationsfelds nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt. Wenn ein übereinstimmendes Element gefunden wird, wird es ausgewählt und in das Bearbeitungssteuerelement kopiert.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- CB_SELECTSTRING Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- CB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bedef20646664e37405c97a97f9e49147cad8acc08c05e33172e44a34298f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019968"
---
# <a name="cb_selectstring-message"></a>CB \_ SELECTSTRING-Nachricht

Durchsucht die Liste eines Kombinationsfelds nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt. Wenn ein übereinstimmendes Element gefunden wird, wird es ausgewählt und in das Bearbeitungssteuerelement kopiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index des Elements vor dem ersten zu durchsuchenden Element. Wenn die Suche am unteren Rand der Liste eingeht, wird sie vom Anfang der Liste zurück zu dem element fortgesetzt, das durch den *wParam-Parameter* angegeben wird. Wenn *wParam* -1 ist, wird die gesamte Liste von Anfang an durchsucht.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die auf NULL endende Zeichenfolge, die die Zeichen enthält, nach denen gesucht werden soll. Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet, sodass diese Zeichenfolge eine beliebige Kombination aus Groß- und Kleinbuchstaben enthalten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Zeichenfolge gefunden wird, ist der Rückgabewert der Index des ausgewählten Elements. Wenn die Suche nicht erfolgreich ist, lautet der Rückgabewert CB \_ ERR, und die aktuelle Auswahl wird nicht geändert.

## <a name="remarks"></a>Hinweise

Eine Zeichenfolge wird nur ausgewählt, wenn die Zeichen vom Anfangspunkt mit den Zeichen in der Präfixzeichenfolge übereinstimmen.

Wenn Sie das Kombinationsfeld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ HASSTRINGS-Stil**](combo-box-styles.md) erstellen, hängt die **CB \_ SELECTSTRING-Nachricht** davon ab, ob Sie den [**CBS \_ SORT-Stil**](combo-box-styles.md) verwenden. Wenn der **CBS \_ SORT-Stil** verwendet wird, sendet das System [**WM \_ COMPAREITEM-Nachrichten**](wm-compareitem.md) an den Besitzer des Kombinationsfelds, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt. Wenn Sie den **CBS \_ SORT-Stil** nicht verwenden, versucht **CB \_ SELECTSTRING,** den **DWORD-Wert** mit dem Wert des *lParam-Parameters* abzugleichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ FINDSTRING**](cb-findstring.md)
</dt> <dt>

[**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

 





