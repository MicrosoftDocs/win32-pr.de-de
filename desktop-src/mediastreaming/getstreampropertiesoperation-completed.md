---
title: Getstreampropertiesoperation. abgeschlossene-Eigenschaft
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von getstreampropertiesasync gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.
ms.assetid: 97194F8E-DE36-4DC6-ADB5-F1EDE8AEF079
keywords:
- Abgeschlossene Eigenschaft Medien Streaming-API
- Abgeschlossene Eigenschaft Medien Streaming-API, getstreampropertiesoperation-Schnittstelle
- Getstreampropertiesoperation-Schnittstelle Medien Streaming-API, abgeschlossene Eigenschaft
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb60ad137c8dafa42a58394d58a105267dabda3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390216"
---
# <a name="getstreampropertiesoperationcompleted-property"></a><span data-ttu-id="b47d4-106">Getstreampropertiesoperation. abgeschlossene-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b47d4-106">GetStreamPropertiesOperation.Completed property</span></span>

<span data-ttu-id="b47d4-107">Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**getstreampropertiesasync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="b47d4-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) is completed.</span></span>

<span data-ttu-id="b47d4-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b47d4-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b47d4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b47d4-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="b47d4-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b47d4-110">Property value</span></span>

<span data-ttu-id="b47d4-111">Der Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="b47d4-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="b47d4-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b47d4-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b47d4-113">**Getstreampropertiesoperation**</span><span class="sxs-lookup"><span data-stu-id="b47d4-113">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

 