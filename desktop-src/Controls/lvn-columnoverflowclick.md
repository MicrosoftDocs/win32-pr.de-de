---
title: LVN_COLUMNOVERFLOWCLICK Benachrichtigungscode (Commctrl.h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn auf die Überlaufschaltfläche geklickt wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 3d3bb7be-b598-450a-b829-a5aa5b1a0c5d
keywords:
- LVN_COLUMNOVERFLOWCLICK Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- LVN_COLUMNOVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb28deb3dd98542791b4c8daf350e618e43db57d5090a93d49af5e55e8b39ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077120"
---
# <a name="lvn_columnoverflowclick-notification-code"></a>LVN \_ COLUMNOVERFLOWCLICK-Benachrichtigungscode

Wird von einem Listenansicht-Steuerelement gesendet, wenn auf die Überlaufschaltfläche geklickt wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_COLUMNOVERFLOWCLICK
     
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* \[ In\]
</dt> <dd>

Zeiger auf eine [**NMLISTVIEW-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) die den Benachrichtigungscode beschreibt. Der Aufrufer ist für die Zuweisung dieser Struktur verantwortlich, einschließlich der enthaltenen [**NMHDR-Struktur.**](/windows/desktop/api/richedit/ns-richedit-nmhdr) Legen Sie die Member der **NMHDR-Struktur** fest. Der **Code** member muss auf LVN \_ COLUMNOVERFLOWCLICK festgelegt werden.

Legen Sie **den iItem-Member** der [**NMLISTVIEW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) auf -1 fest. Legen Sie **das iSubItem-Member** auf den Index des Unteritems fest. Legen Sie **die Member uNewState,** **uOldState** und **lParam** auf 0 fest. Die verbleibenden Member der **NMLISTVIEW-Struktur** werden nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Der Benachrichtigungsempfänger casts *lParam,* um die [**NMLISTVIEW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) abzurufen. Der *wParam-Parameter* enthält die ID des Steuerelements, das den Benachrichtigungscode sendet.

Wenn ein Headersteuersatz ein untergeordnetes Steuerelement der Listview ist, sollte das Headersteuersteuersystem diesen Benachrichtigungscode an das Listview-Steuerelement senden, wenn das Headersteuersteuersatz den [HDN OVERFLOWCLICK-Benachrichtigungscode \_ ](hdn-overflowclick.md) empfängt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





