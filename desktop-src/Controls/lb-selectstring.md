---
title: LB_SELECTSTRING (Winuser.h)
description: Durchsucht ein Listenfeld nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt. Wenn ein übereinstimmendes Element gefunden wird, wird das Element ausgewählt.
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- LB_SELECTSTRING meldungssteuerelemente Windows
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
ms.openlocfilehash: 848a0935a1ca4d3ce717fecae3de76f57e36091ba084041aa9d012d6318a269a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434080"
---
# <a name="lb_selectstring-message"></a>LB \_ SELECTSTRING-Meldung

Durchsucht ein Listenfeld nach einem Element, das mit den Zeichen in einer angegebenen Zeichenfolge beginnt. Wenn ein übereinstimmendes Element gefunden wird, wird das Element ausgewählt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index des Elements vor dem ersten zu durchsuchenden Element. Wenn die Suche den unteren Rand des Listenfelds erreicht, wird sie vom oberen Rand des Listenfelds zurück zu dem Element fortgesetzt, das durch den *wParam-Parameter angegeben* wird. Wenn *wParam* -1 ist, wird das gesamte Listenfeld von Anfang an durchsucht.

Windows 95/Windows 98/Windows Edition (Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, ist die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die nullbeendte Zeichenfolge, die das Präfix enthält, nach dem gesucht werden soll. Die Suche ist unabhängig von der Groß-/Kleinschreibung, sodass diese Zeichenfolge eine beliebige Kombination aus Groß- und Kleinbuchstaben enthalten kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Suche erfolgreich ist, ist der Rückgabewert der Index des ausgewählten Elements. Wenn die Suche nicht erfolgreich ist, ist der Rückgabewert LB \_ ERR, und die aktuelle Auswahl wird nicht geändert.

## <a name="remarks"></a>Hinweise

Das Listenfeld wird bei Bedarf gescrollt, um das ausgewählte Element in die Ansicht zu bringen.

Verwenden Sie diese Meldung nicht mit einem Listenfeld, das über die [**Formate LBS \_ MULTIPLESEL**](list-box-styles.md) oder [**LBS \_ EXTENDEDSEL**](list-box-styles.md) verfügt.

Ein Element wird nur ausgewählt, wenn seine Anfangszeichen vom Anfangspunkt mit den Zeichen in der vom *lParam-Parameter angegebenen Zeichenfolge* übereinstimmen.

Wenn das Listenfeld den vom Besitzer gezeichneten Stil hat, aber nicht den [**LBS \_ HASSTRINGS-Stil,**](list-box-styles.md) hängt die von **LB \_ SELECTSTRING** ergriffene Aktion davon ab, ob der [**LBS \_ SORT-Stil verwendet**](list-box-styles.md) wird. Wenn **LBS \_ SORT verwendet** wird, sendet das System WM [**\_ COMPAREITEM-Nachrichten**](wm-compareitem.md) an den Besitzer des Listenfelds, um zu bestimmen, welches Element der angegebenen Zeichenfolge entspricht. Andernfalls versucht **LB \_ SELECTSTRING,** ein Element zu finden, das über einen long-Wert verfügt (angegeben als *lParam-Parameter* der [**LB \_ ADDSTRING-**](lb-addstring.md) oder [**LB \_ INSERTSTRING-Meldung),**](lb-insertstring.md) der mit dem *lParam-Parameter* entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ FINDSTRING**](lb-findstring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> </dl>

 

 





