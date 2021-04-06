---
title: Getvolumeoperation. abgeschlossene-Eigenschaft
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von getvolumeasync gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.
ms.assetid: 34100EE7-C4CB-4AE0-BD3E-9E23A643F87E
keywords:
- Abgeschlossene Eigenschaft Medien Streaming-API
- Abgeschlossene Eigenschaft Medien Streaming-API, getvolumeoperation-Schnittstelle
- Getvolumeoperation Interface Medien Streaming-API, abgeschlossene Eigenschaft
topic_type:
- apiref
api_name:
- GetVolumeOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21577d57e1e29aff1d2b12b92bcbef58a529eba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101511"
---
# <a name="getvolumeoperationcompleted-property"></a><span data-ttu-id="8d22a-106">Getvolumeoperation. abgeschlossene-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8d22a-106">GetVolumeOperation.Completed property</span></span>

<span data-ttu-id="8d22a-107">Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**getvolumeasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="8d22a-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) is completed.</span></span>

<span data-ttu-id="8d22a-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8d22a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d22a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d22a-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetVolumeCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetVolumeCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="8d22a-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8d22a-110">Property value</span></span>

<span data-ttu-id="8d22a-111">Der Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="8d22a-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d22a-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d22a-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d22a-113">**Getvolumeoperation**</span><span class="sxs-lookup"><span data-stu-id="8d22a-113">**GetVolumeOperation**</span></span>](getvolumeoperation.md)
</dt> </dl>

 

 