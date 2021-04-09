---
title: Ibasicdevice modelnumber-Methode
description: Ruft die Modellnummer des Geräts ab.
ms.assetid: C4199135-0C6C-4427-8152-224D7D29C270
keywords:
- Modelnumber-Methode Medien Streaming-API
- Modelnumber-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, modelnumber-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.ModelNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8034e67e5f3c552f0af83678d75e33881f1318f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857335"
---
# <a name="ibasicdevicemodelnumber-method"></a><span data-ttu-id="ac96e-106">Ibasicdevice:: modelnumber-Methode</span><span class="sxs-lookup"><span data-stu-id="ac96e-106">IBasicDevice::ModelNumber method</span></span>

<span data-ttu-id="ac96e-107">Ruft die Modellnummer des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="ac96e-107">Retrieves the device s model number.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac96e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac96e-108">Syntax</span></span>


```C++
HRESULT ModelNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="ac96e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac96e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac96e-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ac96e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac96e-111">Empfängt einen Zeiger auf die Modellnummer des Geräts.</span><span class="sxs-lookup"><span data-stu-id="ac96e-111">Receives a pointer to the device s model number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac96e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac96e-112">Return value</span></span>

<span data-ttu-id="ac96e-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="ac96e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ac96e-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ac96e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ac96e-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ac96e-115">Return code</span></span>                                                                          | <span data-ttu-id="ac96e-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac96e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ac96e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ac96e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ac96e-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac96e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ac96e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac96e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac96e-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="ac96e-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





