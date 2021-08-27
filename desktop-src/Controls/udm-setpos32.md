---
title: UDM_SETPOS32 (Commctrl.h)
description: Legt die Position eines Auf-Ab-Steuerelements mit 32-Bit-Genauigkeit fest.
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- UDM_SETPOS32 von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d8dee48c580df72a32bb2072b00cc2dfbdf38b386825d686e8bc8510ba47e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088420"
---
# <a name="udm_setpos32-message"></a>UDM \_ SETPOS32-Nachricht

Legt die Position eines Auf-Ab-Steuerelements mit 32-Bit-Genauigkeit fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Variable vom Typ integer, die die neue Position für das Auf-Ab-Steuerelement angibt. Wenn sich der Parameter außerhalb des angegebenen Bereichs des Steuerelements befindet, wird *lParam* auf den nächsten gültigen Wert festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Position zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**UDM \_ GETPOS32**](udm-getpos32.md)
</dt> </dl>

 

 





