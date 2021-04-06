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
# <a name="createmediarendereroperationcompleted-property"></a><span data-ttu-id="8ca76-106">Eigenschaft "kreatemediarendereroperation. abgeschlossen"</span><span class="sxs-lookup"><span data-stu-id="8ca76-106">CreateMediaRendererOperation.Completed property</span></span>

<span data-ttu-id="8ca76-107">Dient zum Abrufen oder Festlegen eines Ereignis Handlers, der aufgerufen wird, wenn der asynchrone Vorgang, der von " [**deatemediarendererasync**](imediarendererfactory-createmediarendererasync.md) " oder " [**deatemediarendererfrombasicdeviceasync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) " gestartet wurde, abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="8ca76-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) or [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) is completed.</span></span>

<span data-ttu-id="8ca76-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8ca76-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca76-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ca76-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a><span data-ttu-id="8ca76-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8ca76-110">Property value</span></span>

<span data-ttu-id="8ca76-111">Der Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="8ca76-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ca76-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ca76-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca76-113">**"Kreatemediarendereroperation"**</span><span class="sxs-lookup"><span data-stu-id="8ca76-113">**CreateMediaRendererOperation**</span></span>](createmediarendereroperation.md)
</dt> </dl>

 

 




