---
title: RB_DRAGMOVE Meldung (kommstrg. h)
description: Aktualisiert die Zieh Position im Grund leisten-Steuerelement nach einer vorherigen RB \_ BeginDrag-Nachricht.
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- Windows-Steuerelemente für RB_DRAGMOVE Meldung
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8657d8f8f73c798f934262804dda83b359b0c0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956803"
---
# <a name="rb_dragmove-message"></a>RB \_ DragMove-Meldung

Aktualisiert die Zieh Position im Grund leisten-Steuerelement nach einer vorherigen [**RB \_ BeginDrag**](rb-begindrag.md) -Nachricht.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

**DWORD** -Wert, der die neuen Maus Koordinaten enthält. Die horizontale Koordinate ist im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthalten, und die vertikale Koordinate ist im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))enthalten. Wenn Sie (DWORD)-1 übergeben, verwendet das Grund leisten-Steuerelement die Position des Mauszeigers, wenn der Thread des Steuer Elements das letzte Mal den Thread [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) oder [**Peer-Message**](/windows/desktop/DevNotes/-peekmessage)aufgerufen hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

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

[**RB- \_ EndDrag**](rb-enddrag.md)
</dt> </dl>

 

