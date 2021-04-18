---
description: Die Partitions-GUID des Ereignis Klassen Objekts.
ms.assetid: 154849ac-350c-4b2f-bb51-ac6973f0a8fa
title: 'IEventSubscription3:: eventclasspartitionid (Eigenschaft)'
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
ms.openlocfilehash: d41d3e2a170deffb73f1f533226421d88f150c01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524203"
---
# <a name="ieventsubscription3eventclasspartitionid-property"></a>IEventSubscription3:: eventclasspartitionid (Eigenschaft)

Die Partitions-GUID des Ereignis Klassen Objekts.

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

Eine Zeichenfolge, die die GUID der Ereignis Klassen Partition enthält.

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

 

 




