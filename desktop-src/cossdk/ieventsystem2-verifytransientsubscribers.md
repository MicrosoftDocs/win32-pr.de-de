---
description: Überprüft, ob alle vorübergehenden Abonnenten im Datenspeicher vorhanden sind. Wenn Sie diese Methode aufrufen, können Sie sicherstellen, dass alle im Datenspeicher aufgelisteten vorübergehenden Abonnenten aktiv sind.
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: 'IEventSystem2:: verifytransientabonnenten-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958320"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a>IEventSystem2:: verifytransientabonnenten-Methode

Überprüft, ob alle vorübergehenden Abonnenten im Datenspeicher vorhanden sind. Wenn Sie diese Methode aufrufen, können Sie sicherstellen, dass alle im Datenspeicher aufgelisteten vorübergehenden Abonnenten aktiv sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ outo fmemory, e \_ unerwartet, e \_ Fail und S OK \_ zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEventSystem2**](ieventsystem2.md)
</dt> </dl>

 

 




