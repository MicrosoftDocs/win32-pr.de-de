---
title: EM_SETMARGINS Meldung (Winuser.h)
description: Legt die Breite des linken und rechten Rands für ein Bearbeitungssteuerelement fest. In der Meldung wird das Steuerelement neu gezeichnet, um die neuen Ränder widerzuspiegeln. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- EM_SETMARGINS Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 396bba6dda0f6dbd132b9f67fa5a1ef012758bbf7cf8fa9517b656dcf164c94c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048360"
---
# <a name="em_setmargins-message"></a>EM \_ SETMARGINS-Nachricht

Legt die Breite des linken und rechten Rands für ein Bearbeitungssteuerelement fest. In der Meldung wird das Steuerelement neu gezeichnet, um die neuen Ränder widerzuspiegeln. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die festzulegende Ränder. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <dt>**EC \_ LEFTMARGIN**</dt> </dl>    | Legt den linken Rand fest.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <dt>**EC \_ RIGHTMARGIN**</dt> </dl> | Legt den rechten Rand fest.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <dt>**EC \_ USEFONTINFO**</dt> </dl> | **Rich Edit-Steuerelemente:** Legt den linken und rechten Rand auf eine schmale Breite fest, die mithilfe der Textmetriken der aktuellen Schriftart des Steuerelements berechnet wird. Wenn für das Steuerelement keine Schriftart festgelegt wurde, werden die Ränder auf 0 (null) festgelegt. Der *lParam-Parameter* wird ignoriert. <br/> **Bearbeiten von Steuerelementen:** Der **EC \_ USEFONTINFO-Wert** kann nicht im *wParam-Parameter* verwendet werden. Sie kann nur im *lParam-Parameter* verwendet werden.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die neue Breite des linken Rands in Pixel an. Dieser Wert wird ignoriert, wenn *wParam* EC **\_ LEFTMARGIN** nicht enthält.

**Bearbeiten von Steuerelementen und Rich Edit 3.0 und höher:** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) kann den **EC \_ USEFONTINFO-Wert** angeben, um den linken Rand auf eine schmale Breite festzulegen, die mithilfe der Textmetriken der aktuellen Schriftart des Steuerelements berechnet wird. Wenn für das Steuerelement keine Schriftart festgelegt wurde, wird der Rand auf 0 (null) festgelegt.

[**HiWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die neue Breite des rechten Rands in Pixel an. Dieser Wert wird ignoriert, wenn *wParam* EC **\_ RIGHTMARGIN** nicht enthält.

**Bearbeiten von Steuerelementen und Rich Edit 3.0 und höher:** [**HiWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) kann den **EC \_ USEFONTINFO-Wert** angeben, um den rechten Rand auf eine schmale Breite festzulegen, die mithilfe der Textmetriken der aktuellen Schriftart des Steuerelements berechnet wird. Wenn für das Steuerelement keine Schriftart festgelegt wurde, wird der Rand auf 0 (null) festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

**Bearbeiten von Steuerelementen:** Sie können **EC \_ USEFONTINFO** nicht im *wParam-Parameter* verwenden, aber sie können sie im *lParam-Parameter* verwenden.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Alle Rich Edit-Versionen unterstützen die Verwendung von **EC \_ USEFONTINFO** im *wParam-Parameter.* Allerdings unterstützen nur Microsoft Rich Edit 3.0 und höher die Verwendung von **EC \_ USEFONTINFO** im *lParam-Parameter.* Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ GETMARGINS**](em-getmargins.md)
</dt> </dl>

 

