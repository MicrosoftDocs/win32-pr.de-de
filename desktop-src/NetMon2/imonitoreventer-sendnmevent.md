---
description: Die sendnmevent-Methode übermittelt Ereignisse an Windows-Verwaltungsinstrumentation (WMI).
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'Imonitoreventer:: sendnmevent-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3286fca4d5b852d4562c13446699c1a6b40f3efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356560"
---
# <a name="imonitoreventersendnmevent-method"></a>Imonitoreventer:: sendnmevent-Methode

Die **sendnmevent** -Methode übermittelt Ereignisse an Windows-Verwaltungsinstrumentation (WMI).

## <a name="syntax"></a>Syntax


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnmeventdata* \[ in\]
</dt> <dd>

Zeiger auf das Ereignis, das an WMI gesendet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert nmerr nicht genügend Arbeits \_ \_ \_ Speicher.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




