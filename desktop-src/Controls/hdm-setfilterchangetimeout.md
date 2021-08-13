---
title: HDM_SETFILTERCHANGETIMEOUT (Commctrl.h)
description: Legt das Timeoutintervall zwischen dem Zeitpunkt, zu dem eine Änderung in den Filterattributen stattfindet, und der Veröffentlichung einer HDN \_ FILTERCHANGE-Benachrichtigung fest. Sie können diese Nachricht explizit senden oder das \_ Header-SetFilterChangeTimeout-Makro verwenden.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- HDM_SETFILTERCHANGETIMEOUT von Windows Steuerelementen
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b5f8df12a7f30baa5f8b7d4bf15698b30cfbb6619fb71a81d4977b259c318b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435860"
---
# <a name="hdm_setfilterchangetimeout-message"></a>\_HDM-Nachricht "SETFILTERCHANGETIMEOUT"

Legt das Timeoutintervall zwischen dem Zeitpunkt, zu dem eine Änderung in den Filterattributen stattfindet, und dem Posten einer [HDN \_ FILTERCHANGE-Benachrichtigung](hdn-filterchange.md) fest. Sie können diese Nachricht explizit senden oder das [**\_ Header-Makro SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Der Timeoutwert in Millisekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des filter-Steuerelements zurück, das geändert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[HDN \_ FILTERCHANGE](hdn-filterchange.md)
</dt> </dl>

 

 





