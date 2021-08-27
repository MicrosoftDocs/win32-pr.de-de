---
title: PSM_REBOOTSYSTEM (Prsht.h)
description: Gibt an, dass das System neu gestartet werden muss, damit die Änderungen wirksam werden. Sie können die PSM \_ REBOOTSYSTEM-Nachricht explizit oder mithilfe des PropSheet \_ RebootSystem-Makros senden.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- PSM_REBOOTSYSTEM-Windows Steuerelemente
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfcfebc931d1dbf01ab053fa2723bdcf361c4be5ef1443b9131115e2300770cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088630"
---
# <a name="psm_rebootsystem-message"></a>PSM \_ REBOOTSYSTEM-Meldung

Gibt an, dass das System neu gestartet werden muss, damit die Änderungen wirksam werden. Sie können die **PSM \_ REBOOTSYSTEM-Nachricht** explizit oder mithilfe des [**PropSheet \_ RebootSystem-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) senden.

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

## <a name="remarks"></a>Hinweise

Eine Anwendung sollte diese Nachricht nur als Antwort auf die [PSN \_ APPLY-](psn-apply.md) oder [PSN \_ KILLACTIVE-Benachrichtigung](psn-killactive.md) senden.

Diese Meldung bewirkt, dass die [**PropertySheet-Funktion**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) den \_ ID-Wert PSREBOOTSYSTEM zurück gibt, jedoch nur, wenn der Benutzer auf die Schaltfläche **OK** klickt, um das Eigenschaftenblatt zu schließen. Es liegt in der Verantwortung der Anwendung, das System neu zu starten. Dies kann mithilfe der [**ExitWindowsEx-Funktion erfolgen.**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex)

Diese Meldung ersetzt alle [**PSM \_ RESTARTWINDOWS-Nachrichten,**](psm-restartwindows.md) die dieser voran- oder folgen.

> [!Note]  
> This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

