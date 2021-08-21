---
title: PSN_QUERYINITIALFOCUS Benachrichtigungscode (Prsht.h)
description: Wird von einem Eigenschaftenblatt gesendet, um einer Eigenschaftenblattseite die Möglichkeit bereitzustellen, anzugeben, welches Dialogfeld-Steuerelement den anfänglichen Fokus erhalten soll. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- PSN_QUERYINITIALFOCUS Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- PSN_QUERYINITIALFOCUS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc82fe11893e728fbc9301868d9acdca5f7110bedfd37b4a16b473de0821f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169640"
---
# <a name="psn_queryinitialfocus-notification-code"></a>PSN \_ QUERYINITIALFOCUS-Benachrichtigungscode

Wird von einem Eigenschaftenblatt gesendet, um einer Eigenschaftenblattseite die Möglichkeit bereitzustellen, anzugeben, welches Dialogfeld-Steuerelement den anfänglichen Fokus erhalten soll. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**PSHNOTIFY-Struktur.**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) Umwandlung des **lParam-Members** dieser Struktur in einen **HWND-Typ,** um das Handle des Steuerelements abzurufen, das standardmäßig den Fokus erhält. Die -Struktur enthält eine [**NMHDR-Struktur**](/windows/desktop/api/richedit/ns-richedit-nmhdr) als erstes Element, **hdr.** Der **hwndFrom-Member** dieser **NMHDR-Struktur** enthält das Handle für das Eigenschaftenblatt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Um anzugeben, welches Steuerelement den Fokus erhalten soll, geben Sie das Handle des Steuerelements zurück. Andernfalls geben Sie 0 (null) zurück, und der Fokus wird an das Standardsteuerelement gerichtet. Um den Rückgabewert festzulegen, muss die Dialogfeldprozedur die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit einem **\_ DWL-MSGRESULT-Wert** aufrufen und **TRUE** zurückgeben.

## <a name="remarks"></a>Hinweise

Eine Anwendung darf die [**SetFocus-Funktion**](/windows/desktop/api/winuser/nf-winuser-setfocus) bei der Verarbeitung dieses Benachrichtigungscodes nicht aufrufen. Gibt das Handle des Steuerelements zurück, das den Fokus erhalten soll, und der Eigenschaftenblatt-Manager verarbeitet die Fokusänderung.

Der PSN \_ QUERYINITIALFOCUS-Benachrichtigungscode wird nicht gesendet, wenn der Eigenschaftenblatt-Manager feststellt, dass kein Steuerelement auf der Seite den Fokus erhalten soll.

Dieses Codefragment implementiert einen einfachen Handler für PSN \_ QUERYINITIALFOCUS. Er fordert an, dass der anfängliche Fokus auf das Standortsteuerelement **(IDC \_ LOCATION**) gelegt wird.

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> Dieser Benachrichtigungscode wird nicht unterstützt, wenn sie den Stil des Assistenten Für Dies verwendet wird ([**\_ PSHWIEWIESWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

