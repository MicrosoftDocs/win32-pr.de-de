---
title: EM_SCROLL (Winuser.h)
description: Führt einen vertikalen Bildlauf des Texts in einem mehrzeilenigen Bearbeitungssteuerfeld durch. Diese Meldung entspricht dem Senden einer WM \_ VSCROLL-Nachricht an das Edit-Steuerelement. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- EM_SCROLL-Windows Steuerelemente
topic_type:
- apiref
api_name:
- EM_SCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c619a50d14185289776e891373dcc7fc9e7cae607a899517a4bf5bc9289a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006207"
---
# <a name="em_scroll-message"></a>EM \_ SCROLL-Nachricht

Führt einen vertikalen Bildlauf des Texts in einem mehrzeilenigen Bearbeitungssteuerfeld durch. Diese Meldung entspricht dem Senden einer [**WM \_ VSCROLL-Nachricht**](wm-vscroll.md) an das Edit-Steuerelement. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Aktion, die die Scrollleiste durchführen soll. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                   | Bedeutung                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> </dl> | Führt einen Bildlauf um eine Zeile nach unten durch<br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ LINEUP**</dt> </dl>       | Führt einen Bildlauf eine Zeile nach oben aus<br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PAGEDOWN**</dt> </dl> | Scrollt eine Seite nach unten<br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PAGEUP**</dt> </dl>       | Führt einen Bildlauf eine Seite nach oben aus<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist [**das HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) des Rückgabewerts **TRUE,** und [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist die Anzahl der Zeilen, die der Befehl scrollt. Die zurückgegebene Zahl ist möglicherweise nicht mit der tatsächlichen Anzahl der gescrollten Zeilen identisch, wenn der Bildlauf an den Anfang oder das Ende des Texts bewegt wird. Wenn der *wParam-Parameter* einen ungültigen Wert angibt, ist der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Um zu einer bestimmten Zeile oder Zeichenposition zu scrollen, verwenden Sie die [**MELDUNG EM \_ LINESCROLL.**](em-linescroll.md) Verwenden Sie die EM SCROLLCARET-Meldung, um das [**\_ Caret-Caret**](em-scrollcaret.md) in die Ansicht zu scrollen.

**Umfangreiche Bearbeitung:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ LINESCROLL**](em-linescroll.md)
</dt> <dt>

[**EM \_ SCROLLCARET**](em-scrollcaret.md)
</dt> <dt>

[**WM \_ VSCROLL**](wm-vscroll.md)
</dt> </dl>

 

