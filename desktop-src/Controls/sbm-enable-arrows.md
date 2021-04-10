---
title: SBM_ENABLE_ARROWS Meldung (Winuser. h)
description: Eine Anwendung sendet die SBM-Option \_ \_ Pfeile aktivieren, um einen oder beide Pfeile eines ScrollBar-Steuer Elements zu aktivieren oder zu deaktivieren.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- Windows-Steuerelemente für SBM_ENABLE_ARROWS Meldung
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
ms.openlocfilehash: 78895b43ec7908172a6164917b33ac8549088db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956883"
---
# <a name="sbm_enable_arrows-message"></a>SBM \_ - \_ Meldung "Pfeile aktivieren"

Eine Anwendung sendet die **SBM-Option \_ \_ Pfeile aktivieren** , um einen oder beide Pfeile eines ScrollBar-Steuer Elements zu aktivieren oder zu deaktivieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob die Schiebe leisten Pfeile aktiviert oder deaktiviert sind, und gibt an, welche Pfeile aktiviert oder deaktiviert werden. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                   | Bedeutung                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <dt>**ESB- \_ Deaktivierung \_**</dt> </dl> | Deaktiviert beide Pfeile auf einer Schiebe Leiste.<br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <dt>**ESB- \_ Deaktivierung \_**</dt> </dl> | Deaktiviert den Pfeil nach unten auf einer vertikalen Schiebe Leiste.<br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <dt>**ESB- \_ Deaktivierung von \_ ltup**</dt> </dl> | Deaktiviert den Pfeil nach links auf einer horizontalen Schiebe Leiste oder den Pfeil nach oben auf einer vertikalen Schiebe Leiste.<br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <dt>**ESB \_ deaktiviert \_ Links**</dt> </dl> | Deaktiviert den Pfeil nach links auf einer horizontalen Schiebe Leiste.<br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <dt>**ESB- \_ Deaktivieren von \_ rtdn**</dt> </dl> | Deaktiviert den Pfeil nach rechts auf einer horizontalen Schiebe Leiste oder den Pfeil nach unten auf einer vertikalen Schiebe Leiste.<br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <dt>**ESB- \_ Deaktivierung \_**</dt> </dl>       | Deaktiviert den Pfeil nach oben auf einer vertikalen Schiebe Leiste.<br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <dt>**ESB \_ aktivieren \_**</dt> </dl>    | Aktiviert beide Pfeile auf einer Schiebe Leiste.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, lautet der Rückgabewert " **true**". Andernfalls ist Sie **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



 

 





