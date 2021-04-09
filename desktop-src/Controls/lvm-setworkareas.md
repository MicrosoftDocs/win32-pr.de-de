---
title: LVM_SETWORKAREAS Meldung (kommstrg. h)
description: Legt die Arbeitsbereiche in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das ListView \_ setworkareas-Makro verwenden.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- Windows-Steuerelemente für LVM_SETWORKAREAS Meldung
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
ms.openlocfilehash: 4166238c97b5766a5f2bbb19e0de853526d83385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956979"
---
# <a name="lvm_setworkareas-message"></a>LVM- \_ setworkareas-Meldung

Legt die Arbeitsbereiche in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**ListView \_ setworkareas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der Strukturen im Array bei *LPRC*. Die maximal zulässige Anzahl von Arbeitsbereichen wird durch den Wert für die maximale Arbeitsbereiche von LV definiert \_ \_ .

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Array von [**Rect**](/previous-versions//dd162897(v=vs.85)) -Strukturen, die die neuen Arbeitsbereiche des Listenansicht-Steuer Elements enthalten. Werte in diesen Strukturen befinden sich in Client Koordinaten. Wenn dieser Parameter **null** ist, wird der Arbeitsbereich auf den Client Bereich des Steuer Elements festgelegt. *wParam* gibt die Anzahl der Strukturen in diesem Array an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von List-View Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

