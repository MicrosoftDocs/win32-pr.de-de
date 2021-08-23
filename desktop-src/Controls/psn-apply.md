---
title: PSN_APPLY Benachrichtigungscode (Prsht.h)
description: Wird an jede Seite im Eigenschaftenblatt gesendet, um anzugeben, dass der Benutzer auf die Schaltfläche OK, Schließen oder Übernehmen geklickt hat und alle Änderungen wirksam werden soll. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- PSN_APPLY Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- PSN_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 522d4a0ea52f4cee495e689e8f0cdc91d7362ec3a1ee37ab81a911bc980d3209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410036"
---
# <a name="psn_apply-notification-code"></a>PSN \_ APPLY-Benachrichtigungscode

Wird an jede Seite im Eigenschaftenblatt gesendet, um anzugeben, dass der Benutzer auf die Schaltfläche OK, Schließen oder Übernehmen geklickt hat und alle Änderungen wirksam werden soll. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**PSHNOTIFY-Struktur,**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) die Informationen zum Benachrichtigungscode enthält, einschließlich der ID der Seite.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Legen Sie PSNRET \_ NOERROR fest, um anzugeben, dass die an dieser Seite vorgenommenen Änderungen gültig sind und angewendet wurden. Wenn alle Seiten PSNRET \_ NOERROR festlegen, kann das Eigenschaftenblatt zerstört werden. Um anzugeben, dass die an dieser Seite vorgenommenen Änderungen ungültig sind, und um zu verhindern, dass das Eigenschaftenblatt zerstört wird, legen Sie einen der folgenden Rückgabewerte fest:

-   PSNRET \_ UNGÜLTIG. Das Eigenschaftenblatt wird nicht zerstört, und der Fokus wird auf diese Seite zurückgegeben.
-   PSNRET \_ INVALID \_ NOCHANGEPAGE. Das Eigenschaftenblatt wird nicht zerstört, und der Fokus wird auf die Seite zurückgegeben, die den Fokus hatte, als die Schaltfläche gedrückt wurde.

Um den Rückgabewert festzulegen, muss die Dialogfeldprozedur für die Seite die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit dem \_ DWL-MSGRESULT-Wert aufrufen, und die Dialogfeldprozedur muss **TRUE** zurückgeben.

## <a name="remarks"></a>Hinweise

Wenn der Benutzer auf die Schaltfläche OK, Übernehmen oder Schließen klickt, sendet das Eigenschaftenblatt eine [PSN \_ KILLACTIVE-Benachrichtigung](psn-killactive.md) an die aktive Seite, sodass die Änderungen des Benutzers überprüft werden können. Wenn die Änderungen gültig sind, sendet das Eigenschaftenblatt einen PSN \_ APPLY-Benachrichtigungscode an jede Seite und weist sie an, die neuen Eigenschaften auf das entsprechende Element anzuwenden.

> [!Note]  
> Das Eigenschaftenblatt wird gerade bearbeitet, wenn der PSN \_ APPLY-Benachrichtigungscode gesendet wird. Versuchen Sie nicht, Seiten hinzuzufügen, zu entfernen oder einzufügen, während Sie diese Benachrichtigung behandeln. Dies führt zu unvorhersehbaren Ergebnissen.

 

Das **lParam-Element** der [**PSHNOTIFY-Struktur,**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) auf das *lParam* zeigt, wird auf **TRUE** festgelegt, wenn der Benutzer auf die Schaltfläche OK klickt. Sie wird auch auf **TRUE** festgelegt, wenn die [**PSM \_ CANCELTOCLOSE-Nachricht**](psm-canceltoclose.md) gesendet wurde und der Benutzer auf die Schaltfläche Schließen klickt. Sie wird auf **FALSE** festgelegt, wenn der Benutzer auf die Schaltfläche Anwenden klickt.

Die [**PSHNOTIFY-Struktur**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) enthält eine [**NMHDR-Struktur**](/windows/desktop/api/richedit/ns-richedit-nmhdr) als erstes Element, **hdr**. Der **hwndFrom-Member** dieser **NMHDR-Struktur** enthält das Handle für das Eigenschaftenblatt.

Rufen Sie die [**EndDialog-Funktion**](/windows/desktop/api/winuser/nf-winuser-enddialog) nicht auf, wenn Sie diesen Benachrichtigungscode verarbeiten.

Ein modales Eigenschaftenblatt wird zerstört, wenn der Benutzer auf die Schaltfläche OK klickt und jede Seite den PSNRET \_ NOERROR-Wert als Antwort auf **PSN \_ APPLY** zurückgibt. Wenn eine Seite PSNRET \_ INVALID oder PSNRET \_ INVALID \_ NOCHANGEPAGE zurückgibt, wird der Apply-Prozess sofort abgebrochen. Seiten nach der Abbruchseite erhalten keinen PSN \_ APPLY-Benachrichtigungscode.

Um diesen Benachrichtigungscode zu erhalten, muss eine Seite den \_ DWL-MSGRESULT-Wert als Antwort auf den [PSN KILLACTIVE-Benachrichtigungscode \_](psn-killactive.md) auf **FALSE** festlegen.

> [!Note]  
> Dieser Benachrichtigungscode wird nicht unterstützt, wenn sie den Stil des Assistenten Für Dies verwendet wird ([**\_ PSHWIEWIESWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

