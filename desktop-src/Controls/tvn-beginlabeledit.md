---
title: TVN_BEGINLABELEDIT Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements über den Beginn der Bezeichnungsbearbeitung für ein Element. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- TVN_BEGINLABELEDIT Benachrichtigungscode Windows Steuerelementen
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
ms.openlocfilehash: e8fdd2b75ee9f3dcc46e5449c275eeea141162f3d31f524b64e114a623bd915e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060090"
---
# <a name="tvn_beginlabeledit-notification-code"></a>TVN \_ BEGINLABELEDIT-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements über den Beginn der Bezeichnungsbearbeitung für ein Element. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTVDISPINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) Das **Elementelement** ist eine [**TVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tvitema) die gültige Informationen über das Element enthält, das in den **Membern hItem**, **state,** **lParam** und **pszText bearbeitet** wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** um die Bezeichnungsbearbeitung abzubricht.

## <a name="remarks"></a>Hinweise

Wenn die Bearbeitung von Bezeichnungen beginnt, wird ein Bearbeitungssteuerzeichen erstellt, aber nicht positioniert oder angezeigt. Bevor es angezeigt wird, sendet das Strukturansicht-Steuerelement dem übergeordneten Fenster einen TVN \_ BEGINLABELEDIT-Benachrichtigungscode.

Implementieren Sie zum Anpassen der Bezeichnungsbearbeitung einen Handler für TVN BEGINLABELEDIT, und lassen Sie ihn eine \_ [**TVM \_ GETEDITCONTROL-Nachricht**](tvm-geteditcontrol.md) an das Strukturansicht-Steuerelement senden. Wenn eine Bezeichnung bearbeitet wird, ist der Rückgabewert ein Handle für das Bearbeitungssteuerzeichen. Verwenden Sie dieses Handle, um das Bearbeitungssteuerzeichen anzupassen, indem Sie die üblichen EM \_ XXX-Nachrichten senden.

Wenn der Benutzer die Bearbeitung abbricht oder abbricht, erhält das übergeordnete Fenster einen [TVN \_ ENDLABELEDIT-Benachrichtigungscode.](tvn-endlabeledit.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ BEGINLABELEDITW** (Unicode) und **TVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





