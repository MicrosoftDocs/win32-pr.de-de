---
title: WM_POINTERCAPTURECHANGED Meldung
description: Wird an ein Fenster gesendet, das die Erfassung eines Eingabe Zeigers verliert.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERCAPTURECHANGED Nachricht
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341023"
---
# <a name="wm_pointercapturechanged-message"></a>WM_POINTERCAPTURECHANGED Meldung

Wird an ein Fenster gesendet, das die Erfassung eines Eingabe Zeigers verliert.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält Informationen über den Eingabe Zeiger, der verloren geht. Verwenden Sie [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) , um die Zeiger-ID zu erhalten.

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält ein Handle für das Fenster, das den Eingabe Zeiger erfasst. Dieser Wert kann NULL sein, wenn der Zeiger nicht mehr vom Fenster erfasst wird.

Wenn diese Meldung aus der internen Verarbeitung generiert wird, kann der Wert das Handle des Fensters sein, in dem die Nachricht empfangen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.

## <a name="remarks"></a>Bemerkungen

Ein Fenster sollte diese Benachrichtigung verwenden, um die Verarbeitung von nachfolgenden Nachrichten zu unterbinden und alle Bereinigungs Vorgänge zu initiieren, die erforderlich sind Die Verarbeitung der dem Zeiger zugeordneten Gesten sollte ebenfalls beendet werden (z. b. durch Aufrufen von [**stopinteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) und verbleibende Kontakte, die dem Fenster erneut zugeordnet werden.

Wenn ein Fenster die **WM_POINTERCAPTURECHANGED** Benachrichtigung empfängt, werden in der Regel keine nachfolgenden Benachrichtigungen zum Eingabe Zeiger empfangen. Aus diesem Grund hängen nicht von gekoppelten Benachrichtigungen wie [**WM_POINTERENTER**](wm-pointerenter.md) und [**WM_POINTERLEAVE**](wm-pointerleave.md)ab.

**WM_POINTERCAPTURECHANGED** enthält keine [**POINTER_INFO**](/previous-versions/windows/desktop/api) Daten. Die von [**getpointerinfo**](/previous-versions/windows/desktop/api) (oder einer beliebigen Variante) zurückgegebenen Daten sind mit denen identisch, die vor der Benachrichtigung zurückgegeben werden. [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md)

Wenn diese Benachrichtigung von der Anwendung nicht verarbeitet wird, generiert [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) möglicherweise eine oder mehrere [**WM_GESTURE**](../wintouch/wm-gesture.md) Meldungen, oder wenn eine Geste nicht erkannt wird, generiert **defwindowproc** möglicherweise Maus Eingaben.

Wenn eine Anwendung selektiv eine Zeiger Eingabe verwendet und den Rest an [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergibt, ist das resultierende Verhalten nicht definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meldungen](messages.md)
</dt> </dl>

 

