---
title: TVM_GETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Ruft den erweiterten Stil für ein Strukturansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des TreeView \_ GetExtendedStyle-Makros.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- Windows-Steuerelemente für TVM_GETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a00e125389ff56c7ff93370ab71945598dba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859234"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a>TVM_GETEXTENDEDSTYLE Meldung (kommstrg. h)

Ruft den erweiterten Stil für ein Strukturansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des [**TreeView \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert des erweiterten Stils zurück. Weitere Informationen zu Stilen finden Sie Unterstruktur [Ansicht-Steuerelement erweiterte Stile](tree-view-control-window-extended-styles.md).

## <a name="remarks"></a>Bemerkungen

Die erweiterten Stile für ein Strukturansicht-Steuerelement haben nichts mit den erweiterten Stilen zu tun, die mit der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " oder der Funktion " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)" verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

