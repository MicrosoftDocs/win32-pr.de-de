---
title: MediaRenderer. pautsasync-Methode
description: Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten. | MediaRenderer. pautsasync-Methode
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- Methode für die Medien Streaming-API
- Pautsasync-Methode Medien Streaming-API, MediaRenderer-Schnittstelle
- MediaRenderer Interface Media Streaming API, pautsasync-Methode
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbbc55931c7cc7fc5e2e5ec39ba63fe7a064478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361831"
---
# <a name="mediarendererpauseasync-method"></a><span data-ttu-id="dcccc-107">MediaRenderer. pautsasync-Methode</span><span class="sxs-lookup"><span data-stu-id="dcccc-107">MediaRenderer.PauseAsync method</span></span>

<span data-ttu-id="dcccc-108">Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="dcccc-108">Instructs the DMR asynchronously to pause playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcccc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcccc-109">Syntax</span></span>


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="dcccc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcccc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcccc-111">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dcccc-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcccc-112">Empfängt einen Verweis auf ein [**playbackoperation**](playbackoperation.md) -Objekt, das verwendet wird, um Ergebnisse aus dem asynchronen Vorgang zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dcccc-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcccc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dcccc-113">Return value</span></span>

<span data-ttu-id="dcccc-114">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="dcccc-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dcccc-115">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="dcccc-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dcccc-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dcccc-116">Return code</span></span>                                                                          | <span data-ttu-id="dcccc-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dcccc-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="dcccc-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dcccc-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dcccc-119">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dcccc-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="dcccc-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcccc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcccc-121">**MediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="dcccc-121">**MediaRenderer**</span></span>](mediarenderer.md)
</dt> </dl>

 

 





