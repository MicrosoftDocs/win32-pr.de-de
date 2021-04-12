---
title: CB_FINDSTRINGEXACT Meldung (Winuser. h)
description: Sucht die erste Listenfeld Zeichenfolge in einem Kombinations Feld, das mit der im lParam-Parameter angegebenen Zeichenfolge übereinstimmt.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- Windows-Steuerelemente für CB_FINDSTRINGEXACT Meldung
topic_type:
- apiref
api_name:
- CB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f70c56a5f13fffa8dfedebd13f9830c62ef941cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519343"
---
# <a name="cb_findstringexact-message"></a>CB- \_ FindStringExact-Nachricht

Sucht die erste Listenfeld Zeichenfolge in einem Kombinations Feld, das mit der im *LPARAM* -Parameter angegebenen Zeichenfolge übereinstimmt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Elements vor dem ersten zu durchsuchenden Element. Wenn die Suche das Ende des Listen Felds erreicht, wird Sie von der obersten Position des Listen Felds zurück zu dem durch den *wParam* -Parameter angegebenen Element weiter angezeigt. Wenn *wParam* den Wert 1 hat, wird das gesamte Listenfeld von Anfang an durchsucht.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die NULL-terminierte Zeichenfolge, nach der gesucht werden soll. Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet, sodass diese Zeichenfolge eine beliebige Kombination von Groß-und Kleinbuchstaben enthalten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der null basierte Index des übereinstimmenden Elements. Wenn die Suche nicht erfolgreich ist, ist Sie CB \_ Err.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nur erfolgreich, wenn die angegebene Zeichenfolge und ein Kombinations Feld Element dieselbe Länge (außer dem abschließenden NULL-Zeichen) und denselben Zeichen aufweisen.

Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, hängt die Funktion der **CB- \_ FindStringExact** -Nachricht davon ab, ob die Anwendung den [**CBS- \_ Sortier**](combo-box-styles.md) Stil verwendet. Bei Verwendung des **CBS- \_ Sortier** Stils werden [**WM \_ compareitem**](wm-compareitem.md) -Nachrichten an den Besitzer des Kombinations Felds gesendet, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt. Wenn Sie den **Sortierungstyp \_ CBS** nicht verwenden, sucht die **CB \_ FindStringExact** -Nachricht nach einem Listenelement, das mit dem Wert des *LPARAM* -Parameters übereinstimmt.

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

[**CB- \_ SelectString**](cb-selectstring.md)
</dt> <dt>

[**WM- \_ compareitem**](wm-compareitem.md)
</dt> </dl>

 

 





