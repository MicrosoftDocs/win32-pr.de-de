---
title: TBM_GETSELEND Meldung (kommstrg. h)
description: Ruft die Endposition des aktuellen Auswahl Bereichs in einer TrackBar ab.
ms.assetid: e365dd4d-eb49-4107-b6d4-cdb558d27fdb
keywords:
- Windows-Steuerelemente für TBM_GETSELEND Meldung
topic_type:
- apiref
api_name:
- TBM_GETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 486d66d3e7fc2dd4d23b89cb5e9406fa81b34638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476803"
---
# <a name="tbm_getselend-message"></a>TBM- \_ getselend-Nachricht

Ruft die Endposition des aktuellen Auswahl Bereichs in einer TrackBar ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der die Endposition des aktuellen Auswahl Bereichs angibt.

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

[**TBM \_ getselstart**](tbm-getselstart.md)
</dt> <dt>

[**TBM- \_ Sekunden**](tbm-setsel.md)
</dt> <dt>

[**TBM- \_ setselend**](tbm-setselend.md)
</dt> <dt>

[**TBM- \_ setselstart**](tbm-setselstart.md)
</dt> </dl>

 

 





