---
title: MediaRenderer. stopasync-Methode
description: Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten. | MediaRenderer. stopasync-Methode
ms.assetid: 04cf6d5a-8aa5-4821-8117-f250bfaf7ebd
keywords:
- Stopasync-Methode Medien Streaming-API
- Stopasync-Methode Medien Streaming-API, MediaRenderer-Schnittstelle
- MediaRenderer Interface Medien Streaming-API, stopasync-Methode
topic_type:
- apiref
api_name:
- MediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 205c69a83572539974c1b8ad2cf45159c45335cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104132261"
---
# <a name="mediarendererstopasync-method"></a><span data-ttu-id="8a301-107">MediaRenderer. stopasync-Methode</span><span class="sxs-lookup"><span data-stu-id="8a301-107">MediaRenderer.StopAsync method</span></span>

<span data-ttu-id="8a301-108">Weist den DMR asynchron an, die Wiedergabe des aktuellen Inhalts anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="8a301-108">Instructs the DMR asynchronously to stop playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a301-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a301-109">Syntax</span></span>


```C++
HRESULT StopAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="8a301-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a301-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a301-111">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8a301-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a301-112">Empfängt einen Verweis auf ein [**playbackoperation**](playbackoperation.md) -Objekt, das verwendet wird, um Ergebnisse aus dem asynchronen Vorgang zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8a301-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a301-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a301-113">Return value</span></span>

<span data-ttu-id="8a301-114">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="8a301-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8a301-115">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8a301-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8a301-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8a301-116">Return code</span></span>                                                                          | <span data-ttu-id="8a301-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a301-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8a301-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8a301-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8a301-119">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a301-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8a301-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a301-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a301-121">**MediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="8a301-121">**MediaRenderer**</span></span>](mediarenderer.md)
</dt> </dl>

 

 





