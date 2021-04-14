---
title: Imediarenderer isvideosupported-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR Videoinhalte abspielen kann.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- Isvideosupported-Methode Medien Streaming-API
- Isvideosupported-Methode Medien Streaming-API, imediarenderer-Schnittstelle
- Imediarenderer-Schnittstelle Medien Streaming-API, isvideosupported-Methode
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9808841bf60a384d6a4566e75f53248b0f86338c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313001"
---
# <a name="imediarendererisvideosupported-method"></a><span data-ttu-id="ce3e5-106">Imediarenderer:: isvideosupported-Methode</span><span class="sxs-lookup"><span data-stu-id="ce3e5-106">IMediaRenderer::IsVideoSupported method</span></span>

<span data-ttu-id="ce3e5-107">Ruft einen Wert ab, der angibt, ob der DMR Videoinhalte abspielen kann.</span><span class="sxs-lookup"><span data-stu-id="ce3e5-107">Retrieves a value that indicates whether the DMR is capable of playing video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce3e5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce3e5-108">Syntax</span></span>


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="ce3e5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce3e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce3e5-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ce3e5-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3e5-111">Ein boolescher Wert, der **true** ist, wenn der DMR Videoinhalte abspielen kann, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="ce3e5-111">A boolean value that is **True** if the DMR is capable of playing video content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce3e5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce3e5-112">Return value</span></span>

<span data-ttu-id="ce3e5-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="ce3e5-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ce3e5-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ce3e5-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ce3e5-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ce3e5-115">Return code</span></span>                                                                          | <span data-ttu-id="ce3e5-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce3e5-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ce3e5-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ce3e5-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ce3e5-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce3e5-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ce3e5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce3e5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce3e5-120">**Imediarenderer**</span><span class="sxs-lookup"><span data-stu-id="ce3e5-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





