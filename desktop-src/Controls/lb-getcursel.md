---
title: LB_GETCURSEL (Winuser.h)
description: Ruft den Index des aktuell ausgewählten Elements in einem Listenfeld mit nur einer Auswahl ab( sofern verfügbar).
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- LB_GETCURSEL message Windows Controls
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67a060669d48a9ab020540c78ece395504c9f0b7e36807e3ac59daf216ea395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085520"
---
# <a name="lb_getcursel-message"></a>LB \_ GETCURSEL-Nachricht

Ruft den Index des aktuell ausgewählten Elements in einem Listenfeld mit nur einer Auswahl ab( sofern verfügbar).

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

In einem Listenfeld mit nur einer Auswahl ist der Rückgabewert der nullbasierte Index des aktuell ausgewählten Elements. Wenn keine Auswahl getroffen wird, ist der Rückgabewert LB \_ ERR.

## <a name="remarks"></a>Hinweise

Um die Indizes der ausgewählten Elemente in einem Mehrfachauswahllistenfeld abzurufen, verwenden Sie die [**LB \_ GETSELITEMS-Meldung.**](lb-getselitems.md) Um zu bestimmen, ob das Element mit dem Fokusrechteck in einem Mehrfachauswahllistenfeld ausgewählt ist, verwenden Sie die [**LB \_ GETSEL-Meldung.**](lb-getsel.md)

Wenn es an ein Mehrfachauswahl-Listenfeld gesendet wird, gibt **LB \_ GETCURSEL** den Index des Elements zurück, das über das Fokusrechteck verfügt. Wenn keine Elemente ausgewählt sind, wird 0 (null) zurückgegeben.

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

[**LB \_ GETCARETINDEX**](lb-getcaretindex.md)
</dt> <dt>

[**LB \_ GETSEL**](lb-getsel.md)
</dt> <dt>

[**LB \_ GETSELITEMS**](lb-getselitems.md)
</dt> <dt>

[**LB \_ SETCURSEL**](lb-setcursel.md)
</dt> </dl>

 

 





