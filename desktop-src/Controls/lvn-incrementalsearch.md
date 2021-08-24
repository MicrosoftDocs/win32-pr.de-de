---
title: LVN_INCREMENTALSEARCH Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansichtssteuerelements, dass eine inkrementelle Suche gestartet wurde. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec3207fbb16bca23bf44ac61fee58bb6e4fad1ff74c38d7b56910ed52997f39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826120"
---
# <a name="lvn_incrementalsearch-notification-code"></a>LVN \_ INCREMENTALSEARCH-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Listenansichtssteuerelements, dass eine inkrementelle Suche gestartet wurde. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* \[ In\]
</dt> <dd>

Zeiger auf eine [**NMLVFINDITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) die den Benachrichtigungscode beschreibt. Der Aufrufer ist für die Zuordnung dieser Struktur verantwortlich, einschließlich der enthaltenen [**NMHDR-**](/windows/desktop/api/richedit/ns-richedit-nmhdr) und [**LVFINDINFO-Strukturen.**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) Legen Sie die Member der **NMHDR-Struktur** fest. Der **Codemember** muss auf LVN INCREMENTALSEARCH festgelegt \_ werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Der Benachrichtigungsempfänger castt *lParam,* um die [**NMLVFINDITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) abzurufen. Der *wParam-Parameter* enthält die ID des Steuerelements, das diesen Benachrichtigungscode sendet.

Dieser Benachrichtigungscode gibt einer Anwendung (oder dem Benachrichtigungsempfänger) die Möglichkeit, eine inkrementelle Suche anzupassen. Wenn die Suchelemente beispielsweise numerisch sind, kann die Anwendung anstelle einer Zeichenfolgensuche eine numerische Suche ausführen.

Die Anwendung legt den **lParam-Member** der [**LVFINDINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) in der [**NMLVFINDITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) auf das Ergebnis der Suche oder auf einen anderen von der Anwendung definierten Wert fest, um bei der Suche einen Fehler zu erzielen und dem Steuerelement anzugeben, wie fortzufahren ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl>   |
| Unicode- und ANSI-Name<br/>   | **LVN \_ INCREMENTALSEARCHW** (Unicode) und **LVN \_ INCREMENTALSEARCHA** (ANSI)<br/> |



 

 





