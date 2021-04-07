---
title: Ibasicdevice-Symbol Methode
description: Gibt einen Vektor von ideviceicon-Schnittstellen zurück.
ms.assetid: 0C083AF3-FE22-4A8E-87B7-0FFA7B65ADBD
keywords:
- Symbol Methode Medien Streaming-API
- Symbol Methode Medien Streaming-API, ibasicdevice-Schnittstelle
- Ibasicdevice-Schnittstelle Medien Streaming-API, Symbol-Methode
topic_type:
- apiref
api_name:
- IBasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fb6e4b708b4e38ffb39f152308cec7b885a772f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724985"
---
# <a name="ibasicdeviceicons-method"></a><span data-ttu-id="8325c-106">Ibasicdevice:: Icons-Methode</span><span class="sxs-lookup"><span data-stu-id="8325c-106">IBasicDevice::Icons method</span></span>

<span data-ttu-id="8325c-107">Gibt einen Vektor von [**ideviceicon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) -Schnittstellen zurück.</span><span class="sxs-lookup"><span data-stu-id="8325c-107">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="8325c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8325c-108">Syntax</span></span>


```C++
HRESULT Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="parameters"></a><span data-ttu-id="8325c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8325c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8325c-110">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8325c-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8325c-111">Empfängt eine Aufzähl Bare Auflistung von [**ideviceicon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) -Schnittstellen Zeigern.</span><span class="sxs-lookup"><span data-stu-id="8325c-111">Receives an enumerable collection of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8325c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8325c-112">Return value</span></span>

<span data-ttu-id="8325c-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="8325c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8325c-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8325c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8325c-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8325c-115">Return code</span></span>                                                                          | <span data-ttu-id="8325c-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8325c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8325c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8325c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8325c-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8325c-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8325c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8325c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8325c-120">**Ibasicdevice**</span><span class="sxs-lookup"><span data-stu-id="8325c-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

