---
title: PSN_KILLACTIVE Benachrichtigungs Code (prsht. h)
description: Benachrichtigt eine Seite, dass Sie im Begriff ist, die Aktivierung zu verlieren, weil eine andere Seite aktiviert oder der Benutzer auf die Schaltfläche "OK" geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- Windows-Steuerelemente für PSN_KILLACTIVE Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae5f90670c79797ef8576c5e6e3911255ab5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949771"
---
# <a name="psn_killactive-notification-code"></a>PSN- \_ killactive-Benachrichtigungs Code

Benachrichtigt eine Seite, dass Sie im Begriff ist, die Aktivierung zu verlieren, weil eine andere Seite aktiviert oder der Benutzer auf die Schaltfläche "OK" geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält. Diese Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt. Der **LPARAM** -Member der **pshnotify** -Struktur enthält keine Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um zu verhindern, dass die Seite die Aktivierung verliert, oder **false** , um Sie zuzulassen.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung verarbeitet diesen Benachrichtigungs Code, um die vom Benutzer eingegebenen Informationen zu überprüfen.

> [!Note]  
> Das Eigenschaften Blatt bearbeitet die Liste der Seiten, wenn der \_ Benachrichtigungs Code "PSN killactive" gesendet wird. Versuchen Sie nicht, während der Verarbeitung dieses Benachrichtigungs Codes Seiten hinzuzufügen, zu entfernen oder einzufügen. Dies führt zu unvorhersehbaren Ergebnissen.

 

Um einen Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit einem DWL- \_ msgresult-Wert aufrufen, der auf den Rückgabewert festgelegt ist. Die Dialogfeld Prozedur muss " **true**" zurückgeben.

Wenn in der Dialogfeld Prozedur DWL \_ msgresult auf **true** festgelegt wird, sollte ein Meldungs Feld angezeigt werden, um das Problem für den Benutzer zu erläutern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

