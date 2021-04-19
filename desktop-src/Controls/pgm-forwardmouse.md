---
title: PGM_FORWARDMOUSE Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert die Maus Weiterleitung für das Pager-Steuerelement. Wenn die Maus Weiterleitung aktiviert ist, leitet das Pager-Steuerelement WM- \_ MouseMove-Nachrichten an das enthaltene Fenster weiter. Sie können diese Nachricht explizit senden oder das Pager- \_ forwardmouse-Makro verwenden.
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- Windows-Steuerelemente für PGM_FORWARDMOUSE Meldung
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: addc1c6bf762f540e9d7d785a5af2ba3fb7da93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345312"
---
# <a name="pgm_forwardmouse-message"></a>PGM \_ forwardmouse-Nachricht

Aktiviert oder deaktiviert die Maus Weiterleitung für das Pager-Steuerelement. Wenn die Maus Weiterleitung aktiviert ist, leitet das Pager-Steuerelement [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachrichten an das enthaltene Fenster weiter. Sie können diese Nachricht explizit senden oder das [**Pager- \_ forwardmouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**Boolescher** Wert, der bestimmt, ob die Maus Weiterleitung aktiviert oder deaktiviert ist. Wenn dieser Wert ungleich 0 (null) ist, wird die Maus Weiterleitung aktiviert. Wenn dieser Wert 0 (null) ist, wird die Maus Weiterleitung deaktiviert.

</dd> <dt>

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



 

