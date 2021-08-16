---
description: Wird an alle Fenster der obersten Ebene gesendet, wenn das System erkennt, dass mehr als 12,5 Prozent der Systemzeit in einem Intervall von 30 bis 60 Sekunden für die Komprimierung des Arbeitsspeichers aufgewendet werden. Dies weist darauf hin, dass der Systemspeicher niedrig ist.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: WM_COMPACTING Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553662bccb223ed7fb987df5d2918e3d8d1c6ab95f125cbacbd50c1e2484c0c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200571"
---
# <a name="wm_compacting-message"></a>WM \_ COMPACTING-Meldung

Wird an alle Fenster der obersten Ebene gesendet, wenn das System erkennt, dass mehr als 12,5 Prozent der Systemzeit in einem Intervall von 30 bis 60 Sekunden für die Komprimierung des Arbeitsspeichers aufgewendet werden. Dies weist darauf hin, dass der Systemspeicher niedrig ist.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> [!Note]  
> Diese Meldung wird nur aus Gründen der Kompatibilität mit 16-Bit-Windows-basierten Anwendungen bereitgestellt.

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Verhältnis der CPU-Zeit (Central Processing Unit), die das System derzeit für die Komprimierung des Arbeitsspeichers auf die CPU-Zeit aufwendet, die das System derzeit für andere Vorgänge aufgewendet hat. Beispielsweise stellt 0x8000 50 Prozent der CPU-Zeit dar, die für die Komprimierung des Arbeitsspeichers aufgewendet wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Wenn eine Anwendung diese Nachricht empfängt, sollte sie unter Berücksichtigung der aktuellen Aktivitätsebene der Anwendung und der Gesamtzahl der auf dem System ausgeführten Anwendungen so viel Arbeitsspeicher wie möglich freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Windows Übersicht](windows.md)
</dt> </dl>

 

 
