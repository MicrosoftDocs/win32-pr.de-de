---
title: Ibasicdevice physicaladressen-Methode
description: Gibt einen Vektor physischer Adressen zurück.
ms.assetid: 85F48EE3-14A1-46DA-A3C3-F94A8A43CF92
keywords:
- Physicaladressen-Methode Medien Streaming-API
- Physicaladressen-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, physicaladressen-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.PhysicalAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f1cd87435c78e1f6877d1bb6afd1b38981b05dc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312449"
---
# <a name="ibasicdevicephysicaladdresses-method"></a><span data-ttu-id="9950b-106">Ibasicdevice::P hysicaladressen-Methode</span><span class="sxs-lookup"><span data-stu-id="9950b-106">IBasicDevice::PhysicalAddresses method</span></span>

<span data-ttu-id="9950b-107">Gibt einen Vektor physischer Adressen zurück.</span><span class="sxs-lookup"><span data-stu-id="9950b-107">Returns a vector of physical addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="9950b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9950b-108">Syntax</span></span>


```C++
HRESULT PhysicalAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="9950b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9950b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9950b-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9950b-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9950b-111">Empfängt eine Aufzähl Bare Auflistung von Zeigern auf physische Adressen.</span><span class="sxs-lookup"><span data-stu-id="9950b-111">Receives an enumerable collection of pointers to physical addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9950b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9950b-112">Return value</span></span>

<span data-ttu-id="9950b-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="9950b-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9950b-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9950b-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9950b-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9950b-115">Return code</span></span>                                                                          | <span data-ttu-id="9950b-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9950b-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9950b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9950b-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9950b-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9950b-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9950b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9950b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9950b-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="9950b-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





