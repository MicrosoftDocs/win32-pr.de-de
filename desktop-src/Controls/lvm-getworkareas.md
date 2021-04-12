---
title: LVM_GETWORKAREAS Meldung (kommstrg. h)
description: Ruft die Arbeitsbereiche aus einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das ListView \_ getworkareas-Makro verwenden.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- Windows-Steuerelemente für LVM_GETWORKAREAS Meldung
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
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478504"
---
# <a name="lvm_getworkareas-message"></a>LVM \_ getworkareas-Meldung

Ruft die Arbeitsbereiche aus einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**ListView \_ getworkareas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der [**Rect**](/previous-versions//dd162897(v=vs.85)) -Strukturen im Array bei *LPARAM*.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein Array von [**Rect**](/previous-versions//dd162897(v=vs.85)) -Strukturen, die die aktuellen Arbeitsbereiche des Listenansicht-Steuer Elements empfangen. Werte in diesen Strukturen befinden sich in Client Koordinaten. *wParam* gibt die Anzahl der Strukturen in diesem Array an.

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

 

