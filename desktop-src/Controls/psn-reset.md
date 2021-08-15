---
title: PSN_RESET Benachrichtigungscode (Prsht.h)
description: Benachrichtigt eine Seite, dass das Eigenschaftenblatt zerstört werden soll. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- PSN_RESET Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb9f14b037d8757469497e644d870a887e6db36172b171f31b00d5615ff39532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409811"
---
# <a name="psn_reset-notification-code"></a>PSN \_ RESET-Benachrichtigungscode

Benachrichtigt eine Seite, dass das Eigenschaftenblatt zerstört werden soll. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**PSHNOTIFY-Struktur,**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) die Informationen zum Benachrichtigungscode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Alle Änderungen, die seit dem letzten [PSN \_ APPLY-Benachrichtigungscode](psn-apply.md) vorgenommen wurden, werden abgebrochen, mit Ausnahme von [**\_ PSHWIEWIZARD,**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)das diesen Benachrichtigungscode nicht unterstützt.

Der **lParam-Member** der [**PSHNOTIFY-Struktur,**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) auf den *lParam* zeigt, wird auf **TRUE** festgelegt, wenn der Benutzer auf die **X-Schaltfläche** in der oberen rechten Ecke des Eigenschaftenblatts geklickt hat. Der Wert ist **FALSE,** wenn der Benutzer auf die Schaltfläche **Abbrechen** geklickt hat. Die **PSHNOTIFY-Struktur** enthält eine [**NMHDR-Struktur**](/windows/desktop/api/richedit/ns-richedit-nmhdr) als erstes Element, **hdr**. Der **hwndFrom-Member** dieser **NMHDR-Struktur** enthält das Handle für das Eigenschaftenblatt.

Eine Anwendung kann diesen Benachrichtigungscode zum Ausführen von Bereinigungsvorgängen verwenden.

> [!Note]  
> Das Eigenschaftenblatt wird gerade bearbeitet, wenn der PSN \_ RESET-Benachrichtigungscode gesendet wird. Versuchen Sie bei der Verarbeitung dieses Benachrichtigungscodes nicht, Seiten hinzuzufügen, zu entfernen oder einzufügen. Dies führt zu unvorhersehbaren Ergebnissen.

 

Rufen Sie die [**EndDialog-Funktion**](/windows/desktop/api/winuser/nf-winuser-enddialog) nicht auf, wenn Sie diesen Benachrichtigungscode verarbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

