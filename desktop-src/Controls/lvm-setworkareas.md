---
title: LVM_SETWORKAREAS (Commctrl.h)
description: Legt die Arbeitsbereiche in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das \_ ListView-Makro SetWorkAreas verwenden.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- LVM_SETWORKAREAS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_SETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1060377fd9aec9014d18d206444355b052f4aafb796403e3e47fa92a0a7aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830661"
---
# <a name="lvm_setworkareas-message"></a>LVM \_ SETWORKAREAS-Meldung

Legt die Arbeitsbereiche in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**\_ ListView-Makro SetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der Strukturen im Array bei *lprc*. Die maximale Anzahl zulässiger Arbeitsbereiche wird durch den LV \_ MAX \_ WORKAREAS-Wert definiert.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Array von [**RECT-Strukturen,**](/previous-versions//dd162897(v=vs.85)) die die neuen Arbeitsbereiche des Listenansicht-Steuerelements enthalten. Werte in diesen Strukturen befinden sich in Clientkoordinaten. Wenn dieser Parameter **NULL ist,** wird der Arbeitsbereich auf den Clientbereich des Steuerelements festgelegt. *wParam* gibt die Anzahl der Strukturen in diesem Array an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Meldung wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verwenden List-View-Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

