---
title: Imediarendereraktioninformation isvolumeavailable-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR die audiovolumeebene anpassen kann.
ms.assetid: 6DFDC37A-3304-4CDB-9928-C113D2F64ED0
keywords:
- Isvolumeavailable-Methode Medien Streaming-API
- Isvolumeavailable-Methode Medien Streaming-API, imediarendereraktioninformation-Schnittstelle
- Imediarendereraktioninformation-Schnittstelle Medien Streaming-API, isvolumeavailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsVolumeAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb8dc60c25cf3ec12e0ebeaa863e239c287d7c46
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101510"
---
# <a name="imediarendereractioninformationisvolumeavailable-method"></a><span data-ttu-id="c82bd-106">Imediarendereraktioninformation:: isvolumeavailable-Methode</span><span class="sxs-lookup"><span data-stu-id="c82bd-106">IMediaRendererActionInformation::IsVolumeAvailable method</span></span>

<span data-ttu-id="c82bd-107">Ruft einen Wert ab, der angibt, ob der DMR die audiovolumeebene anpassen kann.</span><span class="sxs-lookup"><span data-stu-id="c82bd-107">Retrieves a value that indicates whether the DMR is capable of adjusting the audio volume level.</span></span>

## <a name="syntax"></a><span data-ttu-id="c82bd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c82bd-108">Syntax</span></span>


```C++
HRESULT IsVolumeAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="c82bd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c82bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c82bd-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c82bd-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c82bd-111">Ein boolescher Wert, der **true** ist, wenn der DMR die audiovolumeebene anpassen kann, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="c82bd-111">A boolean value that is **True** if the DMR is capable of adjusting the audio volume level and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c82bd-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c82bd-112">Return value</span></span>

<span data-ttu-id="c82bd-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="c82bd-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c82bd-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c82bd-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c82bd-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c82bd-115">Return code</span></span>                                                                          | <span data-ttu-id="c82bd-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c82bd-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c82bd-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c82bd-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c82bd-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c82bd-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c82bd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c82bd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c82bd-120">**Imediarendereraktioninformation**</span><span class="sxs-lookup"><span data-stu-id="c82bd-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

