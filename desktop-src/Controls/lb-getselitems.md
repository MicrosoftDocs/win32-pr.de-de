---
title: LB_GETSELITEMS Meldung (Winuser.h)
description: Füllt einen Puffer mit einem Array von ganzen Zahlen, die die Elementnummern ausgewählter Elemente in einem Listenfeld mit mehrfacher Auswahl angeben.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- LB_GETSELITEMS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a541c7efb0acb8d462cce42f0323393baff58e51d63e6a78a72a9d334c0eae81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085500"
---
# <a name="lb_getselitems-message"></a>LB \_ GETSELITEMS-Nachricht

Füllt einen Puffer mit einem Array von ganzen Zahlen, die die Elementnummern ausgewählter Elemente in einem Listenfeld mit mehrfacher Auswahl angeben.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die maximale Anzahl ausgewählter Elemente, deren Elementnummern im Puffer platziert werden sollen.

Windows 95/Windows 98/Windows Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt. Das bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, ist die Gesamtgröße der Elemente in einem Listenfeld in Byte nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der groß genug für die Anzahl der durch den *wParam-Parameter* angegebenen ganzen Zahlen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Anzahl der Elemente, die im Puffer platziert werden. Wenn das Listenfeld ein Listenfeld mit nur einer Auswahl ist, lautet der Rückgabewert LB \_ ERR.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB \_ GETSELCOUNT**](lb-getselcount.md)
</dt> </dl>

 

 





