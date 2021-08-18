---
title: TBN_MAPACCELERATOR Benachrichtigungscode (Commctrl.h)
description: Fordert den Index der Schaltfläche in der Symbolleiste an, die dem angegebenen Zugriffstastenzeichen entspricht. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488c78ff00b75c42f6646e314c75d63445c7400eb9130464b126e75bcf2df942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434190"
---
# <a name="tbn_mapaccelerator-notification-code"></a>TBN \_ MAPACCELERATOR-Benachrichtigungscode

Fordert den Index der Schaltfläche in der Symbolleiste an, die dem angegebenen Zugriffstastenzeichen entspricht. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMCHAR-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmchar) die das Zugriffstastenzeichen enthält und den Index der entsprechenden Schaltfläche empfängt. Das Feld **dwItemNext** ist -1, wenn die Zugriffstaste keinem Befehl entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

TRUE, wenn **NMCHAR.dwItemNext** auf einen Wert festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





