---
title: PSN_WIZFINISH Benachrichtigungs Code (prsht. h)
description: Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die Schaltfläche Fertigstellen geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- Windows-Steuerelemente für PSN_WIZFINISH Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0654384b0944d90731288922c32326e42019cdc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477892"
---
# <a name="psn_wizfinish-notification-code"></a>\_Benachrichtigungs Code für PSN-witzfinish

Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die Schaltfläche **Fertig** stellen geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält. Diese Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt. Der **LPARAM** -Member der **pshnotify** -Struktur enthält keine Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

-   Gibt **true** zurück, um zu verhindern, dass der Assistent abgeschlossen wird.
-   [Version 5,80.](common-control-versions.md) und höher. Gibt ein Fenster Handle zurück, um zu verhindern, dass der Assistent abgeschlossen wird. Der Fokus wird auf das Fenster festgelegt. Das Fenster muss im Besitz der Assistenten Seite sein.
-   Gibt **false** zurück, damit der Assistent abgeschlossen werden kann.

## <a name="remarks"></a>Bemerkungen

Um den Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit dem DWL \_ msgresult-Wert verwenden, und die Dialogfeld Prozedur muss **true** zurückgeben.

[Version 5,80.](common-control-versions.md) Wenn die Anwendung **true** zurückgibt, um zu verhindern, dass ein Assistent beendet wird, hat Sie keine Kontrolle darüber, welches Fenster auf der Seite den Fokus erhält. Anwendungen, die den Abschluss eines Assistenten beenden müssen, sollten dies normalerweise tun, indem Sie das Fenster Handle auf der Assistenten Seite zurückgeben, das den Fokus erhalten soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

