---
title: LVM_GETTOOLTIPS Meldung (Commctrl.h)
description: Ruft das QuickInfo-Steuerelement ab, das vom Listenansicht-Steuerelement zum Anzeigen von QuickInfos verwendet wird. Sie können diese Nachricht explizit senden oder das ListView \_ GetToolTips-Makro verwenden.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- LVM_GETTOOLTIPS Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: a6ca4340a8c57c6551d3c46f9324e4b66250f383c9412a3772df3114f105c5f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019288"
---
# <a name="lvm_gettooltips-message"></a>LVM \_ GETTOOLTIPS-Nachricht

Ruft das QuickInfo-Steuerelement ab, das vom Listenansicht-Steuerelement zum Anzeigen von QuickInfos verwendet wird. Sie können diese Nachricht explizit senden oder das [**ListView \_ GetToolTips-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle des QuickInfo-Steuerelements zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LVM \_ SETTOOLTIPS**](lvm-settooltips.md)
</dt> </dl>

 

 





