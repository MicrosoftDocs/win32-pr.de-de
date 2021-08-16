---
title: TCM_INSERTITEM Meldung (Commctrl.h)
description: Fügt eine neue Registerkarte in ein Registerkartensteuerelement ein. Sie können diese Nachricht explizit oder mithilfe des TabCtrl \_ InsertItem-Makros senden.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- TCM_INSERTITEM Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c3c17714218562d7ddc82497a7ef27e131e30a2ff04daf36970dfbcf5cc354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829101"
---
# <a name="tcm_insertitem-message"></a>TCM \_ INSERTITEM-Nachricht

Fügt eine neue Registerkarte in ein Registerkartensteuerelement ein. Sie können diese Nachricht explizit oder mithilfe des [**TabCtrl \_ InsertItem-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index der neuen Registerkarte.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TCITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tcitema) die die Attribute der Registerkarte angibt. Die **dwState-** und **dwStateMask-Member** dieser Struktur werden von dieser Meldung ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Index der neuen Registerkarte zurück, andernfalls -1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TCM \_ INSERTITEMW** (Unicode) und **TCM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





