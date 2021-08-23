---
title: UDM_SETACCEL (Commctrl.h)
description: Legt die Beschleunigung für ein Auf-Ab-Steuerelement fest.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- UDM_SETACCEL meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc746e33c14de0dd177ecc31fc237be7cb8be36280bb2a5ceadff31d2b286ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957739"
---
# <a name="udm_setaccel-message"></a>UDM \_ SETACCEL-Nachricht

Legt die Beschleunigung für ein Auf-Ab-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl von [**UDACCEL-Strukturen,**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) die von *aAccels angegeben werden.*

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Array von [**UDACCEL-Strukturen,**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) die Beschleunigungsinformationen enthalten. Elemente sollten basierend auf dem **nSec-Element** in aufsteigender Reihenfolge sortiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**UDM \_ GETACCEL**](udm-getaccel.md)
</dt> </dl>

 

 





