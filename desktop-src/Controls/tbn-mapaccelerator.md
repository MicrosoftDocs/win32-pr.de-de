---
title: TBN_MAPACCELERATOR Benachrichtigungs Code (kommctrl. h)
description: Fordert den Index der Schaltfläche auf der Symbolleiste an, die dem angegebenen Beschleunigungs Zeichen entspricht. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- Windows-Steuerelemente für TBN_MAPACCELERATOR Benachrichtigungs
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
ms.openlocfilehash: d4b20f1908f441c38e23aa7428f8c8edb8a192c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949409"
---
# <a name="tbn_mapaccelerator-notification-code"></a>TBN- \_ mapaccelerator-Benachrichtigungs Code

Fordert den Index der Schaltfläche auf der Symbolleiste an, die dem angegebenen Beschleunigungs Zeichen entspricht. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmchar**](/windows/win32/api/commctrl/ns-commctrl-nmchar) -Struktur, die das Tastenkombination-Zeichen enthält und den Index der entsprechenden Schaltfläche empfängt. Das Feld " **dwitemnext** " ist "-1", wenn die Zugriffstaste keinem Befehl entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

TRUE, wenn **nmchar. dwitemnext** auf einen Wert festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





