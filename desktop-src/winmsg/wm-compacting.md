---
description: Wird an alle Fenster der obersten Ebene gesendet, wenn das System mehr als 12,5 Prozent der Systemzeit über ein Intervall von 30 bis 60 Sekunden erkennt. Dies weist darauf hin, dass der Systemspeicher gering ist.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: WM_COMPACTING Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357906"
---
# <a name="wm_compacting-message"></a>Mit der WM \_ komprimierende Nachricht

Wird an alle Fenster der obersten Ebene gesendet, wenn das System mehr als 12,5 Prozent der Systemzeit über ein Intervall von 30 bis 60 Sekunden erkennt. Dies weist darauf hin, dass der Systemspeicher gering ist.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.

> [!Note]  
> Diese Meldung wird nur für die Kompatibilität mit 16-Bit-Windows-basierten Anwendungen bereitgestellt.

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Verhältnis der CPU-Zeit (Central Processing Unit), die zurzeit vom System für das System zur CPU-Zeit aufgewendet wird, das zurzeit vom System für andere Vorgänge aufgewendet wird. Beispielsweise steht 0X8000 für 50 Prozent der CPU-Zeit, die für den Komprimierungs Speicher aufgewendet wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Wenn eine Anwendung diese Nachricht empfängt, sollte so viel Arbeitsspeicher wie möglich freigegeben werden. dabei wird die aktuelle Aktivität der Anwendung und die Gesamtzahl der Anwendungen berücksichtigt, die auf dem System ausgeführt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Windows](windows.md)
</dt> </dl>

 

 
