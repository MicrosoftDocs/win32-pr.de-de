---
title: PSN_APPLY Benachrichtigungs Code (prsht. h)
description: Wird an jede Seite im Eigenschaften Blatt gesendet, um anzugeben, dass der Benutzer auf die Schaltfläche "OK", "Schließen" oder "übernehmen" geklickt hat und alle Änderungen wirksam werden sollen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- Windows-Steuerelemente für PSN_APPLY Benachrichtigungs
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
ms.openlocfilehash: 13d8206b4e423fb01be3277a9dd0ca3a49b59129
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477547"
---
# <a name="psn_apply-notification-code"></a>\_Benachrichtigungs Code für PSN-Anwendung

Wird an jede Seite im Eigenschaften Blatt gesendet, um anzugeben, dass der Benutzer auf die Schaltfläche "OK", "Schließen" oder "übernehmen" geklickt hat und alle Änderungen wirksam werden sollen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code einschließlich der ID der Seite enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Legen Sie psnret \_ noError fest, um anzugeben, dass die an dieser Seite vorgenommenen Änderungen gültig sind und angewendet wurden. Wenn alle Seiten psnret \_ noError festlegen, kann das Eigenschaften Blatt zerstört werden. Um anzugeben, dass die an dieser Seite vorgenommenen Änderungen ungültig sind, und um zu verhindern, dass das Eigenschaften Blatt zerstört wird, legen Sie einen der folgenden Rückgabewerte fest:

-   psnret ist \_ ungültig. Das Eigenschaften Blatt wird nicht zerstört, und der Fokus wird auf diese Seite zurückgegeben.
-   psnret \_ ungültige \_ nochangepage. Das Eigenschaften Blatt wird nicht zerstört, und der Fokus wird auf die Seite zurückgegeben, die den Fokus hatte, als die Schaltfläche gedrückt wurde.

Um den Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die Funktion [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit dem DWL \_ -Wert msgresult aufrufen, und die Dialogfeld Prozedur muss **true** zurückgeben.

## <a name="remarks"></a>Bemerkungen

Wenn der Benutzer auf die Schaltfläche OK, übernehmen oder schließen klickt, sendet das Eigenschaften Blatt eine [PSN- \_ killactive](psn-killactive.md) -Benachrichtigung an die aktive Seite und gibt dadurch die Möglichkeit, die Änderungen des Benutzers zu überprüfen. Wenn die Änderungen gültig sind, sendet das Eigenschaften Blatt einen "PSN Apply"- \_ Benachrichtigungs Code auf jede Seite und leitet ihn so um, dass die neuen Eigenschaften auf das entsprechende Element angewendet werden.

> [!Note]  
> Das Eigenschaften Blatt bearbeitet die Liste der Seiten, wenn der \_ Benachrichtigungs Code "PSN Apply" gesendet wird. Versuchen Sie nicht, Seiten hinzuzufügen, zu entfernen oder einzufügen, während Sie diese Benachrichtigung verarbeiten. Dies führt zu unvorhersehbaren Ergebnissen.

 

Der **LPARAM** -Member der [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, auf die von *LPARAM* verwiesen wird, ist auf **true** festgelegt, wenn der Benutzer auf die Schaltfläche OK klickt. Sie wird auch auf " **true** " festgelegt, wenn die [**PSM \_ canceldeclose**](psm-canceltoclose.md) -Nachricht gesendet wurde und der Benutzer auf die Schaltfläche "Schließen" klickt. Der Wert ist auf **false** festgelegt, wenn der Benutzer auf die Schaltfläche übernehmen klickt.

Die [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt.

Beim Verarbeiten dieses Benachrichtigungs Codes dürfen Sie die [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) -Funktion nicht aufzurufen.

Ein modales Eigenschaften Blatt wird zerstört, wenn der Benutzer auf die Schaltfläche OK klickt und jede Seite den Wert psnret \_ noError als Antwort auf **PSN \_ Apply** zurückgibt. Wenn eine Seite "psnret \_ invalid" oder "psnret \_ ungültige \_ nochangepage" zurückgibt, wird der Apply-Prozess sofort abgebrochen. Seiten, die auf der Abbruch Seite stehen, erhalten keinen PSN- \_ Benachrichtigungs Code.

Um diesen Benachrichtigungs Code zu erhalten, muss eine Seite den DWL- \_ msgresult-Wert als Antwort auf den Benachrichtigungs Code " [PSN \_ killactive](psn-killactive.md) " auf " **false** " festlegen.

> [!Note]  
> Dieser Benachrichtigungs Code wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

