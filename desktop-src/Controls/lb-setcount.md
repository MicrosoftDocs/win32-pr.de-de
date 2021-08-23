---
title: LB_SETCOUNT (Winuser.h)
description: Legt die Anzahl der Elemente in einem Listenfeld fest, das mit dem LBS NODATA-Stil und nicht mit dem \_ LBS \_ HASSTRINGS-Stil erstellt wurde.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- LB_SETCOUNT message Windows Controls
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b3f68a67de2b7caa77cfd7c9e6f2a5b164e20af42100882fef1aad04eca14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433942"
---
# <a name="lb_setcount-message"></a>LB \_ SETCOUNT-Nachricht

Legt die Anzahl der Elemente in einem Listenfeld fest, das mit dem [**LBS \_ NODATA-Stil**](list-box-styles.md) und nicht mit dem [**LBS \_ HASSTRINGS-Stil erstellt**](list-box-styles.md) wurde.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die neue Anzahl von Elementen im Listenfeld an.

Windows 95/Windows 98/Windows Edition (Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, ist die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, ist der Rückgabewert LB \_ ERR. Wenn nicht genügend Arbeitsspeicher zum Speichern der Elemente verfügbar ist, ist der Rückgabewert LB \_ ERRSPACE.

## <a name="remarks"></a>Hinweise

Die **LB \_ SETCOUNT-Nachricht** wird nur von Listenfeldern unterstützt, die mit dem [**LBS \_ NODATA-Stil**](list-box-styles.md) und nicht mit dem [**LBS \_ HASSTRINGS-Stil erstellt**](list-box-styles.md) wurden. Alle anderen Listenfelder geben LB \_ ERR zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**LB \_ GETCOUNT**](lb-getcount.md)
</dt> </dl>

 

 





