---
title: CB_FINDSTRING (Winuser.h)
description: Durchsucht das Listenfeld eines Kombinationsfelds nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt.
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- CB_FINDSTRING meldungssteuerelemente Windows
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
ms.openlocfilehash: 1af584e04a108c39a76a54c05c311d26e107c132d0c132e7b8fcc99a7cd7321b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089353"
---
# <a name="cb_findstring-message"></a>CB \_ FINDSTRING-Nachricht

Durchsucht das Listenfeld eines Kombinationsfelds nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index des Elements vor dem ersten zu durchsuchenden Element. Wenn die Suche den unteren Rand des Listenfelds erreicht, wird sie vom oberen Rand des Listenfelds zurück zu dem Element fortgesetzt, das durch den *wParam-Parameter angegeben* wird. Wenn *wParam* -1 ist, wird das gesamte Listenfeld von Anfang an durchsucht.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die auf NULL beendete Zeichenfolge, die die zu suchden Zeichen enthält. Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet, sodass diese Zeichenfolge eine beliebige Kombination aus Groß- und Kleinbuchstaben enthalten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der nullbasierte Index des übereinstimmenden Elements. Wenn die Suche nicht erfolgreich ist, ist dies CB \_ ERR.

## <a name="remarks"></a>Hinweise

Wenn Sie das Kombinationsfeld mit einem vom Besitzer gezeichneten Stil erstellen, aber ohne den [**CBS \_ HASSTRINGS-Stil,**](combo-box-styles.md) hängt die **CB \_ FINDSTRING-Meldung** davon ab, ob Ihre Anwendung den [**CBS \_ SORT-Stil verwendet.**](combo-box-styles.md) Wenn Sie den **CBS \_ SORT-Stil** verwenden, werden [**WM \_ COMPAREITEM-Nachrichten**](wm-compareitem.md) an den Besitzer des Kombinationsfelds gesendet, um zu bestimmen, welches Element der angegebenen Zeichenfolge entspricht. Wenn Sie nicht den **CBS \_ SORT-Stil** verwenden, sucht die **CB \_ FINDSTRING-Meldung** nach einem Listenelement, das dem Wert des *lParam-Parameters* entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

 





