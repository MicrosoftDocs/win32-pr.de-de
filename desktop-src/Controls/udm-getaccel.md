---
title: UDM_GETACCEL Meldung (kommstrg. h)
description: Ruft Beschleunigungs Informationen für ein auf-ab-Steuerelement ab.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- Windows-Steuerelemente für UDM_GETACCEL Meldung
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86a9740e59631b737453763a10ccb9820056d95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475735"
---
# <a name="udm_getaccel-message"></a>UDM \_ GetAccel-Nachricht

Ruft Beschleunigungs Informationen für ein auf-ab-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl von Elementen im Array, die von *LPARAM* angegeben werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Array von [**udaccel**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) -Strukturen, die Beschleunigungs Informationen erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Anzahl von Accelerators, die derzeit für das Steuerelement festgelegt sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**UDM- \_ SetAccel**](udm-setaccel.md)
</dt> </dl>

 

 





