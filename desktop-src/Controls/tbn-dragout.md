---
title: TBN_DRAGOUT Benachrichtigungscode (Commctrl.h)
description: Wird von einem Symbolleisten-Steuerelement gesendet, wenn der Benutzer auf eine Schaltfläche klickt und dann den Cursor von der Schaltfläche verschiebt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- TBN_DRAGOUT Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad707fa357a487e271bbe03039745b97521542a1305f9745a71a56044060c950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077944"
---
# <a name="tbn_dragout-notification-code"></a>TBN \_ DRAGOUT-Benachrichtigungscode

Wird von einem Symbolleisten-Steuerelement gesendet, wenn der Benutzer auf eine Schaltfläche klickt und dann den Cursor von der Schaltfläche verschiebt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTOOLBAR-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) die Informationen zu diesem Benachrichtigungscode enthält. Für diesen Benachrichtigungscode sind nur **die Hdr-** und **iItem-Member** dieser Struktur gültig. Das **iItem-Member** dieser -Struktur enthält den Befehlsbezeichner der zu ziehenden Schaltfläche.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Mit diesem Benachrichtigungscode kann eine Anwendung Drag & Drop-Funktionen für Symbolleistenschaltflächen implementieren. Bei der Verarbeitung dieses Benachrichtigungscodes beginnt die Anwendung mit dem Drag & Drop-Vorgang.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





