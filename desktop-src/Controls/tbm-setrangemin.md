---
title: TBM_SETRANGEMIN-Nachricht (Commctrl.h)
description: Legt die minimale logische Position für den Schieberegler in einer Trackleiste fest.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- TBM_SETRANGEMIN Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35cbb162b42636d886cb5e41eb9ba6de1a2101a8327ff8ddffbc71c57fa6735
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046070"
---
# <a name="tbm_setrangemin-message"></a>TBM \_ SETRANGEMIN-Nachricht

Legt die minimale logische Position für den Schieberegler in einer Trackleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Neu gezeichnetes Flag. Wenn dieser Parameter **TRUE** ist, zeichnet die Nachricht die Trackleiste neu, nachdem der Bereich festgelegt wurde. Wenn dieser Parameter **FALSE** ist, legt die Nachricht den Bereich fest, zeichnet die Trackleiste jedoch nicht neu.

</dd> <dt>

*lParam* 
</dt> <dd>

Mindestposition für den Schieberegler.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Wenn die aktuelle Position des Schiebereglers kleiner als der neue Mindestwert ist, legt die **TBM \_ SETRANGEMIN-Meldung** die Position des Schiebereglers auf den neuen Mindestwert fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**TBM \_ SETRANGE**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> </dl>

 

 





