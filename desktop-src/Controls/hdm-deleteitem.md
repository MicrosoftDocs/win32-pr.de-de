---
title: HDM_DELETEITEM (Commctrl.h)
description: Löscht ein Element aus einem Headersteuerelement. Sie können diese Nachricht explizit senden oder das Header \_ DeleteItem-Makro verwenden.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- HDM_DELETEITEM meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28b0a48d769117ffd68f2ba2af9695fe7fce00031f297626ae48c111d4574dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697350"
---
# <a name="hdm_deleteitem-message"></a>HDM \_ DELETEITEM-Nachricht

Löscht ein Element aus einem Headersteuerelement. Sie können diese Nachricht explizit senden oder das [**Header \_ DeleteItem-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Index des zu löschenden Elements.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





