---
title: Imediarendereraktioninformation ismuteavailable-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR das Audioformat mutieren kann.
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- Ismuteavailable-Methode Medien Streaming-API
- Ismuteavailable-Methode Medien Streaming-API, imediarendereraktioninformation-Schnittstelle
- Imediarendereraktioninformation-Schnittstelle Medien Streaming-API, ismuteavailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96751a7f2f1aedcd9e29be981ffadf6c43bf4008
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038877"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a><span data-ttu-id="d82d0-106">Imediarendereraktioninformation:: ismuteavailable-Methode</span><span class="sxs-lookup"><span data-stu-id="d82d0-106">IMediaRendererActionInformation::IsMuteAvailable method</span></span>

<span data-ttu-id="d82d0-107">Ruft einen Wert ab, der angibt, ob der DMR das Audioformat mutieren kann.</span><span class="sxs-lookup"><span data-stu-id="d82d0-107">Retrieves a value that indicates whether the DMR is capable of muting the audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="d82d0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d82d0-108">Syntax</span></span>


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="d82d0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d82d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d82d0-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d82d0-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d82d0-111">Ein boolescher Wert, der **true** ist, wenn der DMR das Audioformat mutieren kann, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="d82d0-111">A boolean value that is **True** if the DMR is capable of muting the audio and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d82d0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d82d0-112">Return value</span></span>

<span data-ttu-id="d82d0-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="d82d0-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d82d0-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d82d0-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d82d0-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d82d0-115">Return code</span></span>                                                                          | <span data-ttu-id="d82d0-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d82d0-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d82d0-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d82d0-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d82d0-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d82d0-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d82d0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d82d0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d82d0-120">**Imediarendereraktioninformation**</span><span class="sxs-lookup"><span data-stu-id="d82d0-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

