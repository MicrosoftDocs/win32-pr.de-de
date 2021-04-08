---
title: LVN_DELETEALLITEMS Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass alle Elemente im Steuerelement gelöscht werden. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- Windows-Steuerelemente für LVN_DELETEALLITEMS Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583ad6e2372649ab5f63bd208fb97b93b1591c12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957264"
---
# <a name="lvn_deleteallitems-notification-code"></a>LVN \_ DeleteAllItems-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass alle Elemente im Steuerelement gelöscht werden. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur. Das **iItem-Element** ist-1, und die anderen Member sind 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Um nachfolgende [LVN \_ DeleteItem](lvn-deleteitem.md) -Benachrichtigungs Codes zu unterdrücken, geben Sie **true** zurück

Um nachfolgende [LVN \_ DeleteItem](lvn-deleteitem.md) -Benachrichtigungs Codes zu erhalten, geben Sie **false** zurück.

## <a name="remarks"></a>Bemerkungen

Ein Listenansicht-Steuerelement sendet den [**LVM- \_ DeleteAllItems**](lvm-deleteallitems.md) -Benachrichtigungs Code, wenn er zerstört wird oder die **LVM \_ DeleteAllItems** -Nachricht empfängt. Wenn " **LVM \_ DeleteAllItems** " nicht " **true**" zurückgibt, sendet das Steuerelement auch einen [LVN \_ DeleteItem](lvn-deleteitem.md) -Benachrichtigungs Code, wenn jedes Element gelöscht wird.

Wenn sich der " [**LVM \_ DeleteAllItems**](lvm-deleteallitems.md) "-Nachrichten Handler in einer Dialogfeld Prozedur befindet, geben Sie " **true** " aus der Dialogfeld Prozedur zurück, und verwenden Sie die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit DWL \_ msgresult, um den Nachrichten Rückgabewert festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

