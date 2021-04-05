---
title: LVM_GETITEMPOSITION Meldung (kommstrg. h)
description: Ruft die Position eines Listen Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getitemposition-Makros senden.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- Windows-Steuerelemente für LVM_GETITEMPOSITION Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40b5899634e2f357068caa6ef96339be82f600b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859158"
---
# <a name="lvm_getitemposition-message"></a>LVM- \_ getitemposition-Nachricht

Ruft die Position eines Listen Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getitemposition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Listen Ansichts Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die die Position der oberen linken Ecke des Elements in Ansichts Koordinaten empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

