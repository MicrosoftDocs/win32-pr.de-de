---
title: TTN_GETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Wird von einem QuickInfo-Steuerelement zum Abrufen der zum Anzeigen eines QuickInfo-Fensters benötigten Informationen gesendet. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: af9ecc27-2004-4c45-9f1d-9ee0b2b50ff6
keywords:
- Windows-Steuerelemente für TTN_GETDISPINFO Benachrichtigungs
topic_type:
- apiref
api_name:
- TTN_GETDISPINFO
- TTN_GETDISPINFOA
- TTN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc1fe07d12331e523fed9e1ff46b9e265487bc31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859048"
---
# <a name="ttn_getdispinfo-notification-code"></a>TTN \_ getdispinfo-Benachrichtigungs Code

Wird von einem QuickInfo-Steuerelement zum Abrufen der zum Anzeigen eines QuickInfo-Fensters benötigten Informationen gesendet. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TTN_GETDISPINFO

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur, die das Tool identifiziert, das Text benötigt und die angeforderten Informationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Füllen Sie die entsprechenden Member der Struktur aus, um die angeforderten Informationen an das ToolTip-Steuerelement zurückzugeben. Wenn Ihr Nachrichten Handler den **uFlags** -Member der [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur auf ttf \_ di \_ SetItem festlegt, speichert das QuickInfo-Steuerelement die Informationen und fordert Sie nicht erneut an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTN \_ Getdispinfow** (Unicode) und **TTN \_ getdispinfoa** (ANSI)<br/>           |



 

 





