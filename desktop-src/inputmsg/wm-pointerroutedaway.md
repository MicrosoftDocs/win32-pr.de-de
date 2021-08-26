---
title: WM_POINTERROUTEDAWAY-Nachricht
description: Tritt auf dem Prozess ein, der Eingaben empfängt, wenn die Zeigereingabe an einen anderen Prozess geroutet wird. AddContentWithCrossProcessChaining).
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- 'WM_POINTERROUTEDAWAY-Nachricht: Eingabemeldungen und Benachrichtigungen'
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDAWAY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: d6df21a5464aa44621c2eca760690806237f9e75a79c5f695d3df5b7604a6878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964220"
---
# <a name="wm_pointerroutedaway-message"></a>WM_POINTERROUTEDAWAY-Nachricht

Tritt auf dem Prozess ein, der Eingaben empfängt, wenn die Zeigereingabe an einen anderen Prozess geroutet wird.

Wird gesendet, wenn Zeigereingaben von einem Prozess in einen anderen über den für prozessübergreifende Verkettung konfigurierten Inhalt übertragen werden ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

Diese Meldung wird an den Prozess gesendet, der derzeit Zeigereingaben empfängt.


```C++
#define WM_POINTERROUTEDAWAY       0x0252
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

Diese Nachricht wird weder [](wm-pointerup.md) mit einer WM_POINTERUP noch mit [**einer**](wm-pointercapturechanged.md) WM_POINTERCAPTURECHANGED gesendet.

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

[**WM_POINTERROUTEDTO**](wm-pointerroutedto.md)
</dt> </dl>

 

