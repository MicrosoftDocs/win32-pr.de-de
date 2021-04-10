---
title: Imediarendereraktioninformation issetnextsourceavailable-Methode
description: Ruft einen Wert ab, der angibt, ob der DMR derzeit die setnextsourcefromuriasync-Methode, die setnextsourcefromstreamasync-Methode oder die setnextsourcefrommediasourceasync-Methode annimmt.
ms.assetid: 7588E992-4070-4E0F-8C4B-7DFC097A5076
keywords:
- Issetnextsourceavailable-Methode Medien Streaming-API
- Issetnextsourceavailable-Methode Medien Streaming-API, imediarendereraktioninformation-Schnittstelle
- Imediarendereraktioninformation-Schnittstelle Medien Streaming-API, issetnextsourceavailable-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSetNextSourceAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 265a9a96d5229e47008c60813fd6c0e3bc567800
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725889"
---
# <a name="imediarendereractioninformationissetnextsourceavailable-method"></a><span data-ttu-id="8db77-106">Imediarendereraktioninformation:: issetnextsourceavailable-Methode</span><span class="sxs-lookup"><span data-stu-id="8db77-106">IMediaRendererActionInformation::IsSetNextSourceAvailable method</span></span>

<span data-ttu-id="8db77-107">Ruft einen Wert ab, der angibt, ob der DMR derzeit die [**setnextsourcefromuriasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) -Methode, die [**setnextsourcefromstreamasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) -Methode oder die [**setnextsourcefrommediasourceasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) -Methode annimmt.</span><span class="sxs-lookup"><span data-stu-id="8db77-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8db77-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8db77-108">Syntax</span></span>


```C++
HRESULT IsSetNextSourceAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="8db77-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8db77-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8db77-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8db77-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8db77-111">Ein boolescher Wert, der **true** ist, wenn der DMR derzeit die [**setnextsourcefromuriasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) -Methode, die [**setnextsourcefromstreamasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) -Methode oder die [**setnextsourcefrommediasourceasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) -Methode akzeptiert, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="8db77-111">A boolean value that is **True** if the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8db77-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8db77-112">Return value</span></span>

<span data-ttu-id="8db77-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="8db77-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8db77-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8db77-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8db77-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8db77-115">Return code</span></span>                                                                          | <span data-ttu-id="8db77-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8db77-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8db77-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8db77-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8db77-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8db77-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8db77-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8db77-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db77-120">**Imediarendereraktioninformation**</span><span class="sxs-lookup"><span data-stu-id="8db77-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

