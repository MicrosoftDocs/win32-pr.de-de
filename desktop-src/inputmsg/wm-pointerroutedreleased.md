---
title: WM_POINTERROUTEDRELEASED Meldung
description: Wird an alle Prozesse gesendet (für die prozessübergreifende Verkettung durch addcontentwithcrossprocesschaining konfiguriert und ist zurzeit keine Zeiger Eingabe), wenn eine WM_POINTERUP Nachricht im aktuellen Prozess empfangen wird.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERROUTEDRELEASED Nachricht
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
ms.openlocfilehash: 8e24a0df1a2bbdf2b0a9df97057686aa6045eff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391925"
---
# <a name="wm_pointerroutedreleased-message"></a>WM_POINTERROUTEDRELEASED Meldung

Wird an alle Prozesse gesendet (für die prozessübergreifende Verkettung durch [**addcontentwithcrossprocesschaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) konfiguriert und ist zurzeit keine Zeiger Eingabe), wenn eine [**WM_POINTERUP**](wm-pointerup.md) Nachricht im aktuellen Prozess empfangen wird.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meldungen](messages.md)
</dt> </dl>

 

