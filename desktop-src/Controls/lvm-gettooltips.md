---
title: LVM_GETTOOLTIPS Meldung (kommstrg. h)
description: Ruft das QuickInfo-Steuerelement ab, das vom Listenansicht-Steuerelement zum Anzeigen von Quick Infos verwendet wird. Sie können diese Nachricht explizit senden oder das ListView \_ gettooltips-Makro verwenden.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- Windows-Steuerelemente für LVM_GETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478510"
---
# <a name="lvm_gettooltips-message"></a>LVM \_ gettooltips-Meldung

Ruft das QuickInfo-Steuerelement ab, das vom Listenansicht-Steuerelement zum Anzeigen von Quick Infos verwendet wird. Sie können diese Nachricht explizit senden oder das [**ListView \_ gettooltips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle des QuickInfo-Steuer Elements zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LVM- \_ SetToolTips**](lvm-settooltips.md)
</dt> </dl>

 

 





