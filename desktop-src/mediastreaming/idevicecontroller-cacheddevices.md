---
title: Idevicecontroller-cacheddevices-Methode
description: Ruft eine Auflistung von ibasicdevice-Schnittstellen Zeigern ab, die die zwischengespeicherte Ansicht aller ermittelbaren DLNA-Geräte darstellt. | Idevicecontroller-cacheddevices-Methode
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- Cacheddevices-Methode Medien Streaming-API
- Cacheddevices-Methode Medien Streaming-API, idevicecontroller-Schnittstelle
- Idevicecontroller-Schnittstelle Medien Streaming-API, cacheddevices-Methode
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69be1faea277fa8999ae5ddf3658aaa61a1116b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961520"
---
# <a name="idevicecontrollercacheddevices-method"></a><span data-ttu-id="00e5b-107">Idevicecontroller:: cacheddevices-Methode</span><span class="sxs-lookup"><span data-stu-id="00e5b-107">IDeviceController::CachedDevices method</span></span>

<span data-ttu-id="00e5b-108">Ruft eine Auflistung von [**ibasicdevice**](ibasicdevice.md) -Schnittstellen Zeigern ab, die die zwischengespeicherte Ansicht aller ermittelbaren DLNA-Geräte darstellt.</span><span class="sxs-lookup"><span data-stu-id="00e5b-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="00e5b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="00e5b-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="00e5b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="00e5b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00e5b-111">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="00e5b-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00e5b-112">Empfängt eine Aufzähl Bare Auflistung von [**ibasicdevice**](ibasicdevice.md) -Schnittstellen Zeigern.</span><span class="sxs-lookup"><span data-stu-id="00e5b-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00e5b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00e5b-113">Return value</span></span>

<span data-ttu-id="00e5b-114">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="00e5b-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="00e5b-115">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="00e5b-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="00e5b-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="00e5b-116">Return code</span></span>                                                                          | <span data-ttu-id="00e5b-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00e5b-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="00e5b-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="00e5b-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="00e5b-119">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00e5b-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="00e5b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00e5b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e5b-121">**Idevicecontroller**</span><span class="sxs-lookup"><span data-stu-id="00e5b-121">**IDeviceController**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

