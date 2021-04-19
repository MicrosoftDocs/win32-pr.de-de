---
title: Ibasicdevice modelname-Methode
description: Ruft den Modellnamen des Geräts ab.
ms.assetid: 8F871E89-97C1-4788-83AB-B7E0D8D6E0B5
keywords:
- Modelname-Methode Medien Streaming-API
- Modelname-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, modelname-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.ModelName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e486b372b2108bc85153f416032ef6bfbe8a397
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339027"
---
# <a name="ibasicdevicemodelname-method"></a><span data-ttu-id="92079-106">Ibasicdevice:: modelname-Methode</span><span class="sxs-lookup"><span data-stu-id="92079-106">IBasicDevice::ModelName method</span></span>

<span data-ttu-id="92079-107">Ruft den Modellnamen des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="92079-107">Retrieves the device s model name.</span></span>

## <a name="syntax"></a><span data-ttu-id="92079-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="92079-108">Syntax</span></span>


```C++
HRESULT ModelName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="92079-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="92079-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92079-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="92079-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92079-111">Empfängt einen Zeiger auf den Modellnamen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="92079-111">Receives a pointer to the device s model name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92079-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92079-112">Return value</span></span>

<span data-ttu-id="92079-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="92079-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="92079-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="92079-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="92079-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="92079-115">Return code</span></span>                                                                          | <span data-ttu-id="92079-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92079-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="92079-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="92079-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="92079-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92079-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="92079-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92079-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92079-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="92079-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





