---
title: Imediarendereraktioninformation isstopavailable-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR derzeit die stopasync-Methode annimmt.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- Isstopavailable-Methode Medien Streaming-API
- Isstopavailable-Methode Medien Streaming-API, imediarendereraktioninformation-Schnittstelle
- Imediarendereraktioninformation-Schnittstelle Medien Streaming-API, isstopavailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e0a031bafc9a755dfec2498f4e2a52cdd9ef5b1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101582"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a><span data-ttu-id="f4340-106">Imediarendereraktioninformation:: isstopavailable-Methode</span><span class="sxs-lookup"><span data-stu-id="f4340-106">IMediaRendererActionInformation::IsStopAvailable method</span></span>

<span data-ttu-id="f4340-107">Ruft einen Wert ab, der angibt, ob der DMR derzeit die [**stopasync**](imediarenderer-stopasync.md) -Methode annimmt.</span><span class="sxs-lookup"><span data-stu-id="f4340-107">Retrieves a value that indicates whether the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4340-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4340-108">Syntax</span></span>


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="f4340-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4340-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4340-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f4340-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4340-111">Ein boolescher Wert, der **true** ist, wenn der DMR derzeit die [**stopasync**](imediarenderer-stopasync.md) -Methode annimmt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="f4340-111">A boolean value that is **True** if the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4340-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4340-112">Return value</span></span>

<span data-ttu-id="f4340-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="f4340-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f4340-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f4340-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f4340-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f4340-115">Return code</span></span>                                                                          | <span data-ttu-id="f4340-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4340-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f4340-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f4340-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f4340-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4340-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f4340-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4340-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4340-120">**Imediarendereraktioninformation**</span><span class="sxs-lookup"><span data-stu-id="f4340-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

