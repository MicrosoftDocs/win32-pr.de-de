---
title: PSM_RESTARTWINDOWS Meldung (prsht. h)
description: Gibt an, dass Windows neu gestartet werden muss, damit die Änderungen wirksam werden.
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- Windows-Steuerelemente für PSM_RESTARTWINDOWS Meldung
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb12126ae0a2b9187a941ccc1aff53186a0cda7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858820"
---
# <a name="psm_restartwindows-message"></a>PSM- \_ restartwindows-Meldung

Gibt an, dass Windows neu gestartet werden muss, damit die Änderungen wirksam werden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung sollte diese Nachricht nur als Antwort auf den Benachrichtigungs Code " [PSN \_ Apply](psn-apply.md) " oder " [PSN \_ killactive](psn-killactive.md) " senden. Sie können die **PSM- \_ restartwindows** -Nachricht explizit oder mithilfe des " [**propsheet \_ restartwindows**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) "-Makros senden.

Diese Meldung bewirkt, dass die [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) -Funktion den ID \_ psrestartwindows-Wert zurückgibt, jedoch nur, wenn der Benutzer auf die Schaltfläche " **OK** " klickt, um das Eigenschaften Blatt zu schließen. Es ist Aufgabe der Anwendung, Windows neu zu starten. Dies kann mithilfe der [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) -Funktion erfolgen.

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

