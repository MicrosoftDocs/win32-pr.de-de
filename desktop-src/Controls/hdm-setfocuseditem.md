---
title: HDM_SETFOCUSEDITEM (Commctrl.h)
description: Legt den Fokus auf ein angegebenes Element in einem Headersteuerelement fest. Senden Sie diese Nachricht explizit oder mithilfe des \_ Header-Makros SetFocusedItem.
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- HDM_SETFOCUSEDITEM meldungssteuerelemente Windows
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
ms.openlocfilehash: 9ea853cf625473bee608111eddf877eb09457ee5c2ac6089542b5add0a212195
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171075"
---
# <a name="hdm_setfocuseditem-message"></a>HDM \_ SETFOCUSEDITEM-Nachricht

Legt den Fokus auf ein angegebenes Element in einem Headersteuerelement fest. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ Header-Makros SetFocusedItem.**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Wird nicht verwendet. Muss Null sein.</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Der Index des Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Informationen zu Headersteuerelementen](header-controls.md)
</dt> </dl>

 

 





