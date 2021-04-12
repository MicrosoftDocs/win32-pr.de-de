---
title: CB_FINDSTRING Meldung (Winuser. h)
description: Durchsucht das Listenfeld eines Kombinations Felds nach einem Element, beginnend mit den Zeichen in einer angegebenen Zeichenfolge.
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- Windows-Steuerelemente für CB_FINDSTRING Meldung
topic_type:
- apiref
api_name:
- CB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 295300790a27a956bce953e4e293c07c22ec0d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103631"
---
# <a name="cb_findstring-message"></a>CB- \_ FindString-Nachricht

Durchsucht das Listenfeld eines Kombinations Felds nach einem Element, beginnend mit den Zeichen in einer angegebenen Zeichenfolge.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Elements vor dem ersten zu durchsuchenden Element. Wenn die Suche das Ende des Listen Felds erreicht, wird Sie von der obersten Position des Listen Felds zurück zu dem durch den *wParam* -Parameter angegebenen Element weiter angezeigt. Wenn *wParam* den Wert-1 hat, wird das gesamte Listenfeld von Anfang an durchsucht.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die NULL-terminierte Zeichenfolge, die die zu durchsuchenden Zeichen enthält. Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet, sodass diese Zeichenfolge eine beliebige Kombination von Groß-und Kleinbuchstaben enthalten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der null basierte Index des übereinstimmenden Elements. Wenn die Suche nicht erfolgreich ist, ist Sie CB \_ Err.

## <a name="remarks"></a>Bemerkungen

Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, hängt die **CB- \_ FindString** -Nachricht davon ab, ob die Anwendung den CBS- [**\_ Sortier**](combo-box-styles.md) Stil verwendet. Bei Verwendung des **CBS- \_ Sortier** Stils werden [**WM \_ compareitem**](wm-compareitem.md) -Nachrichten an den Besitzer des Kombinations Felds gesendet, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt. Wenn Sie den **Sortierungstyp \_ CBS** nicht verwenden, sucht die **CB- \_ FindString** -Nachricht nach einem Listenelement, das mit dem Wert des *LPARAM* -Parameters übereinstimmt.

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

[**CB- \_ FindStringExact**](cb-findstringexact.md)
</dt> <dt>

[**CB- \_ SelectString**](cb-selectstring.md)
</dt> <dt>

[**CB \_ setcurrsel**](cb-setcursel.md)
</dt> <dt>

[**WM- \_ compareitem**](wm-compareitem.md)
</dt> </dl>

 

 





