---
description: Die Anwendungs-GUID des Ereignisklassenobjekts.
ms.assetid: 0d19183a-429c-4564-b6a5-f06481d27e00
title: IEventSubscription3::EventClassApplicationID (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassApplicationID
- IEventSubscription3.get_EventClassApplicationID
- IEventSubscription3.put_EventClassApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 228650f97f8662e60f7866fd36c184583316e494286b55c1f70e03a148e5e979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813831"
---
# <a name="ieventsubscription3eventclassapplicationid-property"></a>IEventSubscription3::EventClassApplicationID (Eigenschaft)

Die Anwendungs-GUID des Ereignisklassenobjekts.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_EventClassApplicationID(
  [in]          BSTR bstrEventClassApplicationID
);

HRESULT get_EventClassApplicationID(
  [out, retval] BSTR *pbstrEventClassApplicationID
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die die GUID der Ereignisklassenanwendung enthält.

## <a name="error-codes"></a>Fehlercodes

Diese Methode kann die Standard-Rückgabewerte E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED, E \_ FAIL und S \_ OK zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEventSubscription3**](ieventsubscription3.md)
</dt> </dl>

 

 




