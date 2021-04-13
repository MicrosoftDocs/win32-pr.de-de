---
title: Getpositioninformationoperation. abgeschlossene (Eigenschaft)
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von getpositioninformationasync gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.
ms.assetid: 144065AE-6C23-4E9D-B9D0-6849E7FB74C4
keywords:
- Abgeschlossene Eigenschaft Medien Streaming-API
- Abgeschlossene Eigenschaft Medien Streaming-API, getpositioninformationoperation-Schnittstelle
- Getpositioninformationoperation-Schnittstelle Medien Streaming-API, abgeschlossene Eigenschaft
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90b4ed4a6402b8c7bfc1ee559bd0b43765a64cec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390284"
---
# <a name="getpositioninformationoperationcompleted-property"></a><span data-ttu-id="e4ddb-106">Getpositioninformationoperation. abgeschlossene (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e4ddb-106">GetPositionInformationOperation.Completed property</span></span>

<span data-ttu-id="e4ddb-107">Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**getpositioninformationasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="e4ddb-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) is completed.</span></span>

<span data-ttu-id="e4ddb-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e4ddb-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ddb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4ddb-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetPositionInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetPositionInformationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="e4ddb-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e4ddb-110">Property value</span></span>

<span data-ttu-id="e4ddb-111">Der Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="e4ddb-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4ddb-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4ddb-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4ddb-113">**Getpositioninformationoperation**</span><span class="sxs-lookup"><span data-stu-id="e4ddb-113">**GetPositionInformationOperation**</span></span>](getpositioninformationoperation.md)
</dt> </dl>

 

 