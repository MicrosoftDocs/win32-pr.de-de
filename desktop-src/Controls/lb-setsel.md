---
title: LB_SETSEL Meldung (Winuser. h)
description: Wählt ein Element in einem Listenfeld mit Mehrfachauswahl aus und führt ggf. einen Bildlauf in der Ansicht durch.
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- Windows-Steuerelemente für LB_SETSEL Meldung
topic_type:
- apiref
api_name:
- LB_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd50f12c4190ba9ecafad11b167c1ac60adf691d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478537"
---
# <a name="lb_setsel-message"></a>LB-Aktivität \_ Nachricht

Wählt ein Element in einem Listenfeld mit Mehrfachauswahl aus und führt ggf. einen Bildlauf in der Ansicht durch.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, wie die Auswahl festgelegt wird. Wenn dieser Parameter **true** ist, wird das Element ausgewählt und hervorgehoben. Wenn der Wert **false** ist, wird die Hervorhebung entfernt, und das Element wird nicht mehr ausgewählt.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt den NULL basierten Index des festzulegenden Elements an. Wenn dieser Parameter-1 ist, wird die Auswahl in Abhängigkeit vom Wert von *wParam* hinzugefügt oder aus allen Elementen entfernt, und es erfolgt kein Bildlauf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Meldung nur für Listenfelder mit Mehrfachauswahl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**LB- \_ GetSEL**](lb-getsel.md)
</dt> <dt>

[**LB- \_ selitemrange**](lb-selitemrange.md)
</dt> </dl>

 

 





