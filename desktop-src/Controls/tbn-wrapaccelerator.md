---
title: TBN_WRAPACCELERATOR Benachrichtigungscode (Commctrl.h)
description: Fordert den Index der Schaltfläche in einer oder mehreren Symbolleisten an, die dem angegebenen Zugriffstastenzeichen entsprechen. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c5ec222f387108e2cb4d240e6dddf0fcb904d814097a96624a177425eb805ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105030"
---
# <a name="tbn_wrapaccelerator-notification-code"></a>TBN \_ WRAPACCELERATOR-Benachrichtigungscode

Fordert den Index der Schaltfläche in einer oder mehreren Symbolleisten an, die dem angegebenen Zugriffstastenzeichen entsprechen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine -Struktur, die das Zugriffstastenzeichen enthält und den Index der entsprechenden Schaltfläche empfängt. Der Index ist -1, wenn die Zugriffstaste keinem Befehl entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**TRUE,** wenn ein Index zurückgegeben wird, andernfalls **FALSE**.

## <a name="remarks"></a>Hinweise

Anwendungen mit einer oder mehreren Symbolleisten erhalten möglicherweise diesen Benachrichtigungscode.

Die **NMTBWRAPACCELERATOR-Struktur** muss von der Anwendung wie folgt definiert werden:

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





