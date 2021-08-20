---
title: LVN_ENDLABELEDIT Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuerelements über das Ende der Bezeichnungsbearbeitung für ein Element. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- LVN_ENDLABELEDIT Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- LVN_ENDLABELEDIT
- LVN_ENDLABELEDITA
- LVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060855b858a4539be7d786a0d4de8764f6aec543568b8c270248e398eed92ee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005691"
---
# <a name="lvn_endlabeledit-notification-code"></a>LVN \_ ENDLABELEDIT-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuerelements über das Ende der Bezeichnungsbearbeitung für ein Element. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLVDISPINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) Das **Elementelement** dieser Struktur ist eine [**LVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deren **iItem-Member** das bearbeitete Element identifiziert. Das **pszText-Element** des Elements enthält einen gültigen Wert, wenn der LVN ENDLABELEDIT-Benachrichtigungscode gesendet wird, unabhängig davon, ob das LVIF TEXT-Flag im Maskenelement der  \_ \_ **LVITEM-Struktur festgelegt** ist.  Wenn der Benutzer die Bearbeitung abbricht, ist das **pszText-Member** der **LVITEM-Struktur** **NULL.** **andernfalls ist pszText** die Adresse des bearbeiteten Texts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der **pszText-Member** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) nicht **NULL** ist, geben Sie **TRUE** zurück, um die Bezeichnung des Elements auf den bearbeiteten Text zu setzen. Geben **Sie FALSE** zurück, um den bearbeiteten Text abzulehnen und zur ursprünglichen Bezeichnung zurückzukehren.

Wenn der **pszText-Member** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) **NULL ist,** wird der Rückgabewert ignoriert.

## <a name="remarks"></a>Hinweise

Der Rückgabewert der Dialogprozedur ist, ob die Nachricht behandelt wurde. Der zweite Rückgabewert muss durch Aufrufen von [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) **mit** DWLP_MSGRESULT.

Wenn der Benutzer mit der Bearbeitung einer Elementbezeichnung beginnt, empfängt das übergeordnete Fenster des Listenansicht-Steuerelements einen [LVN \_ BEGINLABELEDIT-Benachrichtigungscode.](lvn-beginlabeledit.md) Wenn der Benutzer die Bearbeitung abbricht oder abbricht, erhält das übergeordnete Fenster einen LVN \_ ENDLABELEDIT-Benachrichtigungscode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVN \_ ENDLABELEDITW** (Unicode) und **LVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





