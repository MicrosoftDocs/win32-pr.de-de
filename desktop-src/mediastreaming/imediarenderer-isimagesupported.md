---
title: Imediarenderer-Methode (isimagesupported)
description: Ruft einen Wert ab, der angibt, ob der DMR Bilder anzeigen kann.
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- Isimagesupported-Methode Medien Streaming-API
- Isimagesupported-Methode Medien Streaming-API, imediarenderer-Schnittstelle
- Imediarenderer-Schnittstelle Medien Streaming-API, isimagesupported-Methode
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd68f4d758c67b81c1eefcbc83a0f0a505ec27b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342101"
---
# <a name="imediarendererisimagesupported-method"></a><span data-ttu-id="38a85-106">Imediarenderer:: isimagesupported-Methode</span><span class="sxs-lookup"><span data-stu-id="38a85-106">IMediaRenderer::IsImageSupported method</span></span>

<span data-ttu-id="38a85-107">Ruft einen Wert ab, der angibt, ob der DMR Bilder anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="38a85-107">Retrieves a value that indicates whether the DMR is capable of displaying images.</span></span>

## <a name="syntax"></a><span data-ttu-id="38a85-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="38a85-108">Syntax</span></span>


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="38a85-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="38a85-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38a85-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="38a85-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38a85-111">Ein boolescher Wert, der **true** ist, wenn der DMR Bilder anzeigen kann, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="38a85-111">A boolean value that is **True** if the DMR is capable of displaying images and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38a85-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38a85-112">Return value</span></span>

<span data-ttu-id="38a85-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="38a85-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="38a85-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="38a85-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="38a85-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="38a85-115">Return code</span></span>                                                                          | <span data-ttu-id="38a85-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38a85-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="38a85-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38a85-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="38a85-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38a85-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="38a85-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38a85-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a85-120">**Imediarenderer**</span><span class="sxs-lookup"><span data-stu-id="38a85-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





