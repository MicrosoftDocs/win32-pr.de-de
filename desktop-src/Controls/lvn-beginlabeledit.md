---
title: LVN_BEGINLABELEDIT Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansichtssteuerelements über den Beginn der Bearbeitung von Bezeichnungen für ein Element. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- LVN_BEGINLABELEDIT Benachrichtigungscode Windows Controls
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
ms.openlocfilehash: ab5b5ecfed8fdc15ec2779e204d01b0375c7da702e2a2e9fe8a3cdc3b178b0fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830651"
---
# <a name="lvn_beginlabeledit-notification-code"></a>LVN \_ BEGINLABELEDIT-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Listenansichtssteuerelements über den Beginn der Bearbeitung von Bezeichnungen für ein Element. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLVDISPINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) Der **Elementmember** dieser Struktur ist eine [**LVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deren **iItem-Member** das zu bearbeitende Element identifiziert. Beachten Sie, dass Unteritems nicht bearbeitet werden können. Der **iSubItem-Member** ist immer auf 0 (null) festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Damit der Benutzer die Bezeichnung bearbeiten kann, geben Sie **FALSE zurück.**

Um zu verhindern, dass der Benutzer die Bezeichnung bearbeitet, geben Sie **TRUE** zurück.

## <a name="remarks"></a>Hinweise

Wenn die Bearbeitung von Bezeichnungen beginnt, wird ein Bearbeitungssteuerelement erstellt, positioniert und initialisiert. Bevor es angezeigt wird, sendet das Listenansichtssteuerelement seinem übergeordneten Fenster einen LVN \_ BEGINLABELEDIT-Benachrichtigungscode.

Implementieren Sie zum Anpassen der Bearbeitung von Bezeichnungen einen Handler für LVN \_ BEGINLABELEDIT, und senden Sie eine [**LVM \_ GETEDITCONTROL-Nachricht**](lvm-geteditcontrol.md) an das Listenansichtssteuerelement. Wenn eine Bezeichnung bearbeitet wird, ist der Rückgabewert ein Handle für das Bearbeitungssteuerelement. Verwenden Sie dieses Handle, um das Bearbeitungssteuerelement anzupassen, indem Sie die üblichen **EM \_ XXX-Nachrichten** senden.

Wenn der Benutzer die Bearbeitung abbricht oder abschließt, empfängt das übergeordnete Fenster einen [LVN \_ ENDLABELEDIT-Benachrichtigungscode.](lvn-endlabeledit.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVN \_ BEGINLABELEDITW** (Unicode) und **LVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





