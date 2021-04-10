---
title: Imediarenderer Action Information-Methode
description: Ruft Informationen darüber ab, welche Methoden aktuell für die DMR aufgerufen werden können.
ms.assetid: 7681FF92-DD13-4BBC-B860-E2BDFDA74FB9
keywords:
- Aktioninformation-Methode Medien Streaming-API
- Action Information-Methode Medien Streaming-API, imediarenderer-Schnittstelle
- Imediarenderer-Schnittstelle Medien Streaming-API, Action Information-Methode
topic_type:
- apiref
api_name:
- IMediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 346e43d6aaf3503c21f6a7586db5a731f0a7c478
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038905"
---
# <a name="imediarendereractioninformation-method"></a><span data-ttu-id="93351-106">Imediarenderer:: Action Information-Methode</span><span class="sxs-lookup"><span data-stu-id="93351-106">IMediaRenderer::ActionInformation method</span></span>

<span data-ttu-id="93351-107">Ruft Informationen darüber ab, welche Methoden aktuell für die DMR aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="93351-107">Retrieves information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="93351-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="93351-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="93351-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="93351-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93351-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="93351-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93351-111">Empfängt einen Verweis auf eine [**imediarendereraktioninformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="93351-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93351-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93351-112">Return value</span></span>

<span data-ttu-id="93351-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="93351-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="93351-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="93351-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="93351-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="93351-115">Return code</span></span>                                                                          | <span data-ttu-id="93351-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93351-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="93351-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="93351-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="93351-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93351-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="93351-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93351-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93351-120">**Imediarenderer**</span><span class="sxs-lookup"><span data-stu-id="93351-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

