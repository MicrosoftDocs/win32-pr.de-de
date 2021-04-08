---
title: WM_CTLCOLORDLG Meldung (Winuser. h)
description: Wird an ein Dialogfeld gesendet, bevor das System das Dialogfeld zeichnet. Wenn Sie auf diese Meldung reagieren, kann das Dialogfeld die Text-und Hintergrundfarben mithilfe des angegebenen Kontext Handles für den Anzeigegerät festlegen.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- Dialog Felder WM_CTLCOLORDLG Meldung
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833d3894a85342b0f26323ceed0f4fb3356c48ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740153"
---
# <a name="wm_ctlcolordlg-message"></a>WM \_ ctlcolordlg-Meldung

Wird an ein Dialogfeld gesendet, bevor das System das Dialogfeld zeichnet. Wenn Sie auf diese Meldung reagieren, kann das Dialogfeld die Text-und Hintergrundfarben mithilfe des angegebenen Kontext Handles für den Anzeigegerät festlegen.


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Gerätekontext für das Dialogfeld.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle des Dialogfelds.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, muss Sie ein Handle für einen Pinsel zurückgeben. Das System verwendet den Pinsel zum Zeichnen des Hintergrunds des Dialog Felds.

## <a name="remarks"></a>Bemerkungen

Standardmäßig wählt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Standard Systemfarben für das Dialogfeld aus.

Das System zerstört den zurückgegebenen Pinsel nicht automatisch. Es ist Aufgabe der Anwendung, den Pinsel zu zerstören, wenn er nicht mehr benötigt wird.

Die " **WM \_ ctlcolordlg** "-Meldung wird nie zwischen Threads gesendet. Sie wird nur innerhalb eines Threads gesendet.

Beachten Sie, dass die " **WM \_ ctlcolordlg** "-Nachricht an das Dialogfeld selbst gesendet wird. alle anderen **WM \_ CtlColor \** _-Meldungen werden an den Besitzer des Steuer Elements gesendet.

Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in ein _ *int- \_ ptr** umwandeln und den Wert direkt zurückgeben. Wenn die Dialogfeld Prozedur **false** zurückgibt, wird die standardmäßige Nachrichtenverarbeitung ausgeführt. Der von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte **DWL- \_ msgresult** -Wert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Licher**
</dt> <dt>

[Dialog Felder](dialog-boxes.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

