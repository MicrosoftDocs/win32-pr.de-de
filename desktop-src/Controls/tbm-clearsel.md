---
title: TBM_CLEARSEL Meldung (kommstrg. h)
description: Löscht den aktuellen Auswahlbereich in einer TrackBar.
ms.assetid: ccf69fb7-d616-4a7a-8c7c-7a82827758b1
keywords:
- Windows-Steuerelemente für TBM_CLEARSEL Meldung
topic_type:
- apiref
api_name:
- TBM_CLEARSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d2474f3978dc80b2611bd6b454c45e515ee159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859327"
---
# <a name="tbm_clearsel-message"></a>TBM- \_ ClearSEL-Meldung

Löscht den aktuellen Auswahlbereich in einer TrackBar.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu zeichnen. Wenn dieser Parameter **true** ist, wird die TrackBar nach dem Löschen der Auswahl neu gezeichnet.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

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

[**TBM- \_ Sekunden**](tbm-setsel.md)
</dt> <dt>

[**TBM- \_ setselend**](tbm-setselend.md)
</dt> <dt>

[**TBM- \_ setselstart**](tbm-setselstart.md)
</dt> </dl>

 

 





