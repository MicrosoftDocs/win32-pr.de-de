---
title: LB_FINDSTRINGEXACT Meldung (Winuser. h)
description: Sucht die erste Listenfeld Zeichenfolge, die exakt mit der angegebenen Zeichenfolge übereinstimmt
ms.assetid: 9bfe21af-626d-4416-aa20-65c425bd99af
keywords:
- Windows-Steuerelemente für LB_FINDSTRINGEXACT Meldung
topic_type:
- apiref
api_name:
- LB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b4f817eabae95c6021647b0c47926b2163722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040956"
---
# <a name="lb_findstringexact-message"></a>LB- \_ FindStringExact-Nachricht

Sucht die erste Listenfeld Zeichenfolge, die exakt mit der angegebenen Zeichenfolge übereinstimmt

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index des Elements vor dem ersten zu durchsuchenden Element. Wenn die Suche das Ende des Listen Felds erreicht, wird die Suche vom oberen Rand des Listen Felds zurück zu dem durch den *wParam* -Parameter angegebenen Element fortgesetzt. Wenn *wParam* den Wert-1 hat, wird das gesamte Listenfeld von Anfang an durchsucht.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die NULL-terminierte Zeichenfolge, nach der gesucht werden soll. Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet, sodass diese Zeichenfolge eine beliebige Kombination von Groß-und Kleinbuchstaben enthalten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der null basierte Index des übereinstimmenden Elements oder der LB- \_ Err, wenn die Suche nicht erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nur erfolgreich, wenn die angegebene Zeichenfolge und ein Listenfeld Element dieselbe Länge aufweisen (mit Ausnahme von Null am Ende der angegebenen Zeichenfolge) und genau die gleichen Zeichen aufweisen.

Wenn im Listenfeld der vom Besitzer gezeichnete Stil, jedoch nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, hängt die von **lb \_ FindStringExact** ausgeführte Aktion davon ab, ob der [**lbs- \_ Sortier**](list-box-styles.md) Stil verwendet wird. Wenn **lbs \_ Sort** verwendet wird, sendet das System [**WM \_ compareitem**](wm-compareitem.md) -Nachrichten an den Listenfeld Besitzer, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt. Andernfalls versucht **lb \_ FindStringExact** , ein Element zu finden, das über einen Long-Wert verfügt (angegeben als *LPARAM* -Parameter der [**lb \_ AddString**](lb-addstring.md) -oder [**lb \_ InsertString**](lb-insertstring.md) -Nachricht), der mit dem *LPARAM* -Parameter übereinstimmt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB- \_ FindString**](lb-findstring.md)
</dt> </dl>

 

 





