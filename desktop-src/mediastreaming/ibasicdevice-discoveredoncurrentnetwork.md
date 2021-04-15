---
title: Ibasicdevice discoveredoncurrentnetwork-Methode
description: Ruft einen Wert ab, der angibt, ob sich das Gerät im aktuellen Netzwerk befindet.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- Discoveredoncurrentnetwork-Methode Medien Streaming-API
- Discoveredoncurrentnetwork-Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, discoveredoncurrentnetwork-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e79a012413b3b3d78a9c4617f01ca6cc01cf7e1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389047"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a><span data-ttu-id="19c8e-106">Ibasicdevice::D iscoveredoncurrentnetwork-Methode</span><span class="sxs-lookup"><span data-stu-id="19c8e-106">IBasicDevice::DiscoveredOnCurrentNetwork method</span></span>

<span data-ttu-id="19c8e-107">Ruft einen Wert ab, der angibt, ob sich das Gerät im aktuellen Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="19c8e-107">Retrieves a value that indicates if the device is on the current network.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c8e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="19c8e-108">Syntax</span></span>


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="19c8e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="19c8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19c8e-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="19c8e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19c8e-111">Empfängt einen Zeiger auf einen booleschen Wert, der **true** ist, wenn sich das Gerät im aktuellen Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="19c8e-111">Receives a pointer to a boolean value that is **True** if the device is on the current network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19c8e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19c8e-112">Return value</span></span>

<span data-ttu-id="19c8e-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="19c8e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="19c8e-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="19c8e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="19c8e-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="19c8e-115">Return code</span></span>                                                                          | <span data-ttu-id="19c8e-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19c8e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="19c8e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="19c8e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="19c8e-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19c8e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="19c8e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19c8e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c8e-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="19c8e-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





