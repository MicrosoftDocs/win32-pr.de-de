---
title: TBM_SETPOS Meldung (kommstrg. h)
description: Legt die aktuelle logische Position des Schiebereglers in einer TrackBar fest.
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- Windows-Steuerelemente für TBM_SETPOS Meldung
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e8da6e8e231a26b216ca8f9314d59474384857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957215"
---
# <a name="tbm_setpos-message"></a>TBM- \_ SetPos-Nachricht

Legt die aktuelle logische Position des Schiebereglers in einer TrackBar fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu zeichnen. Wenn dieser Parameter **true** ist, zeichnet die Nachricht das Steuerelement mit dem Schieberegler an der Position, die von *LPARAM* angegeben wird. Wenn dieser Parameter **false** ist, wird der Schieberegler von der Nachricht nicht an der neuen Position neu gezeichnet. Beachten Sie, dass die Nachricht unabhängig vom *wParam* -Parameter den Wert der Schieberegler-Position festlegt (wie von der [**TBM- \_ GetPos**](tbm-getpos.md) -Nachricht zurückgegeben).

</dd> <dt>

*lParam* 
</dt> <dd>

Neue logische Position des Schiebereglers. Gültige logische Positionen sind die ganzzahligen Werte in der TrackBar-Bereich der minimalen bis maximalen Schieberegler-Positionen. Wenn dieser Wert außerhalb des maximalen und minimalen Bereichs des Steuer Elements liegt, wird die Position auf den maximalen oder minimalen Wert festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





