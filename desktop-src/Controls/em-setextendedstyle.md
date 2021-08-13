---
title: EM_SETEXTENDEDSTYLE-Nachricht (Commctrl.h)
description: Informiert das Bearbeitungssteuerelement, um erweiterte Stile festzulegen. Senden Sie diese Nachricht, oder verwenden Sie das Makro \_ SetExtendedStyle bearbeiten.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- EM_SETEXTENDEDSTYLE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 710ad6535bd7891f322a4bf02a5fed0f766dd97c2569fa5ec9b961478bf6a457
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673076"
---
# <a name="em_setextendedstyle-message"></a>EM \_ SETEXTENDEDSTYLE-Meldung

Informiert das Bearbeitungssteuerelement, um erweiterte Stile festzulegen. Senden Sie diese Nachricht, oder verwenden Sie das Makro [**\_ SetExtendedStyle bearbeiten.**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Maske, die zum Auswählen der festzulegenden Stile verwendet wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Wert, der den erweiterten Stil angibt. Weitere Informationen zu Stilen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Meldung erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die erweiterten Stile für ein Bearbeitungssteuerelement haben nichts mit den erweiterten Stilen zu tun, die mit der [**Funktion CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) oder [**der Funktion SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10, Version 1809 Nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2019-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

