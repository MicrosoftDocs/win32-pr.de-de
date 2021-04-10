---
title: TBM_SETTICFREQ Meldung (kommstrg. h)
description: Legt die Intervall Häufigkeit für Teil Striche in einer TrackBar fest.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- Windows-Steuerelemente für TBM_SETTICFREQ Meldung
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040358"
---
# <a name="tbm_setticfreq-message"></a>TBM- \_ mescfreq-Nachricht

Legt die Intervall Häufigkeit für Teil Striche in einer TrackBar fest. Wenn die Häufigkeit z. b. auf zwei festgelegt ist, wird für jedes andere Inkrement im Bereich der TrackBar ein Teil Strich angezeigt. Die Standardeinstellung für die Häufigkeit ist 1. Das heißt, jedes Inkrement im Bereich ist einem Teil Strich zugeordnet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Häufigkeit der Teil Striche.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die TrackBar muss den TSB-Stil " [**\_ autoticks**](trackbar-control-styles.md) " aufweisen, um diese Meldung zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





