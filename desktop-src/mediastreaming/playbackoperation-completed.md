---
title: Playbackoperation. abgeschlossene-Eigenschaft
description: Dient zum Abrufen oder Festlegen eines Ereignis Handlers, der aufgerufen wird, wenn der asynchrone Vorgang, der von einer der MediaRenderer-Wiedergabe Methoden gestartet wurde, abgeschlossen ist.
ms.assetid: E8F8D3FC-C31F-485C-A30B-2457F4B1DE82
keywords:
- Abgeschlossene Eigenschaft Medien Streaming-API
- Abgeschlossene Eigenschaft Medien Streaming-API, playbackoperation-Schnittstelle
- Playbackoperation-Schnittstelle Medien Streaming-API, abgeschlossene Eigenschaft
topic_type:
- apiref
api_name:
- PlaybackOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bf305b4028e223c36df0c8a59c5246228c5b8d40
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338226"
---
# <a name="playbackoperationcompleted-property"></a><span data-ttu-id="32150-106">Playbackoperation. abgeschlossene-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="32150-106">PlaybackOperation.Completed property</span></span>

<span data-ttu-id="32150-107">Dient zum Abrufen oder Festlegen eines Ereignis Handlers, der aufgerufen wird, wenn der asynchrone Vorgang, der von einer der [**MediaRenderer**](mediarenderer.md) -Wiedergabe Methoden gestartet wurde, abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="32150-107">Gets or sets an event handler that is invoked when the asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods is completed.</span></span>

<span data-ttu-id="32150-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="32150-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="32150-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="32150-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  PlaybackOperationCompletedHandler *value
);

HRESULT get_Completed(
  [out] PlaybackOperationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="32150-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="32150-110">Property value</span></span>

<span data-ttu-id="32150-111">Der Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="32150-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="32150-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32150-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32150-113">**Playbackoperation**</span><span class="sxs-lookup"><span data-stu-id="32150-113">**PlaybackOperation**</span></span>](playbackoperation.md)
</dt> </dl>

 

 




