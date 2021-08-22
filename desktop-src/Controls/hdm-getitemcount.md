---
title: HDM_GETITEMCOUNT Nachricht (Commctrl.h)
description: Ruft die Anzahl der Elemente in einem Headersteuerelement ab. Sie können diese Nachricht explizit senden oder das Headermakro \_ GetItemCount verwenden.
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- HDM_GETITEMCOUNT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e4500277528cc76012631734d6f7316b29fdcb7a5a92cec3cf7b6bbb42693ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436030"
---
# <a name="hdm_getitemcount-message"></a>HDM \_ GETITEMCOUNT-Nachricht

Ruft die Anzahl der Elemente in einem Headersteuerelement ab. Sie können diese Nachricht explizit senden oder das Headermakro [**\_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg die Anzahl der Elemente zurück, andernfalls -1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





