---
title: Ibasicdevice ManufacturerUrl-Methode
description: Ruft die Hersteller-URL des Geräts ab.
ms.assetid: E8372D15-D8B5-49E4-950A-96B4A88B0450
keywords:
- ManufacturerUrl-Methode Medien Streaming-API
- ManufacturerUrl-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, ManufacturerUrl-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e41ca83c98507c65ead8d1faf2922ee84b45649
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037928"
---
# <a name="ibasicdevicemanufacturerurl-method"></a><span data-ttu-id="933a6-106">Ibasicdevice:: ManufacturerUrl-Methode</span><span class="sxs-lookup"><span data-stu-id="933a6-106">IBasicDevice::ManufacturerUrl method</span></span>

<span data-ttu-id="933a6-107">Ruft die Hersteller-URL des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="933a6-107">Retrieves the device s manufacturer URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="933a6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="933a6-108">Syntax</span></span>


```C++
HRESULT ManufacturerUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="933a6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="933a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="933a6-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="933a6-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="933a6-111">Empfängt einen Zeiger auf die Hersteller-URL des Geräts.</span><span class="sxs-lookup"><span data-stu-id="933a6-111">Receives a pointer to the device s manufacturer URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="933a6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="933a6-112">Return value</span></span>

<span data-ttu-id="933a6-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="933a6-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="933a6-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="933a6-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="933a6-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="933a6-115">Return code</span></span>                                                                          | <span data-ttu-id="933a6-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="933a6-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="933a6-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="933a6-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="933a6-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="933a6-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="933a6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="933a6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="933a6-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="933a6-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





