---
title: Devicecontroller. cacheddevices-Methode
description: Ruft eine Auflistung von ibasicdevice-Schnittstellen Zeigern ab, die die zwischengespeicherte Ansicht aller ermittelbaren DLNA-Geräte darstellt. | Devicecontroller. cacheddevices-Methode
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- Cacheddevices-Methode Medien Streaming-API
- Cacheddevices-Methode Medien Streaming-API, devicecontroller-Schnittstelle
- Devicecontroller-Schnittstelle Medien Streaming-API, cacheddevices-Methode
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0bb39e03a9788e0c444f682b61d39fc1c65781b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350627"
---
# <a name="devicecontrollercacheddevices-method"></a><span data-ttu-id="38931-107">Devicecontroller. cacheddevices-Methode</span><span class="sxs-lookup"><span data-stu-id="38931-107">DeviceController.CachedDevices method</span></span>

<span data-ttu-id="38931-108">Ruft eine Auflistung von [**ibasicdevice**](ibasicdevice.md) -Schnittstellen Zeigern ab, die die zwischengespeicherte Ansicht aller ermittelbaren DLNA-Geräte darstellt.</span><span class="sxs-lookup"><span data-stu-id="38931-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="38931-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="38931-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="38931-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="38931-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38931-111">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="38931-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38931-112">Empfängt eine Aufzähl Bare Auflistung von [**ibasicdevice**](ibasicdevice.md) -Schnittstellen Zeigern.</span><span class="sxs-lookup"><span data-stu-id="38931-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38931-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38931-113">Return value</span></span>

<span data-ttu-id="38931-114">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="38931-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="38931-115">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="38931-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="38931-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="38931-116">Return code</span></span>                                                                          | <span data-ttu-id="38931-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38931-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="38931-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38931-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="38931-119">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38931-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="38931-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38931-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="38931-121">[**Geräte-econtroller**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38931-121">[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span></span>
</dt> </dl>

 

