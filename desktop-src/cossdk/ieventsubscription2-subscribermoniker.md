---
description: Der Abonnenten Moniker.
ms.assetid: d33d8c80-3251-4ec7-9cf3-d0b60d91ed5a
title: IEventSubscription2SubscriberMoniker-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.SubscriberMoniker
- IEventSubscription2.get_SubscriberMoniker
- IEventSubscription2.put_SubscriberMoniker
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9496a3046b4bb0e99a88322892e557588a92aab8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748304"
---
# <a name="ieventsubscription2subscribermoniker-property"></a>IEventSubscription2:: abonniert-Eigenschaft

Der Moniker des Abonnenten.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SubscriberMoniker(
  [in]          BSTR bstrMoniker
);

HRESULT get_SubscriberMoniker(
  [out, retval] BSTR *pbstrMoniker
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine Monikerzeichenfolge, die den Abonnenten angibt.

## <a name="error-codes"></a>Fehlercodes

Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ outo fmemory, e \_ unerwartet, e \_ Fail und S OK \_ zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




