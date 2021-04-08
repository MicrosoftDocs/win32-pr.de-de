---
title: TBM_GETNUMTICS Meldung (kommstrg. h)
description: Ruft die Anzahl der Teil Striche in einer TrackBar ab.
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- Windows-Steuerelemente für TBM_GETNUMTICS Meldung
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949591"
---
# <a name="tbm_getnumtics-message"></a>TBM \_ GetNumTics-Nachricht

Ruft die Anzahl der Teil Striche in einer TrackBar ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn kein [Tick-Flag](trackbar-control-styles.md) festgelegt ist, gibt es für den Anfangs-und den endticks den Wert 2 zurück. Wenn " [**TSB \_ noticks**](trackbar-control-styles.md) " festgelegt ist, wird NULL zurückgegeben. Andernfalls nimmt Sie den Unterschied zwischen dem minimal-und Maximalwert des Bereichs, dividiert durch die Taktfrequenz und addiert 2.

## <a name="remarks"></a>Bemerkungen

Die **TBM \_ GetNumTics** -Nachricht zählt alle Teil Striche, einschließlich der ersten und letzten Teil Striche, die von der TrackBar erstellt wurden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





