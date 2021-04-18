---
title: PSN_TRANSLATEACCELERATOR Benachrichtigungs Code (prsht. h)
description: Benachrichtigt ein Eigenschaften Blatt, dass eine Tastatur Meldung empfangen wurde. Die Seite bietet die Möglichkeit, eine private Tastatur Zugriffstaste zu übersetzen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- Windows-Steuerelemente für PSN_TRANSLATEACCELERATOR Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337492"
---
# <a name="psn_translateaccelerator-notification-code"></a>PSN \_ TranslateAccelerator-Benachrichtigungs Code

Benachrichtigt ein Eigenschaften Blatt, dass eine Tastatur Meldung empfangen wurde. Die Seite bietet die Möglichkeit, eine private Tastatur Zugriffstaste zu übersetzen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält. Diese Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member der **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt. Der **LPARAM** -Member der **pshnotify** -Struktur ist ein Zeiger [**auf die Meldung**](/windows/win32/api/winuser/ns-winuser-msg)der Nachricht. Sie kann in einen **lpmsg** -Typ umgewandelt werden, um Zugriff auf die Parameter der zu über setzenden Nachricht zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt psnret \_ messagebehandelte zurück, um anzugeben, dass keine weitere Verarbeitung erforderlich ist. Gibt psnret \_ noError zurück, um die normale Verarbeitung anzufordern.

## <a name="remarks"></a>Bemerkungen

Um den Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit dem DWL \_ msgresult-Wert verwenden. Die Dialogfeld Prozedur muss " **true**" zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

