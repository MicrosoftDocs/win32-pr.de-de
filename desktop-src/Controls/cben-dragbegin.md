---
title: CBEN_DRAGBEGIN Benachrichtigungscode (Commctrl.h)
description: Wird gesendet, wenn der Benutzer mit dem Ziehen des Bilds des Elements beginnt, das im Bearbeitungsteil des Steuerelements angezeigt wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- CBEN_DRAGBEGIN Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 626ad4d6abbcaaeb6f647aa94657ee1a681801a3ce13a9b5539216b1b67565a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414060"
---
# <a name="cben_dragbegin-notification-code"></a>CBEN \_ DRAGBEGIN-Benachrichtigungscode

Wird gesendet, wenn der Benutzer mit dem Ziehen des Bilds des Elements beginnt, das im Bearbeitungsteil des Steuerelements angezeigt wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMCBEDRAGBEGIN-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) die Informationen zum Benachrichtigungscode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Wenn die empfangende Anwendung Drag & Drop-Funktionen aus dem Steuerelement implementiert, beginnt die Anwendung den Drag & Drop-Vorgang als Reaktion auf diesen Benachrichtigungscode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **CBEN \_ DRAGBEGINW** (Unicode) und **CBEN \_ DRAGBEGINA** (ANSI)<br/>             |



 

 





