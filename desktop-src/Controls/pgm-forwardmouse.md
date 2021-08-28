---
title: PGM_FORWARDMOUSE Nachricht (Commctrl.h)
description: Aktiviert oder deaktiviert die Mausweiterleitung für das Pagersteuerelement. Wenn die Mausweiterleitung aktiviert ist, leitet das Pager-Steuerelement WM \_ MOUSEMOVE-Meldungen an das enthaltene Fenster weiter. Sie können diese Nachricht explizit senden oder das Pager \_ ForwardMouse-Makro verwenden.
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- PGM_FORWARDMOUSE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 705b63ad39faea86e1f38a5b59dc73c6fc12f1e19fc17d0619c9a4b3dd5c6d26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046970"
---
# <a name="pgm_forwardmouse-message"></a>PGM \_ FORWARDMOUSE-Nachricht

Aktiviert oder deaktiviert die Mausweiterleitung für das Pagersteuerelement. Wenn die Mausweiterleitung aktiviert ist, leitet das Pager-Steuerelement [**WM \_ MOUSEMOVE-Meldungen**](/windows/desktop/inputdev/wm-mousemove) an das enthaltene Fenster weiter. Sie können diese Nachricht explizit senden oder das [**Pager \_ ForwardMouse-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**BOOL-Wert,** der bestimmt, ob die Mausweiterleitung aktiviert oder deaktiviert ist. Wenn dieser Wert ungleich 0 (null) ist, ist die Mausweiterleitung aktiviert. Wenn dieser Wert 0 (null) ist, ist die Mausweiterleitung deaktiviert.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

