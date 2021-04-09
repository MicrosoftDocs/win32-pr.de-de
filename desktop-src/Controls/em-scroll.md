---
title: EM_SCROLL Meldung (Winuser. h)
description: Führt einen vertikalen Bildlauf in einem mehrzeiligen Bearbeitungs Steuerelement aus. Diese Meldung entspricht dem Senden einer WM- \_ VScroll-Nachricht an das Bearbeitungs Steuerelement. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- Windows-Steuerelemente für EM_SCROLL Meldung
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
ms.openlocfilehash: 09eb185fb14ef866ab0e7ea8c8064445193347d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106268"
---
# <a name="em_scroll-message"></a>EM- \_ scrollnachricht

Führt einen vertikalen Bildlauf in einem mehrzeiligen Bearbeitungs Steuerelement aus. Diese Meldung entspricht dem Senden einer [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht an das Bearbeitungs Steuerelement. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Aktion, die von der Scrollleiste ausgeführt werden soll. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                   | Bedeutung                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB- \_ LineDown**</dt> </dl> | Führt einen Bildlauf um eine Zeile nach unten durch<br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ -Auflistung**</dt> </dl>       | Führt einen Bildlauf eine Zeile nach oben aus<br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB- \_ PageDown**</dt> </dl> | Scrollt eine Seite nach unten<br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB- \_ PageUp**</dt> </dl>       | Führt einen Bildlauf eine Seite nach oben aus<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) des Rückgabewerts **true**, und das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist die Anzahl der Zeilen, in denen der Befehl einen Bildlauf durchführt. Die zurückgegebene Zahl ist möglicherweise nicht identisch mit der tatsächlichen Anzahl der Zeilen, die gescrollt werden, wenn der Bildlauf an den Anfang oder das Ende des Texts verschoben wird. Wenn der *wParam* -Parameter einen ungültigen Wert angibt, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Um einen Bildlauf zu einer bestimmten Zeile oder Zeichenposition durchführen zu können, verwenden Sie die [**EM \_ linescroll**](em-linescroll.md) -Nachricht. Wenn Sie die Einfügemarke in die Ansicht scrollen möchten, verwenden Sie die [**EM \_ scrollcaret**](em-scrollcaret.md)

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM- \_ linescroll**](em-linescroll.md)
</dt> <dt>

[**EM \_ scrollcaret**](em-scrollcaret.md)
</dt> <dt>

[**WM- \_ VScroll**](wm-vscroll.md)
</dt> </dl>

 

