---
title: LB_INITSTORAGE (Winuser.h)
description: Reserviert Arbeitsspeicher zum Speichern von Listenfeldelementen. Diese Meldung wird verwendet, bevor eine Anwendung einem Listenfeld eine große Anzahl von Elementen hinzufügt.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- LB_INITSTORAGE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe873244358bf171c3fcedc994facd36e194edf38e0ee0442f12556cc4342514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544270"
---
# <a name="lb_initstorage-message"></a>LB \_ INITSTORAGE-Nachricht

Reserviert Arbeitsspeicher zum Speichern von Listenfeldelementen. Diese Meldung wird verwendet, bevor eine Anwendung einem Listenfeld eine große Anzahl von Elementen hinzufügt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der hinzuzufügenden Elemente.

Windows 95/Windows 98/Windows Edition (Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, ist die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Menge des Arbeitsspeichers in Byte, der elementzeichenfolgen zuteilen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **LB\_INITSTORAGE** messages.

Wenn die Meldung fehlschlägt, ist der Rückgabewert LB \_ ERRSPACE.

Microsoft Windows NT 4.0: Diese Meldung weist nicht die angegebene Arbeitsspeichermenge zu. es wird jedoch immer der im *wParam-Parameter angegebene Wert* zurückgegeben.

## <a name="remarks"></a>Hinweise

Die **LB \_ INITSTORAGE-Nachricht** beschleunigt die Initialisierung von Listenfeldern mit einer großen Anzahl von Elementen (mehr als 100). Die angegebene Arbeitsspeichermenge wird reserviert, sodass nachfolgende [**LB \_ ADDSTRING-,**](lb-addstring.md) [**LB \_ INSERTSTRING-,**](lb-insertstring.md) [**LB \_ DIR-**](lb-dir.md)und [**LB \_ ADDFILE-Nachrichten**](lb-addfile.md) so kurz wie möglich dauern. Sie können Schätzungen für die *Parameter wParam* und *lParam* verwenden. Wenn Sie überschätzen, wird der zusätzliche Arbeitsspeicher zugeordnet. Wenn Sie sich nicht sicher sind, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.

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

[**LB \_ ADDFILE**](lb-addfile.md)
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ DIR**](lb-dir.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> </dl>

 

 





