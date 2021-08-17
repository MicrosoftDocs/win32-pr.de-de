---
title: LVM_GETWORKAREAS (Commctrl.h)
description: Ruft die Arbeitsbereiche aus einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das \_ ListView-Makro GetWorkAreas verwenden.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- LVM_GETWORKAREAS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aed6173ef00860900d7690199cfb2c81535f088790290e30cc01898666bb068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968230"
---
# <a name="lvm_getworkareas-message"></a>LVM \_ GETWORKAREAS-Nachricht

Ruft die Arbeitsbereiche aus einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**\_ ListView-Makro GetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der [**RECT-Strukturen**](/previous-versions//dd162897(v=vs.85)) im Array bei *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Array von [**RECT-Strukturen,**](/previous-versions//dd162897(v=vs.85)) die die aktuellen Arbeitsbereiche des Listenansicht-Steuerelements empfangen. Werte in diesen Strukturen befinden sich in Clientkoordinaten. *wParam* gibt die Anzahl der Strukturen in diesem Array an.

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

[Verwenden von List-View Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

