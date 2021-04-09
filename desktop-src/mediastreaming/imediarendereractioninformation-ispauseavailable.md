---
title: Imediarendereraktioninformation ispauseravailable-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR derzeit die Methode "paugasync" annimmt.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- Ispaugavailable-Methode Medien Streaming-API
- Ispauseravailable-Methode Medien Streaming-API, imediarendereraktioninformation-Schnittstelle
- Imediarendereraktioninformation-Schnittstelle Medien Streaming-API, ispauseravailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9eb0b750f5a04528aef830d87376c276bdaf6674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858227"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a><span data-ttu-id="acf03-106">Imediarendereraktioninformation:: ispauseravailable-Methode</span><span class="sxs-lookup"><span data-stu-id="acf03-106">IMediaRendererActionInformation::IsPauseAvailable method</span></span>

<span data-ttu-id="acf03-107">Ruft einen Wert ab, der angibt, ob der DMR derzeit die Methode " [**paugasync**](imediarenderer-pauseasync.md) " annimmt.</span><span class="sxs-lookup"><span data-stu-id="acf03-107">Retrieves a value that indicates whether the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="acf03-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="acf03-108">Syntax</span></span>


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="acf03-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="acf03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acf03-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="acf03-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acf03-111">Ein boolescher Wert, der **true** ist, wenn der DMR derzeit die Methode " [**pausiasync**](imediarenderer-pauseasync.md) " annimmt, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="acf03-111">A boolean value that is **True** if the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acf03-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="acf03-112">Return value</span></span>

<span data-ttu-id="acf03-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="acf03-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="acf03-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="acf03-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="acf03-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="acf03-115">Return code</span></span>                                                                          | <span data-ttu-id="acf03-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="acf03-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="acf03-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="acf03-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="acf03-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="acf03-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="acf03-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acf03-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf03-120">**Imediarendereraktioninformation**</span><span class="sxs-lookup"><span data-stu-id="acf03-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

