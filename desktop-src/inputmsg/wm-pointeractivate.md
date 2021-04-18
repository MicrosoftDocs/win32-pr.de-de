---
title: WM_POINTERACTIVATE Meldung
description: Wird an ein inaktives Fenster gesendet, wenn ein primärer Zeiger eine WM_POINTERDOWN über das Fenster generiert.
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERACTIVATE Nachricht
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: b9bda11b5cb7a27f7744df6e20890a125a66bd88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344486"
---
# <a name="wm_pointeractivate-message"></a>WM_POINTERACTIVATE Meldung

Wird an ein inaktives Fenster gesendet, wenn ein primärer Zeiger eine [**WM_POINTERDOWN**](wm-pointerdown.md) über das Fenster generiert. Solange die Nachricht nicht behandelt wird, wird die übergeordnete Fenster Kette nach oben verschoben, bis Sie das Fenster der obersten Ebene erreicht. Anwendungen können auf diese Meldung reagieren, um anzugeben, ob Sie aktiviert werden sollen.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält den Zeiger Bezeichner und zusätzliche Informationen. Verwenden Sie die folgenden Makros, um diese Informationen abzurufen.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Zeiger Bezeichner

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): Treffer Test Wert, der von der Verarbeitung der [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) Nachricht zurückgegeben wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält das Handle für das Fenster auf oberster Ebene des Fensters, das aktiviert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie einen der im Abschnitt "Hinweise" beschriebenen Werte zurückgeben.

Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann diese Nachricht verarbeiten und einen der folgenden Werte zurückgeben, um zu bestimmen, wie das System die Aktivierung und die Aktivierungs Eingabe verarbeitet:

-   PA_ACTIVATE
-   PA_NOACTIVATE

Beachten Sie Folgendes: Wenn der Benutzer mit dem System mit mehreren gleichzeitigen Zeigern interagiert, ist die Aktivierungs Chance, die die **WM_POINTERACTIVATE** Nachricht darstellt, für Anwendungen nur für die ersten dieser Zeiger verfügbar. Anwendungen sollten daher beachten, dass Sie möglicherweise weiterhin Eingaben von Zeigern empfangen, wenn Sie inaktiv sind.

Wenn die Anwendung diese Nachricht nicht verarbeitet, übergibt [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) die Nachricht an das übergeordnete Fenster.

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

 

