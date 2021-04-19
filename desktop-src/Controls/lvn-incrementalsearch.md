---
title: LVN_INCREMENTALSEARCH Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass eine inkrementelle Suche gestartet wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- Windows-Steuerelemente für LVN_INCREMENTALSEARCH Benachrichtigungs
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
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345534"
---
# <a name="lvn_incrementalsearch-notification-code"></a>LVN \_ IncrementalSearch-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass eine inkrementelle Suche gestartet wurde. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Zeiger auf eine [**nmlvfinditem**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) -Struktur, die den Benachrichtigungs Code beschreibt. Der Aufrufer ist dafür verantwortlich, diese Struktur zuzuordnen, einschließlich der enthaltenen [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -und [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) -Strukturen. Legen Sie die Member der **NMHDR** -Struktur fest. Der **Codemember** muss auf LVN \_ IncrementalSearch festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Der Benachrichtigungs Empfänger wandelt *LPARAM* ein, um die [**nmlvfinditem**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) -Struktur abzurufen. Der *wParam* -Parameter enthält die ID des Steuer Elements, das diesen Benachrichtigungs Code sendet.

Dieser Benachrichtigungs Code gibt einer Anwendung (oder dem Benachrichtigungs Empfänger) die Möglichkeit, eine inkrementelle Suche anzupassen. Wenn die Such Elemente beispielsweise numerisch sind, kann die Anwendung anstelle einer Zeichen folgen Suche eine numerische Suche durchführen.

Die Anwendung legt den **LPARAM** -Member der [**in der**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) [**nmlvfinditem**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) -Struktur enthaltenen vParam-Struktur auf das Ergebnis der Suche oder einen anderen Anwendungs definierten Wert fest, um die Suche zu misslingen und dem Steuerelement mitzuteilen, wie der Vorgang fortgesetzt werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl>   |
| Unicode- und ANSI-Name<br/>   | **LVN \_ Incrementalsearchw** (Unicode) und **LVN \_ incrementalsearcha** (ANSI)<br/> |



 

 





