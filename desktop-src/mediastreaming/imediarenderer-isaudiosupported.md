---
title: Imediarenderer isaudiosupported-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR Audioinhalt abspielen kann.
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- Isaudiosupported-Methode Medien Streaming-API
- Isaudiosupported-Methode Medien Streaming-API, imediarenderer-Schnittstelle
- Imediarenderer-Schnittstelle Medien Streaming-API, isaudiosupported-Methode
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7670d0a2818cf5518bee0b2586531caeea20fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106340659"
---
# <a name="imediarendererisaudiosupported-method"></a><span data-ttu-id="1f88e-106">Imediarenderer:: isaudiosupported-Methode</span><span class="sxs-lookup"><span data-stu-id="1f88e-106">IMediaRenderer::IsAudioSupported method</span></span>

<span data-ttu-id="1f88e-107">Ruft einen Wert ab, der angibt, ob der DMR Audioinhalt abspielen kann.</span><span class="sxs-lookup"><span data-stu-id="1f88e-107">Retrieves a value that indicates whether the DMR is capable of playing audio content.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f88e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f88e-108">Syntax</span></span>


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="1f88e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f88e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f88e-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1f88e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f88e-111">Ein boolescher Wert, der **true** ist, wenn der DMR Audioinhalt abspielen kann, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="1f88e-111">A boolean value that is **True** if the DMR is capable of playing audio content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f88e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f88e-112">Return value</span></span>

<span data-ttu-id="1f88e-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="1f88e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1f88e-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1f88e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1f88e-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1f88e-115">Return code</span></span>                                                                          | <span data-ttu-id="1f88e-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f88e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1f88e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f88e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1f88e-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f88e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1f88e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f88e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f88e-120">**Imediarenderer**</span><span class="sxs-lookup"><span data-stu-id="1f88e-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





