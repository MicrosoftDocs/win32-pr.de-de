---
title: Ibasicdevice-Beschreibungs Methode
description: Ruft eine Beschreibung des Geräts ab.
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- Beschreibungs Methode für Medien Streaming-API
- Description-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, Description-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f094246d1424c458e624d4a49358b63a84b9b7d2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037862"
---
# <a name="ibasicdevicedescription-method"></a><span data-ttu-id="5723c-106">Ibasicdevice::D escription-Methode</span><span class="sxs-lookup"><span data-stu-id="5723c-106">IBasicDevice::Description method</span></span>

<span data-ttu-id="5723c-107">Ruft eine Beschreibung des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="5723c-107">Retrieves a description of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5723c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5723c-108">Syntax</span></span>


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="5723c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5723c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5723c-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5723c-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5723c-111">Empfängt einen Zeiger auf die Beschreibung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="5723c-111">Receives a pointer to the description of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5723c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5723c-112">Return value</span></span>

<span data-ttu-id="5723c-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="5723c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5723c-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5723c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5723c-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5723c-115">Return code</span></span>                                                                          | <span data-ttu-id="5723c-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5723c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5723c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5723c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5723c-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5723c-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="5723c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5723c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5723c-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="5723c-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





