---
title: TCM_SETCURSEL Meldung (Commctrl.h)
description: Wählt eine Registerkarte in einem Registerkartensteuerelement aus. Sie können diese Nachricht explizit oder mithilfe des \_ TabCtrl-Makros SetCurSel senden.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- TCM_SETCURSEL Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdfd0861f5249a823d9406b437fd0efbca64a757a4bcadd7991155a87ddbc59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104850"
---
# <a name="tcm_setcursel-message"></a>TCM \_ SETCURSEL-Nachricht

Wählt eine Registerkarte in einem Registerkartensteuerelement aus. Sie können diese Nachricht explizit oder mithilfe des [**\_ TabCtrl-Makros SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index der auszuwählende Registerkarte.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Index der zuvor ausgewählten Registerkarte zurück, andernfalls -1.

## <a name="remarks"></a>Hinweise

Ein Registerkartensteuerelement sendet keinen [TCN \_ SELCHANGING-](tcn-selchanging.md) oder [TCN SELCHANGE-Benachrichtigungscode, \_ ](tcn-selchange.md) wenn eine Registerkarte mit dieser Meldung ausgewählt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





