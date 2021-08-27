---
title: SB_SIMPLE (Commctrl.h)
description: Gibt an, ob in einem Statusfenster einfacher Text oder alle Fensterteile angezeigt werden, die durch eine vorherige SB \_ SETPARTS-Meldung festgelegt wurden.
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- SB_SIMPLE von Windows Steuerelementen
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f0a896c9adcab6886151753761c62aefb8f4dc6ee21b7e85bb7507bda11f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132210"
---
# <a name="sb_simple-message"></a>SB \_ SIMPLE-Nachricht

Gibt an, ob in einem Statusfenster einfacher Text oder alle Fensterteile angezeigt werden, die durch eine vorherige [**SB \_ SETPARTS-Meldung festgelegt**](sb-setparts.md) wurden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzeigetypflag. Wenn dieser Parameter **TRUE ist,** zeigt das Fenster einfachen Text an. Wenn der Wert **FALSE ist,** werden mehrere Teile angezeigt.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Wenn das Statusfenster von "nonsimple" in "simple" oder umgekehrt geändert wird, wird das Fenster sofort neu gezeichnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





