---
title: LB_GETCARETINDEX (Winuser.h)
description: Ruft den Index des Elements ab, das den Fokus in einem Mehrfachauswahl-Listenfeld besitzt. Das Element kann ausgewählt oder nicht ausgewählt werden.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- LB_GETCARETINDEX meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74732bae571cdcba0cfe8096437bf681e7a339c5c0edb3f18d378ea610bdf8c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085540"
---
# <a name="lb_getcaretindex-message"></a>LB \_ GETCARETINDEX-Nachricht

Ruft den Index des Elements ab, das den Fokus in einem Mehrfachauswahl-Listenfeld besitzt. Das Element kann ausgewählt oder nicht ausgewählt werden.

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

Der Rückgabewert ist der nullbasierte Index des fokussierten Listenfeldelements oder 0, wenn kein Element den Fokus besitzt.

## <a name="remarks"></a>Hinweise

Diese Meldung kann auch verwendet werden, um den Index des Elements zu erhalten, das derzeit in einem Listenfeld mit nur einer Auswahl ausgewählt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB \_ SETCARETINDEX**](lb-setcaretindex.md)
</dt> </dl>

 

 





