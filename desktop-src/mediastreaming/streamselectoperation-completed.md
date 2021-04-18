---
title: Streamselectoperation. abgeschlossene Eigenschaft
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von selectbeststreamasync gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- Abgeschlossene Eigenschaft Medien Streaming-API
- Abgeschlossene Eigenschaft Medien Streaming-API, streamselectoperation-Schnittstelle
- Streamselectoperation-Schnittstelle Medien Streaming-API, abgeschlossene Eigenschaft
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74cfdf1a3db4f6843a5f12522b688e889e156f33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338055"
---
# <a name="streamselectoperationcompleted-property"></a><span data-ttu-id="8c83b-106">Streamselectoperation. abgeschlossene Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8c83b-106">StreamSelectOperation.Completed property</span></span>

<span data-ttu-id="8c83b-107">Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**selectbeststreamasync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="8c83b-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span>

<span data-ttu-id="8c83b-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8c83b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c83b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c83b-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="8c83b-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8c83b-110">Property value</span></span>

<span data-ttu-id="8c83b-111">Der Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="8c83b-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c83b-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c83b-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c83b-113">**Streamselectoperation**</span><span class="sxs-lookup"><span data-stu-id="8c83b-113">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

 