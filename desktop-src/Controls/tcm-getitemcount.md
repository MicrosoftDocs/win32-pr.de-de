---
title: TCM_GETITEMCOUNT Meldung (Commctrl.h)
description: Ruft die Anzahl der Registerkarten im Registerkartensteuerelement ab. Sie können diese Nachricht explizit oder mithilfe des \_ GetItemCount-Makros TabCtrl senden.
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- TCM_GETITEMCOUNT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9bbb954c75a19f15ecee9f946e338a186b6e9903a405aa1c550fb0ccc31392
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104880"
---
# <a name="tcm_getitemcount-message"></a>TCM \_ GETITEMCOUNT-Nachricht

Ruft die Anzahl der Registerkarten im Registerkartensteuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**\_ GetItemCount-Makros TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg die Anzahl der Elemente zurück, andernfalls 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





