---
title: EM_GETEXTENDEDSTYLE Meldung (Commctrl.h)
description: Ruft den erweiterten Stil für ein Bearbeitungssteuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des \_ Makros GetExtendedStyle bearbeiten.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETEXTENDEDSTYLE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 77aa5827cc256c040d34ca24574dfa0b12816accaff9e5c0e92b4400195cae2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019668"
---
# <a name="em_getextendedstyle-message-commctrlh"></a>EM_GETEXTENDEDSTYLE Meldung (Commctrl.h)

Ruft den erweiterten Stil für ein Strukturansichtssteuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ GetExtendedStyle-Makros bearbeiten.**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert des erweiterten Stils zurück. Weitere Informationen zu Stilen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md).

## <a name="remarks"></a>Hinweise

Die erweiterten Stile für ein Bearbeitungssteuerelement haben nichts mit den erweiterten Stilen zu tun, die mit der [**Funktion CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) oder [**der Funktion SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10, Version 1809 Nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2019-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

