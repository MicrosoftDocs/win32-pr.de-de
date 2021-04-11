---
title: LVM_GETVIEWRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck aller Elemente im Listenansicht-Steuerelement ab. Die Listenansicht muss in der Symbol Ansicht oder in der kleinen Symbol Ansicht angezeigt werden. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetViewRect-Makros senden.
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- Windows-Steuerelemente für LVM_GETVIEWRECT Meldung
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d4c4fdf0e8466d3fb0b2ad164241c3f6a541570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040886"
---
# <a name="lvm_getviewrect-message"></a>LVM \_ GetViewRect-Nachricht

Ruft das umgebende Rechteck aller Elemente im Listenansicht-Steuerelement ab. Die Listenansicht muss in der Symbol Ansicht oder in der kleinen Symbol Ansicht angezeigt werden. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das umschließende Rechteck empfängt. Alle Koordinaten sind relativ zum sichtbaren Bereich des Listenansicht-Steuer Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

