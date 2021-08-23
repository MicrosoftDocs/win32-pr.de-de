---
title: PSM_CHANGED (Prsht.h)
description: Informiert ein Eigenschaftenblatt darüber, dass sich die Informationen auf einer Seite geändert haben. Sie können diese Nachricht explizit oder mithilfe des PropSheet \_ Changed-Makros senden.
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- PSM_CHANGED von Windows-Steuerelementen
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
ms.openlocfilehash: 2002801d21e4e89a6ccf762b9c9932671b210217a950f5494fb736feda35d32e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826020"
---
# <a name="psm_changed-message"></a>PSM \_ CHANGED-Meldung

Informiert ein Eigenschaftenblatt darüber, dass sich die Informationen auf einer Seite geändert haben. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ Changed-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für die geänderte Seite.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Das Eigenschaftenblatt aktiviert die **Schaltfläche** Anwenden.

> [!Note]  
> This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





