---
title: RB_MOVEBAND (Commctrl.h)
description: Verschiebt ein Band von einem Index in einen anderen.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- RB_MOVEBAND meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab45f63b46b8bb883ef9f1fd8708f915dba2a6860ef2f6fabb09e2b00bd8fe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798540"
---
# <a name="rb_moveband-message"></a>RB \_ MOVEBAND-Nachricht

Verschiebt ein Band von einem Index in einen anderen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des zu verschobenen Bandes.

</dd> <dt>

*lParam* 
</dt> <dd>

Nullbasierter Index der neuen Bandposition.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Diese Meldung ändert wahrscheinlich den Index anderer Bänder im Rebar-Steuerelement. Wenn ein Band von Index 6 in Index 0 verschoben wird, wird der Index aller Bänder dazwischen um eins erhöht.

*lParam* darf nie größer als die Anzahl der Bänder minus eins sein. Die Anzahl der Bänder kann mit der [**RB \_ GETBANDCOUNT-Nachricht ermittelt**](rb-getbandcount.md) werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





