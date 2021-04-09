---
title: TCM_SETCURSEL Meldung (kommstrg. h)
description: Wählt eine Registerkarte in einem Register Steuerelement aus. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ setcurrsel-Makros senden.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- Windows-Steuerelemente für TCM_SETCURSEL Meldung
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
ms.openlocfilehash: 90033c5a19b0eb7b73f9ed886e8dad8d1ca4c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956496"
---
# <a name="tcm_setcursel-message"></a>TCM- \_ setcurrsel-Meldung

Wählt eine Registerkarte in einem Register Steuerelement aus. Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ setcurrsel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index der auszuwählen Registerkarte.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index der zuvor ausgewählten Registerkarte zurück, wenn erfolgreich, andernfalls-1.

## <a name="remarks"></a>Bemerkungen

Ein Registerkarten-Steuerelement sendet keinen [TCN \_ selchanging](tcn-selchanging.md) -oder [TCN \_ selChange](tcn-selchange.md) -Benachrichtigungs Code, wenn mithilfe dieser Meldung eine Registerkarte ausgewählt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





