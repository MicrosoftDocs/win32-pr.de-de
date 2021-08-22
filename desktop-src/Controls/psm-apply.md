---
title: PSM_APPLY (Prsht.h)
description: Simuliert die Auswahl der Schaltfläche Anwenden, die angibt, dass sich eine oder mehrere Seiten geändert haben und die Änderungen überprüft und aufgezeichnet werden müssen.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- PSM_APPLY Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- PSM_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f753eb2465ec835f467493bdbd83d10b8ba174b11c83abffcb91d20f8beba002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544160"
---
# <a name="psm_apply-message"></a>PSM \_ APPLY-Nachricht

Simuliert die Auswahl  der Schaltfläche Anwenden, die angibt, dass sich eine oder mehrere Seiten geändert haben und die Änderungen überprüft und aufgezeichnet werden müssen.

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

Gibt **TRUE zurück,** wenn die Änderungen auf alle Seiten erfolgreich angewendet wurden, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Das Eigenschaftenblatt sendet den [PSN \_ KILLACTIVE-Benachrichtigungscode](psn-killactive.md) an die aktuelle Seite. Wenn die aktuelle Seite **FALSE zurückgibt,** sendet das Eigenschaftenblatt den [PSN APPLY-Benachrichtigungscode \_](psn-apply.md) an alle aktiven Seiten. Sie können die PSM \_ APPLY-Nachricht explizit oder mithilfe des [**PropSheet \_ Apply-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) senden.

> [!Note]  
> This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





