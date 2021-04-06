---
title: Eigenschaft "kreatemediarendereroperation. abgeschlossen"
description: Dient zum Abrufen oder Festlegen eines Ereignis Handlers, der aufgerufen wird, wenn der asynchrone Vorgang, der von "deatemediarendererasync" oder "deatemediarendererfrombasicdeviceasync" gestartet wurde, abgeschlossen ist
ms.assetid: B62CF929-13D0-4665-89E4-DEC48A38DDF7
keywords:
- Abgeschlossene Eigenschaft Medien Streaming-API
- Abgeschlossene Eigenschaft Medien Streaming-API, Schnittstelle von "kreatemediarendereroperation"
- "\"Kreatemediarendereroperation\"-Schnittstelle Medien Streaming-API, abgeschlossene Eigenschaft"
topic_type:
- apiref
api_name:
- CreateMediaRendererOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3b4ebafc1441741a352f4573709495228bf13e4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718419"
---
# <a name="createmediarendereroperationcompleted-property"></a>Eigenschaft "kreatemediarendereroperation. abgeschlossen"

Dient zum Abrufen oder Festlegen eines Ereignis Handlers, der aufgerufen wird, wenn der asynchrone Vorgang, der von " [**deatemediarendererasync**](imediarendererfactory-createmediarendererasync.md) " oder " [**deatemediarendererfrombasicdeviceasync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) " gestartet wurde, abgeschlossen ist

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Ereignishandler.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Kreatemediarendereroperation"**](createmediarendereroperation.md)
</dt> </dl>

 

 




