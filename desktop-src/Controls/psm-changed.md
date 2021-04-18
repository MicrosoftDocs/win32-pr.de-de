---
title: PSM_CHANGED Meldung (prsht. h)
description: Teilt einem Eigenschaften Blatt mit, dass sich die Informationen in einer Seite geändert haben. Sie können diese Nachricht explizit oder mithilfe des von propsheet \_ geänderten Makros senden.
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- Windows-Steuerelemente für PSM_CHANGED Meldung
topic_type:
- apiref
api_name:
- PSM_CHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f931db5e25f816f7ea164ca5871a4e3e7757a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338759"
---
# <a name="psm_changed-message"></a>PSM- \_ geänderte Nachricht

Teilt einem Eigenschaften Blatt mit, dass sich die Informationen in einer Seite geändert haben. Sie können diese Nachricht explizit oder mithilfe des von [**propsheet \_ geänderten**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle der Seite, die geändert wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Auf dem Eigenschaften Blatt wird die Schaltfläche **anwenden** aktiviert.

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





