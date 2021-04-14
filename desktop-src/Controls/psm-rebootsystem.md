---
title: PSM_REBOOTSYSTEM Meldung (prsht. h)
description: Gibt an, dass das System neu gestartet werden muss, damit die Änderungen wirksam werden. Sie können die PSM- \_ rebootsystem-Nachricht explizit oder mithilfe des propsheet \_ rebootsystem-Makros senden.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- Windows-Steuerelemente für PSM_REBOOTSYSTEM Meldung
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
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476059"
---
# <a name="psm_rebootsystem-message"></a>PSM- \_ rebootsystemmeldung

Gibt an, dass das System neu gestartet werden muss, damit die Änderungen wirksam werden. Sie können die **PSM- \_ rebootsystem** -Nachricht explizit oder mithilfe des [**propsheet \_ rebootsystem**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) -Makros senden.

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

Eine Anwendung sollte diese Nachricht nur als Antwort auf die Benachrichtigungs Meldung " [PSN \_ Apply](psn-apply.md) " oder " [PSN \_ killactive](psn-killactive.md) " senden.

Diese Meldung bewirkt, dass die [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) -Funktion den \_ psrebootsystem-ID-Wert zurückgibt, jedoch nur, wenn der Benutzer auf die Schaltfläche **OK** klickt, um das Eigenschaften Blatt zu schließen. Es liegt in der Verantwortung der Anwendung, das System neu zu starten. Dies kann mithilfe der [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) -Funktion erfolgen.

Diese Nachricht ersetzt alle [**PSM- \_ restartwindows**](psm-restartwindows.md) -Meldungen, die vor oder nach der Nachricht liegen.

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

