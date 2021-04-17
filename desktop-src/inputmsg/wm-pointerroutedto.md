---
title: WM_POINTERROUTEDTO Meldung
description: Wird gesendet, wenn fortlaufende Zeiger Eingaben für eine vorhandene Zeiger-ID von einem Prozess in einen anderen über den Inhalt, der für prozessübergreifende Verkettung konfiguriert ist (addcontentwithcrossprocesschaining), übertragen werden.
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERROUTEDTO Nachricht
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
ms.openlocfilehash: 7658aeef77a0f7e19f2449213e9332b4e60c9450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391788"
---
# <a name="wm_pointerroutedto-message"></a>WM_POINTERROUTEDTO Meldung

Wird gesendet, wenn fortlaufende Zeiger Eingaben für eine vorhandene Zeiger-ID von einem Prozess in einen anderen über den Inhalt, der für prozessübergreifende Verkettung konfiguriert ist ([**addcontentwithcrossprocesschaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)), übertragen werden.

Diese Meldung wird an den Prozess gesendet, der derzeit keine Zeiger Eingaben empfängt.


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

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird nicht gesendet, wenn eine [**WM_POINTERDOWN**](wm-pointerdown.md) Nachricht für eine neue Zeiger-ID in einem anderen Prozess gepostet wird.

Eine [**WM_POINTERDOWN**](wm-pointerdown.md) Meldung wird nicht gesendet, wenn zuerst eine **WM_POINTERROUTEDTO** Meldung gesendet wird.

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

[**WM_POINTERROUTEDAWAY**](wm-pointerroutedaway.md)
</dt> </dl>

 

