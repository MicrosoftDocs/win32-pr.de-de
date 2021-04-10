---
title: EM_SETMARGINS Meldung (Winuser. h)
description: Legt die Breite des linken und rechten Rands für ein Bearbeitungs Steuerelement fest. Die Meldung zeichnet das Steuerelement neu, um die neuen Ränder widerzuspiegeln. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- Windows-Steuerelemente für EM_SETMARGINS Meldung
topic_type:
- apiref
api_name:
- EM_SETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c68f3394234a6f86b3c5ff69622b86e61afc556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956641"
---
# <a name="em_setmargins-message"></a>EM- \_ setMargin-Meldung

Legt die Breite des linken und rechten Rands für ein Bearbeitungs Steuerelement fest. Die Meldung zeichnet das Steuerelement neu, um die neuen Ränder widerzuspiegeln. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die festzulegenden Ränder. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <dt>**EC- \_ LeftMargin**</dt> </dl>    | Legt den linken Rand fest.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <dt>**EC- \_ RightMargin**</dt> </dl> | Legt den rechten Rand fest.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <dt>**EC \_ usefontinfo**</dt> </dl> | **Rich Edit-Steuerelemente:** Legt den linken und rechten Rand auf eine schmale Breite fest, die mithilfe der Textmetrik der aktuellen Schriftart des Steuer Elements berechnet wird. Wenn für das Steuerelement keine Schriftart festgelegt wurde, werden die Ränder auf 0 (null) festgelegt. Der *LPARAM* -Parameter wird ignoriert. <br/> Steuer **Elemente bearbeiten:** Der Wert " **EC \_ usefontinfo** " kann nicht im *wParam* -Parameter verwendet werden. Sie kann nur im *LPARAM* -Parameter verwendet werden.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die neue Breite des linken Rands in Pixel an. Dieser Wert wird ignoriert, wenn der **EC- \_ LeftMargin** von *wParam* nicht eingeschlossen wird.

**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 3,0 und höher:** Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) kann den Wert des **EC- \_ usefontinfo** angeben, um den linken Rand auf eine schmale Breite festzulegen, die mithilfe der Textmetrik der aktuellen Schriftart des Steuer Elements berechnet wird. Wenn für das Steuerelement keine Schriftart festgelegt wurde, wird der Rand auf 0 (null) festgelegt.

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die neue Breite des rechten Rands in Pixel an. Dieser Wert wird ignoriert, wenn *wParam* den **EC- \_ RightMargin** nicht einschließt.

**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 3,0 und höher:** Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) kann den Wert des **EC- \_ usefontinfo** angeben, um den rechten Rand auf eine schmale Breite festzulegen, die mithilfe der Textmetrik der aktuellen Schriftart des Steuer Elements berechnet wird. Wenn für das Steuerelement keine Schriftart festgelegt wurde, wird der Rand auf 0 (null) festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Steuer **Elemente bearbeiten:** Sie können " **EC \_ usefontinfo** " nicht im *wParam* -Parameter verwenden, aber Sie können es im *LPARAM* -Parameter verwenden.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Alle Rich Edit-Versionen unterstützen die Verwendung von " **EC \_ usefontinfo** " im *wParam* -Parameter. Allerdings unterstützt nur Microsoft Rich Edit 3,0 und höher die Verwendung von " **EC \_ usefontinfo** " im *LPARAM* -Parameter. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM- \_ getMargin**](em-getmargins.md)
</dt> </dl>

 

