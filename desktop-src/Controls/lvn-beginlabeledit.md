---
title: LVN_BEGINLABELEDIT Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements über den Anfang der Bezeichnungs Bearbeitung für ein Element. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- Windows-Steuerelemente für LVN_BEGINLABELEDIT Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f77550b474534cee096b610a0805bce547d9b429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949460"
---
# <a name="lvn_beginlabeledit-notification-code"></a>LVN \_ beginlabeledit-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements über den Anfang der Bezeichnungs Bearbeitung für ein Element. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur. Das **Element Element** dieser Struktur ist eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, deren **iItem** -Member das Element identifiziert, das bearbeitet wird. Beachten Sie, dass unter Elemente nicht bearbeitet werden können. der **iSubItem** -Member ist immer auf 0 (null) festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Um dem Benutzer die Bearbeitung der Bezeichnung zu ermöglichen, geben Sie **false** zurück.

Um zu verhindern, dass der Benutzer die Bezeichnung bearbeitet, geben Sie " **true**" zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die Bezeichnungs Bearbeitung beginnt, wird ein Bearbeitungs Steuerelement erstellt, positioniert und initialisiert. Bevor es angezeigt wird, sendet das Listenansicht-Steuerelement seinen übergeordneten Fenster einen LVN \_ beginlabeledit-Benachrichtigungs Code.

Implementieren Sie zum Anpassen der Bezeichnungs Bearbeitung einen Handler für LVN \_ beginlabeledit, und senden Sie eine [**LVM \_ geteditcontrol**](lvm-geteditcontrol.md) -Nachricht an das Listenansicht-Steuerelement. Wenn eine Bezeichnung bearbeitet wird, ist der Rückgabewert ein Handle für das Bearbeitungs Steuerelement. Verwenden Sie dieses Handle, um das Bearbeitungs Steuerelement anzupassen, indem Sie die üblichen **EM \_ xxx** -Meldungen senden.

Wenn der Benutzer die Bearbeitung abbricht oder abschließt, empfängt das übergeordnete Fenster einen [LVN \_ endlabeledit](lvn-endlabeledit.md) -Benachrichtigungs Code.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVN \_ Beginlabeleditw** (Unicode) und **LVN \_ beginlabeledita** (ANSI)<br/>     |



 

 





