---
title: PSM_UNCHANGED Meldung (prsht. h)
description: Teilt einem Eigenschaften Blatt mit, dass die Informationen in einer Seite in den zuvor gespeicherten Zustand zurückversetzt wurden. Sie können diese Nachricht explizit oder mithilfe des unveränderten propsheet- \_ Makros senden.
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- Windows-Steuerelemente für PSM_UNCHANGED Meldung
topic_type:
- apiref
api_name:
- PSM_UNCHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d6216f94afd610bb49710a3e84b4c21a673f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213740"
---
# <a name="psm_unchanged-message"></a>PSM- \_ Nachricht unverändert

Teilt einem Eigenschaften Blatt mit, dass die Informationen in einer Seite in den zuvor gespeicherten Zustand zurückversetzt wurden. Sie können diese Nachricht explizit oder mithilfe des [**\_ unveränderten propsheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für die Seite, die in den zuvor gespeicherten Zustand zurückversetzt wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Auf dem Eigenschaften Blatt wird die Schaltfläche **anwenden** deaktiviert, wenn keine anderen Seiten Änderungen mit dem Eigenschaften Blatt registriert haben.

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





