---
title: DTN_DATETIMECHANGE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Steuerelement für die Datums-und Zeitauswahl (DTP) gesendet, wenn eine Änderung auftritt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- Windows-Steuerelemente für DTN_DATETIMECHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40072a54732a0a3575e3153ddb901ca1df291b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859077"
---
# <a name="dtn_datetimechange-notification-code"></a>DTN \_ datetimechange-Benachrichtigungs Code

Wird von einem Steuerelement für die Datums-und Zeitauswahl (DTP) gesendet, wenn eine Änderung auftritt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmdatetimechange**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) -Struktur, die Informationen über die Änderung enthält, die im Steuerelement stattfindet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Besitzer des Steuer Elements muss 0 (null) zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





