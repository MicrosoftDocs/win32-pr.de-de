---
title: LVM_SETTOOLTIPS Meldung (kommstrg. h)
description: Legt das QuickInfo-Steuerelement fest, das vom Listenansicht-Steuerelement zum Anzeigen von Quick Infos verwendet wird. Sie können diese Nachricht explizit senden oder das ListView \_ SetToolTips-Makro verwenden.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- Windows-Steuerelemente für LVM_SETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff749c24a35cf73de2d75b8a3b516197b57aac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476074"
---
# <a name="lvm_settooltips-message"></a>LVM- \_ SetToolTips-Meldung

Legt das QuickInfo-Steuerelement fest, das vom Listenansicht-Steuerelement zum Anzeigen von Quick Infos verwendet wird. Sie können diese Nachricht explizit senden oder das [**ListView \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Handle für das festzulegende QuickInfo-Steuerelement.</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das vorherige QuickInfo-Steuerelement zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LVM \_ gettooltips**](lvm-gettooltips.md)
</dt> </dl>

 

 





