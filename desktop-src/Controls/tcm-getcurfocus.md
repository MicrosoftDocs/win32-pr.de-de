---
title: TCM_GETCURFOCUS Meldung (Commctrl.h)
description: Gibt den Index des Elements zurück, das den Fokus in einem Registerkartensteuerelement hat. Sie können diese Nachricht explizit oder mithilfe des \_ GetCurFocus-Makros TabCtrl senden.
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- TCM_GETCURFOCUS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 694fb64b033d279292a687c39959925a68999c0b232c847bdf6ec6b476c725e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104940"
---
# <a name="tcm_getcurfocus-message"></a>TCM \_ GETCURFOCUS-Nachricht

Gibt den Index des Elements zurück, das den Fokus in einem Registerkartensteuerelement hat. Sie können diese Nachricht explizit oder mithilfe des [**\_ GetCurFocus-Makros TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Registerkartenelements zurück, das den Fokus besitzt.

## <a name="remarks"></a>Hinweise

Das Element, das den Fokus besitzt, kann sich von dem ausgewählten Element unterscheiden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





