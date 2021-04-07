---
title: Getmuteoperation. abgeschlossene-Eigenschaft
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von getmuteasync gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.
ms.assetid: B8E1DE71-46AC-4F6A-B873-AE3239BE492C
keywords:
- Abgeschlossene Eigenschaft Medien Streaming-API
- Abgeschlossene Eigenschaft Medien Streaming-API, getmuteoperation-Schnittstelle
- Getmuteoperation-Schnittstelle Medien Streaming-API, abgeschlossene Eigenschaft
topic_type:
- apiref
api_name:
- GetMuteOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40c360dc3597d8cf04d1a8c505e479a38136f592
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726577"
---
# <a name="getmuteoperationcompleted-property"></a><span data-ttu-id="cde04-106">Getmuteoperation. abgeschlossene-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cde04-106">GetMuteOperation.Completed property</span></span>

<span data-ttu-id="cde04-107">Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**getmuteasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="cde04-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) is completed.</span></span>

<span data-ttu-id="cde04-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="cde04-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde04-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cde04-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetMuteCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetMuteCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="cde04-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cde04-110">Property value</span></span>

<span data-ttu-id="cde04-111">Der Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="cde04-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="cde04-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cde04-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde04-113">**Getmuteoperation**</span><span class="sxs-lookup"><span data-stu-id="cde04-113">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

 