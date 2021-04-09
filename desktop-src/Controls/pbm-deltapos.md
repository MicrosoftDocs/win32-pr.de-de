---
title: PBM_DELTAPOS Meldung (kommstrg. h)
description: Verschiebt die aktuelle Position einer Statusleiste um ein angegebenes Inkrement und zeichnet den Balken neu, um die neue Position widerzuspiegeln.
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- Windows-Steuerelemente für PBM_DELTAPOS Meldung
topic_type:
- apiref
api_name:
- PBM_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d0c36bbfdf5a812c8a7ffb2b2cdda6720fb757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040799"
---
# <a name="pbm_deltapos-message"></a>PBM- \_ Delta POS-Nachricht

Verschiebt die aktuelle Position einer Statusleiste um ein angegebenes Inkrement und zeichnet den Balken neu, um die neue Position widerzuspiegeln.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Betrag, um die Position zu verschieben.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Position zurück.

## <a name="remarks"></a>Bemerkungen

Wenn das Inkrement zu einem Wert außerhalb des Bereichs des Steuer Elements führt, wird die Position auf die nächstgelegene Grenze festgelegt.

Das Verhalten dieser Nachricht ist nicht definiert, wenn Sie an ein Steuerelement gesendet wird, das den [**PSB- \_ Marquee**](progress-bar-control-styles.md) -Stil hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





