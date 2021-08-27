---
description: Die Filterkriterien für das Abonnement.
ms.assetid: cfc3ba9e-0566-45fd-917f-34842b8ff377
title: IEventSubscription2::FilterCriteria -Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.FilterCriteria
- IEventSubscription2.get_FilterCriteria
- IEventSubscription2.put_FilterCriteria
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3d973066ef637882d3477cb9992d01afad72ae3bd314b1a413d628e5c561c007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070660"
---
# <a name="ieventsubscription2filtercriteria-property"></a>IEventSubscription2::FilterCriteria -Eigenschaft

Die Filterkriterien für das Abonnement.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FilterCriteria(
  [in]          BSTR bstrFilterCriteria
);

HRESULT get_FilterCriteria(
  [out, retval] BSTR *pbstrFilterCriteria
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Filterkriterien oder die CLSID für eine Klasse, die [**IPublisherFilter implementiert.**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter)

## <a name="error-codes"></a>Fehlercodes

Diese Methode kann die Standard-Rückgabewerte E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED, E \_ FAIL und S \_ OK zurückgeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




