---
title: TVN_BEGINLABELEDIT Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements über den Anfang der Bezeichnungs Bearbeitung für ein Element. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- Windows-Steuerelemente für TVN_BEGINLABELEDIT Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34eccdeda553d0792a2862e3ca81a0889539d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338736"
---
# <a name="tvn_beginlabeledit-notification-code"></a>TVN \_ beginlabeledit-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements über den Anfang der Bezeichnungs Bearbeitung für ein Element. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) -Struktur. Das **Element Element** ist eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die gültige Informationen über das Element enthält, das in den Elementen **Hitem**, **State**, **LPARAM** und **pszText** bearbeitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um die Bezeichnungs Bearbeitung abzubrechen.

## <a name="remarks"></a>Bemerkungen

Wenn die Bezeichnungs Bearbeitung beginnt, wird ein Bearbeitungs Steuerelement erstellt, aber nicht positioniert oder angezeigt. Bevor es angezeigt wird, sendet das Strukturansicht-Steuerelement seinen übergeordneten Fenster einen TVN \_ beginlabeledit-Benachrichtigungs Code.

Zum Anpassen der Bezeichnungs Bearbeitung implementieren Sie einen Handler für TVN \_ beginlabeledit und senden eine [**TVM \_ geteditcontrol**](tvm-geteditcontrol.md) -Nachricht an das Strukturansicht-Steuerelement. Wenn eine Bezeichnung bearbeitet wird, ist der Rückgabewert ein Handle für das Bearbeitungs Steuerelement. Verwenden Sie dieses Handle, um das Bearbeitungs Steuerelement anzupassen, indem Sie die üblichen EM \_ xxx-Meldungen senden.

Wenn der Benutzer die Bearbeitung abbricht oder abschließt, empfängt das übergeordnete Fenster einen [TVN- \_ endlabeledit](tvn-endlabeledit.md) -Benachrichtigungs Code.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ Beginlabeleditw** (Unicode) und **TVN \_ beginlabeledita** (ANSI)<br/>     |



 

 





