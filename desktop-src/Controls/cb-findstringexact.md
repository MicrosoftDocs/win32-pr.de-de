---
title: CB_FINDSTRINGEXACT Meldung (Winuser.h)
description: Sucht die erste Listenfeldzeichenfolge in einem Kombinationsfeld, das mit der im lParam-Parameter angegebenen Zeichenfolge übereinstimmt.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- CB_FINDSTRINGEXACT Meldung Windows-Steuerelemente
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
ms.openlocfilehash: 7f99d85c7dddb95bdfb168443d6f977c22273a87
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327175"
---
# <a name="cb_findstringexact-message"></a>CB \_ FINDSTRINGEXACT-Nachricht

Sucht die erste Listenfeldzeichenfolge in einem Kombinationsfeld, das mit der im *lParam-Parameter* angegebenen Zeichenfolge übereinstimmt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index des Elements vor dem ersten zu durchsuchenden Element. Wenn die Suche den unteren Rand des Listenfelds erreicht, wird sie vom oberen Rand des Listenfelds zurück zu dem durch den *wParam-Parameter* angegebenen Element fortgesetzt. Wenn *wParam* -1 ist, wird das gesamte Listenfeld von Anfang an durchsucht.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die auf NULL endende Zeichenfolge, nach der gesucht werden soll. Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet, sodass diese Zeichenfolge eine beliebige Kombination aus Groß- und Kleinbuchstaben enthalten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der nullbasierte Index des übereinstimmenden Elements. Wenn die Suche nicht erfolgreich ist, handelt es sich um CB \_ ERR.

## <a name="remarks"></a>Hinweise

Diese Funktion ist nur erfolgreich, wenn die angegebene Zeichenfolge und ein Kombinationsfeldelement dieselbe Länge (mit Ausnahme des abschließenden NULL-Zeichens) und dieselben Zeichen aufweisen.

Wenn Sie das Kombinationsfeld mit einem vom Besitzer gezeichneten Stil erstellen, jedoch ohne den [**CBS \_ HASSTRINGS-Stil,**](combo-box-styles.md) hängt die Funktionalität der **CB \_ FINDSTRINGEXACT-Nachricht** davon ab, ob Ihre Anwendung den [**CBS \_ SORT-Stil**](combo-box-styles.md) verwendet. Wenn Sie den **CBS \_ SORT-Stil** verwenden, werden [**WM \_ COMPAREITEM-Meldungen**](wm-compareitem.md) an den Besitzer des Kombinationsfelds gesendet, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt. Wenn Sie den **CBS \_ SORT-Stil** nicht verwenden, sucht die **CB \_ FINDSTRINGEXACT-Nachricht** nach einem Listenelement, das dem Wert des *lParam-Parameters* entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (windows.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Verweis**
</dt> <dt>

[**CB \_ FINDSTRING**](cb-findstring.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

 





