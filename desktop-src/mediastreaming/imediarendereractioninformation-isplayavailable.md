---
title: Imediarendereraktioninformation isplayavailable-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR derzeit akzeptiert, dass die playasync-Methode und die playatspeedasync-Methode akzeptiert werden.
ms.assetid: 969C55FA-872D-4063-B85C-573C8DA5593C
keywords:
- Isplayavailable-Methode Medien Streaming-API
- Isplayavailable-Methode Medien Streaming-API, imediarendereraktioninformation-Schnittstelle
- Imediarendereraktioninformation-Schnittstelle Medien Streaming-API, isplayavailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPlayAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 87fa3a2005772a4d948bafe32d2a0e10cc5a6914
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390258"
---
# <a name="imediarendereractioninformationisplayavailable-method"></a><span data-ttu-id="213b4-106">Imediarendereraktioninformation:: isplayavailable-Methode</span><span class="sxs-lookup"><span data-stu-id="213b4-106">IMediaRendererActionInformation::IsPlayAvailable method</span></span>

<span data-ttu-id="213b4-107">Ruft einen Wert ab, der angibt, ob der DMR derzeit akzeptiert, dass die [**playasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) -Methode und die [**playatspeedasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) -Methode akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="213b4-107">Retrieves a value that indicates whether the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="213b4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="213b4-108">Syntax</span></span>


```C++
HRESULT IsPlayAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="213b4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="213b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="213b4-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="213b4-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="213b4-111">Ein boolescher Wert, der **true** ist, wenn der DMR derzeit akzeptiert, dass die [**playasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) -Methode und die [**playatspeedasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) -Methode akzeptiert, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="213b4-111">A boolean value that is **True** if the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="213b4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="213b4-112">Return value</span></span>

<span data-ttu-id="213b4-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="213b4-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="213b4-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="213b4-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="213b4-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="213b4-115">Return code</span></span>                                                                          | <span data-ttu-id="213b4-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="213b4-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="213b4-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="213b4-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="213b4-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="213b4-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="213b4-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="213b4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="213b4-120">**Imediarendereraktioninformation**</span><span class="sxs-lookup"><span data-stu-id="213b4-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

