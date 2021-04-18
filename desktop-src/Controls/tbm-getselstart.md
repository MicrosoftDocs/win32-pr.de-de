---
title: TBM_GETSELSTART Meldung (kommstrg. h)
description: Ruft die Anfangsposition des aktuellen Auswahl Bereichs in einer TrackBar ab.
ms.assetid: 0000df2a-c40d-40c2-b120-e5d4fe6c5016
keywords:
- Windows-Steuerelemente für TBM_GETSELSTART Meldung
topic_type:
- apiref
api_name:
- TBM_GETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af796c57adb3615241a8f5b702ff58062468509
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341609"
---
# <a name="tbm_getselstart-message"></a>TBM \_ getselstart-Nachricht

Ruft die Anfangsposition des aktuellen Auswahl Bereichs in einer TrackBar ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der die Anfangsposition des aktuellen Auswahl Bereichs angibt.

## <a name="remarks"></a>Bemerkungen

Eine TrackBar kann nur dann einen Auswahlbereich haben, wenn Sie den TSB-Formatvorlagen [**\_ Bereich**](trackbar-control-styles.md) bei der Erstellung angegeben haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**TBM- \_ getselend**](tbm-getselend.md)
</dt> <dt>

[**TBM- \_ Sekunden**](tbm-setsel.md)
</dt> <dt>

[**TBM- \_ setselend**](tbm-setselend.md)
</dt> <dt>

[**TBM- \_ setselstart**](tbm-setselstart.md)
</dt> </dl>

 

 





