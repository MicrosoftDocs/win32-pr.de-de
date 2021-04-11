---
title: TBM_SETTIC Meldung (kommstrg. h)
description: Legt einen Teil Strich in einer TrackBar an der angegebenen logischen Position fest.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- Windows-Steuerelemente für TBM_SETTIC Meldung
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103222"
---
# <a name="tbm_settic-message"></a>TBM- \_ SetTic-Nachricht

Legt einen Teil Strich in einer TrackBar an der angegebenen logischen Position fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Position des Teil Strichs. Bei diesem Parameter kann es sich um einen beliebigen ganzzahligen Wert in der TrackBar-Bereich der minimalen bis maximalen Schieberegler-Positionen handeln.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn der Teil Strich festgelegt ist, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Eine TrackBar erstellt eigene erste und letzte Teil Striche. Verwenden Sie diese Meldung nicht, um den ersten und den letzten Teil Strich festzulegen.

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

[**TBM- \_ getptics**](tbm-getptics.md)
</dt> <dt>

[**TBM \_ GetTic**](tbm-gettic.md)
</dt> </dl>

 

 





