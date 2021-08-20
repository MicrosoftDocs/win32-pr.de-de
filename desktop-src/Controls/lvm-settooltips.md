---
title: LVM_SETTOOLTIPS Nachricht (Commctrl.h)
description: Legt das QuickInfo-Steuerelement fest, das vom Listenansicht-Steuerelement zum Anzeigen von QuickInfos verwendet wird. Sie können diese Nachricht explizit senden oder das ListView \_ SetToolTips-Makro verwenden.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- LVM_SETTOOLTIPS Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 7bf2256d94630b8e792fd1f148864f3588b27e73ea5781eb0bdcd24bf9571507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170396"
---
# <a name="lvm_settooltips-message"></a>LVM \_ SETTOOLTIPS-Nachricht

Legt das QuickInfo-Steuerelement fest, das vom Listenansicht-Steuerelement zum Anzeigen von QuickInfos verwendet wird. Sie können diese Nachricht explizit senden oder das [**ListView \_ SetToolTips-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Handle für das festzulegende QuickInfo-Steuerelement.</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle zum vorherigen QuickInfo-Steuerelement zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LVM \_ GETTOOLTIPS**](lvm-gettooltips.md)
</dt> </dl>

 

 





