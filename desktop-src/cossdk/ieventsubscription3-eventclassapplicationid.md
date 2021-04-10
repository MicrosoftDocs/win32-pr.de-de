---
description: Die Anwendungs-GUID des Ereignis Klassen Objekts.
ms.assetid: 0d19183a-429c-4564-b6a5-f06481d27e00
title: 'IEventSubscription3:: eventclassapplicationid (Eigenschaft)'
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
ms.openlocfilehash: 3e80a8d8f557c80a1b2605328728260eb8ae7bd7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127029"
---
# <a name="ieventsubscription3eventclassapplicationid-property"></a>IEventSubscription3:: eventclassapplicationid (Eigenschaft)

Die Anwendungs-GUID des Ereignis Klassen Objekts.

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

Eine Zeichenfolge, die die GUID der Ereignis Klassen Anwendung enthält.

## <a name="error-codes"></a>Fehlercodes

Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ outo fmemory, e \_ unerwartet, e \_ Fail und S OK \_ zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEventSubscription3**](ieventsubscription3.md)
</dt> </dl>

 

 




