---
title: PSN_QUERYCANCEL Benachrichtigungs Code (prsht. h)
description: Gibt an, dass der Benutzer das Eigenschaften Blatt abgebrochen hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- Windows-Steuerelemente für PSN_QUERYCANCEL Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27d39a7a02d80235db5f8fbe31809dcc913d51c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949769"
---
# <a name="psn_querycancel-notification-code"></a>\_Benachrichtigungs Code für "PSN querycancel"

Gibt an, dass der Benutzer das Eigenschaften Blatt abgebrochen hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält. Diese Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt. Der **LPARAM** -Member der **pshnotify** -Struktur enthält keine Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um den Abbruch Vorgang zu verhindern, oder **false** , um dies zuzulassen.

## <a name="remarks"></a>Bemerkungen

Dieser Benachrichtigungs Code wird in der Regel gesendet, wenn ein Benutzer auf die Schaltfläche **Abbrechen** klickt. Sie wird auch gesendet, wenn ein Benutzer auf die Schaltfläche **X** in der rechten oberen Ecke des Eigenschaften Blatts klickt oder die Escapetaste drückt. Mit diesem Benachrichtigungs Code kann eine Eigenschaften Blattseite den Benutzer bitten, den Abbruch Vorgang zu überprüfen.

Um einen Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit DWL \_ msgresult aufrufen, die auf den Rückgabewert festgelegt ist. Die Dialogfeld Prozedur muss " **true**" zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

