---
title: DTN_CLOSEUP Benachrichtigungscode (Commctrl.h)
description: Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, wenn der Benutzer den Kalender des Dropdownmonats schließt.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- DTN_CLOSEUP Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- DTN_CLOSEUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97cd2d799d05afc638b60adc9203eaad80feb159f985df8b3813403bf5ca0d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877720"
---
# <a name="dtn_closeup-notification-code"></a>DTN \_ CLOSEUP-Benachrichtigungscode

Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, wenn der Benutzer den Kalender des Dropdownmonats schließt. Der Monatskalender wird geschlossen, wenn der Benutzer ein Datum aus dem Monatskalender ausgibt oder auf den Dropdownpfeil klickt, während der Kalender geöffnet ist. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die Informationen über die Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="remarks"></a>Hinweise

DTP-Steuerelemente verwalten kein statisches Untergeordnetes Monatskalender-Steuerelement. Das DTP-Steuerelement zerstört das Untergeordnete Monatskalender-Steuerelement vor dem Senden dieses Benachrichtigungscodes. Daher darf sich Ihre Anwendung nicht auf ein statisches Fensterhandle für den untergeordneten Monatskalender des Steuerelements verlassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[\_DTN-DROPDOWNLISTE](dtn-dropdown.md)
</dt> <dt>

[**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)
</dt> </dl>

 

 





