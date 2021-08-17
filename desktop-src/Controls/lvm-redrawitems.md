---
title: LVM_REDRAWITEMS (Commctrl.h)
description: Erzwingt, dass ein Listenansicht-Steuerelement einen Bereich von Elementen neu gezeichnet. Sie können diese Nachricht explizit oder mit dem ListView \_ RedrawItems-Makro senden.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- LVM_REDRAWITEMS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53fbee43ff8cfcbb14ab357b6e76ab709df3e4a797143d5c4fa2c9b1179153af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261730"
---
# <a name="lvm_redrawitems-message"></a>LVM \_ REDRAWITEMS-Nachricht

Erzwingt, dass ein Listenansicht-Steuerelement einen Bereich von Elementen neu gezeichnet. Sie können diese Nachricht explizit oder mit dem [**ListView \_ RedrawItems-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des ersten elements, das neu gezeichnet werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Index des letzten elements, das neu gezeichnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Die angegebenen Elemente werden erst neu gezeichnet, wenn das Listenansichtsfenster eine [**WM \_ PAINT-Nachricht**](/windows/desktop/gdi/wm-paint) empfängt, die neu gezeichnet werden soll. Rufen Sie die [**UpdateWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-updatewindow) auf, nachdem Sie dieses Makro verwendet haben, um sofort neu zu bemalen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

