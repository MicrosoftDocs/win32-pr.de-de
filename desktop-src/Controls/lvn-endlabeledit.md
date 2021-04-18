---
title: LVN_ENDLABELEDIT Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements über das Ende der Bezeichnungs Bearbeitung für ein Element. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- Windows-Steuerelemente für LVN_ENDLABELEDIT Benachrichtigungs
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
ms.openlocfilehash: 1a33ab69a04202aeb3817d3eeadf01fb6f1fcaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341044"
---
# <a name="lvn_endlabeledit-notification-code"></a>LVN \_ endlabeledit-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements über das Ende der Bezeichnungs Bearbeitung für ein Element. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur. Das **Element Element** dieser Struktur ist eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, deren **iItem** -Member das Element identifiziert, das bearbeitet wird. Der **pszText** -Member des **Elements** enthält einen gültigen Wert, wenn der LVN \_ endlabeledit-Benachrichtigungs Code gesendet wird, unabhängig davon, ob das lvif- \_ textflag im **Mask** -Member der **lvitem** -Struktur festgelegt ist. Wenn der Benutzer die Bearbeitung abbricht, ist der **pszText** -Member der **lvitem** -Struktur **null**. Andernfalls ist **pszText** die Adresse des bearbeiteten Texts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der **pszText** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur nicht **null** ist, wird **true** zurückgegeben, um die Bezeichnung des Elements auf den bearbeiteten Text festzulegen. Gibt **false** zurück, um den bearbeiteten Text abzulehnen und zur ursprünglichen Bezeichnung zurückzukehren.

Wenn der **pszText** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur **null** ist, wird der Rückgabewert ignoriert.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert der Dialogfeld Prozedur ist, ob die Nachricht behandelt wurde. Der zweite Rückgabewert muss festgelegt werden, indem [**setwindowlongptr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) mit **DWLP_MSGRESULT** aufgerufen wird.

Wenn der Benutzer mit dem Bearbeiten einer Element Bezeichnung beginnt, empfängt das übergeordnete Fenster des Listenansicht-Steuer Elements einen [LVN \_ beginlabeledit](lvn-beginlabeledit.md) -Benachrichtigungs Code. Wenn der Benutzer die Bearbeitung abbricht oder abschließt, empfängt das übergeordnete Fenster einen LVN \_ endlabeledit-Benachrichtigungs Code.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVN \_ Endlabeleditw** (Unicode) und **LVN \_ endlabeledita** (ANSI)<br/>         |



 

 





