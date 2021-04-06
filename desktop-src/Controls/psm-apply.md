---
title: PSM_APPLY Meldung (prsht. h)
description: Simuliert die Auswahl der Schaltfläche anwenden und gibt an, dass sich mindestens eine Seite geändert hat und die Änderungen überprüft und aufgezeichnet werden müssen.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- Windows-Steuerelemente für PSM_APPLY Meldung
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
ms.openlocfilehash: 67d798d4a9a2f780ac81cc84c90a57d0efd4e299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859122"
---
# <a name="psm_apply-message"></a>PSM- \_ Nachricht anwenden

Simuliert die Auswahl der Schaltfläche **anwenden** und gibt an, dass sich mindestens eine Seite geändert hat und die Änderungen überprüft und aufgezeichnet werden müssen.

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

Gibt **true** zurück, wenn alle Seiten die Änderungen erfolgreich angewendet haben, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Das Eigenschaften Blatt sendet den Benachrichtigungs Code " [PSN \_ killactive](psn-killactive.md) " an die aktuelle Seite. Wenn die aktuelle Seite **false** zurückgibt, sendet das Eigenschaften Blatt den " [PSN \_ Apply](psn-apply.md) "-Benachrichtigungs Code auf alle aktiven Seiten. Sie können die PSM-Anwendungs \_ Nachricht explizit oder mithilfe des [**propsheet \_ Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) -Makros senden.

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





