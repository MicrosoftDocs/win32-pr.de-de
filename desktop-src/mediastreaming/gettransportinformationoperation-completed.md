---
title: Abgeschlossene gettransportinformationoperation-Eigenschaft
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von gettransportinformationasync gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.
ms.assetid: 11E60E00-75B5-4412-B115-4438255AEB8A
keywords:
- Abgeschlossene Eigenschaft Medien Streaming-API
- Abgeschlossene Eigenschaft Medien Streaming-API, gettransportinformationoperation-Schnittstelle
- Gettransportinformationoperation-Schnittstelle Medien Streaming-API, abgeschlossene Eigenschaft
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.Completed
- GetTransportInformationOperation.get_Completed
- GetTransportInformationOperation.put_Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2948af2ed84a70c9f37efbc4aae985e9b1ab5804
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339062"
---
# <a name="gettransportinformationoperationcompleted-property"></a><span data-ttu-id="a2cc5-106">Gettransportinformationoperation:: Abgeschlossene Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a2cc5-106">GetTransportInformationOperation::Completed property</span></span>

<span data-ttu-id="a2cc5-107">Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**gettransportinformationasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="a2cc5-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) is completed.</span></span>

<span data-ttu-id="a2cc5-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a2cc5-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2cc5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2cc5-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="a2cc5-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a2cc5-110">Property value</span></span>

<span data-ttu-id="a2cc5-111">Der Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="a2cc5-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2cc5-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2cc5-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2cc5-113">**Gettransportinformationoperation**</span><span class="sxs-lookup"><span data-stu-id="a2cc5-113">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

 