---
title: EM_GETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Ruft den erweiterten Stil für ein Bearbeitungs Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des \_ Makros GetExtendedStyle bearbeiten.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Windows-Steuerelemente für EM_GETEXTENDEDSTYLE Meldung
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
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477922"
---
# <a name="em_getextendedstyle-message-commctrlh"></a>EM_GETEXTENDEDSTYLE Meldung (kommstrg. h)

Ruft den erweiterten Stil für ein Strukturansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des [**Makros \_ GetExtendedStyle bearbeiten**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) .

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert des erweiterten Stils zurück. Weitere Informationen zu Stilen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md).

## <a name="remarks"></a>Bemerkungen

Die erweiterten Stile für ein Bearbeitungs Steuerelement haben nichts mit den erweiterten Stilen zu tun, die mit der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " oder der Funktion " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)" verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809, \[ nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2019 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

