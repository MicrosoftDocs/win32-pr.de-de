---
title: TBM_GETPTICS Meldung (kommstrg. h)
description: Ruft die Adresse eines Arrays ab, das die Positionen der Teil Striche für eine TrackBar enthält.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- Windows-Steuerelemente für TBM_GETPTICS Meldung
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5d81e67156c0118310017413b8e73714246b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956501"
---
# <a name="tbm_getptics-message"></a>TBM- \_ getptics-Nachricht

Ruft die Adresse eines Arrays ab, das die Positionen der Teil Striche für eine TrackBar enthält.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Adresse eines Arrays von **DWORD** -Werten zurück. Die Elemente des Arrays geben die logischen Positionen der TrackBar-Teil Striche an, ohne die ersten und letzten Teil Striche, die von der TrackBar erstellt werden. Bei den logischen Positionen kann es sich um beliebige ganzzahlige Werte in der TrackBar-Bereich der minimalen bis maximalen Schieberegler-Positionen handeln.

## <a name="remarks"></a>Bemerkungen

Die Anzahl der Elemente im Array ist kleiner als die von der [**TBM \_ GetNumTics**](tbm-getnumtics.md) -Nachricht zurückgegebene Tick-Anzahl. Beachten Sie, dass die Werte im Array doppelte Positionen enthalten können und möglicherweise nicht in sequenzieller Reihenfolge vorliegen. Der zurückgegebene Zeiger ist gültig, bis die Teil Striche der TrackBar geändert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





