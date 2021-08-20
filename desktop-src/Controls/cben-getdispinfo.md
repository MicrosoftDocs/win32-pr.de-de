---
title: CBEN_GETDISPINFO Benachrichtigungscode (Commctrl.h)
description: Wird gesendet, um Anzeigeinformationen zu einem Rückrufelement abzurufen. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- CBEN_GETDISPINFO Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896d282426c11f40fe949c73f44eb963a399c5c210e839198527f9bc903e2fdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413693"
---
# <a name="cben_getdispinfo-notification-code"></a>CBEN \_ GETDISPINFO-Benachrichtigungscode

Wird gesendet, um Anzeigeinformationen zu einem Rückrufelement abzurufen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMCOMBOBOXEX-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) die Informationen zum Benachrichtigungscode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung, die diesen Benachrichtigungscode verarbeitet, muss null zurückgeben.

## <a name="remarks"></a>Hinweise

Die [**NMCOMBOBOXEX-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) enthält eine [**COMBOBOXEXITEM-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) Der **Maskenmember** gibt die Informationen an, die vom Steuerelement angefordert werden.

Füllen Sie die entsprechenden Member der -Struktur aus, um die angeforderten Informationen an das Steuerelement zurückzugeben. Wenn Ihr Nachrichtenhandler den **Maskenmember** der [**COMBOBOXEXITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) auf CBEIF \_ DI \_ SETITEM festlegt, speichert das Steuerelement die Informationen und fordert sie nicht erneut an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **CBEN \_ GETDISPINFOW** (Unicode) und **CBEN \_ GETDISPINFOA** (ANSI)<br/>         |



 

 





