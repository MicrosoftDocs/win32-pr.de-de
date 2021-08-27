---
description: Die Partitions-GUID des Ereignisklassenobjekts.
ms.assetid: 154849ac-350c-4b2f-bb51-ac6973f0a8fa
title: IEventSubscription3::EventClassPartitionID-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassPartitionID
- IEventSubscription3.get_EventClassPartitionID
- IEventSubscription3.put_EventClassPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: a305e18677c6a12e14b71b062324630021407231dac6b749f289b58396f4c1f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070650"
---
# <a name="ieventsubscription3eventclasspartitionid-property"></a>IEventSubscription3::EventClassPartitionID-Eigenschaft

Die Partitions-GUID des Ereignisklassenobjekts.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_EventClassPartitionID(
  [in]          BSTR bstrEventClassPartitionID
);

HRESULT get_EventClassPartitionID(
  [out, retval] BSTR *pbstrEventClassPartitionID
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die die GUID der Ereignisklassenpartition enthält.

## <a name="error-codes"></a>Fehlercodes

Diese Methode kann die Standardrückgabewerte E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED, E \_ FAIL und S \_ OK zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEventSubscription3**](ieventsubscription3.md)
</dt> </dl>

 

 




