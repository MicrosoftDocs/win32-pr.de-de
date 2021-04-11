---
title: Imediarendereraktioninformation-playbeschleunigt-Methode
description: Ruft die gesamte Liste der playspeed-Werte ab, die von der DMR akzeptiert werden.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- Playbeschleunigt-Methode Medien Streaming-API
- Playbeschleunigt-Methode Medien Streaming-API, imediarendereraktioninformation-Schnittstelle
- Imediarendereraktioninformation-Schnittstelle Medien Streaming-API, playbeschleunigt-Methode
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31089dd7616c035ebde4079c51988b94d1c27562
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314985"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a><span data-ttu-id="bab3f-106">Imediarendereraktioninformation::P laybeschleunigt-Methode</span><span class="sxs-lookup"><span data-stu-id="bab3f-106">IMediaRendererActionInformation::PlaySpeeds method</span></span>

<span data-ttu-id="bab3f-107">Ruft die gesamte Liste der [**playspeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) -Werte ab, die von der DMR akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="bab3f-107">Retrieves the complete list of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) values that are accepted by the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab3f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bab3f-108">Syntax</span></span>


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a><span data-ttu-id="bab3f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bab3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab3f-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bab3f-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bab3f-111">Empfängt einen Vektor von [**playspeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) -Strukturen, der die gesamte Liste der von DMR akzeptierten **playspeed** -Werte angibt.</span><span class="sxs-lookup"><span data-stu-id="bab3f-111">Receives a vector of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) structures specifying the complete list of **PlaySpeed** values that are accepted by the DMR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bab3f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bab3f-112">Return value</span></span>

<span data-ttu-id="bab3f-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="bab3f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bab3f-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="bab3f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bab3f-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bab3f-115">Return code</span></span>                                                                          | <span data-ttu-id="bab3f-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bab3f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bab3f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bab3f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bab3f-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bab3f-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="bab3f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bab3f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab3f-120">**Imediarendereraktioninformation**</span><span class="sxs-lookup"><span data-stu-id="bab3f-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

