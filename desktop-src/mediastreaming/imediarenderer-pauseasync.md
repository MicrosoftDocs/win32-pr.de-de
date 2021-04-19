---
title: Imediarenderer-Methode "pauabasync"
description: Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten. | Imediarenderer-Methode "pauabasync"
ms.assetid: 2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B
keywords:
- Methode für die Medien Streaming-API
- Pautsasync-Methode Medien Streaming-API, imediarenderer-Schnittstelle
- Imediarenderer-Schnittstelle Medien Streaming-API, pautsasync-Methode
topic_type:
- apiref
api_name:
- IMediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8713fa4b2fe46a694024c2873cd50a0ec89ce898
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353695"
---
# <a name="imediarendererpauseasync-method"></a><span data-ttu-id="7e737-107">Imediarenderer::P autsasync-Methode</span><span class="sxs-lookup"><span data-stu-id="7e737-107">IMediaRenderer::PauseAsync method</span></span>

<span data-ttu-id="7e737-108">Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="7e737-108">Instructs the DMR asynchronously to pause playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e737-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e737-109">Syntax</span></span>


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="7e737-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e737-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e737-111">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7e737-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e737-112">Empfängt einen Verweis auf ein [**playbackoperation**](playbackoperation.md) -Objekt, das verwendet wird, um Ergebnisse aus dem asynchronen Vorgang zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7e737-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e737-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e737-113">Return value</span></span>

<span data-ttu-id="7e737-114">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="7e737-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7e737-115">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7e737-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7e737-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7e737-116">Return code</span></span>                                                                          | <span data-ttu-id="7e737-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e737-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7e737-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7e737-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7e737-119">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e737-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="7e737-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e737-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e737-121">**Imediarenderer**</span><span class="sxs-lookup"><span data-stu-id="7e737-121">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





