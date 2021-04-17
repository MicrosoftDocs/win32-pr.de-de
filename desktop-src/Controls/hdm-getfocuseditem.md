---
title: HDM_GETFOCUSEDITEM Meldung (kommstrg. h)
description: Ruft das Element in einem Header Steuerelement ab, das über den Fokus verfügt. Senden Sie diese Nachricht explizit oder mithilfe des Headers \_ getfocuseditem-Makro.
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- Windows-Steuerelemente für HDM_GETFOCUSEDITEM Meldung
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477586"
---
# <a name="hdm_getfocuseditem-message"></a>HDM \_ getfocuseditem-Meldung

Ruft das Element in einem Header Steuerelement ab, das über den Fokus verfügt. Senden Sie diese Nachricht explizit oder mithilfe des [**Headers \_ getfocuseditem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) -Makro.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Nicht verwendet. Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Nicht verwendet. Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Elements zurück, das den Fokus besitzt.

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

 

 





