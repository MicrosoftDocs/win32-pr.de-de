---
title: PSN_QUERYINITIALFOCUS Benachrichtigungs Code (prsht. h)
description: Wird von einem Eigenschaften Blatt gesendet, um der Seite eines Eigenschaften Blatts anzugeben, welches Dialogfeld-Steuerelement den Anfangs Fokus erhalten soll. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- Windows-Steuerelemente für PSN_QUERYINITIALFOCUS Benachrichtigungs
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
ms.openlocfilehash: bc542332440009f6564f384b415657e725edda00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102974"
---
# <a name="psn_queryinitialfocus-notification-code"></a>PSN \_ queryinitialfocus-Benachrichtigungs Code

Wird von einem Eigenschaften Blatt gesendet, um der Seite eines Eigenschaften Blatts anzugeben, welches Dialogfeld-Steuerelement den Anfangs Fokus erhalten soll. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur. Wandelt den **LPARAM** -Member dieser-Struktur in einen **HWND** -Typ um, um das Handle des Steuer Elements abzurufen, dem der Fokus standardmäßig zugewiesen wird. Die Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Um anzugeben, welches Steuerelement den Fokus erhalten soll, geben Sie das Handle des Steuer Elements zurück. Andernfalls wird NULL zurückgegeben, und der Fokus wird auf das Standard Steuerelement zurückgesetzt. Um den Rückgabewert festzulegen, muss die Dialogfeld Prozedur die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit einem **DWL- \_ msgresult** -Wert aufrufen und **true** zurückgeben.

## <a name="remarks"></a>Bemerkungen

Bei der Verarbeitung dieses Benachrichtigungs Codes darf eine Anwendung die [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) -Funktion nicht aufrufen. Gibt das Handle des Steuer Elements zurück, das den Fokus erhalten soll, und der Eigenschaften Blatt-Manager behandelt die Fokus Änderung.

Der "PSN \_ queryinitialfocus"-Benachrichtigungs Code wird nicht gesendet, wenn der Eigenschaften Blatt-Manager feststellt, dass kein Steuerelement auf der Seite den Fokus erhalten soll.

Dieses Code Fragment implementiert einen einfachen Handler für "PSN \_ queryinitialfocus". Sie fordert an, dass der anfängliche Fokus an die Location Control (**IDC- \_ Speicherort**) gegeben wird.

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> Dieser Benachrichtigungs Code wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

