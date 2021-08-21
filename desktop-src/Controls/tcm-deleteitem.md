---
title: TCM_DELETEITEM Meldung (Commctrl.h)
description: Entfernt ein Element aus einem Registerkartensteuerelement. Sie können diese Nachricht explizit oder mithilfe des TabCtrl \_ DeleteItem-Makros senden.
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- TCM_DELETEITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc9e90ab63e34545628019cd9dcde74c7b4e953fb6ee0b9eed138151129e7b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077874"
---
# <a name="tcm_deleteitem-message"></a>TCM \_ DELETEITEM-Nachricht

Entfernt ein Element aus einem Registerkartensteuerelement. Sie können diese Nachricht explizit oder mithilfe des [**TabCtrl \_ DeleteItem-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des zu löschende Elements.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





