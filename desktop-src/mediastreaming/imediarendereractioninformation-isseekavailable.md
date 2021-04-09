---
title: Imediarendereraktioninformation isseekavailable-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR derzeit die SeekAsync-Methode annimmt.
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- Isseekavailable-Methode Medien Streaming-API
- Isseekavailable-Methode Medien Streaming-API, imediarendereraktioninformation-Schnittstelle
- Imediarendereraktioninformation-Schnittstelle Medien Streaming-API, isseekavailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 700afb72efbab01bbd3a8f5e15fa444eb6b06272
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858226"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a><span data-ttu-id="61539-106">Imediarendereraktioninformation:: isseekavailable-Methode</span><span class="sxs-lookup"><span data-stu-id="61539-106">IMediaRendererActionInformation::IsSeekAvailable method</span></span>

<span data-ttu-id="61539-107">Ruft einen Wert ab, der angibt, ob der DMR derzeit die [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) -Methode annimmt.</span><span class="sxs-lookup"><span data-stu-id="61539-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="61539-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="61539-108">Syntax</span></span>


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="61539-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="61539-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61539-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="61539-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61539-111">Ein boolescher Wert, der **true** ist, wenn der DMR derzeit die [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) -Methode annimmt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="61539-111">A boolean value that is **True** if the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61539-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61539-112">Return value</span></span>

<span data-ttu-id="61539-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="61539-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="61539-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="61539-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="61539-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="61539-115">Return code</span></span>                                                                          | <span data-ttu-id="61539-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61539-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="61539-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="61539-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="61539-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61539-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="61539-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61539-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61539-120">**Imediarendereraktioninformation**</span><span class="sxs-lookup"><span data-stu-id="61539-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

