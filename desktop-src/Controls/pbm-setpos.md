---
title: PBM_SETPOS Meldung (kommstrg. h)
description: Legt die aktuelle Position für eine Statusanzeige fest und zeichnet den Balken neu, um die neue Position widerzuspiegeln.
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- Windows-Steuerelemente für PBM_SETPOS Meldung
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337530"
---
# <a name="pbm_setpos-message"></a>PBM- \_ SetPos-Nachricht

Legt die aktuelle Position für eine Statusanzeige fest und zeichnet den Balken neu, um die neue Position widerzuspiegeln.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ganzzahl mit Vorzeichen, die zur neuen Position wird.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Position zurück.

## <a name="remarks"></a>Bemerkungen

Wenn sich *wParam* außerhalb des Bereichs des Steuer Elements befindet, wird die Position auf die nächstgelegene Grenze festgelegt.

Senden Sie diese Nachricht nicht an ein Steuerelement, das den [**PSB- \_ Marquee**](progress-bar-control-styles.md) -Stil hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





