---
title: LB_SETITEMDATA (Winuser.h)
description: Legt einen Wert fest, der dem angegebenen Element in einem Listenfeld zugeordnet ist.
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- LB_SETITEMDATA der Windows Steuerelemente
topic_type:
- apiref
api_name:
- LB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd9a705014ef770edba5b540a7acbd2512b685d5ebf8ca913df8fa329dc6058a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085330"
---
# <a name="lb_setitemdata-message"></a>LB \_ SETITEMDATA-Nachricht

Legt einen Wert fest, der dem angegebenen Element in einem Listenfeld zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den nullbasierten Index des Elements an. Wenn dieser Wert -1 ist, gilt *der lParam-Wert* für alle Elemente im Listenfeld.

Windows 95/Windows 98/Windows Edition (Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, ist die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt den Wert an, der dem Element zugeordnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, ist der Rückgabewert LB \_ ERR.

## <a name="remarks"></a>Hinweise

Wenn sich das Element in einem vom Besitzer gezeichneten Listenfeld befindet, das ohne [**den LBS \_ HASSTRINGS-Stil**](list-box-styles.md) erstellt wurde, ersetzt diese Meldung den Wert, der im *lParam-Parameter* der [**LB \_ ADDSTRING-**](lb-addstring.md) oder [**LB \_ INSERTSTRING-Meldung**](lb-insertstring.md) enthalten ist, die das Element dem Listenfeld hinzugefügt hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ GETITEMDATA**](lb-getitemdata.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> </dl>

 

 





