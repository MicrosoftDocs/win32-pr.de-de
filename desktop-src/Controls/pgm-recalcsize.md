---
title: PGM_RECALCSIZE Meldung (kommstrg. h)
description: Erzwingt die Neuberechnung der Größe des enthaltenen Fensters durch das Pager-Steuerelement. Das Senden dieser Nachricht führt dazu, dass eine PGN \_ calcsize-Benachrichtigung gesendet wird. Sie können diese Nachricht explizit senden oder das Pager \_ recalcsize-Makro verwenden.
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- Windows-Steuerelemente für PGM_RECALCSIZE Meldung
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407221543a42b4dbff4490508a02b570622d69c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476311"
---
# <a name="pgm_recalcsize-message"></a>PGM- \_ Nachricht "recalcsize"

Erzwingt die Neuberechnung der Größe des enthaltenen Fensters durch das Pager-Steuerelement. Das Senden dieser Nachricht führt dazu, dass eine [PGN \_ calcsize](pgn-calcsize.md) -Benachrichtigung gesendet wird. Sie können diese Nachricht explizit senden oder das [**Pager \_ recalcsize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





