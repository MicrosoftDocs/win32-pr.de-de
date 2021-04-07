---
title: Itransportparameters-Methode "aktioninformation"
description: Ruft eine imediarendereraktioninformation-Schnittstelle ab, die Informationen darüber bereitstellt, welche Methoden aktuell für die DMR aufgerufen werden können.
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- Aktioninformation-Methode Medien Streaming-API
- Aktions Information-Methode Medien Streaming-API, itransportparameters-Schnittstelle
- Itransportparameters-Schnittstelle Medien Streaming-API, aktioninformation-Methode
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b194da50e71402b6af69eb4cc9d67902e8ae89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038890"
---
# <a name="itransportparametersactioninformation-method"></a><span data-ttu-id="6cd42-106">Itransportparameters:: aktioninformation-Methode</span><span class="sxs-lookup"><span data-stu-id="6cd42-106">ITransportParameters::ActionInformation method</span></span>

<span data-ttu-id="6cd42-107">Ruft eine [**imediarendereraktioninformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) -Schnittstelle ab, die Informationen darüber bereitstellt, welche Methoden aktuell für die DMR aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="6cd42-107">Obtains an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface that provides information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd42-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cd42-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="6cd42-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cd42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cd42-110">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6cd42-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd42-111">Empfängt einen Verweis auf eine [**imediarendereraktioninformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6cd42-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cd42-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6cd42-112">Return value</span></span>

<span data-ttu-id="6cd42-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="6cd42-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6cd42-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6cd42-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6cd42-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6cd42-115">Return code</span></span>                                                                          | <span data-ttu-id="6cd42-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cd42-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6cd42-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6cd42-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6cd42-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cd42-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="6cd42-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cd42-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd42-120">**Itransportparameters**</span><span class="sxs-lookup"><span data-stu-id="6cd42-120">**ITransportParameters**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

