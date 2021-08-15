---
title: WM_POINTERROUTEDTO-Nachricht
description: Wird gesendet, wenn eine laufende Zeigereingabe für eine vorhandene Zeiger-ID zwischen den inhalten über geht, die für prozessübergreifende Verkettung konfiguriert sind (AddContentWithCrossProcessChaining).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- 'WM_POINTERROUTEDTO-Nachricht: Eingabemeldungen und Benachrichtigungen'
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9b7de7dd1affb9100a29613e3b4186d3d5bdaa32d853e683579fdcc62e7f981f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695621"
---
# <a name="wm_pointerroutedto-message"></a>WM_POINTERROUTEDTO-Nachricht

Wird bei laufender Zeigereingabe für eine vorhandene Zeiger-ID gesendet und über den für prozessübergreifende Verkettung konfigurierten Inhalt von einem Prozess in einen anderen übergewechselt ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

Diese Meldung wird an den Prozess gesendet, der derzeit keine Zeigereingabe empfängt.


```C++
#define WM_POINTERROUTEDTO       0x0251
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

## <a name="remarks"></a>Hinweise

Diese Meldung wird nicht gesendet, [**wenn WM_POINTERDOWN**](wm-pointerdown.md) eine neue Zeiger-ID in einem anderen Prozess gesendet wird.

Eine [**WM_POINTERDOWN**](wm-pointerdown.md) wird nicht gesendet, wenn **eine** WM_POINTERROUTEDTO zuerst gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Meldungen](messages.md)
</dt> <dt>

[**WM_POINTERROUTEDAWAY**](wm-pointerroutedaway.md)
</dt> </dl>

 

