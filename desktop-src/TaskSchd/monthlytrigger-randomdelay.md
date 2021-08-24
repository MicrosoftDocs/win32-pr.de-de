---
title: MonthlyTrigger.RandomDelay -Eigenschaft
description: Für die Skripterstellung ruft eine Verzögerungszeit ab, die zufällig zur Startzeit des Triggers hinzugefügt wird, oder legt diese fest. | MonthlyTrigger.RandomDelay -Eigenschaft
ms.assetid: 5334356f-fef1-4d0e-9879-6ec996b75dff
keywords:
- RandomDelay-Taskplaner
- RandomDelay-Eigenschaft Taskplaner , MonthlyTrigger-Objekt
- MonthlyTrigger-Objekt Taskplaner , RandomDelay-Eigenschaft
topic_type:
- apiref
api_name:
- MonthlyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d751b31f31cdba9233ea2932976fc69f6880ab8e4c3b81c8743e6c381bdc9a5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253770"
---
# <a name="monthlytriggerrandomdelay-property"></a>MonthlyTrigger.RandomDelay -Eigenschaft

Für die Skripterstellung ruft eine Verzögerungszeit ab, die zufällig zur Startzeit des Triggers hinzugefügt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
MonthlyTrigger.RandomDelay As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Verzögerungszeit, die zufällig zur Startzeit des Triggers hinzugefügt wird. Das Format für diese Zeichenfolge ist (z. B. `P<days>DT<hours>H<minutes>M<seconds>S` ist P2DT5S eine Verzögerung von 2 Tag, 5 Sekunden).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MonthlyTrigger**](monthlytrigger.md)
</dt> </dl>

 

 





