---
title: WM_POINTERROUTEDAWAY Meldung
description: Tritt für den Prozess auf, der Eingaben empfängt, wenn die Zeiger Eingabe an einen anderen Prozess weitergeleitet wird. Addcontentwithcrossprocesschaining).
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERROUTEDAWAY Nachricht
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
ms.openlocfilehash: 3c099c02338aa70817d75717064e0b99ac13c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040775"
---
# <a name="wm_pointerroutedaway-message"></a>WM_POINTERROUTEDAWAY Meldung

Tritt für den Prozess auf, der Eingaben empfängt, wenn die Zeiger Eingabe an einen anderen Prozess weitergeleitet wird.

Wird gesendet, wenn die Zeiger Eingabe von einem Prozess in einen anderen über Inhalt übergeht, der für prozessübergreifende Verkettung konfiguriert ist ([**addcontentwithcrossprocesschaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

Diese Meldung wird an den Prozess gesendet, der derzeit Zeiger Eingaben empfängt.


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

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird nicht mit einer [**WM_POINTERUP**](wm-pointerup.md) Nachricht oder einer [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) Nachricht gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meldungen](messages.md)
</dt> <dt>

[**WM_POINTERROUTEDTO**](wm-pointerroutedto.md)
</dt> </dl>

 

