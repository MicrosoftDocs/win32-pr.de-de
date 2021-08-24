---
title: WM_POINTERROUTEDRELEASED-Nachricht
description: Wird an alle Prozesse gesendet (für prozessübergreifende Verkettung über AddContentWithCrossProcessChaining konfiguriert und verarbeitet derzeit keine Zeigereingaben), die jemals einer bestimmten Zeiger-ID zugeordnet sind, wenn eine WM_POINTERUP-Nachricht im aktuellen Prozess empfangen wird.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- 'WM_POINTERROUTEDRELEASED-Nachricht: Eingabemeldungen und Benachrichtigungen'
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 318134779d94824daef0b05903f45121665892fbcafbeb48589ef150f324d2b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611290"
---
# <a name="wm_pointerroutedreleased-message"></a>WM_POINTERROUTEDRELEASED-Nachricht

Wird an alle Prozesse gesendet (für prozessübergreifende Verkettung über [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) konfiguriert und verarbeitet derzeit keine Zeigereingaben), die jemals einer bestimmten Zeiger-ID zugeordnet sind, wenn eine [**WM_POINTERUP-Nachricht**](wm-pointerup.md) im aktuellen Prozess empfangen wird.


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

NULL

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meldungen](messages.md)
</dt> </dl>

 

