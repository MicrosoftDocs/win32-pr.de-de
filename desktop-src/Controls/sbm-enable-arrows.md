---
title: SBM_ENABLE_ARROWS (Winuser.h)
description: Eine Anwendung sendet die SBM ENABLE ARROWS-Meldung, um einen oder beide Pfeile eines \_ \_ Bildlaufleisten-Steuerelements zu aktivieren oder zu deaktivieren.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- SBM_ENABLE_ARROWS von Windows Steuerelementen
topic_type:
- apiref
api_name:
- SBM_ENABLE_ARROWS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e7f3ef8728befe72ec4f2c4afe39caeb10bc0b58984612a5db2445963dc549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770020"
---
# <a name="sbm_enable_arrows-message"></a>SBM \_ ENABLE \_ ARROWS message

Eine Anwendung sendet die **SBM \_ ENABLE \_ ARROWS-Meldung,** um einen oder beide Pfeile eines Bildlaufleisten-Steuerelements zu aktivieren oder zu deaktivieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob die Scrollleistenpfeile aktiviert oder deaktiviert sind, und gibt an, welche Pfeile aktiviert oder deaktiviert sind. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                   | Bedeutung                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <dt>**ESB \_ DISABLE \_ BOTH**</dt> </dl> | Deaktiviert beide Pfeile auf einer Bildlaufleiste.<br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <dt>**ESB \_ DISABLE \_ DOWN**</dt> </dl> | Deaktiviert den Pfeil nach unten auf einer vertikalen Scrollleiste.<br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <dt>**ESB \_ DISABLE \_ LTUP**</dt> </dl> | Deaktiviert den Pfeil nach links auf einer horizontalen Scrollleiste oder den Nach-oben-Pfeil auf einer vertikalen Bildlaufleiste.<br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <dt>**ESB \_ DISABLE \_ LEFT**</dt> </dl> | Deaktiviert den Pfeil nach links auf einer horizontalen Scrollleiste.<br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <dt>**ESB \_ DISABLE \_ RTDN**</dt> </dl> | Deaktiviert den Pfeil nach rechts auf einer horizontalen Scrollleiste oder den Pfeil nach unten auf einer vertikalen Bildlaufleiste.<br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <dt>**ESB \_ DISABLE \_ UP**</dt> </dl>       | Deaktiviert den Nach-oben-Pfeil auf einer vertikalen Scrollleiste.<br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <dt>**ESB \_ AKTIVIEREN SIE \_ BEIDES.**</dt> </dl>    | Aktiviert beide Pfeile auf einer Scrollleiste.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert **TRUE.** Andernfalls ist dies **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



 

 





