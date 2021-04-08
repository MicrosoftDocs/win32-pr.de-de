---
title: Ibasicdevice-Methode canwakedevices
description: Ruft einen Wert ab, der angibt, ob das Gerät aktiviert werden kann.
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- Canwakedevices-Methode Medien Streaming-API
- Canwakedevices-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, canwakedevices-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08a893ac880a426f604f2dc1c73173585e507cc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038056"
---
# <a name="ibasicdevicecanwakedevices-method"></a><span data-ttu-id="a0f6d-106">Ibasicdevice:: canwakedevices-Methode</span><span class="sxs-lookup"><span data-stu-id="a0f6d-106">IBasicDevice::CanWakeDevices method</span></span>

<span data-ttu-id="a0f6d-107">Ruft einen Wert ab, der angibt, ob das Gerät aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0f6d-107">Retrieves a value that indicates if the device can wake.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f6d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0f6d-108">Syntax</span></span>


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="a0f6d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0f6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f6d-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a0f6d-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f6d-111">Empfängt einen Zeiger auf einen booleschen Wert, der **true** ist, wenn das Gerät aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0f6d-111">Receives a pointer to a boolean value that is **True** if the device can wake.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f6d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0f6d-112">Return value</span></span>

<span data-ttu-id="a0f6d-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="a0f6d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a0f6d-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a0f6d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a0f6d-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a0f6d-115">Return code</span></span>                                                                          | <span data-ttu-id="a0f6d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0f6d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a0f6d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a0f6d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a0f6d-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0f6d-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="a0f6d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0f6d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f6d-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="a0f6d-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





