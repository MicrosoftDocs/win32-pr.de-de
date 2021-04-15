---
title: TBM_CLEARTICS Meldung (kommstrg. h)
description: Entfernt die aktuellen Teil Striche aus einer TrackBar. Diese Meldung entfernt nicht die ersten und letzten Teil Striche, die automatisch von der TrackBar erstellt werden.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- Windows-Steuerelemente für TBM_CLEARTICS Meldung
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1ecb4f9f931c976b2542a1f263fc069f1eca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475921"
---
# <a name="tbm_cleartics-message"></a>TBM- \_ ClearTics-Nachricht

Entfernt die aktuellen Teil Striche aus einer TrackBar. Diese Meldung entfernt nicht die ersten und letzten Teil Striche, die automatisch von der TrackBar erstellt werden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu zeichnen. Wenn dieser Parameter **true** ist, wird die TrackBar neu gezeichnet, nachdem die Teil Striche gelöscht wurden. Wenn dieser Parameter **false** ist, löscht die Nachricht die Teil Striche, aber die TrackBar wird nicht neu gezeichnet.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





