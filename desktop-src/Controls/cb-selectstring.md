---
title: CB_SELECTSTRING Meldung (Winuser. h)
description: Durchsucht die Liste eines Kombinations Felds nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt. Wenn ein übereinstimmendes Element gefunden wird, wird es ausgewählt und in das Bearbeitungs Steuerelement kopiert.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- Windows-Steuerelemente für CB_SELECTSTRING Meldung
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
ms.openlocfilehash: 2913b95c02cdfd3c7a9c96a8652038a04d8fde8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040593"
---
# <a name="cb_selectstring-message"></a>CB- \_ SelectString-Nachricht

Durchsucht die Liste eines Kombinations Felds nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt. Wenn ein übereinstimmendes Element gefunden wird, wird es ausgewählt und in das Bearbeitungs Steuerelement kopiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Elements vor dem ersten zu durchsuchenden Element. Wenn die Suche das Ende der Liste erreicht, wird Sie von der Spitze der Liste zurück zu dem durch den *wParam* -Parameter angegebenen Element weiter angezeigt. Wenn *wParam* den Wert-1 hat, wird die gesamte Liste von Anfang an durchsucht.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die NULL-terminierte Zeichenfolge, die die zu durchsuchenden Zeichen enthält. Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet, sodass diese Zeichenfolge eine beliebige Kombination von Groß-und Kleinbuchstaben enthalten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Zeichenfolge gefunden wird, ist der Rückgabewert der Index des ausgewählten Elements. Wenn die Suche nicht erfolgreich ist, ist der Rückgabewert CB \_ Err, und die aktuelle Auswahl wird nicht geändert.

## <a name="remarks"></a>Bemerkungen

Eine Zeichenfolge wird nur ausgewählt, wenn die Zeichen vom Startpunkt den Zeichen in der Präfix Zeichenfolge entsprechen.

Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, hängt die **CB- \_ SelectString** -Nachricht davon ab, ob Sie das CBS- [**\_ Sortier**](combo-box-styles.md) Format verwenden. Wenn der **CBS- \_ Sortier** Stil verwendet wird, sendet das System [**WM \_ compareitem**](wm-compareitem.md) -Nachrichten an den Besitzer des Kombinations Felds, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt. Wenn Sie den **sortierungstil \_ CBS** nicht verwenden, versucht **CB \_ SelectString** , den **DWORD** -Wert mit dem Wert des *LPARAM* -Parameters abzugleichen.

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

[**CB- \_ FindString**](cb-findstring.md)
</dt> <dt>

[**CB- \_ FindStringExact**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ setcurrsel**](cb-setcursel.md)
</dt> <dt>

[**WM- \_ compareitem**](wm-compareitem.md)
</dt> </dl>

 

 





