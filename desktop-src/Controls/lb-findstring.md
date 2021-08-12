---
title: LB_FINDSTRING Nachricht (Winuser.h)
description: Sucht die erste Zeichenfolge in einem Listenfeld, das mit der angegebenen Zeichenfolge beginnt.
ms.assetid: 1b7f25a7-0892-4d12-b3e3-21180d9ddfb1
keywords:
- LB_FINDSTRING Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a4eb2abbff27c6bde6a4bb44d0faa192ca75229be657bd787aa437b243cd59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671303"
---
# <a name="lb_findstring-message"></a>LB \_ FINDSTRING-Nachricht

Sucht die erste Zeichenfolge in einem Listenfeld, das mit der angegebenen Zeichenfolge beginnt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index des Elements vor dem ersten zu durchsuchenden Element. Wenn die Suche den unteren Rand des Listenfelds erreicht, wird die Suche vom oberen Rand des Listenfelds zurück zu dem durch den *wParam-Parameter* angegebenen Element fortgesetzt. Wenn *wParam* -1 ist, wird das gesamte Listenfeld von Anfang an durchsucht.

Windows 95/Windows 98/Windows Edition (Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt. Das bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, ist die Gesamtgröße der Elemente in einem Listenfeld in Byte nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die auf NULL endende Zeichenfolge, die die Zeichenfolge enthält, nach der gesucht werden soll. Die Suche ist unabhängig von Groß-/Kleinschreibung, sodass diese Zeichenfolge eine beliebige Kombination aus Groß- und Kleinbuchstaben enthalten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Index des übereinstimmenden Elements oder LB \_ ERR, wenn die Suche nicht erfolgreich war.

## <a name="remarks"></a>Hinweise

Wenn das Listenfeld den vom Besitzer gezeichneten Stil, aber nicht den [**LBS \_ HASSTRINGS-Stil**](list-box-styles.md) aufwies, hängt die von **LB \_ FINDSTRING** ausgeführte Aktion davon ab, ob der [**LBS \_ SORT-Stil**](list-box-styles.md) verwendet wird. Wenn **LBS \_ SORT** verwendet wird, sendet das System [**WM \_ COMPAREITEM-Nachrichten**](wm-compareitem.md) an den Besitzer des Listenfelds, um zu bestimmen, welches Element mit der angegebenen Zeichenfolge übereinstimmt. Andernfalls versucht **LB \_ FINDSTRING,** ein Element zu finden, das über einen long-Wert verfügt (bereitgestellt als *lParam-Parameter* der [**LB \_ ADDSTRING-**](lb-addstring.md) oder [**LB \_ INSERTSTRING-Nachricht),**](lb-insertstring.md) der mit dem *lParam-Parameter* übereinstimmt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LB \_ FINDSTRINGEXACT**](lb-findstringexact.md)
</dt> </dl>

 

 





