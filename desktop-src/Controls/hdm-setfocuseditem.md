---
title: HDM_SETFOCUSEDITEM Meldung (kommstrg. h)
description: Legt den Fokus auf ein angegebenes Element in einem Header Steuerelement fest. Senden Sie diese Nachricht explizit oder mithilfe des Headers \_ setfocuseditem-Makro.
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- Windows-Steuerelemente für HDM_SETFOCUSEDITEM Meldung
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105291"
---
# <a name="hdm_setfocuseditem-message"></a>HDM- \_ setfocuseditem-Meldung

Legt den Fokus auf ein angegebenes Element in einem Header Steuerelement fest. Senden Sie diese Nachricht explizit oder mithilfe des [**Headers \_ setfocuseditem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) -Makro.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Nicht verwendet. Muss Null sein.</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Der Index des Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Informationen über Header Steuerelemente](header-controls.md)
</dt> </dl>

 

 





