---
title: TCM_GETCURSEL (Commctrl.h)
description: Bestimmt die aktuell ausgewählte Registerkarte in einem Registerkarten-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des TabCtrl \_ GetCurSel-Makros senden.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- TCM_GETCURSEL von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6555194972467486789296377b5aaf87ca5520846ec9bf4c03ec345f635b6557
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104900"
---
# <a name="tcm_getcursel-message"></a>TCM \_ GETCURSEL-Nachricht

Bestimmt die aktuell ausgewählte Registerkarte in einem Registerkarten-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des [**TabCtrl \_ GetCurSel-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index der ausgewählten Registerkarte zurück, falls erfolgreich, oder -1, wenn keine Registerkarte ausgewählt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





